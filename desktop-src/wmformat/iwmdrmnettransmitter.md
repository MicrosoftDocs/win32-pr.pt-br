---
title: Interface IWMDRMNetTransmitter
description: a interface IWMDRMNetTransmitter fornece métodos necessários para usar Windows DRM de mídia para dispositivos de rede como um transmissor. Para obter uma instância dessa interface, chame IWMDRMProvider CreateObject. Passe \_ IWMDRMNETTRANSMITTER IID como o parâmetro riid.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- Formato de mídia do Windows da interface IWMDRMNetTransmitter
- Formato de mídia do Windows da interface IWMDRMNetTransmitter, descrito
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7526ad349403abdb74f1e5684356af1b51b91f99b40e8e26a3b04932d4e5cf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027554"
---
# <a name="iwmdrmnettransmitter-interface"></a>Interface IWMDRMNetTransmitter

a interface **IWMDRMNetTransmitter** fornece métodos necessários para usar Windows DRM de mídia para dispositivos de rede como um transmissor.

Para obter uma instância dessa interface, chame [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Passe **\_ IWMDRMNetTransmitter IID** como o parâmetro *riid* .

## <a name="members"></a>Membros

A interface **IWMDRMNetTransmitter** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMNetTransmitter** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMNetTransmitter** tem esses métodos.



| Método                                                                        | Descrição                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) | Gera uma mensagem de resposta de licença de folha.<br/>                                                       |
| [**GetRootLicenseResponse**](iwmdrmnettransmitter-getrootlicenseresponse.md) | Gera uma mensagem de resposta de licença raiz<br/>                                                        |
| [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md)       | processa um desafio de licença enviado por um Microsoft Windows Media DRM para dispositivos de rede receptor<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**Interface IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> </dl>

 

