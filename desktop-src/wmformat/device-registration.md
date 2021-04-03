---
title: Registro de dispositivo
description: Registro de dispositivo
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- SDK do Windows Media Format, registro de dispositivo
- SDK do Windows Media Format, registro de dispositivos
- ASF (Advanced Systems Format), registro de dispositivo
- ASF (formato de sistemas avançados), registro de dispositivo
- ASF (Advanced Systems Format), registro de dispositivos
- ASF (formato de sistemas avançados), registro de dispositivos
- DRM (gerenciamento de direitos digitais), registro de dispositivo
- DRM (gerenciamento de direitos digitais), registro de dispositivo
- DRM (gerenciamento de direitos digitais), registro de dispositivos
- DRM (gerenciamento de direitos digitais), registro de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf4954d9b59abfb62f3a86127a387299d45cb4a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007110"
---
# <a name="device-registration"></a>Registro de dispositivo

O SDK do Windows Media Format fornece acesso ao banco de dados de registro do dispositivo. Esse banco de dados é protegido no computador cliente e é usado para registrar dispositivos que dão suporte ao Windows Media DRM 10 para dispositivos de rede.

Quando um dispositivo é adicionado a uma rede à qual o computador cliente está conectado, o dispositivo tenta contatar um aplicativo Windows Media DRM 10 para dispositivos de rede transmissor. Depois de estabelecer as comunicações, o dispositivo envia uma mensagem de solicitação de registro.

Seu aplicativo deve executar as seguintes etapas ao receber uma mensagem de solicitação de registro:

1.  Analise a mensagem chamando o método [**IWMDRMMessageParser::P arseregistrationreqmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) . Esse método recupera o certificado do dispositivo e o número de série do dispositivo, ambos necessários para identificar o dispositivo.
2.  Chame o método [**IWMDeviceRegistration:: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) , passando o certificado e o número de série do dispositivo recuperado na etapa 1. Se o dispositivo for encontrado, ele já estará registrado e você poderá ignorar a próxima etapa.
3.  Chame o método [**IWMDeviceRegistration:: RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) para adicionar o dispositivo ao banco de dados de registro do dispositivo.

Você pode acessar informações sobre qualquer dispositivo no banco de dados de registro recuperando o objeto de dispositivo registrado associado a ele. Há duas maneiras de obter um objeto de dispositivo registrado. Se você tiver o certificado e o número de série do dispositivo, poderá chamar o método [**IWMDeviceRegistration:: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) . Se você não tiver o certificado e o número de série do dispositivo, poderá enumerar todos os dispositivos no banco de dados chamando [**IWMDeviceRegistration:: GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) seguido por chamadas repetidas para [**IWMDeviceRegistration:: GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) até que uma chamada retorne S \_ false.

Antes que o aplicativo possa enviar dados para um dispositivo, você deve garantir que o dispositivo seja aprovado, validado e aberto.

A aprovação do dispositivo deve envolver a interação com o usuário. Quando um dispositivo envia uma mensagem de registro, seu aplicativo pode solicitar que o usuário decida se o dispositivo é aquele que deve receber os dados desse usuário. Em seguida, atualize o banco de dados de registro do dispositivo chamando o método [**IWMRegisteredDevice:: Approve**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) , passando **true** ou **false** conforme apropriado.

A validação também é chamada de detecção de proximidade. Esse é um processo pelo qual os objetos DRM internos do Windows Media Format SDK determinam se o dispositivo é "próximo" o suficiente para o computador que está executando seu aplicativo para transmitir mídia com segurança. A proximidade é determinada pelo tempo necessário para obter uma resposta a uma mensagem. Esse recurso destina-se a impedir que usuários não autorizados acessem sua rede e obtenham sua mídia segura. Para obter mais informações, consulte [executando a detecção de proximidade](performing-proximity-detection.md).

Para abrir um dispositivo, chame [**IWMRegisteredDevice:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[**Usando o protocolo Windows Media DRM 10 para dispositivos de rede**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




