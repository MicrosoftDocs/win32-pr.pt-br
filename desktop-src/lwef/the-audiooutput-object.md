---
title: O objeto AudioOutput
description: O objeto AudioOutput
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07bfef883e5cb40d0a72ec4d848ad0d77f63f58aaeefd907f632e16798be4397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474946"
---
# <a name="the-audiooutput-object"></a>O objeto AudioOutput

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Esse objeto fornece acesso a propriedades de saída de áudio mantidas pelo servidor. As propriedades são somente leitura, mas o usuário pode alterá-las na folha de propriedades do Microsoft Agent.

Se você declarar uma variável de objeto do tipo [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), não será possível acessar todas as propriedades do objeto [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) . Embora o Agent também dê suporte a [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), essa última interface é fornecida apenas para fins de compatibilidade com versões anteriores e dá suporte apenas a essas propriedades em versões antigas.

-   [**habilitado**](enabled-property-ao.md)
-   [**SoundEffects**](soundeffects-property.md)
-   [**Estado**](status-property.md)

 

 