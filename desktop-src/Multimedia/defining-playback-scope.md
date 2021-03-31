---
title: Definindo o escopo de reprodução
description: Definindo o escopo de reprodução
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- Macro MCIWndPlayFrom
- Macro MCIWndPlayTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518fc80588147c4ccbbca619452b714333a8a34d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916245"
---
# <a name="defining-playback-scope"></a>Definindo o escopo de reprodução

O MCIWnd fornece macros que permitem que você defina o *escopo* de reprodução. O escopo é a parte da reprodução que você deseja reproduzir. Por exemplo, você pode reproduzir o conteúdo de uma posição diferente da posição inicial usando a macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) . Essa macro passa para a posição especificada, começa a reprodução e continua até o final do conteúdo. Da mesma forma, você pode reproduzir o conteúdo para um ponto de extremidade especificado usando a macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) . Essa macro começa na posição de reprodução atual e é reproduzida até atingir a posição especificada ou o final do conteúdo é atingido, o que vier primeiro.

Além disso, você pode definir as posições inicial e final usando a macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) . Essa macro é movida para a posição inicial especificada e é reproduzida até que a posição final especificada ou o final do conteúdo seja atingido.

 

 




