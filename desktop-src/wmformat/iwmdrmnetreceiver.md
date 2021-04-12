---
title: Interface IWMDRMNetReceiver
description: A interface IWMDRMNetReceiver fornece métodos necessários para usar o DRM do Microsoft Windows Media para dispositivos de rede como um receptor. Para obter uma instância dessa interface, chame IWMDRMProvider CreateObject. Passe \_ IWMDRMNETRECEIVER IID como o parâmetro riid.
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
ms.openlocfilehash: 7a85ae1525a81e97984e29a5dd28763d934dba2b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104365031"
---
# <a name="iwmdrmnetreceiver-interface"></a>Interface IWMDRMNetReceiver

A interface **IWMDRMNetReceiver** fornece métodos necessários para usar o DRM do Microsoft Windows Media para dispositivos de rede como um receptor.

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

 

 





