---
title: ITTSNotifySinkW
description: ITTSNotifySinkW
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86cedf8c4a349da800f34f2f6acd7266f9cd0c3c383be9accb72dd162df8e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748704"
---
# <a name="ittsnotifysinkw"></a>ITTSNotifySinkW

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O mecanismo deve chamar de [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**)e [**Visual**](https://www.bing.com/search?q=**Visual**). O retorno de chamada **Visual** deve fornecer fonemas IPA. (O alfabeto \[ fonético internacional IPA \] é uma notação universal para descrever o conteúdo fonético da comunicação falada. Todos os fonemas de Altova que têm representações no IPA. Os detalhes de IPA estão na parte de especificação do Microsoft Speech API \[ do Speech SDK 4,0 download \] em [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) .)

Embora a notificação [**Visual**](https://www.bing.com/search?q=**Visual**) seja bastante rica, o Microsoft Agent usa apenas o valor **cIPAPhoneme** para animar a boca à medida que o caractere fala. Qualquer mecanismo compatível com o Microsoft Agent deve fornecer um fluxo de notificações **visuais** bem sincronizado que reflete o conteúdo fonético do expressão produzido. Nesse caso, "notificação relativamente oportuna" não é adequada, pois os ouvintes dos palestrantes são bastante sensíveis a discrepâncias entre a posição da boca e o conteúdo acústico. As notificações **visuais** precisam ser retornadas imediatamente.

 

 




