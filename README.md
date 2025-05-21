# Bootcamp-Bradesco-Cloud

# Principais Recursos do Microsoft Azure

## O que é o Azure?

O Microsoft Azure é como alugar computadores e serviços de TI pela internet, em vez de comprar e manter equipamentos próprios. Você paga apenas pelo que usar, como uma conta de luz.

## Área de Trabalho Virtual do Azure

### O que faz?

Permite usar um computador completo através da internet. É como acessar seu computador do trabalho de casa, mas o computador na verdade está nos servidores da Microsoft.

### Por que usar?

Você pode trabalhar de qualquer lugar, em qualquer dispositivo. Seus arquivos e programas ficam seguros na nuvem, não no seu computador pessoal.

### Exemplo prático

Uma empresa quer que seus funcionários trabalhem de casa, mas precisa que todos usem os mesmos programas e tenham acesso aos mesmos arquivos. Com a Área de Trabalho Virtual, cada funcionário acessa o mesmo ambiente de trabalho, não importa se está em casa, no escritório ou viajando.

## Chaves SSH

### O que são?

É um método super seguro para acessar computadores remotamente. Em vez de usar senha (que pode ser descoberta), você usa um par de "chaves digitais".

### Como funciona?

Imagine uma fechadura especial onde só existe uma chave no mundo inteiro que a abre. A "fechadura" fica no servidor que você quer acessar, e a "chave" fica só com você.

### Vantagem principal

É praticamente impossível de ser hackeado, muito mais seguro que senhas normais.

## Contas de Lab

### Para que serve?

É como uma sala de aula virtual onde um professor pode criar computadores para os alunos usarem durante as aulas.

### Como funciona?

O professor configura um ambiente (como um computador com programas específicos instalados) e automaticamente cria cópias desse ambiente para cada aluno.

### Exemplo de uso

Um curso de programação onde todos os alunos precisam usar o mesmo software. Em vez de cada aluno instalar complicadas ferramentas no seu computador, todos acessam máquinas virtuais já prontas.

## Conjuntos de Dimensionamento de Máquinas Virtuais

### O que resolve?

Automaticamente adiciona ou remove servidores conforme a necessidade, como ter mais garçons num restaurante quando está cheio.

### Como funciona?

Você define regras como "se muitas pessoas estão acessando meu site ao mesmo tempo, adicione mais servidores automaticamente".

### Exemplo real

Um site de vendas online que normalmente usa 5 servidores, mas na Black Friday precisa de 50 servidores. O sistema automaticamente liga 45 servidores extras durante o pico e os desliga depois, assim você só paga pelos servidores extras quando realmente precisa.

## Coleções de Ponto de Restauração

### O que são?

São como "fotografias" do seu servidor em diferentes momentos. Se algo der errado, você pode voltar para uma "foto" anterior quando tudo estava funcionando.

### Como ajuda?

Se você fez uma atualização que quebrou o sistema, ou se alguém apagou arquivos importantes, você pode restaurar tudo para como estava antes do problema.

### Comparação simples

É como o "Ctrl+Z" do computador, mas para servidores inteiros. Você pode desfazer mudanças que deram errado.

## Conjuntos de Disponibilidade

### O que garantem?

Que seu sistema continue funcionando mesmo se algum equipamento quebrar no datacenter da Microsoft.

### Como funciona?

Em vez de colocar todos os seus servidores virtuais no mesmo "rack" físico, o Azure os espalha em diferentes locais. Se um rack tiver problema, os outros continuam funcionando.

### Analogia

É como não colocar todos os seus ovos na mesma cesta. Se uma cesta cair, você ainda tem ovos nas outras cestas.

## Como esses recursos trabalham juntos

Imagine uma escola online que usa todos esses recursos:

A escola usa **Contas de Lab** para criar ambientes de estudo para os alunos. Esses ambientes rodam em **Conjuntos de Dimensionamento** que automaticamente criam mais salas virtuais quando muitos alunos se conectam ao mesmo tempo.

Os professores acessam o sistema de administração usando **Chaves SSH** para máxima segurança. Alguns cursos avançados usam **Área de Trabalho Virtual** para dar acesso a softwares especializados.

Todo o sistema é protegido por **Conjuntos de Disponibilidade** para garantir que as aulas nunca sejam interrompidas por problemas técnicos. E **Coleções de Ponto de Restauração** fazem backup de tudo automaticamente, caso precise recuperar alguma informação.

## Começando

Para quem está começando, o Azure oferece contas gratuitas para experimentar esses serviços. A documentação oficial da Microsoft tem tutoriais passo a passo para each um desses recursos.
