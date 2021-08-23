---
title: Listen, Dont Just Recognize
description: Listen, Dont Just Recognize
ms.assetid: 74bb2122-98c1-4a51-b894-93e1481aa46b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b226b9172b10c70e4e699a98df49acc002dcd5add95986c9efbdf9e8f057648d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888086"
---
# <a name="listen-dont-just-recognize"></a>Listen, Dont Just Recognize

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

A comunicação bem-sucedida envolve mais do que o reconhecimento de palavras. O processo de diálogo implica a troca de dicas para sinalizar a compreensão e a tomada de turnos. Os caracteres podem melhorar as interfaces de conversa fornecendo dicas como inclinações de cabeça, nós ou tremadas para indicar quando o mecanismo de fala está no estado de escuta e quando algo é reconhecido. Por exemplo, o Microsoft Agent reproduz  animações atribuídas ao estado De escuta quando um usuário pressiona  a tecla de escuta push-to-talk e animações atribuídas ao estado Auditivo quando um enunciado é detectado. Ao definir seu próprio caractere, crie e atribua animações apropriadas a esses estados. Para obter mais informações sobre como criar caracteres, consulte [Projetando caracteres para o Microsoft Agent.](designing-characters-for-microsoft-agent.md)

Além de dicas não verbais, uma conversa envolve um contexto comum entre as partes que conversam. Da mesma forma, os cenários de entrada de fala com caracteres têm maior probabilidade de ter êxito quando o contexto é bem estabelecido. Estabelecer o contexto permite que você interprete melhor frases semelhantes, como "check-s no email" e "verifique meu email". Talvez você também queira permitir que o usuário consulte o contexto fornecendo um comando, como "Ajuda" ou "Onde estou", ao qual você responde ao reabilitar o contexto atual, como a última ação executada pelo aplicativo.

O Microsoft Agent fornece interfaces que permitem que você acesse a melhor combinação e as duas melhores alternativas retornadas pelo mecanismo de reconhecimento de fala. Além disso, você pode acessar pontuações de confiança para todas as partidas. Você pode usar essas informações para determinar melhor o que foi falado. Por exemplo, se as pontuações de confiança da melhor combinação e da primeira alternativa estão próximas, isso pode indicar que o mecanismo de fala teve dificuldade para distinguir a diferença entre elas. Nesse caso, talvez você queira pedir ao usuário para repetir ou reformular a solicitação em um esforço para melhorar o desempenho. No entanto, se a melhor combinação e a primeira ou segunda alternativas retornarem o mesmo comando, ela fortalecerá a indicação do reconhecimento correto.

A natureza de uma conversa ou diálogo implica que deve haver uma resposta à entrada falada. Portanto, a entrada de um usuário sempre deve ser respondida com comentários verbais ou visuais que indicam que uma ação foi executada ou um problema foi encontrado ou fornece uma resposta apropriada.

 

 




