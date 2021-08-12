---
title: Fornecer uma boa recuperação de erro
description: Fornecer uma boa recuperação de erro
ms.assetid: 48e00638-9274-49db-93ec-ed444f526441
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486e6db4365e9a279c844e7637ca3281a66b51a2e47d6d2d74d374ab4c55f146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246916"
---
# <a name="provide-good-error-recovery"></a>Fornecer uma boa recuperação de erro

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Assim como acontece com qualquer interface bem projetada, o processo interativo deve minimizar as circunstâncias que levam a erros. No entanto, raramente é possível eliminar todos os erros, portanto, dar suporte à boa recuperação de erro é essencial para manter a confiança e o interesse do usuário. Em geral, a recuperação de erros envolve a detecção de um erro, a determinação da causa e a definição de uma maneira de resolver o erro. Os usuários respondem melhor às interfaces que são cooperativas, que trabalham com o usuário para realizar uma tarefa.

A primeira etapa na recuperação de erro de fala é detectar a condição de falha. O reconhecimento de fala pode falhar devido a uma variedade de erros. As condições de erro geralmente podem ser detectadas como resultado de entrada inválida, correção explícita do usuário ou cancelamento ou repetição do usuário.

Um *erro de rejeição* ocorre quando o mecanismo de reconhecimento não tem nenhuma correspondência para o que o usuário disse. Ruídos de fundo ou inícios antecipados também são causas comuns de falha de reconhecimento, portanto, pedir ao usuário para repetir um comando é, muitas vezes, uma boa solução inicial. No entanto, se a frase estiver fora da gramática ativa atual, pedir ao usuário para reformular a solicitação pode resolver o problema. A diferença no texto pode resultar em uma correspondência com algo na gramática atual. A listagem ou a sugestão de opções de entrada esperadas apropriadas é outra alternativa.

Uma boa estratégia para a recuperação de erros de rejeição é combinar essas técnicas para que o usuário volte a acompanhar, oferecendo mais assistência se a falha persistir. Por exemplo, você pode começar respondendo à falha inicial com uma interrogação como "não?" ou "o quê?" ou um gesto de mão-para-Ear. Uma resposta curta aumenta a probabilidade de que a instrução repetida do usuário não falhe, pois o usuário falou muito cedo. Após uma falha repetida, a solicitação subsequente para reformular melhora a chance de correspondência de algo dentro de uma determinada gramática. A partir daqui, o fornecimento de prompts explícitos de comandos aceitos aumenta ainda mais a chance de uma correspondência. Essa técnica é ilustrada no exemplo a seguir:

**Usuário**: Eu gostaria de ter uma pizza estilo Chicago com anchovies.

**Caractere**: (mão para EAR) não?

**Usuário**: desejo uma pizza de Chicago com anchovies.

**Caractere**: (agite cabeça) reformular sua solicitação.

**Usuário**: Eu disse Chicago pizza, com anchovies.

**Caractere**: (ombros) eu sinto. Diga-me o estilo de pizza que você deseja.

**Usuário**: Chicago, com anchovies.

**Caractere**: ainda não há sorte. Veja o que você pode dizer: "Chicago", "havaiano" ou "combo".

Para que o tratamento de erros fique mais natural, certifique-se de fornecer um grau de variação aleatória ao responder a erros. Além disso, uma reação natural do usuário a qualquer solicitação para repetir uma resposta é exagerar ou aumentar o volume ao repetir a instrução. Pode ser útil lembrar ocasionalmente o usuário de falar normalmente e de forma clara, pois o volume mais complicado ou maior pode dificultar o reconhecimento das palavras no mecanismo de fala.

A assistência progressiva deve fazer mais do que trazer o erro para a atenção do usuário; Ele deve orientar o usuário para falar sobre a gramática atual fornecendo sucessivamente mais mensagens informativas. As interfaces que parecem estar tentando entender estimulam um alto grau de satisfação e tolerância do usuário.

*Erros de substituição*, em que o mecanismo de fala reconhece a entrada, mas corresponde ao comando errado, é mais difícil de resolver porque o mecanismo de fala detecta um expressão correspondente. Uma incompatibilidade também pode ocorrer quando o mecanismo de fala interpreta sons incorretos como uma entrada válida (também conhecida como um *erro de inserção*). Nessas situações, a assistência do usuário é necessária para identificar a condição de erro. Para fazer isso, você pode repetir o que o mecanismo de fala retornou e pedir ao usuário para confirmá-lo antes de continuar:

**Usuário**: Eu gostaria de ter uma pizza estilo Chicago.

**Caractere**: você disse que gostaria de uma "pizza estilo Chicago"?

