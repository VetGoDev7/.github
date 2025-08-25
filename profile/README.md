# Vet Go 🐾 

A VetGo é uma clínica veterinária digital moderna, especializada no atendimento de animais de pequeno porte, especificamente cães e gatos. A plataforma tem como objetivo facilitar o acesso de tutores aos serviços oferecidos pela clínica, otimizando o processo de agendamento, cadastro e acompanhamento de profissionais. A clínica conta com uma equipe de médicos veterinários com diferentes especializações, e busca garantir um atendimento acolhedor, prático e eficaz para os animais e seus tutores.

Professor: [Marco André Mendes](github.com/marcoandre)

## Equipe:

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/GabrieliMarta.png" width="100px;" alt="Foto do membro"/><br />
      <sub><b>Gabrieli Rocha</b></sub>
    </td>
    <td align="center">
      <img src="https://github.com/Rafabitte17.png" width="100px;" alt="Foto do membro"/><br />
      <sub><b> Rafael Bittencourt</b></sub>
    </td>
  </tr>
</table>

# Links do projeto:

-   Backend: [VetGo-Backend](https://github.com/VetGoDev7/VetGo-Backend.git) | [Render](https://vetgo-backend.onrender.com)
-   Frontend: [VetGo-Frontend](https://github.com/VetGoDev7/VetGo-Frontend.git) | [Vercel](https://vet-go-frontend-ft967ixx1-gabrielimartas-projects.vercel.app)
  
-   Figma: [VetGO-Figma](https://www.figma.com/design/4HrIaF1HcX1gVBJ93KZihL/VetGo?node-id=0-1&t=HmxWiTJKUazFVIeo-1)
-   Docs: [VetGo-Docs](https://github.com/VetGoDev7/.github.git)


# 1. Desenvolvimento

 **Ordem de Serviço (O.S.)**

O sistema escolhido pela equipe será voltado para uma clínica veterinária específica, representada pela marca VetGo. Diferente de uma plataforma que conecta profissionais diversos, a VetGo funcionará como uma única clínica digital com foco em prestar serviços veterinários exclusivamente para cães e gatos. A proposta é criar uma solução web que permita o agendamento de consultas, cadastro de tutores e pets, além de gerenciar o cadastro dos veterinários que atuam na clínica. A plataforma será simples, intuitiva e voltada à experiência do usuário, visando facilitar o atendimento e otimizar a gestão interna da clínica.


# 2. Situação Problema

- A VetGo é uma clínica veterinária que atua com foco no atendimento de animais de pequeno porte, ou seja, cães e gatos. A clínica oferece diferentes serviços voltados ao cuidado desses pets, contando com uma equipe de médicos veterinários especializados. Atualmente, a gestão dos atendimentos e cadastros é feita de forma manual, o que pode gerar atrasos, desencontros de informação e dificuldade na organização dos agendamentos.

- Além disso, o processo de marcação de consultas é feito presencialmente ou por contato direto (telefone/WhatsApp), o que demanda tempo da equipe e pode gerar conflitos de horário ou sobrecarga nos atendimentos. Médicos também não possuem uma interface própria para organizar seus atendimentos e registrar sua especialidade.

- Diante desses desafios, percebe-se a necessidade de um sistema digital que centralize o gerenciamento da clínica, desde os cadastros de clientes e médicos até os agendamentos e organização dos serviços prestados. Isso permitirá maior controle, agilidade no atendimento, organização interna e uma experiência mais eficiente para os tutores.


# 3. Descrição da Proposta 

A proposta do projeto VetGo é desenvolver um sistema web para uso interno de uma clínica veterinária, com funcionalidades que atendam tanto os tutores quanto os médicos veterinários. A plataforma permitirá que tutores cadastrem seus dados e os de seus pets (apenas cães e gatos), visualizem os serviços disponíveis e realizem agendamentos online com base na especialidade do médico veterinário.

O sistema contará com três tipos de usuários:

- Administrador: responsável por aprovar ou cadastrar médicos veterinários, gerenciar os agendamentos e supervisionar o sistema.

- Veterinário: profissional que poderá se cadastrar (ou ser cadastrado), informar sua especialidade (ex: clínico geral, vacinação, etc.) e visualizar seus agendamentos.

- Tutor (cliente): poderá criar sua conta, cadastrar seu pet, visualizar os serviços da clínica e agendar consultas com base nas especialidades dos médicos.

# 4. Regras de negócio

- **RN01 - Cadastro de Veterinários:** Apenas médicos veterinários previamente cadastrados pelo administrador poderão atender na plataforma. Eles serão visíveis na listagem de agendamentos de acordo com sua especialidade.

- **RN02 - Cadastro de Tutores e Pets:** Cada tutor pode possuir uma única conta e poderá cadastrar múltiplos pets, sendo obrigatória a definição de espécie (apenas cães ou gatos), idade, raça e observações de saúde.

- **RN03 - Associação única de pet:** Um animal poderá estar vinculado a apenas um tutor no sistema, não sendo possível compartilhamento entre contas.

- **RN04 -  Filtros sem resultados:** Se durante o agendamento, o tutor não encontrar veterinários disponíveis para o tipo de serviço desejado, o sistema deve informar de forma clara que não há profissionais disponíveis no momento.

- **RN05 - Retorno vazio na busca por profissionais:** Quando não houver profissionais compatíveis com o tipo de animal e a localização selecionados, o sistema deverá informar claramente ao usuário que não há resultados disponíveis no momento.
  
- **RN06 - Atualização de dados pelos veterinários::** Os veterinários poderão atualizar suas informações de contato e especialidade dentro do sistema. O não preenchimento ou informações incorretas poderão limitar sua exibição na listagem de agendamento.

- **RN007 -  Login único:** Todos os usuários do sistema (tutores, veterinários e administradores) deverão possuir um login único baseado em e-mail para acesso à plataforma.

- **RN008 – Permissão do administrador:** Somente o administrador poderá cadastrar, aprovar ou remover veterinários no sistema. Também será responsável por visualizar e gerenciar todos os agendamentos realizados na clínica.

- **RN010 – Serviços fixos da clínica:** Os serviços disponíveis para agendamento são definidos previamente pela administração da VetGo, e não poderão ser adicionados ou modificados pelos veterinários.



# Requisitos Funcionais:




- **RF001** – O sistema deve permitir o cadastro de tutores com dados pessoais e informações dos seus pets (nome, espécie, raça, idade, peso, histórico de saúde).

- **RF002** – O sistema deve permitir o cadastro de veterinários, com informações como nome, especialidade, contato e horário de atendimento.

- **RF003** – O sistema deve permitir que apenas o administrador cadastre os veterinários.

- **RF004** – O sistema deve permitir que tutores, veterinários e administradores façam login por meio de e-mail e senha.

- **RF005** – O sistema deve permitir que os tutores visualizem os veterinários disponíveis na clínica com base na especialidade selecionada.

- **RF006** – O sistema deve permitir que os tutores realizem agendamentos informando o pet, o tipo de serviço desejado e o veterinário disponível.

- **RF007** – O sistema deve permitir que o administrador e os veterinários visualizem, editem e cancelem os agendamentos realizados.

- **RF008** – O sistema deve exibir os serviços disponíveis para consulta, previamente definidos pelo administrador.

- **RF009** – O sistema deve permitir que o tutor visualize o histórico de agendamentos e atendimentos de seus animais.





# Modelagem de Dados

![modelagem-vetgo]()

  
