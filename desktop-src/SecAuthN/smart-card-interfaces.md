---
description: Uma interface de cartão inteligente consiste em um conjunto predefinido de serviços disponíveis em um cartão inteligente, os protocolos necessários para invocar os serviços e as suposições referentes ao contexto dos serviços.
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: Interfaces de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f11f619e69cafa484e209c3346357aa5a031d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662785"
---
# <a name="smart-card-interfaces"></a>Interfaces de cartão inteligente

Uma interface de [*cartão inteligente*](../secgloss/s-gly.md) consiste em um conjunto predefinido de serviços disponíveis em um *cartão inteligente*, os protocolos necessários para invocar os serviços e as suposições referentes ao contexto dos serviços.

Em relação a cartões inteligentes, o termo "interface" é semelhante a como ele é usado em COM, que, por sua vez, é semelhante em conceito ao identificador de aplicativo ISO 7816/5, mas com um escopo diferente.

Cada interface de cartão inteligente é identificada por um GUID. Por exemplo, uma interface pode ser definida que fornece informações de Biorhythm para seu detentor. Se um determinado cartão inteligente der suporte a esse serviço, ele poderá reivindicar suporte a esse GUID de interface. Usando os GUIDs de interface, um aplicativo pode pesquisar um determinado conjunto de interfaces, localizando qualquer cartão que dê suporte a esse conjunto, para concluir uma tarefa.

Embora uma interface tenha um GUID, ela pode ser implementada de forma diferente em cartões diferentes. Por exemplo, a interface Biorhythm mencionada acima pode ter várias implementações diferentes, mas todas são referenciadas usando o mesmo GUID. As diferentes implementações não alterariam a interação entre o aplicativo e o cartão inteligente; no entanto, a interação entre o [*provedor de serviços*](../secgloss/c-gly.md) e os cartões inteligentes pode diferir dependendo da implementação da interface.

O conjunto de interfaces com suporte de um cartão inteligente é definido durante a introdução do cartão inteligente (consulte [apresentando cartões inteligentes ao sistema](introducing-smart-cards-to-the-system.md)).

 

 
