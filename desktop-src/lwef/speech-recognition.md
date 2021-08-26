---
title: Reconhecimento de fala
description: Reconhecimento de fala
ms.assetid: cb5ac509-12a4-4ca4-8776-424568cf780d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd36ea5754d53ceda2761635ecb838fdfb0328617827ca90fc969af915b4ea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960846"
---
# <a name="speech-recognition"></a>Reconhecimento de fala

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O reconhecimento de fala fornece uma interface muito natural e familiar para interagir com caracteres. No entanto, a entrada de fala também apresenta muitos desafios. Atualmente, os mecanismos de fala operam sem partes substanciais dopertoire de comunicação de fala humana, como gestos, etonação e expressões faciais. Além disso, a fala natural normalmente não é desaconsudida. É fácil para o locutor exceder o vocabulário atual ou *a* gramática do mecanismo. Da mesma forma, a palavra ou a ordem de palavras pode variar para qualquer solicitação ou resposta determinada. Além disso, os mecanismos de reconhecimento de fala geralmente devem lidar com grandes variações no ambiente do locutor. Por exemplo, o ruído de fundo, a qualidade do microfone e o local podem afetar a qualidade da entrada. Da mesma forma, pronúncias diferentes do locutor ou até mesmo variações do mesmo locutor, como quando o locutor tem um resfriado, torna um desafio converter os dados acústicos em compreensão representacional. Por fim, os mecanismos de fala também devem lidar com palavras ou frases semelhantes em um idioma, como "novo", "conhecido" e "gnu", ou "reconhecer uma boa praia" e "reconhecer fala".

A fala nem sempre é a melhor forma de entrada para uma tarefa. Devido à natureza de tomada de turnos da fala, ela geralmente pode ser mais lenta do que outras formas de entrada. Assim como o teclado, a entrada de fala é uma interface ruim para apontar, a menos que algum tipo de representação mnemônica seja fornecido. Portanto, sempre considere se a fala é a entrada mais apropriada para uma tarefa. É melhor evitar o uso de fala como a interface exclusiva para qualquer tarefa. Forneça outras maneiras de acessar qualquer funcionalidade básica usando métodos como o mouse ou o teclado. Além disso, aproveite a natureza multi modal do uso de fala na interface visual combinando a entrada de fala com informações visuais que ajudam a especificar o contexto e as opções.

Por fim, o uso bem-sucedido da entrada de fala deve-se apenas em parte à qualidade da tecnologia. Até mesmo o reconhecimento humano, que excede qualquer tecnologia de reconhecimento atual, às vezes falha. No entanto, na comunicação humana, usamos estratégias que melhoram a probabilidade de sucesso e que fornecem recuperação de erro quando algo dá errado. Portanto, a eficácia da entrada de fala também depende da qualidade da interface do usuário que a apresenta.

Estudar modelos humanos de interação de fala pode ser útil ao criar interfaces de fala mais naturais. A gravação de diálogos de fala humana reais para cenários específicos pode ajudá-lo a entender melhor os constructos e padrões usados, bem como formas efetivas de comentários e recuperação de erros. Ele pode ajudar a determinar o vocabulário apropriado a ser usado (para entrada e saída). É melhor criar uma interface de fala com base em como as pessoas realmente falam do que simplesmente derivar da interface gráfica na qual ela opera.

Observe que o Microsoft Agent usa o SAPI (Microsoft Speech API) para dar suporte ao reconhecimento de fala. Isso permite que o Microsoft Agent seja usado com uma variedade de mecanismos compatíveis. Embora o Microsoft Agent especifique determinadas interfaces básicas, os requisitos de desempenho e a qualidade de um mecanismo podem variar.

A fala não é o único meio de dar suporte a interfaces de conversa. Você também pode usar o processamento em idioma natural da entrada do teclado no lugar de ou além da fala. Nessas situações, você ainda pode aplicar diretrizes para entrada de fala.

-   [Listen, Don't Just Recognize](listen--dont-just-recognize.md)
-   [Esclarecer e limitar opções](clarify-and-limit-choices.md)
-   [Fornecer uma boa recuperação de erro](provide-good-error-recovery.md)

 

 




