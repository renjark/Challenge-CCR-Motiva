# 🌿 Grovia — Gestão de Vegetação em Rodovias
 
> Solução mobile para monitoramento e gestão da vegetação nas rodovias concedidas à Motiva.
 
---
 
## 👥 Integrantes
 
| Nome | RM |
|---|---|
| Bernardo Silva Berwanger | 565776 |
| Gregory Debom Ferreira | 562346 |
| João Vitor Angeloti Sena | 563473 |
| Laís Krajner Lacerda | 563182 |
| Luana Magalhães Freire | 565305 |
| Pamella Souza da Silva Ferreira | 566172 |
 
---
 
## 🚧 Problema Escolhido
 
A Motiva — empresa de infraestrutura de mobilidade responsável pela gestão e operação de rodovias — realiza o monitoramento da vegetação nas margens das rodovias de forma inteiramente manual. Um inspetor percorre toda a extensão da rodovia de carro, registra o estado da vegetação em prancheta (classificando como baixa, média ou alta) e, ao retornar, transcreve essas informações para planilhas Excel organizadas em trechos de 500 metros.
 
Esse processo apresenta fragilidades críticas: subjetividade nas avaliações, alto tempo de deslocamento, ausência de histórico confiável por trecho, desalinhamento entre campo e gestão e incapacidade de aprender com os dados coletados.
 
A gestão da vegetação nas rodovias concedidas está sujeita às exigências regulatórias da **ARTESP** (no estado de São Paulo) e da **ANTT** (em nível federal), que estabelecem padrões mínimos de conservação e visibilidade viária. O descumprimento dessas normas pode resultar em penalidades contratuais e comprometer a renovação das concessões. O processo manual atual dificulta a comprovação de conformidade e o registro de evidências para fiscalizações.
 
⤷ Recorte escolhido pelo grupo: a perspectiva do supervisor/gestor, que hoje não tem acesso a dados consolidados, em tempo real ou com histórico estruturado, e toma decisões com base em informações fragmentadas e desatualizadas.
 
---
 
## 👤 Persona
 
⤷ Nome: Marcos  
⤷ Cargo: Supervisor de Conservação de Rodovias — Motiva  
⤷ Contexto: Marcos coordena as equipes de campo em um trecho de 180km de rodovia. Ele recebe relatórios em planilha com atraso, não tem visibilidade do estado atual da vegetação em tempo real e precisa tomar decisões de priorização de manutenção sem dados confiáveis. Frequentemente descobre situações críticas apenas quando já geraram reclamações ou riscos reais ao tráfego.
 
**Objetivos:**  
⤷ Visualizar o estado atual de todos os trechos de forma consolidada  
⤷ Priorizar intervenções com base em dados objetivos, não em "achismo"  
⤷ Acompanhar histórico de manutenções por trecho  
⤷ Receber alertas automáticos de situações críticas  
 
**Frustrações:**  
⤷ Planilhas desatualizadas e fragmentadas  
⤷ Falta de rastreabilidade histórica  
⤷ Decisões baseadas em percepção subjetiva do inspetor  
⤷ Impossibilidade de escalar a operação sem aumentar a complexidade  
 
---
 
## 💡 Proposta de Solução
 
Um aplicativo mobile voltado ao supervisor de conservação, oferecendo:
 
⤷ Dashboard com visão geral dos trechos da rodovia: quantidade de trechos críticos, manutenções pendentes e última inspeção realizada  
⤷ Mapa interativo com colorização por status (verde / amarelo / vermelho) por trecho  
⤷ Detalhe por trecho: histórico de inspeções, fotos registradas e acionamento de equipe de manutenção  
⤷ Ranking de urgência: lista priorizada automaticamente pelos trechos mais críticos  
⤷ Alertas automáticos para anomalias (obstrução de placas, crescimento acelerado, situações pontuais)  
 
---
 
## 🗺️ Telas do Protótipo
 
