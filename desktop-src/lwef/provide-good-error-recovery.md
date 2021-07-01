---
title: Fornecer uma boa recuperação de erro
description: Fornecer uma boa recuperação de erro
ms.assetid: 48e00638-9274-49db-93ec-ed444f526441
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a20a3d203ab0fcd93a6f4645be4af44b049f3cd
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120791"
---
# <a name="provide-good-error-recovery"></a>Fornecer uma boa recuperação de erro

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Assim como ocorre com qualquer interface bem projetada, o processo interativo deve minimizar as circunstâncias que levam a erros. No entanto, raramente é possível eliminar todos os erros, portanto, dar suporte à boa recuperação de erros é essencial para manter a confiança e o interesse do usuário. Em geral, a recuperação de erro envolve detectar um erro, determinar a causa e definir uma maneira de resolver o erro. Os usuários respondem melhor às interfaces que são cooperativas, que trabalham com o usuário para realizar uma tarefa.

A primeira etapa na recuperação de erro de fala é detectar a condição de falha. O reconhecimento de fala pode falhar devido a uma variedade de erros. As condições de erro geralmente podem ser detectadas como resultado de entrada inválida, correção explícita do usuário ou cancelamento ou repetição do usuário.

Um *erro de rejeição* ocorre quando o mecanismo de reconhecimento não tem nenhuma corresponder ao que o usuário disse. Ruído em segundo plano ou inícios iniciais também são causas comuns de falha de reconhecimento, portanto, pedir ao usuário para repetir um comando geralmente é uma boa solução inicial. No entanto, se a frase estiver fora da gramática ativa atual, pedir ao usuário para reformular a solicitação poderá resolver o problema. A diferença na redação pode resultar em uma combinação com algo na gramática atual. Listar ou sugerir opções de entrada esperadas apropriadas é outra alternativa.

Uma boa estratégia para a recuperação de erros de rejeição é combinar essas técnicas para que o usuário volte ao caminho certo, oferecendo cada vez mais assistência se a falha persistir. Por exemplo, você pode começar respondendo à falha inicial com um interrogativo como "Paulo?" ou "O quê?" ou um gesto de mão para o ouvido. Uma resposta curta aumenta a probabilidade de que a instrução repetida do usuário não falhe porque o usuário fala muito cedo. Após uma falha repetida, a solicitação subsequente de reformulação melhora a chance de corresponder algo dentro da gramática determinada. Daqui em diante, fornecer prompts explícitos de comandos aceitos aumenta ainda mais a chance de uma combinação. Essa técnica é ilustrada no exemplo a seguir:

**Usuário:** eu gostaria de uma pizza no estilo Chicago com anáries.

**Caractere:**(Hand to ear) Boo?

**Usuário:** quero uma pizza de Chicago com anáries.

**Caractere**: (balancear a cabeça) Reformular sua solicitação.

**Usuário:** eu disse pizza de Chicago, com anáries.

