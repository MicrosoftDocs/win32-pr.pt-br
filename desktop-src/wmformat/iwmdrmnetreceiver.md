---
title: Interface IWMDRMNetReceiver
description: a interface IWMDRMNetReceiver fornece métodos necessários para usar o Microsoft Windows Media DRM para dispositivos de rede como um receptor. Para obter uma instância dessa interface, chame IWMDRMProvider CreateObject. Passe \_ IWMDRMNETRECEIVER IID como o parâmetro riid.
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- Formato de mídia do Windows da interface IWMDRMNetReceiver
- Formato de mídia do Windows da interface IWMDRMNetReceiver, descrito
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb917d7d229b81a6792461c506b2a6b50aaee2af3bd5f133e44273077924f86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930106"
---
# <a name="iwmdrmnetreceiver-interface"></a>Interface IWMDRMNetReceiver

a interface **IWMDRMNetReceiver** fornece métodos necessários para usar o Microsoft Windows Media DRM para dispositivos de rede como um receptor.

Para obter uma instância dessa interface, chame [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Passe **\_ IWMDRMNetReceiver IID** como o parâmetro *riid* .

## <a name="members"></a>Membros

A interface **IWMDRMNetReceiver** herda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMNetReceiver** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMNetReceiver** tem esses métodos.



| Método                                                                               | Descrição                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)                 | Gera um desafio de licença que é enviado ao transmissor ao solicitar conteúdo protegido.<br/>                     |
| [**GetRegistrationChallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)       | Gera um desafio de registro que é enviado para o transmissor quando o receptor está se registrando ou revalidando.<br/> |
| [**ProcessLicenseResponse**](iwmdrmnetreceiver-processlicenseresponse.md)           | Processa a resposta de licença enviada pelo transmissor em resposta a um desafio de licença.<br/>                              |
| [**ProcessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md) | Processa a resposta de registro enviada pelo transmissor em resposta a um desafio de registro.<br/>                    |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> <dt>

[**Interface IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





