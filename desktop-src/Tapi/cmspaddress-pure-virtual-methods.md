---
description: Esses métodos devem ser substituídos por classes derivadas.
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: Métodos virtuais puros CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93c9b2a995554dd2f7412c8fa5bf153ea8871e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811014"
---
# <a name="cmspaddress-pure-virtual-methods"></a>Métodos virtuais puros CMSPAddress

Esses métodos devem ser substituídos por classes derivadas.



| Métodos virtuais puros CMSPAddress                           | Descrição                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | Método AddRef privado para o endereço.                                                                                                                                                 |
| [**MSPAddressRelease**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | Método de liberação particular para o endereço.                                                                                                                                                |
| [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | Chamado pela TAPI para criar um objeto de chamada. A implementação na classe derivada deve simplesmente chamar a função [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) .        |
| [**ShutdownMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | Chamado pela TAPI para desligar um objeto de chamada. A implementação na classe derivada deve simplesmente chamar a função [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) . |
| [**GetCallMediaTypes**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | Obtém os tipos de mídia com suporte no MSP.                                                                                                                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



