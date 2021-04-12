---
title: O objeto AudioOutput
description: O objeto AudioOutput
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919b435edf31b6ae24a8b5c6977d5aed542efac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366010"
---
# <a name="the-audiooutput-object"></a>O objeto AudioOutput

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Esse objeto fornece acesso a propriedades de saída de áudio mantidas pelo servidor. As propriedades são somente leitura, mas o usuário pode alterá-las na folha de propriedades do Microsoft Agent.

Se você declarar uma variável de objeto do tipo [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), não será possível acessar todas as propriedades do objeto [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) . Embora o Agent também dê suporte a [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), essa última interface é fornecida apenas para fins de compatibilidade com versões anteriores e dá suporte apenas a essas propriedades em versões antigas.

-   [**habilitado**](enabled-property-ao.md)
-   [**SoundEffects**](soundeffects-property.md)
-   [**Estado**](status-property.md)

 

 