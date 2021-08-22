---
title: Registro de dispositivo
description: Registro de dispositivo
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- Windows SDK de Formato de Mídia, registro de dispositivo
- Windows SDK de Formato de Mídia, registro de dispositivos
- ASF (Advanced Systems Format), registro de dispositivo
- ASF (Formato de Sistemas Avançados), registro de dispositivo
- ASF (Advanced Systems Format), registro de dispositivos
- ASF (Formato de Sistemas Avançados), registro de dispositivos
- DRM (gerenciamento de direitos digitais), registro de dispositivo
- DRM (gerenciamento de direitos digitais), registro de dispositivo
- DRM (gerenciamento de direitos digitais), registro de dispositivos
- DRM (gerenciamento de direitos digitais), registro de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2efbfefaaabf3af0a33f304ad2cc32f7fe3b84691da8242203eddbb18fdb90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027924"
---
# <a name="device-registration"></a>Registro de dispositivo

O SDK Windows Formato de Mídia fornece acesso ao banco de dados de registro do dispositivo. Esse banco de dados é protegido no computador cliente e é usado para registrar dispositivos que Windows drm de mídia 10 para dispositivos de rede.

Quando um dispositivo é adicionado a uma rede à qual o computador cliente está conectado, o dispositivo tenta entrar em contato com um Windows drm de mídia 10 para o aplicativo de transmissor de Dispositivos de Rede. Depois de estabelecer comunicações, o dispositivo envia uma mensagem de solicitação de registro.

Seu aplicativo deve executar as seguintes etapas quando receber uma mensagem de solicitação de registro:

1.  Analisar a mensagem chamando o [**método IWMDRMMessageParser::P arseRegistrationReqMsg.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) Esse método recupera o certificado do dispositivo e o número de série do dispositivo, ambos necessários para identificar o dispositivo.
2.  Chame o [**método IWMDeviceRegistration::GetRegisteredDeviceByID,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) passando o certificado e o número de série do dispositivo recuperados na etapa 1. Se o dispositivo for encontrado, ele já está registrado e você poderá ignorar a próxima etapa.
3.  Chame o [**método IWMDeviceRegistration::RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) para adicionar o dispositivo ao banco de dados de registro do dispositivo.

Você pode acessar informações sobre qualquer dispositivo no banco de dados de registro recuperando o objeto de dispositivo registrado associado a ele. Há duas maneiras de obter um objeto de dispositivo registrado. Se você tiver o certificado e o número de série do dispositivo, poderá chamar o método [**IWMDeviceRegistration::GetRegisteredDeviceByID.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) Se você não tiver o certificado e o número de série do dispositivo, poderá enumerar todos os dispositivos no banco de dados chamando [**IWMDeviceRegistration::GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) seguido por chamadas repetidas para [**IWMDeviceRegistration::GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) até que uma chamada retorne S \_ FALSE.

Antes que seu aplicativo possa enviar dados para um dispositivo, você deve garantir que o dispositivo seja aprovado, validado e aberto.

A aprovação do dispositivo deve envolver a interação com o usuário. Quando um dispositivo envia uma mensagem de registro, seu aplicativo pode solicitar que o usuário decida se o dispositivo é aquele que deve receber os dados desse usuário. Em seguida, atualize o banco de dados de registro do dispositivo chamando o método [**IWMRegisteredDevice::Approve,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) passando **TRUE** ou **FALSE** conforme apropriado.

A validação também é chamada de detecção de proximidade. Esse é um processo pelo qual os objetos DRM internos do SDK de Formato de Mídia Windows determinam se o dispositivo está "próximo" o suficiente para o computador que executa seu aplicativo transmitir mídia com segurança. A proximidade é determinada pelo tempo necessário para obter uma resposta a uma mensagem. Esse recurso destina-se a impedir que usuários não autorizados acessem sua rede e obtenham sua mídia protegida. Para obter mais informações, consulte [Executando a detecção de proximidade.](performing-proximity-detection.md)

Para abrir um dispositivo, chame [**IWMRegisteredDevice::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).

> [!Note]  
> O DRM não é suportado pela versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[**Usando o Windows DRM de Mídia 10 para o Protocolo de Dispositivos de Rede**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




