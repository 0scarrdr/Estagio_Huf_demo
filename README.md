# Estágio_Huf_demo

[EN]
360° Cockpit of a Machine

📄 Project Description
This project was developed as part of an internship at 

Huf Portuguesa, as part of the Computer Engineering Degree at the Polytechnic Institute of Viseu. The goal was to create a responsive web application to centralise and streamline access to all information related to the company's industrial machines.


The application arose from the need to reduce the time spent by the maintenance team searching for scattered information, such as manuals, incident history, or parts stock. The direct impact of this optimisation is increased productivity and reduced machine downtime.


🎯 Main Objective
To develop and implement a responsive web application capable of reading a machine's QR Code and displaying all existing information about it, in order to facilitate access to data and increase the productivity of maintenance workers.

⚙️ Architecture and Workflow
The application was designed with a logical workflow to ensure speed and accuracy in obtaining data:

Data Entry: The user initiates the process in two ways:

By scanning a QR code affixed to the machine with a tablet camera.


By selecting the desired machine from a search list.


API Consumption: The machine ID (obtained from the QR code or list) is used to call a REST API and obtain the main data.


Complex Data Processing: A challenge was identified in which the same machine could have two IDs (one new and one old), with fragmented information. The solution implemented involves:

A first call to the API with the ID read.

A query to an internal mapping table (loaded from an Excel file) to find the corresponding ID (old or new).


A second call to the API with this second ID to obtain the complementary data.

The use of a customised Java Action in Mendix to merge the data from the two objects into a single complete and consistent object.



Presentation: The final, unified data object is then presented on the ‘Cockpit 360°’ page, which serves as a central dashboard.

Integration with SharePoint: Links to documentation are generated dynamically. A 

Nanoflow (logic that runs on the client side) builds the SharePoint URL based on the machine manufacturer and brand, automatically redirecting the user to the correct folder.


Detailed Features

QR Code Reading and Search: Allows quick access to machine data, either by optical reading or manual search.


360° Dashboard Cockpit: Main screen that displays the machine name and centralises access to all other features through intuitive buttons. It also provides a summary of the latest recorded incidents.


Access to Documentation (SharePoint):


Supplier Documentation: Redirects to the specific folder in SharePoint containing manufacturer manuals and technical files.


Documentation by Brand: Accesses a different folder structure, organised by brand, for internally obtained documents.


Parts Stock Query: Displays a table with the parts associated with the machine, their code, manufacturer, quantity in stock and their physical location in the warehouse.


Maintenance and Incident History: Allows you to view a list of all past interventions and malfunctions. When you select an incident, a details page is displayed with information such as severity, the technician responsible, the probable cause, and the solution applied.



Graphs and Analyses: A visual section that displays bar graphs on machine performance, including its power consumption and productivity over time.



General Report: A dashboard of indicators (KPIs) on the overall status of the factory, showing data such as the ‘machine with the most occurrences,’ the ‘average resolution time,’ and the "most common cause of av

🛠️ Technologies and Tools Used
Development Platform: Mendix (Low-Code)

Justification: This was the strategic choice because it was a technology that the company was adopting, allowing us to accelerate development to meet the internship deadlines.

Backend and API (simulated): Node.js and Express.js

Justification: Used to create a local API with fictitious data, which allowed for the development and testing of the application while the real data was not available.

Communication Protocols: RESTful API and OData

Justification: The REST architecture allowed for flexible and scalable communication. OData was particularly important for standardising queries, simulating the structure used internally by Huf.

Document Management: Microsoft SharePoint

Justification: It was integrated because it was the company's existing document management system, ensuring that the new application aligned with established work processes.

Design and Prototyping (UI/UX): Figma

Justification: Used to create high-fidelity prototypes that allowed the design and user experience to be validated with the team before implementation began.

Version Control: Git

Justification: Essential for managing the project's change history and ensuring the security of the work developed.

Management and Collaboration: Microsoft Teams

Justification: Used for task management and communication with the team, ensuring transparent and organised progress monitoring of the internship.

✍️ Author
Óscar Rafael Dias Rodrigues


[PT]

Cockpit 360° de uma Máquina

📄 Descrição do Projeto
Este projeto foi desenvolvido no âmbito de um estágio na empresa 

Huf Portuguesa, como parte da Licenciatura em Engenharia Informática do Politécnico de Viseu. O objetivo foi criar uma aplicação web responsiva para centralizar e agilizar o acesso a todas as informações relativas às máquinas industriais da empresa.


A aplicação nasceu da necessidade de reduzir o tempo despendido pela equipa de manutenção na procura de informação dispersa, como manuais, histórico de incidentes ou stock de peças. O impacto direto desta otimização é o aumento da produtividade e a diminuição do tempo de paragem das máquinas.


