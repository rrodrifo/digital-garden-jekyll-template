Blockchain

Repositório de textos, artigos, fontes, notícias e exemplos relacionados ao Blockchain.

[[NFTs]]
[[Attack of the 50 foot Blockchain]]
[[Gasto energético do blockchain]]


### Bitcoin

> Short Version

> 1) Should I buy Bitcoins?

> No.

> 2) But I keep seeing all this stuff in the news about them and how

> No. Tech journalism is uniformly terrible, always remember this.

> 3) How does this work? It doesn’t make any sense!

> No, it really doesn’t. It’s impossible to accurately explain Bitcoin in anything less than mind-numbingly 
> boring technical terms so you should probably just not worry about it. Go do something useful instead.

> --- David Gerard, "Attack of the 50 foot Blockchain"

O bitcoin surgiu durante a explosão da crise econômica de 2008 como uma resposta à desconfiança em relação aos bancos centrais e ao poder do Estado em interferir na economia por meio de política monetária. Seu objetivo inicial, conforme descrito no White Paper publicado pelo anônimo Satoshi Nakamoto, era o de permitir pagamentos online enviados diretamente de uma parte para a outra sem a necessidade de passar por instituições financeiras por meio de uma versão peer-to-peer do dinheiro eletrônico.  

Para tanto, um fator essencial é a garantia de confiança. Sem a presença de bancos ou outras instituições financeiras mediadas pelo Estado, é necessário que esteja presente alguma estrutura confiável que possa comprovar as transações e impedir o gasto duplo. 

A proposta do bitcoin é então a de garantir a confiança nos sistemas de pagamento eletrônico por meio de provas criptográficas (matemáticas). 

Imagine 1 Bitcoin como uma moeda com um dono. A identificação do dono (uma chave criptográfica pública) fica registrada na própria moeda, e cada vez que a moeda é passada a um novo dono a identificação deste novo dono é gravada na moeda sem apagar as identificações dos antigos proprietários. Assim é feito um registro cronológico de todos os donos da moeda. (Este registro atua como um livro razão (ledger), que será a base para o blockchain).

Sendo essa moeda digital, surge um problema: o dono da moeda poderia facilmente “duplicar” o arquivo da moeda em sua posse e repassar duas vezes a mesma moeda para pessoas diferentes, registrando a identificação de cada uma nas diferentes moedas. Essa multiplicação poderia ser feita infinitamente, desvalorizando completamente a moeda. 

Para impedir que isto ocorra, é necessário que todos saibam de todas as transações que ocorrem por meio do anúncio público de todas as transações, somado com algum método para dar segurança ao receptor da moeda de que a parte que a está enviando não enviou aquela mesma moeda a qualquer outra pessoa anteriormente. 

Este método é o que se chama de blockchain.

Blockchain literalmente significa uma cadeia de blocos consecutivos. No caso do bitcoin, o blockchain funciona quando uma série de informações sobre as moedas existentes são gravadas em um bloco. Informações sobre quantas moedas existem e quais as identidades de seus donos, por exemplo, são registradas em um bloco, e esse bloco gera um hash.

Um “hash” é como uma representação numérica de uma parte de um arquivo, uma identidade única gerada quando se passa parte de um arquivo por uma função matemática hash (MORO; ZHANG; TSOTRAS, 2009). 

Ao se passar a frase “The quick brown fox jumps over the lazy dog” pela função hash SHA-512, por exemplo, temos como resultado o resumo hash 
> 07E547D9586F6A73F73FBAC0435ED76951
> 218FB7D0C8D788A309D785436BBB642E9A
> 252A954F23912547D1E8A3B5ED6E1BFD70
> 97821233FA0538F3DB854FEE. 

Como cada hash é praticamente único, e como os hashes são criados a partir de pequenos recortes de cada bloco, qualquer ligeira modificação em um bloco modifica completamente o seu hash. 

Além do hash, cada bloco recebe um timestamp que registra o momento em que foi criado.

