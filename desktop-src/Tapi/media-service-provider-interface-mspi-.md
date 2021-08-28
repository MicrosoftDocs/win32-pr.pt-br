---
description: A Interface do Provedor de Serviços de Mídia (MSPI) é um conjunto de interfaces e métodos implementados por um MSP para permitir um controle de aplicativo TAPI 3 sobre o transporte de mídia durante uma sessão de comunicação.
ms.assetid: 53b7bcbd-571a-44da-a6db-10d4c3e5d30a
title: Interface do Provedor de Serviços de Mídia (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b99f78d62c0784e38ede7a4019eef40cf8a48cf9480a4326c5d7b7129ca971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073006"
---
# <a name="media-service-provider-interface-mspi"></a>Interface do Provedor de Serviços de Mídia (MSPI)

A Interface do Provedor de Serviços de Mídia (MSPI) é um conjunto de interfaces e métodos implementados por um MSP para permitir um controle de aplicativo TAPI 3 sobre o transporte de mídia durante uma sessão de comunicação. Um MSP trata os mecanismos específicos do dispositivo e específicos do protocolo necessários para aplicação desses controles e se comunica com seu TSP emparelhado ou um aplicativo por meio do uso dos métodos fornecidos no MSPI.

A seção a seguir ( Referência da [MSPI (Interface](media-service-provider-interface-mspi-reference.md)do Provedor de Serviços de Mídia) detalha as interfaces que um MSP expõe para interagir com o ambiente de Telefonia da Microsoft.

Além disso, um MSP pode expor interfaces e métodos privados específicos do provedor para auxiliar ainda mais no controle de mídia. Por exemplo, o [MSP de Conferência de IP](ipconf-msp.md) expõe interfaces que fornecem controle de participante. Consulte [Interfaces específicas](provider-specific-interfaces.md) do provedor para obter informações sobre como os objetos privados funcionam e [Interfaces IPConf MSP](ipconf-msp-interfaces.md) para obter uma listagem de referência de IPConf.

A maior parte do esforço de programação na criação de um MSP é altamente específica para uma determinada plataforma, dispositivo e protocolo de transporte e está fora do escopo deste documento. No entanto, a Microsoft fornece um conjunto de classes base do MSP, que será útil para a maioria dos autores do MSP. Consulte [Classes base do TAPI 3 MSP](tapi-3-msp-base-classes.md) para obter informações sobre como usar essas classes.

A [**interface ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) representa um provedor de serviços de mídia para a DLL tapi. Essa interface não é usada pelo ou exposta a um aplicativo do usuário final. A DLL tapi 3 chama **CoCreateInstance** nessa interface para criar o objeto MSP principal. Os métodos nesse objeto permitem que um aplicativo carregue e descarregue o MSP, receba informações de um TSP e crie a interface [**ITStreamControl,**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) que é exposta no objeto de chamada.

As interfaces [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) [**e ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) fornecem métodos paralelos em relação a substreams. O suporte a substream é opcional. Todas as outras interfaces devem ser implementadas por um MSP.

> [!Note]  
> As operações implementadas por um par TSP/MSP devem estar localizadas em uma DLL para permitir que um usuário atualize o provedor de serviços sem reinicializar seu sistema.

 

 

 
