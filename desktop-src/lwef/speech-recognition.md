---
title: Reconhecimento de fala
description: Reconhecimento de fala
ms.assetid: cb5ac509-12a4-4ca4-8776-424568cf780d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5c037ced96c386a5e0baf18eeba258422e0193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811687"
---
# <a name="speech-recognition"></a>Reconhecimento de fala

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O reconhecimento de fala fornece uma interface muito natural e familiar para interagir com caracteres. No entanto, a entrada de fala também apresenta muitos desafios. Atualmente, os mecanismos de fala funcionam sem partes substanciais do repertório de comunicação de fala humana, como gestos, intonation e expressões faciais. Além disso, a fala natural normalmente é desassociada. É fácil para o orador exceder o vocabulário atual ou a *gramática* do mecanismo. Da mesma forma, a palavra ou a ordem das palavras pode variar para qualquer solicitação ou resposta específica. Além disso, os mecanismos de reconhecimento de fala geralmente devem lidar com grandes variações no ambiente do orador. Por exemplo, ruído de fundo, qualidade do microfone e localização podem afetar a qualidade de entrada. Da mesma forma, pronúncias de alto-falantes ou até mesmo variações de alto-falante, como quando o orador tem um frio, torna-o um desafio para converter os dados acústicos em compreensão da apresentação. Por fim, os mecanismos de fala também devem lidar com palavras ou frases de som semelhantes em uma linguagem, como "novo", "soubesse" e "GNU", ou "amolecer uma boa praia" e "reconhecer a fala".

A fala nem sempre é a melhor forma de entrada para uma tarefa. Devido à natureza do processo de fala, geralmente pode ser mais lento do que outras formas de entrada. Como o teclado, a entrada de fala é uma interface ruim para apontar, a menos que algum tipo de representação mnemônico seja fornecido. Portanto, sempre considere se a fala é a entrada mais apropriada para uma tarefa. É melhor evitar o uso de fala como a interface exclusiva para qualquer tarefa. Fornecer outras maneiras de acessar qualquer funcionalidade básica usando métodos como o mouse ou o teclado. Além disso, aproveite a natureza de várias modalidades do uso de fala na interface visual combinando a entrada de fala com informações visuais que ajudam a especificar o contexto e as opções.

Por fim, o uso bem-sucedido da entrada de fala é devido apenas em parte da qualidade da tecnologia. Até mesmo o reconhecimento humano, que excede qualquer tecnologia de reconhecimento atual, às vezes falha. No entanto, na comunicação humana, usamos estratégias que melhoram a probabilidade de sucesso e que fornecem recuperação de erros quando algo dá errado. Portanto, a eficácia da entrada de fala também depende da qualidade da interface do usuário que a apresenta.

Estudar modelos humanos de interação de fala pode ser útil ao criar interfaces de fala mais naturais. A gravação de diálogos reais de fala humana para cenários específicos pode ajudá-lo a entender melhor as construções e os padrões usados, bem como formas efetivas de comentários e recuperação de erros. Ele pode ajudar a determinar o vocabulário apropriado a ser usado (para entrada e saída). É melhor criar uma interface de fala com base em como as pessoas realmente falam do que simplesmente derivar da interface gráfica na qual opera.

Observe que o Microsoft Agent usa o SAPI (Microsoft Speech API) para dar suporte ao reconhecimento de fala. Isso permite que o Microsoft Agent seja usado com uma variedade de mecanismos compatíveis. Embora o Microsoft Agent especifique determinadas interfaces básicas, os requisitos de desempenho e a qualidade de um mecanismo podem variar.

A fala não é o único meio de dar suporte a interfaces de conversação. Você também pode usar o processamento de idioma natural de entrada de teclado no lugar de ou além de fala. Nessas situações, você ainda pode aplicar diretrizes para entrada de fala.

-   [Escute, não apenas reconheça](listen--dont-just-recognize.md)
-   [Esclarecer e limitar opções](clarify-and-limit-choices.md)
-   [Fornecer uma boa recuperação de erro](provide-good-error-recovery.md)

 

 




