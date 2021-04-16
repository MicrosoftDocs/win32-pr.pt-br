---
description: O objeto de chamada representa uma conexão de endereço entre o endereço local e um ou mais endereços.
ms.assetid: 67c063ba-8b12-40d6-9011-923bdee8b214
title: Objeto de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b8ea40b7b2cadece9c89a45f9296995ad92fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768581"
---
# <a name="call-object"></a>Objeto de chamada

O objeto de chamada representa a conexão de um endereço entre o endereço local e um ou mais endereços. Todo o controle de chamada é feito por meio do objeto de chamada. [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) e [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) são as interfaces usadas com mais frequência no objeto de chamada. Essas interfaces implementam uma variedade de operações e consultas, como a aquisição de ponteiros de interface para fluxos de mídia ou a obtenção da ID do chamador. Consulte as principais seções de visão geral sobre [operações de sessão](session-operations-ovr.md) e [informações de sessão](session-information-ovr.md) para ver as revisões com suporte da TAPI.

Um provedor de serviços de mídia pode implementar [interfaces específicas do provedor](provider-specific-interfaces.md), que são agregadas em um objeto de chamada pela TAPI. Para obter informações detalhadas sobre o que um provedor implementou, consulte a documentação do provedor de serviços.

Os exemplos [fazer uma chamada](make-a-call.md) e [receber um](receive-a-call.md) código de chamada mostram algumas ilustrações de como usar um objeto de chamada.

Consulte [interfaces do objeto de chamada](call-object-interfaces.md) para obter uma lista de todas as interfaces associadas ao objeto de chamada.

 

 



