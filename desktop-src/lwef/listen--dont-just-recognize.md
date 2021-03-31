---
title: Escute, não apenas reconheça
description: Escute, não apenas reconheça
ms.assetid: 74bb2122-98c1-4a51-b894-93e1481aa46b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e972a8c98460e58d0f7080d7de7641fb856c8317
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637026"
---
# <a name="listen-dont-just-recognize"></a>Escute, não apenas reconheça

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

A comunicação bem-sucedida envolve mais do que o reconhecimento de palavras. O processo de caixa de diálogo implica a troca de indicações para a ativação e a compreensão de sinal. Os caracteres podem melhorar as interfaces de conversação fornecendo indicações como as inclinações de cabeça, nós nesta ou agites para indicar quando o mecanismo de fala está no estado de escuta e quando algo é reconhecido. Por exemplo, o Microsoft Agent reproduz animações atribuídas ao estado de **escuta** quando um usuário pressiona a tecla de escuta push para conversar e animações atribuídas ao estado **audição** quando um expressão é detectado. Ao definir seu próprio caractere, certifique-se de criar e atribuir animações apropriadas a esses Estados. Para obter mais informações sobre como criar caracteres, consulte [criando caracteres para o Microsoft Agent](designing-characters-for-microsoft-agent.md).

Além de indicações não verbal, uma conversa envolve um contexto comum entre as partes convertidas. Da mesma forma, os cenários de entrada de fala com caracteres têm maior probabilidade de serem bem-sucedidos quando o contexto é bem estabelecido. O estabelecimento do contexto permite que você interprete melhor as frases de som semelhantes, como "verificar no email" e "verificar meus emails". Você também pode permitir que o usuário consulte o contexto fornecendo um comando, como "Help" ou "Where am", ao qual você responde reafirmando o contexto atual, como a última ação que seu aplicativo realizou.

O Microsoft Agent fornece interfaces que permitem que você acesse a melhor correspondência e as duas melhores alternativas retornadas pelo mecanismo de reconhecimento de fala. Além disso, você pode acessar as pontuações de confiança para todas as correspondências. Você pode usar essas informações para determinar melhor o que foi falado. Por exemplo, se as pontuações de confiança da melhor correspondência e da primeira alternativa forem próximas, isso poderá indicar que o mecanismo de fala teve dificuldade em distinguir a diferença entre elas. Nesse caso, talvez você queira pedir ao usuário para repetir ou reformular a solicitação em um esforço para melhorar o desempenho. No entanto, se a melhor correspondência e a primeira ou segunda alternativas retornarem o mesmo comando, o reforçará a indicação do reconhecimento correto.

A natureza de uma conversa ou caixa de diálogo implica que deve haver uma resposta à entrada falada. Portanto, a entrada de um usuário sempre deve responder com comentários visuais ou verbal que indica que uma ação foi executada ou um problema foi encontrado ou fornece uma resposta apropriada.

 

 




