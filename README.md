<p style="font-size: 1.3rem;">Projeto_2   2348160: Sidney Alexandre Ferracin Junior, 2348012: João Pedro Vaciloto Montilha, 2383969: Marcus Vinícius Molina Freitas</p>

<h2>Projeto 2 - Análise e Documentação da Arquitetura em Camadas do Sistema Map-OS</h2>

<br>

<p style="text-align: center;">
    <img src="https://raw.githubusercontent.com/RamonSilva20/mapos/master/assets/img/logo.png" alt="MapOS Logo" style="width:400px;">
</p>

<br>

<h3>Estrutura da Documentação</h3>

- [Introdução](#Introdução)
- [Descrição do Sistema](#descricao-do-sistema)
- [Arquitetura do Sistema](#arquitetura-do-sistema)
- [Processos Principais](#processos-principais)
- [Proposta de Melhoria](#proposta-de-melhoria)
- [Conclusão](#conclusao)
- [Referências](#referencias)

<h3>Introdução</h3>
Devido à sua complexidade e abrangência, o Map-OS foi selecionado como objeto de estudo para a documentação detalhada de sua arquitetura, como parte de uma atividade avaliativa da disciplina de Arquitetura de Software na UTFPR de Cornélio Procópio. Esta documentação tem como objetivo explorar e detalhar os principais processos e recursos presentes em cada camada do sistema, fornecendo uma visão clara e precisa de como a aplicação é estruturada e como seus componentes interagem para atender às necessidades dos usuários.</p>

<h3>Descrição do Sistema</h3>
<p>O Map-OS (Manutenção e Automação de Processos de Ordens de Serviço) é um projeto de código aberto para gestão de ordens de serviço, com uma arquitetura robusta e modular e com uma boa base de usuários ativos e desenvolvedores, se tornando uma ótima escolha de software alvo para documentação de sua arquitetura.</p>
<p>O objetivo é ser um sistema de assistência técnica, facilitando o gerenciamento da empresa do usuário, o possibilitando realizar sua gestão de ordens e serviços, a gestão de clientes e estoques, geração de relatório sobre as finanças, entre outras funcionalidades. Tendo sido desenvolvido em PHP, ele é um programa de código aberto disponível no GitHub e dividido em uma arquitetura de camadas, o que permite que cada componente do sistema comunique-se com outros de forma clara, faciilitando também sua manutenção. Sua utilização no mercado se da principalmente por pequenas e médias empresas que focam em serviços de atendimento ao cliente.</p>

<h2>Seção A</h2>

<h3>Arquitetura do Sistema</h3>
<p>A arquitetura do MapOS é organizada nas seguintes camadas: apresentação, ligação de negócio, persistência e infraestrutura.</p>
<ul>
  <li><strong>Camada de Apresentação:</strong> Esta camada é responsável pela interface gráfica do usuário usuário, utilizando o framework <em>Matrix Admin</em>, que oferece componentes pré-configurados, facilitando o desenvolvimento do frontend e tornando sua aplicação atraente e funcional. A interação com os usuários é facilitada também por componentes como Bootstrap, AJAX e jQuery, ferramentas famosas que possibilitam aumentar a funcionalidade e responsividade da interface.</li>
  
  <li><strong>Camada de Lógica de Negócio:</strong> A lógica de negócio do Map-OS é o componente central do software, sendo implementada através do framework <em>CodeIgniter</em>. Esta camada se responsabiliza por gerenciar as operações das regras de negócio, como a criação e gerenciamento de ordens de serviço, controle de clientes. Isso permite que o sistema faça a criação e atualização das ordens de serviço, cadastro e gerenciamento dos clientes e os notifica, tanto sobre o status do serviço como marketing e propaganda. Além disso, essa camada também é responsável por realizar a integração com APIs externas, sendo utilizado principalmente para integrar APIs de gateways de pagamento.</li>
  
  <li><strong>Camada de Persistência:</strong> A camada de persistência é responsável por recuperar e gerenciar o armazenamento de dados do sistema, utilizando o banco de dados MySQL. Entre esses dados estão presentes informações de clientes, ordens de serviço e configurações do sistema. Devido a sensibilidade desses dados, tanto para os clientes como para a empresa, Também está presente nessa camada medidas de segurança como controle de acesso e criptografia dos dados.  As operações de CRUD (Create Read Update Delete) são realizadas nesta camada, que são otimizados no MySQL através do uso de índices.</li>
  
  <li><strong>Camada de Infraestrutura:</strong> A infraestrutura do Map-OS é projetada visando oferecer um suporte robusto e flexível, possibilitando ser hospedado por servidores web famosos, como Apache e Nginx. Para simplificar a instalação e configuração inicial, foi feito o uso do <em>Composer</em>, que gerencia as dependências para PHP, tais como as bibliotecas e pacotes necessários para seu funcionamento, e opcionalmente <em>Docker</em>, que se utiliza de contêineres para encapsular o sistema, mantendo sua consistência independentemente das configurações do ambiente, ambos garantindo um ambiente de execução estável e replicável.</li>
</ul>

<h3>Processos Principais</h3>
<p>A análise dos processos principais do Map-OS abrange:</p>
<ul>
  <li><strong>Gestão de Ordens de Serviço:</strong> Fluxo que abrange desde a criação de uma nova ordem de serviço até seu fechamento, incluindo atribuição de técnicos e notificação de clientes.</li>
  <li><strong>Autenticação e Controle de Acesso:</strong> Sistema de autenticação de usuários com diferentes níveis de permissão, garantindo a segurança e integridade das operações.</li>
  <li><strong>Integração com APIs:</strong> Descrição das integrações disponíveis com APIs externas para expandir as funcionalidades do sistema, como gateways de pagamento e serviços de email.</li>
</ul>

<h2>Seção B</h2>

<h3>Proposta de Melhoria</h3>
<p>Esta seção propõe estratégias para aumentar a escalabilidade e melhorar a arquitetura do Map-OS:</p>

<h4>Proposta de Escalabilidade</h4>
<ul>
  <li><strong>Escalabilidade Vertical:</strong> Recomenda-se a melhoria do hardware do servidor, incluindo aumento de memória e poder de processamento para suportar maiores volumes de dados e usuários.</li>
  <li><strong>Escalabilidade Horizontal:</strong> Implementação de balanceamento de carga e configuração de clusters de servidores para distribuir as requisições e aumentar a disponibilidade do sistema.</li>
</ul>

<h4>Proposta de Refatoração</h4>
<ul>
  <li><strong>Modularização de Funcionalidades:</strong> Refatorar o código para melhorar a separação de responsabilidades, facilitando a manutenção e adição de novas funcionalidades.</li>
  <li><strong>Otimização do Banco de Dados:</strong> Propor melhorias nas consultas SQL e na estrutura do banco de dados para aumentar a eficiência no processamento de grandes volumes de dados.</li>
</ul>

<h4>Conclusão</h4>
<p>Na conclusão, será feito um resumo das análises realizadas e das propostas de melhoria, destacando como essas sugestões podem impactar positivamente a performance e a manutenção do sistema Map-OS.</p>

<h4>Referências</h4>
<ul>
  <li><a href="https://github.com/RamonSilva20/mapos">Repositório Oficial do Map-OS</a></li>
  <li><a href="https://codeigniter.com/userguide3/">Documentação do CodeIgniter</a></li>
  <li><a href="https://dev.mysql.com/doc/">Documentação do MySQL</a></li>
</ul>