🎯 Objetivo Principal 
Desenvolver e implementar uma aplicação web responsiva capaz de ler o QR Code de uma máquina e apresentar todas as informações existentes sobre ela, com o fim de facilitar o acesso aos dados e aumentar a produtividade dos trabalhadores da manutenção.


Markdown

[![Demonstração do Cockpit 360](https://youtu.be/aQbpwHOzxdk)


⚙️ Arquitetura e Fluxo de Funcionamento
A aplicação foi desenhada com um fluxo lógico para garantir rapidez e precisão na obtenção dos dados:

Entrada de Dados: O utilizador inicia o processo de duas formas:

Lendo um QR Code afixado na máquina com a câmara de um tablet.

Selecionando a máquina desejada a partir de uma lista de pesquisa.


Consumo de API: O ID da máquina (obtido pelo QR Code ou pela lista) é usado para fazer uma chamada a uma API REST e obter os dados principais.


Tratamento de Dados Complexos: Foi identificado um desafio em que uma mesma máquina poderia ter dois IDs (um novo e um antigo), com informações fragmentadas. A solução implementada envolve:

Uma primeira chamada à API com o ID lido.

Uma consulta a uma tabela de mapeamento interna (carregada a partir de um ficheiro Excel) para encontrar o ID correspondente (antigo ou novo).


Uma segunda chamada à API com este segundo ID para obter os dados complementares.

A utilização de uma 

Java Action customizada no Mendix para fundir os dados dos dois objetos num único objeto completo e consistente.



Apresentação: O objeto de dados final e unificado é então apresentado na página "Cockpit 360°", que serve como dashboard central.

Integração com SharePoint: As ligações para a documentação são geradas dinamicamente. Um 

Nanoflow (lógica que corre no lado do cliente) constrói o URL do SharePoint com base no fabricante e na marca da máquina, redirecionando o utilizador para a pasta correta de forma automática.


✨ Funcionalidades Detalhadas

Leitura de QR Code e Pesquisa: Permite o acesso rápido aos dados de uma máquina, quer por leitura ótica, quer por pesquisa manual.


Dashboard Cockpit 360°: Ecrã principal que exibe o nome da máquina e centraliza o acesso a todas as outras funcionalidades através de botões intuitivos. Apresenta também um resumo dos últimos incidentes registados.


Acesso à Documentação (SharePoint):


Documentação do Fornecedor: Redireciona para a pasta específica no SharePoint contendo manuais e ficheiros técnicos do fabricante.


Documentação por Marcas: Acede a uma estrutura de pastas diferente, organizada por marcas, para documentos obtidos internamente.


Consulta de Stock de Peças: Exibe uma tabela com as peças associadas à máquina, o seu código, fabricante, quantidade em stock e a sua localização física no armazém.


Histórico de Manutenções e Incidentes: Permite visualizar uma lista de todas as intervenções e avarias passadas. Ao selecionar um incidente, é exibida uma página de detalhes com informações como a gravidade, o técnico responsável, a causa provável e a solução aplicada.



Gráficos e Análises: Uma secção visual que apresenta gráficos de barras sobre o desempenho da máquina, incluindo o seu consumo elétrico e a produtividade ao longo do tempo.



Relatório Geral (Report): Um painel de indicadores (KPIs) sobre o estado geral da fábrica, mostrando dados como a "máquina com mais ocorrências", o "tempo médio de resolução" e a "causa mais comum de avarias".


🛠️ Tecnologias e Ferramentas Utilizadas
Plataforma de Desenvolvimento: Mendix (Low-Code)


Justificação: Foi a escolha estratégica por ser uma tecnologia que a empresa estava a adotar, permitindo acelerar o desenvolvimento para cumprir os prazos do estágio.


Backend e API (simulada): Node.js e Express.js


Justificação: Utilizados para criar uma API local com dados fictícios, o que permitiu o desenvolvimento e teste da aplicação enquanto os dados reais não estavam disponíveis.


Protocolos de Comunicação: API RESTful e OData

Justificação: A arquitetura REST permitiu uma comunicação flexível e escalável. O OData foi particularmente importante por padronizar as consultas, simulando a estrutura utilizada internamente pela Huf.


Gestão Documental: Microsoft SharePoint


Justificação: Foi integrado por ser o sistema de gestão documental já existente na empresa, garantindo que a nova aplicação se alinhasse com os processos de trabalho já estabelecidos.


Design e Prototipagem (UI/UX): Figma


Justificação: Utilizado para criar protótipos de alta fidelidade que permitiram validar o design e a experiência do utilizador com a equipa antes do início da implementação.


Controlo de Versões: Git


Justificação: Essencial para gerir o histórico de alterações do projeto e garantir a segurança do trabalho desenvolvido.

Gestão e Colaboração: Microsoft Teams


Justificação: Usado para a gestão de tarefas e comunicação com a equipa, assegurando um acompanhamento transparente e organizado do progresso do estágio.

✍️ Autor
Óscar Rafael Dias Rodrigues
