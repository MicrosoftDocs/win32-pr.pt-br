---
title: Interface IWMDRMNetTransmitter
description: A interface IWMDRMNetTransmitter fornece métodos necessários para usar o DRM do Windows Media para dispositivos de rede como um transmissor. Para obter uma instância dessa interface, chame IWMDRMProvider CreateObject. Passe \_ IWMDRMNETTRANSMITTER IID como o parâmetro riid.
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
ms.openlocfilehash: a56db31bb7c03aa70aa136dcd07a8f41f1d9b84d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294266"
---
# <a name="iwmdrmnettransmitter-interface"></a>Interface IWMDRMNetTransmitter

A interface **IWMDRMNetTransmitter** fornece métodos necessários para usar o DRM do Windows Media para dispositivos de rede como um transmissor.

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
| [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md)       | Processa um desafio de licença enviado por um Microsoft Windows Media DRM para dispositivos de rede receptor<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**Interface IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> </dl>

 

