---
title: Objeto de registro de dispositivo
description: Objeto de registro de dispositivo
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- Windows SDK do formato de mídia, objetos de registro de dispositivo
- ASF (Advanced Systems Format), objetos de registro de dispositivo
- ASF (formato de sistemas avançados), objetos de registro de dispositivo
- objetos, objetos de registro de dispositivo
- objetos de registro de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4594b17f6824e4e3a9e7690e5ea933e24670e9c8b5d95feb16e555f577f87f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433882"
---
# <a name="device-registration-object"></a>Objeto de registro de dispositivo

O objeto de registro de dispositivo gerencia o banco de dados de registro de dispositivo. Esse banco de dados armazena informações sobre dispositivos de rede, como players de vídeo de conjunto superior, que estão conectados ao computador cliente. a principal finalidade do banco de dados de registro de dispositivos é gerenciar dispositivos que usam o Windows mídia DRM 10 para o protocolo de dispositivos de rede para receber fluxos de dados protegidos.

se seu aplicativo der suporte a Windows mídia DRM 10 para dispositivos de rede, você deverá usar as interfaces desse objeto para registrar dispositivos de rede e para validar esses dispositivos. você também pode usar o banco de dados de registro de dispositivo para armazenar informações sobre dispositivos de rede que não usam Windows mídia DRM 10 para dispositivos de rede, embora nem todas as informações no banco de dados sejam aplicadas a tais dispositivos.

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

[**Objeto**](objects.md)
</dt> </dl>

 

 




