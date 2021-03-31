---
description: O monitoramento de Tom monitora o fluxo de mídia de uma chamada para os tons especificados.
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: Monitoramento de Tom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a3275e5207999896792ee04dc1842b01f4ad0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011132"
---
# <a name="tone-monitoring"></a>Monitoramento de Tom

O monitoramento de Tom monitora o fluxo de mídia de uma chamada para os tons especificados. Um tom é descrito por suas frequências e cadência de componentes. Uma implementação da API pode permitir que vários tons diferentes sejam monitorados simultaneamente. Um aplicativo pode marcar cada tom para poder distinguir os diferentes tons para os quais ele solicita a detecção.

Um aplicativo pode habilitar ou desabilitar o monitoramento de Tom em uma chamada especificada com [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones). Com essa função, o aplicativo indica quais tons detectar em uma chamada especificada. Quando o monitoramento de Tom está habilitado, os dígitos detectados fazem com que o aplicativo seja notificado com a mensagem de [**linha \_ MONITORTONE**](line-monitortone.md) . Essa mensagem fornece o identificador de chamada no qual o Tom foi detectado, bem como a marca do aplicativo para o Tom.

O escopo do monitoramento de Tom é associado pelo tempo de vida da chamada. O monitoramento de Tom em uma chamada termina assim que a chamada é *desconectada* ou fica *ociosa*.

> [!Note]  
> O monitoramento de tons, dígitos ou tipos de mídia geralmente requer o uso de recursos dos quais o provedor de serviços pode ter apenas um valor finito. Uma solicitação de monitoramento poderá ser rejeitada se os recursos não estiverem disponíveis. Pelo mesmo motivo, um aplicativo deve desabilitar qualquer monitoramento desnecessário.

 

 

 



