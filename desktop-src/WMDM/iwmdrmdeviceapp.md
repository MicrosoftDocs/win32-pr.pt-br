---
title: Interface IWMDRMDeviceApp
description: A interface IWMDRMDeviceApp permite que um aplicativo meça, sincronize licenças e atualize os componentes drm de um dispositivo.
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- Interface IWMDRMDeviceApp windows Media Gerenciador de Dispositivos
- IWMDRMDeviceApp interface windows Media Gerenciador de Dispositivos , descrito
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d618a0534592ebe01a961ba9b0fdd462fcda70597b5f909b30e8fb92f6bdbeb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055624"
---
# <a name="iwmdrmdeviceapp-interface"></a>Interface IWMDRMDeviceApp

\[O Windows drm de mídia de mídia foi preterido e não deve ser usado. Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) em vez disso.\]

A interface **IWMDRMDeviceApp** permite que um aplicativo meça, sincronize licenças e atualize os componentes drm de um dispositivo. Essa interface só funcionará com dispositivos que suportam Windows DRM de Mídia 10 para Dispositivos Portáteis.

Para obter essa interface, chame **CoCreateInstance,** passando CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Essa interface é definida no arquivo de header criado com base em WMDRMDeviceApp.idl. Esse header **\# inclui**"wmdm.h". Talvez seja necessário alterar esse nome de arquivo para corresponder ao header criado do WMDM.idl.

 

## <a name="members"></a>Membros

A interface **IWMDRMDeviceApp** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMDeviceApp** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMDeviceApp** tem esses métodos.



| Método                                                                   | Descrição                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)           | Inicializa ou redefine um relógio seguro do dispositivo<br/>                                                                                     |
| [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md) | Adquire dados de medição de um dispositivo.<br/>                                                                                           |
| [**ProcessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md)     | Redefine algumas ou todas as contagens de medição em um dispositivo, depois que os dados do dispositivo são enviados e processados pelo servidor.<br/> |
| [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)           | Consulta um dispositivo quanto ao status e às funcionalidades atuais do DRM.<br/>                                                                   |
| [**SynchronizeLicenses**](iwmdrmdeviceapp-synchronizelicenses.md)       | Atualiza licenças em um dispositivo quando eles estão próximos de expirar.<br/>                                                                   |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Manipulando conteúdo protegido no aplicativo**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaces para aplicativos**](interfaces-for-applications.md)
</dt> <dt>

[**Medição do uso de conteúdo**](metering-content-usage.md)
</dt> </dl>

 

