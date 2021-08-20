---
title: Convertendo um arquivo DRM-Protected em um Windows drm de mídia 10 para fluxo de dispositivos de rede
description: Convertendo um arquivo DRM-Protected em um Windows drm de mídia 10 para fluxo de dispositivos de rede
ms.assetid: 11aa0cfd-6d87-4ec4-82d8-db2507402911
keywords:
- Windows SDK de Formato de Mídia, convertendo arquivos protegidos por DRM
- Windows SDK de Formato de Mídia, arquivos protegidos por DRM
- ASF (Advanced Systems Format), convertendo arquivos protegidos por DRM
- ASF (Formato de Sistemas Avançados), convertendo arquivos protegidos por DRM
- AsF (Advanced Systems Format), arquivos protegidos por DRM
- ASF (Formato de Sistemas Avançados), arquivos protegidos por DRM
- DRM (gerenciamento de direitos digitais), convertendo arquivos protegidos por DRM
- DRM (gerenciamento de direitos digitais), convertendo arquivos protegidos por DRM
- DRM (gerenciamento de direitos digitais), arquivos protegidos por DRM
- DRM (gerenciamento de direitos digitais), arquivos protegidos por DRM
- Windows SDK de formato de mídia, Windows DRM de mídia 10 para dispositivos de rede
- Windows SDK de formato de mídia, DRM 10 para dispositivos de rede
- ASF (Advanced Systems Format), Windows MEDIA DRM 10 para dispositivos de rede
- ASF (formato de sistemas avançados), Windows DRM de mídia 10 para dispositivos de rede
- ASF (Advanced Systems Format), DRM 10 for Network Devices
- ASF (formato de sistemas avançados), DRM 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), Windows DRM de mídia 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), Windows DRM de mídia 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), DRM 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), DRM 10 para dispositivos de rede
- Windows DRM de mídia 10 para dispositivos de rede, convertendo arquivos protegidos por DRM
- DRM 10 para dispositivos de rede, convertendo arquivos protegidos por DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe5aa16b13f41c0376da84237a846612b7ae6e730e630be6ec4a45ce48ff4fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848907"
---
# <a name="converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream"></a>Convertendo um arquivo DRM-Protected em um Windows drm de mídia 10 para fluxo de dispositivos de rede

Depois que um dispositivo é registrado e validado, você pode começar a processar mensagens de solicitação de licença dele. As mensagens de solicitação de licença são enviadas pelos dispositivos quando a ação do aplicativo é necessária. A única ação atualmente com suporte é "Reproduzir", que é uma solicitação de dados seguros para reprodução.

Ao receber uma mensagem de solicitação de licença, você deve executar as seguintes etapas:

1.  Analisar a mensagem de solicitação de licença chamando o [**método IWMDRMMessageParser::P arseLicenseRequestMsg.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg)
2.  Obtenha a interface [**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice) para o dispositivo chamando o método [**IWMDeviceRegistration::GetRegisteredDeviceByID,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) passando o certificado e o número de série obtidos na etapa 1.
3.  Verifique se o dispositivo está pronto para receber dados seguros:
    -   Chame [**IWMRegisteredDevice::IsApproved**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved) para verificar se o dispositivo foi aprovado. A aprovação sempre deve ser baseada na preferência do usuário.
    -   Chame [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) para verificar se o dispositivo foi validado nas últimas 48 horas. Se o dispositivo não for válido, você precisará executar a detecção de proximidade. Para obter mais informações, consulte [Executando a detecção de proximidade.](performing-proximity-detection.md)
    -   Chame [**IWMRegisteredDevice::IsOpened**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened) para verificar se o dispositivo foi aberto. Se o dispositivo não estiver aberto, você poderá abri-lo chamando [**IWMRegisteredDevice::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open). Você só pode ter 10 dispositivos abertos no computador por vez. É possível que você precise fechar outro dispositivo antes de abrir o para o qual você está processando a solicitação. Para fechar um dispositivo, chame [**o método IWMRegisteredDevice::Close.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close)
4.  Crie uma instância do objeto de transscriptografador DRM chamando a [**função WMCreateDRMTranscryptor.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)
5.  Chame o [**método IWMDRMTranscryptor::Initialize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize) para inicializar o transscriptografador. Esse método usa um ponteiro para sua implementação da interface [**IWMStatusCallback,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) que ele usa para entregar mensagens de status. Esse método também retorna uma mensagem de solicitação de licença que deve ser enviada ao dispositivo antes de continuar.
6.  Quando o método [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) do seu aplicativo receber a mensagem de status WMT TRANSCRYPTOR INIT, chame o método \_ \_ [**IWMDRMTranscryptor::Seek**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-seek) para buscar a posição inicial apropriada no arquivo. Para iniciar no início do arquivo, você deve chamar **Seek** com a hora 0.
7.  O transscriptografador envia uma mensagem WMT TRANSCRYPTOR SEEKED quando ele está pronto para entregar dados do arquivo \_ no novo momento da \_ apresentação. Faça chamadas repetidas para o [**método IWMDRMTranscryptor::Read**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read) para obter partes convertidas de dados de mídia. Cada chamada é assíncrona e não é concluída até que uma mensagem WMT \_ TRANSCRYPTOR \_ READ seja recebida. Ao receber a mensagem, você pode enviar os dados para o dispositivo receptor.
8.  Quando você recebe uma mensagem WMT TRANSCRYPTOR READ com o parâmetro hr definido como \_ \_  \_ \_ EOF TRANSCRYPTOR NS S, todo o arquivo \_ foi lido. Neste ponto, chame o método [**IWMDRMTranscryptor::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-close) para fechar o arquivo e liberar recursos.
9.  Quando a mensagem WMT TRANSCRYPTOR CLOSED for recebida, você poderá liberar a \_ \_ interface [**IWMDRMTranscryptor.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor)

> [!Note]  
> O DRM não é suportado pela versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o Windows DRM de mídia 10 para o protocolo de dispositivos de rede**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




