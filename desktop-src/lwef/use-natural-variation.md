---
title: Usar variação natural
description: Usar variação natural
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6259730599966205f4751c4ada9b8ef361cedf6d1a1a59dd1ce7d67aaf0fb448
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474504"
---
# <a name="use-natural-variation"></a>Usar variação natural

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Embora a consistência da apresentação na interface convencional de seu aplicativo, como menus e caixas de diálogo, torne a interface mais previsível, varie a animação e a saída falada na interface do caractere. Adequadamente, a variação das respostas do caractere fornece uma interface mais natural. Se um caractere sempre endereçar o usuário exatamente da mesma forma; por exemplo, sempre dizendo as mesmas palavras, é provável que o usuário considere o caractere enfadonho, disinterested ou até mesmo rude. A comunicação humana raramente envolve a repetição precisa. Mesmo ao repetir algo em uma situação semelhante, podemos alterar o texto, os gestos ou a expressão facial.

O Microsoft Agent permite que você crie em alguma variação um caractere. Ao definir as animações de um caractere, você pode usar probabilidades de ramificação em qualquer quadro de animação para alterar uma animação quando ela for reproduzida. Você também pode atribuir várias animações a cada Estado. O Microsoft Agent escolhe aleatoriamente uma das animações atribuídas cada vez que inicia um estado. Para saída de fala, você também pode incluir caracteres de barra vertical no texto de saída para variar automaticamente o texto falado. Por exemplo, o Microsoft Agent selecionará aleatoriamente uma das seguintes instruções ao processar este texto como parte do método [**Speak**](speak-method.md) :

"Eu posso dizer isso. \| Posso dizer isso. \| Posso dizer algo mais. "

 

 




