---
description: O fragmento de código a seguir ilustra como solicitar e definir um endereço de multicast para uma conferência.
ms.assetid: faff57a9-88b3-45ce-bf9e-3f7087dfd1fd
title: Adquirindo um endereço multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb451bb403002a4b2dc347abf51e587d8ea02a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090161"
---
# <a name="acquiring-a-multicast-address"></a>Adquirindo um endereço multicast

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O fragmento de código a seguir ilustra como solicitar e definir um endereço de multicast para uma conferência.

Para simplificar, esse fragmento mostra a atribuição de um endereço de multicast a um item de mídia. Na realidade, a seleção de um escopo, a solicitação de endereço multicast e a atribuição serão executadas para cada item de mídia envolvido na conferência.

Este fragmento pressupõe que [a conexão com um servidor ILS](connecting-to-an-ils-server.md) já foi executada. As operações mostradas aqui seriam executadas na seção "modificar as configurações, se necessário", de [criar um comunicado de conferência](creating-a-conference-announcement.md).


```C++
// If ( hr != S_OK ) process the error here.
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces COM multicast](multicast-com-interfaces.md)
</dt> <dt>

[**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)
</dt> <dt>

[**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)
</dt> <dt>

[**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)
</dt> <dt>

[**IEnumMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)
</dt> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> <dt>

[**IEnumBstr**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)
</dt> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

 