**Caractere**: (Sh sh sh. Diga-me o estilo de pizza que você deseja.

**Usuário:** Chicago, com anáries.

**Caractere:** ainda sem sorte. Veja o que você pode dizer: "Chicago", "Desintente" ou "Combinação".

Para tornar o tratamento de erro mais natural, certifique-se de fornecer um grau de variação aleatória ao responder a erros. Além disso, uma reação do usuário natural a qualquer solicitação para repetir uma resposta é desabocar ou aumentar o volume ao repetir a instrução. Pode ser útil ocasionalmente lembrar o usuário de falar normalmente e claramente, pois a desrecisão ou o aumento do volume pode dificultar o reconhecimento das palavras pelo mecanismo de fala.

A assistência progressiva deve fazer mais do que chamar o erro para a atenção do usuário; ele deve orientar o usuário para falar na gramática atual fornecendo sucessivamente mais mensagens informativas. Interfaces que parecem estar tentando entender incentivam um alto grau de satisfação e tolerância do usuário.

*Erros de substituição*, em que o mecanismo de fala reconhece a entrada, mas corresponde ao comando errado, são mais difíceis de resolver porque o mecanismo de fala detecta um enunciado correspondente. Uma incompatibilidade também pode ocorrer quando o mecanismo de fala interpreta sons estranho como entrada válida (também conhecido como erro *de inserção*). Nessas situações, a assistência do usuário é necessária para identificar a condição de erro. Para fazer isso, você pode repetir o que o mecanismo de fala retornou e pedir ao usuário para confirmá-lo antes de continuar:

**Usuário:** eu gostaria de uma pizza no estilo Chicago.

**Caractere:** você disse que gostaria de uma "pizza no estilo Chicago"?

**Usuário:** Sim.

**Caractere:** quais ingredientes adicionais você gostaria?

**Usuário:** Anções.

**Caractere:** você disse "aniaies"?

**Usuário:** Sim.

No entanto, o uso dessa técnica para cada enunciado torna-se ineficiente e cansativa. Para lidar com isso, restrinja a confirmação a situações que têm consequências negativas significativas ou aumente a complexidade da tarefa imediata. Se for fácil para o usuário fazer ou reverter alterações, você poderá evitar solicitar confirmação de suas escolhas. Da mesma forma, se você fizer escolhas visíveis, talvez não precise fornecer correção explícita. Por exemplo, escolher um item de uma lista pode não exigir verificação porque o usuário pode ver os resultados e alterá-los facilmente. Você também pode usar pontuações alternativas e de confiança para fornecer um limite para confirmação. Você pode ajustar o limite mantendo um histórico das ações do usuário em uma determinada situação e eliminando a verificação com base na confirmação consistente do usuário. Por fim, considere a natureza multi modal da interface. A confirmação do mouse ou do teclado também pode ser apropriada.

Escolha cuidadosamente o texto das confirmações. Por exemplo, "Você disse...?" ou "Acho que você disse..." são melhores do que "Você realmente deseja...?" porque as frases antigas implicam que a precisão da escuta do caractere (reconhecimento) está sendo consultada, não que o usuário possa ter feito o erro.

Considere também a gramática para uma resposta. Por exemplo, uma resposta negativa provavelmente gerará um erro de rejeição, exigindo um prompt adicional, conforme mostrado no exemplo a seguir:

**Usuário:** eu gostaria de um pouco de pimentão.

**Caractere:** você disse "sem ham"?

**Usuário:** Não, eu disse pimentão.

**Caractere**: Personagem?

**Usuário:** Pimentão.

Modificar sua gramática para incluir prefixos para lidar com variações de resposta natural aumenta a eficiência do processo de recuperação, especialmente quando o usuário não confirma o prompt de verificação. Neste exemplo, a confirmação pode ter sido manipulada em uma única etapa modificando a gramática para o "pimentão" incluindo também "não disse pimentão", "Eu disse pimentão" e "sem pimentão".

Você também pode tratar erros de substituição usando as correspondeções alternativas retornadas pelo mecanismo de fala como a confirmação corretiva:

**Usuário:** eu gostaria de um pouco de pimentão.

**Caractere**: (escuta "sem ham" como melhor combinação, "pimentão" como a primeira alternativa) Você disse "sem ham"?

**Usuário:** não, pimentão.

**Caractere**: (ainda escuta "sem ham" como melhor combinação, mas agora oferece a primeira alternativa) "Pimentão"?

Da mesma forma, você pode manter um histórico de erros comuns de substituição e, se um erro específico for frequente, ofereça a alternativa na primeira vez.

Em qualquer situação de erro de reconhecimento, evite desamocar o usuário. Se o caractere sugerir ou até mesmo implicar que o usuário é o responsável ou se o caractere parecer suspeito para o erro, o usuário poderá se sentir errado. Aqui também, escolha cuidadosamente as palavras que aceitam explicitamente a responsabilidade, é apropriada para a situação e usa a variedade para criar uma resposta mais natural. Ao expressar uma expressão, evite palavras ambíguas, como "oops" ou "uh-oh", que podem ser interpretadas como desajosando o usuário. Em vez disso, use frases como "Me desculpe" ou "Meu erro". Erros repetidos ou mais sérios podem usar um mais elaborado, como "Eu realmente estou triste sobre isso". Considere também a personalidade do caractere ao determinar o tipo de resposta. Outra opção é responsabilizar uma situação externa. Comentários como "Meu filho, está barulhento lá fora", levam a responsabilidade do usuário e do caractere. Lembrar o usuário da natureza cooperativa da interação também pode ser útil: considere frases como "Vamos ver o que podemos fazer para fazer isso funcionar".

O Microsoft Agent também dá suporte a alguns comentários automáticos para reconhecimento. Quando um enunciado é detectado, a Dica de Escuta exibe o texto de voz da melhor combinação escutada. Você pode definir seu próprio texto a ser exibido com base na configuração de confiança para um comando que você definir.

Devido ao potencial de erro, sempre exige confirmação para qualquer opção que tenha consequências negativas graves e que sejam irreversíveis. Naturalmente, você deve exigir confirmação quando os resultados de uma ação puderem ser destrutivas. No entanto, considere também exigir confirmação para situações que anulam qualquer operação ou processo demorado.

 

 




