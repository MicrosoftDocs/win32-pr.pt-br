---
title: Objeto de registro de dispositivo
description: Objeto de registro de dispositivo
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- SDK do Windows Media Format, objetos de registro do dispositivo
- ASF (Advanced Systems Format), objetos de registro de dispositivo
- ASF (formato de sistemas avançados), objetos de registro de dispositivo
- objetos, objetos de registro de dispositivo
- objetos de registro de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6b72637cf7ba439d0bb38109645742cda4ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105783779"
---
# <a name="device-registration-object"></a>Objeto de registro de dispositivo

O objeto de registro de dispositivo gerencia o banco de dados de registro de dispositivo. Esse banco de dados armazena informações sobre dispositivos de rede, como players de vídeo de conjunto superior, que estão conectados ao computador cliente. A principal finalidade do banco de dados de registro de dispositivos é gerenciar dispositivos que usam o protocolo Windows Media DRM 10 para dispositivos de rede para receber fluxos de dados protegidos.

Se seu aplicativo der suporte ao Windows Media DRM 10 para dispositivos de rede, você deverá usar as interfaces desse objeto para registrar dispositivos de rede e para validar esses dispositivos. Você também pode usar o banco de dados de registro de dispositivo para armazenar informações sobre dispositivos de rede que não usam o Windows Media DRM 10 para dispositivos de rede, embora nem todas as informações no banco de dados sejam aplicadas a tais dispositivos.

O objeto de registro de dispositivo é criado pela função [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) , que define um ponteiro para uma interface **IWMDeviceRegistration** . Os outros métodos do objeto de registro de dispositivo podem ser obtidos chamando o método **QueryInterface** .

As interfaces a seguir têm suporte do objeto de registro de dispositivo.



| Interface                                              | Descrição                               |
|--------------------------------------------------------|-------------------------------------------|
| [**IWMDeviceRegistration**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | Gerencia o banco de dados de registro de dispositivo. |
| [**IWMDRMMessageParser**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | Analisa as mensagens enviadas por dispositivos.          |
| [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | Gerencia a validação de dispositivo.                |



 

A interface de retorno de chamada a seguir deve ser implementada pelo aplicativo para usar os métodos da interface **IWMProximityDetection** .



| Interface                                      | Descrição                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Recebe mensagens de status de processos que são executados em um thread separado. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> </dl>

 

 