| Tela | Descrição |
|---|---|
| Tela Inicial | Dashboard com status dos trechos, manutenções pendentes e alertas recentes |
| Mapa da Rodovia | Visualização geográfica com trechos coloridos por urgência e card de trecho selecionado |
| Ranking de Urgência | Lista priorizada dos trechos mais críticos com barra de urgência e botão de acionamento |
| Notificações | Central de alertas automáticos organizados por data |
 
---
 
## 🛠️ Stack Tecnológica
 
| Tecnologia | Justificativa |
|---|---|
| **React Native** | Permite desenvolvimento multiplataforma (iOS e Android) com uma única base de código, reduzindo tempo e esforço de desenvolvimento |
| **Expo** | Facilita o setup inicial, oferece APIs nativas prontas (câmera, geolocalização, notificações) e simplifica o processo de build e distribuição |
| **Expo Router** | Navegação baseada em arquivos, intuitiva e alinhada com o padrão moderno do ecossistema Expo |
| **React Native Maps** | Integração com mapas nativos (Google Maps / Apple Maps) para exibição dos trechos geolocalizados com colorização por status |
| **Expo Location** | Acesso à geolocalização do dispositivo para rastreamento de posição do inspetor e vinculação de registros a coordenadas exatas |
| **Expo Camera** | Captura de imagens geolocalizadas durante a inspeção de campo |
| **AsyncStorage** | Armazenamento local para suporte offline, garantindo funcionamento mesmo em trechos com baixa conectividade |
| **Axios** | Comunicação com a API backend para envio e recebimento de dados de inspeção e manutenção |
 
---
 
## 📋 Requisitos
 
### Requisitos Funcionais (RF)
 
⤷ O sistema deve exibir um dashboard com resumo do estado atual dos trechos (críticos, atenção, ok)  
⤷ O sistema deve exibir um mapa interativo com colorização dos trechos por nível de urgência  
⤷ O usuário deve poder tocar em um trecho no mapa para visualizar seus detalhes  
⤷ O sistema deve exibir o histórico de inspeções e manutenções por trecho  
⤷ O sistema deve exibir um ranking de trechos ordenado por urgência de intervenção  
⤷ O sistema deve permitir o acionamento de equipe de manutenção diretamente pelo app  
⤷ O sistema deve emitir alertas automáticos para anomalias detectadas nos trechos  
⤷ O sistema deve exibir relatório histórico com filtros por data e rodovia  
⤷ O sistema deve funcionar com funcionalidades básicas mesmo sem conexão à internet (modo offline)  
 
### Requisitos Não Funcionais (RNF)
 
⤷ O app deve ser compatível com Android e iOS  
⤷ O tempo de carregamento das telas principais não deve ultrapassar 3 segundos em conexão 4G  
⤷ A interface deve seguir princípios de acessibilidade (contraste adequado, tamanho de texto legível)  
⤷ Os dados de inspeção devem ser armazenados localmente quando offline e sincronizados ao retomar conexão  
⤷ O sistema deve garantir autenticação segura com token JWT  
⤷ O mapa deve renderizar trechos com suavidade, sem travamentos, para rodovias de até 500km  
⤷ A identidade visual deve ser consistente com a marca Motiva em todas as telas  
 
### Restrições Técnicas
 
⤷ Trechos de rodovia podem ter sinal instável ou inexistente, exigindo suporte offline obrigatório  
⤷ A solução deve funcionar em dispositivos Android e iOS de diferentes fabricantes, sem depender de hardware específico  
⤷ Funcionalidades de mapa dependem do GPS do dispositivo, com possível precisão reduzida em áreas rurais  
⤷ O protótipo desta sprint é navegável no Figma e não requer integração real com API ou banco de dados  
 
---
 
## 🔗 Links
 
⤷ Protótipo no Figma: [Grovia — Figma](https://www.figma.com/design/2q0e7OFOKzfeIxQZSM0S6a/Motiva-Grovia?node-id=130-115&t=BfQdEL27nJ99Mdng-0)
---
 