**Usuário**: Sim.

**Caractere**: Quais ingredientes adicionais você gostaria?

**Usuário**: anchovies.

**Caractere**: você disse "anchovies"?

**Usuário**: Sim.

No entanto, usar essa técnica para cada expressão se torna ineficiente e cansativo. Para lidar com isso, restrinja a confirmação para situações que tenham consequências negativas significativas ou aumente a complexidade da tarefa imediata. Se for fácil para o usuário fazer ou reverter alterações, você poderá evitar a solicitação de confirmação de suas escolhas. Da mesma forma, se você tornar as escolhas visíveis, talvez não seja necessário fornecer uma correção explícita. Por exemplo, a escolha de um item de uma lista pode não exigir verificação, pois o usuário pode ver os resultados e alterá-los facilmente. Você também pode usar as pontuações de confiança e alternativas para fornecer um limite de confirmação. Você pode ajustar o limite mantendo um histórico das ações do usuário em uma determinada situação e eliminando a verificação com base na confirmação consistente do usuário. Por fim, considere a natureza de várias modalidades da interface. A confirmação do mouse ou do teclado também pode ser apropriada.

Escolha cuidadosamente a palavra de confirmações. Por exemplo, "você disse...?" ou "Acho que você disse..." é melhor do que "você realmente quer...?" Porque as frases anteriores sugerem que a precisão da escuta do caractere (reconhecimento) está sendo consultada, e não que o usuário pode ter um spoke incorreto.

Considere também a gramática de uma resposta. Por exemplo, uma resposta negativa provavelmente gerará um erro de rejeição, exigindo um prompt adicional, conforme mostrado no exemplo a seguir:

**Usuário**: Eu gostaria de alguma pepperoni.

**Caractere**: você disse "sem Ham"?

**Usuário**: não, eu disse pepperoni.

**Caractere**: não?

**Usuário**: pepperoni.

Modificar sua gramática para incluir prefixos para lidar com variações de resposta naturais aumenta a eficiência do processo de recuperação, especialmente quando o usuário não confirma o prompt de verificação. Neste exemplo, a confirmação poderia ter sido tratada em uma única etapa modificando a gramática para "pepperoni" incluindo também "não disse pepperoni", "Eu disse pepperoni" e "no pepperoni".

Você também pode manipular erros de substituição usando as correspondências alternativas retornadas pelo mecanismo de fala como a confirmação corretiva:

**Usuário**: Eu gostaria de alguma pepperoni.

**Caractere**: (ouve "sem Ham" como a melhor correspondência, "pepperoni" como primeira alternativa) você disse "no Ham"?

**Usuário**: não, pepperoni.

**Caractere**: (ainda ouve "sem Ham" como a melhor correspondência, mas agora oferece a primeira alternativa) "pepperoni"?

Da mesma forma, você pode manter um histórico dos erros de substituição comuns e, se um erro específico for freqüente, oferecer a alternativa na primeira vez.

Em qualquer situação de erro de reconhecimento, evite culpando o usuário. Se o caractere sugerir ou até mesmo implica que o usuário é culpado ou o caractere parece não ser diferente do erro, o usuário pode se tornar incomodados. Aqui, você também escolhe cuidadosamente as palavras que aceitam explicitamente a responsabilidade, é apropriado para a situação e usa a variedade para criar uma resposta mais natural. Ao expressar um Desculpa, evite palavras ambíguas como "Ops" ou "Ah-Oh" que poderiam ser interpretadas como culpando usuário. Em vez disso, use frases como "Desculpe" ou "meu erro". Erros repetidos ou mais graves podem usar um desculpa mais elaborado como "Eu realmente sinto isso". Considere também a personalidade do caractere ao determinar o tipo de resposta. Outra opção é a culpa de uma situação externa. Comentários como "menino, está com ruídos", retire o culpado do usuário e do caractere. Lembrar o usuário da natureza cooperativa da interação também pode ser útil: considere frases como, "Vamos ver o que podemos fazer para fazer isso funcionar".

O Microsoft Agent também dá suporte a alguns comentários automáticos para reconhecimento. Quando um expressão é detectado, a dica de escuta exibe o texto de voz da melhor correspondência ouvida. Você pode definir seu próprio texto para ser exibido com base na configuração de confiança para um comando que você definir.

Devido ao erro potencial, sempre exija confirmação para qualquer opção que tenha conseqüências negativas sérias e seja irreversível. Naturalmente, você desejará exigir confirmação quando os resultados de uma ação puderem ser destrutivos. No entanto, considere também exigir confirmação para situações que anulem qualquer processo ou operação demorada.

 

 




