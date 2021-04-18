---
description: A MSPI (interface do provedor de serviços de mídia) é um conjunto de interfaces e métodos implementados por um MSP para permitir um controle de aplicativo TAPI 3 sobre o transporte de mídia durante uma sessão de comunicações.
ms.assetid: 53b7bcbd-571a-44da-a6db-10d4c3e5d30a
title: MSPI (interface do provedor de serviços de mídia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1ce09e626ede14515c0abbbd5c3a35921026d6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105779452"
---
# <a name="media-service-provider-interface-mspi"></a>MSPI (interface do provedor de serviços de mídia)

A MSPI (interface do provedor de serviços de mídia) é um conjunto de interfaces e métodos implementados por um MSP para permitir um controle de aplicativo TAPI 3 sobre o transporte de mídia durante uma sessão de comunicações. Um MSP manipula os mecanismos específicos do dispositivo e do protocolo necessários para aplicar esses controles e se comunica com seu TSP ou aplicativo emparelhado usando os métodos fornecidos no MSPI.

A seção a seguir ( [referência de MSPI (interface do provedor de serviços de mídia](media-service-provider-interface-mspi-reference.md))) detalha as interfaces que o MSP expõe para interagir com o ambiente de telefonia da Microsoft.

Além disso, um MSP pode expor interfaces privadas e métodos específicos do provedor para auxiliar ainda mais no controle de mídia. Por exemplo, o [IP Conference MSP](ipconf-msp.md) expõe interfaces que fornecem controle de participante. Consulte [interfaces específicas do provedor](provider-specific-interfaces.md) para obter informações sobre como os objetos privados funcionam e [IPConf as interfaces MSP](ipconf-msp-interfaces.md) para obter uma listagem de referência de IPConf.

A maior parte do esforço de programação na criação de um MSP é altamente específica para uma determinada plataforma, dispositivo e protocolo de transporte e está fora do escopo deste documento. No entanto, a Microsoft fornece um conjunto de classes base MSP, que será útil para a maioria dos autores MSP. Consulte [classes base TAPI 3 MSP](tapi-3-msp-base-classes.md) para obter informações sobre como usar essas classes.

A interface [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) representa um provedor de serviços de mídia para a dll TAPI. Essa interface não é usada pelo ou exposta a um aplicativo de usuário final. A DLL TAPI 3 chama **CoCreateInstance** nessa interface para criar o objeto MSP principal. Os métodos nesse objeto permitem que um aplicativo carregue e descarregue o MSP, receba informações de um TSP e crie a interface [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) , que é exposta no objeto de chamada.

As interfaces [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) e [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) fornecem métodos paralelos em relação aos subfluxos. O suporte a Subfluxo é opcional. Todas as outras interfaces devem ser implementadas por um MSP.

> [!Note]  
> As operações implementadas por um par de TSP/MSP devem estar localizadas em uma DLL para permitir que um usuário atualize o provedor de serviços sem reinicializar seu sistema.

 

 

 
