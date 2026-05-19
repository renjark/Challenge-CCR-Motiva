# NOME (a definir) - Gestão de Vegetação em Rodovias
> Solução mobile para monitoramento e gestão da vegetação nas rodovias concedidas à Motiva.

---

## Integrantes

Bernardo Silva Berwanger          565776 <br> 
Gregory Debom Ferreira            562346 <br> 
João Vitor Angeloti Sena	        563473 <br> 
Laís Krajner Lacerda	          	563182 <br>
Luana Magalhães Freire	      	  565305 <br>
Pamella Souza da Silva Ferreira   566172 <br>

---

## Problema Escolhido

A Motiva — empresa de infraestrutura de mobilidade responsável pela gestão e operação de rodovias — realiza o monitoramento da vegetação nas margens das rodovias de forma inteiramente manual. Um inspetor percorre toda a extensão da rodovia de carro, registra o estado da vegetação em prancheta (classificando como baixa, média ou alta) e, ao retornar, transcreve essas informações para planilhas Excel organizadas em trechos de 500 metros.

Esse processo apresenta fragilidades críticas: subjetividade nas avaliações, alto tempo de deslocamento, ausência de histórico confiável por trecho, desalinhamento entre campo e gestão e incapacidade de aprender com os dados coletados.

⤷ Recorte escolhido pelo grupo: a perspectiva do supervisor/gestor, que hoje não tem acesso a dados consolidados, em tempo real ou com histórico estruturado, e toma decisões com base em informações fragmentadas e desatualizadas.

---

## Persona

⤷ Nome: Carlos Eduardo, 43 anos  
⤷ Cargo: Supervisor de Conservação de Rodovias — Motiva  
⤷ Contexto: Carlos coordena as equipes de campo em um trecho de 180km de rodovia. Ele recebe relatórios em planilha com atraso, não tem visibilidade do estado atual da vegetação em tempo real e precisa tomar decisões de priorização de manutenção sem dados confiáveis. Frequentemente descobre situações críticas apenas quando já geraram reclamações ou riscos reais ao tráfego.

**Objetivos:** <br>
⤷ Visualizar o estado atual de todos os trechos de forma consolidada <br>
⤷ Priorizar intervenções com base em dados objetivos, não em "achismo" <br>
⤷ Acompanhar histórico de manutenções por trecho <br>
⤷ Receber alertas automáticos de situações críticas <br>

**Frustrações:** <br>
⤷ Planilhas desatualizadas e fragmentadas <br>
⤷ Falta de rastreabilidade histórica <br>
⤷ Decisões baseadas em percepção subjetiva do inspetor <br>
⤷ Impossibilidade de escalar a operação sem aumentar a complexidade <br>

---

## Proposta de Solução

Um aplicativo mobile voltado ao supervisor de conservação, oferecendo: <br>

⤷ Dashboard com visão geral dos trechos da rodovia: quantidade de trechos críticos, manutenções pendentes e última inspeção realizada <br>
⤷ Mapa interativo com colorização por status (verde / amarelo / vermelho) por trecho <br>
⤷ Detalhe por trecho: histórico de inspeções, fotos registradas e acionamento de equipe de manutenção <br>
⤷ Ranking de urgência: lista priorizada automaticamente pelos trechos mais críticos <br>
⤷ Alertas automáticos para anomalias (obstrução de placas, crescimento acelerado, situações pontuais) <br>
⤷ Relatório histórico com filtros por data e rodovia, e gráfico de evolução do status <br>

---

## Stack Tecnológica

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

## Requisitos

### Requisitos Funcionais (RF) <br>

⤷ O sistema deve exibir um dashboard com resumo do estado atual dos trechos (críticos, atenção, ok) <br>
⤷ O sistema deve exibir um mapa interativo com colorização dos trechos por nível de urgência <br>
⤷ O usuário deve poder tocar em um trecho no mapa para visualizar seus detalhes <br>
⤷ O sistema deve exibir o histórico de inspeções e manutenções por trecho <br>
⤷ O sistema deve exibir um ranking de trechos ordenado por urgência de intervenção <br>
⤷ O sistema deve permitir o acionamento de equipe de manutenção diretamente pelo app <br>
⤷ O sistema deve emitir alertas automáticos para anomalias detectadas nos trechos <br>
⤷ O sistema deve exibir relatório histórico com filtros por data e rodovia <br>
⤷ O sistema deve suportar autenticação de usuário (login) <br>
⤷ O sistema deve funcionar com funcionalidades básicas mesmo sem conexão à internet (modo offline) <br>

### Requisitos Não Funcionais (RNF) <br>

⤷ O app deve ser compatível com Android e iOS <br>
⤷ O tempo de carregamento das telas principais não deve ultrapassar 3 segundos em conexão 4G <br>
⤷ A interface deve seguir princípios de acessibilidade (contraste adequado, tamanho de texto legível) <br>
⤷ Os dados de inspeção devem ser armazenados localmente quando offline e sincronizados ao retomar conexão <br>
⤷ O sistema deve garantir autenticação segura com token JWT <br>
⤷ O mapa deve renderizar trechos com suavidade, sem travamentos, para rodovias de até 500km <br>
⤷ A identidade visual deve ser consistente com a marca Motiva em todas as telas <br>

---

## Links

⤷ Protótipo no Figma: [link]
