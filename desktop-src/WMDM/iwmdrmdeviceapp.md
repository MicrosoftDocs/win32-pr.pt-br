---
title: Interface IWMDRMDeviceApp
description: A interface IWMDRMDeviceApp permite que um aplicativo seja medido, sincronize licenças e atualize os componentes DRM de um dispositivo.
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- Interface IWMDRMDeviceApp Windows Media Gerenciador de Dispositivos
- Interface IWMDRMDeviceApp Windows Media Gerenciador de Dispositivos, descrita
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9cf44295c9972d7549eb4a82fda7c415ba81c31d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105800182"
---
# <a name="iwmdrmdeviceapp-interface"></a>Interface IWMDRMDeviceApp

\[O recurso DRM do Windows Media foi preterido e não deve ser usado. Em vez disso, use [o Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

A interface **IWMDRMDeviceApp** permite que um aplicativo seja medido, sincronize licenças e atualize os componentes DRM de um dispositivo. Esta interface só funcionará com dispositivos que dão suporte ao Windows Media DRM 10 para dispositivos portáteis.

Para obter essa interface, chame **CoCreateInstance**, passando em CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Essa interface é definida no arquivo de cabeçalho criado a partir de WMDRMDeviceApp. idl. Esse cabeçalho **\# inclui** os s "WMDM. h". Talvez seja necessário alterar esse nome de arquivo para corresponder ao cabeçalho criado a partir de WMDM. idl.

 

## <a name="members"></a>Membros

A interface **IWMDRMDeviceApp** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMDeviceApp** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMDeviceApp** tem esses métodos.



| Método                                                                   | Descrição                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)           | Inicializa ou redefine um relógio seguro do dispositivo<br/>                                                                                     |
| [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md) | Adquire dados de medição de um dispositivo.<br/>                                                                                           |
| [**ProcessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md)     | Redefine algumas ou todas as contagens de medição em um dispositivo, depois que os dados do dispositivo tiverem sido enviados e processados pelo servidor.<br/> |
| [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)           | Consulta um dispositivo quanto ao seu status e recursos de DRM atuais.<br/>                                                                   |
| [**SynchronizeLicenses**](iwmdrmdeviceapp-synchronizelicenses.md)       | Atualiza licenças em um dispositivo quando elas estiverem próximas de expirar.<br/>                                                                   |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lidando com conteúdo protegido no aplicativo**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaces para aplicativos**](interfaces-for-applications.md)
</dt> <dt>

[**Uso de conteúdo de medição**](metering-content-usage.md)
</dt> </dl>

 