### Proof-of-Work

A garantia de que o bloco não foi alterado e suas informações são legítimas se dá por meio de um processo chamado Proof-of-Work (PoW). Este processo consiste de diferentes computadores jogando valores aleatórios (nonces) na função hash com a esperança de chegar no mesmo valor do hash escrito no bloco. 

Imagine que você não sabe matemática mas quer descobrir a resposta da equação 3x = 15. Você pode trocar números aleatórios por X até chegar na solução do problema quando jogar o número 5. 

Agora imagine isso só que em uma equação cujo resultado é um algoritmo de 64 dígitos incluindo números de 0 a 9 e letras de A até F. Para chegar nesse resultado é necessário que milhares de computadores tentem aleatoriamente milhares de valores distintos até que algum deles encontre o valor que corretamente chega na resposta da equação.

Esse é o processo que os chamados “Miners” ou mineradores fazem com o bitcoin. Cada minerador utiliza o poder computacional dos computadores a sua disposição para tentar validar um bloco por meio do Proof-of-Work, e cada vez que um minerador encontra o nonce correto para validar o bloco ele recebe um valor em troca (em 2019 esse valor era de 12.5 Bitcoins por bloco validado).

Como é fácil de constatar, esse não é um processo muito eficiente, mas é uma das poucas maneiras já implementadas de garantir a validade da informação de forma descentralizada. Importante notar que todo esse trabalho feito pelos mineradores é necessário somente porque os usuários do bitcoin não querem depender de nenhuma autoridade central confiável que possa validar os blocos. 

Nos bancos tradicionais, o próprio banco mantém um registro das transações e consegue facilmente validar as transações sem precisar do Proof-of-Work, e todo o desperdício de poder computacional gasto com esse processo é o custo para manter um sistema descentralizado sem depender da confiança em um ator central. 

Sabendo o que é Proof-of-Work e considerando que um Node é um computador presente na rede do bitcoin, podemos visualizar o funcionamento dessa rede da seguinte forma:

> The steps to run the network are as follows:

> 1) New transactions are broadcast to all nodes.
> 2) Each node collects new transactions into a block.
> 3) Each node works on finding a difficult proof-of-work for its block.
> 4) When a node finds a proof-of-work, it broadcasts the block to all nodes.
> 5) Nodes accept the block only if all transactions in it are valid and not already spent.
> 6) Nodes express their acceptance of the block by working on creating the next block in the chain, using the hash of the accepted block as the previous hash.

> --- Satoshi Nakamoto, "Bitcoin: a peer-to-peer Electronic cash system"

<img src="/assets/bloco.png"/>

### Outras aplicações do blockchain

O bitcoin e outras criptomoedas não são as únicas utilizações possíveis da estrutura do blockchain. Com a explosão em popularidade do bitcoin a partir de 2011 diversas propostas foram criadas para a utilização desse método tanto nos setores privados quanto públicos. 

<img src="/assets/propostas.png"/>

Ao pensar na aplicação do blockchain em outras áreas e projetos é importante sempre manter em mente quais são as principais características do blockchain e comparar se estas características realmente resolvem os problemas que se pretende resolver com sua aplicação.

É importante notar que o blockchain é uma estrutura de registro de dados imutável e descentralizada. Isso significa que qualquer um poderá tentar adicionar novos dados (em um blockchain público “permissionless”). Significa também que será impossível modificar ou corrigir dados após a aceitação do bloco em que estes se encontram. 

Além disso, como já foi mostrado acima o Proof-of-Work é um método de garantia de confiança extremamente ineficiente é com alto custo energético, visto que o poder computacional é decorrente de gastos com energia elétrica. Não faz sentido implementar sistemas que se utilizem do PoW e tragam enorme gasto energético em ambientes nos quais já há uma autoridade confiável. 

<img src="/assets/flow1.jpg"/>     <img src="/assets/flowchart.png"/>
