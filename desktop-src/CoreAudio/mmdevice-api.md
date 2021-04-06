---
description: Sobre a API do MMDevice
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: Sobre a API do MMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82843bbecf004d0931575d73ec2459c3e72a3cf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646469"
---
# <a name="about-mmdevice-api"></a>Sobre a API do MMDevice

A API do dispositivo de multimídia do Windows (MMDevice) permite que os clientes de áudio descubram [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md), determinem seus recursos e criem instâncias de driver para esses dispositivos.

O arquivo de cabeçalho Mmdeviceapi. h define as interfaces na API MMDevice.

A API MMDevice consiste em várias interfaces. A primeira delas é a interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Para acessar as interfaces na API MMDevice, um cliente obtém uma referência à interface **IMMDeviceEnumerator** de um objeto de enumerador de dispositivo chamando a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , conforme mostrado no fragmento de código a seguir:


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



No fragmento de código anterior, CLSID \_ MMDeviceEnumerator e IID \_ IMMDeviceEnumerator são os valores de GUID anexados como atributos ao objeto de classe **MMDeviceEnumerator** e à interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . A chamada [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) passa esses valores por referência. Variable `hr` é do tipo **HRESULT**, e Variable `pEnumerator` é um ponteiro para a interface **IMMDeviceEnumerator** de um objeto de enumerador de dispositivo. **IMMDeviceEnumerator** fornece métodos para enumerar dispositivos de ponto de extremidade de áudio. Para obter informações sobre o operador **\_ \_ uuidof** , a função **CoCreateInstance** e as constantes CLSCTX \_ *xxx* , consulte a documentação do SDK do Windows.

Por meio da interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) , o cliente pode obter referências às outras interfaces na API MMDevice. A API MMDevice implementa as interfaces a seguir.



| Interface                                          | Descrição                                     |
|----------------------------------------------------|-------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | Representa um dispositivo de áudio.                     |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | Representa uma coleção de dispositivos de áudio.       |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | Fornece métodos para enumerar dispositivos de áudio. |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | Representa um dispositivo de ponto de extremidade de áudio.            |



 

Além disso, os clientes da API MMDevice que exigem notificação de alterações de status em dispositivos de ponto de extremidade de áudio devem implementar a interface a seguir.



| Interface                                              | Descrição                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Fornece notificações quando um dispositivo de ponto de extremidade de áudio é adicionado ou removido, quando o estado ou as propriedades de um dispositivo são alterados ou quando há uma alteração na função padrão atribuída a um dispositivo. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md)
</dt> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 
