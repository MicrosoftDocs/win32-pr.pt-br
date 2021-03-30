---
title: Convertendo um arquivo de DRM-Protected em um fluxo do Windows Media DRM 10 para dispositivos de rede
description: Convertendo um arquivo de DRM-Protected em um fluxo do Windows Media DRM 10 para dispositivos de rede
ms.assetid: 11aa0cfd-6d87-4ec4-82d8-db2507402911
keywords:
- SDK do Windows Media Format, convertendo arquivos protegidos por DRM
- SDK do Windows Media Format, arquivos protegidos por DRM
- ASF (Advanced Systems Format), convertendo arquivos protegidos por DRM
- ASF (formato de sistemas avançados), convertendo arquivos protegidos por DRM
- ASF (Advanced Systems Format), arquivos protegidos por DRM
- ASF (formato de sistemas avançados), arquivos protegidos por DRM
- DRM (gerenciamento de direitos digitais), convertendo arquivos protegidos por DRM
- DRM (gerenciamento de direitos digitais), convertendo arquivos protegidos por DRM
- DRM (gerenciamento de direitos digitais), arquivos protegidos por DRM
- DRM (gerenciamento de direitos digitais), arquivos protegidos por DRM
- SDK do Windows Media Format, Windows Media DRM 10 para dispositivos de rede
- SDK do Windows Media Format, DRM 10 para dispositivos de rede
- ASF (Advanced Systems Format), Windows Media DRM 10 para dispositivos de rede
- ASF (formato de sistemas avançados), Windows Media DRM 10 para dispositivos de rede
- Formato de sistema avançado (ASF), DRM 10 para dispositivos de rede
- Formato ASF 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), Windows Media DRM 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), Windows Media DRM 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), DRM 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), DRM 10 para dispositivos de rede
- Windows Media DRM 10 para dispositivos de rede, convertendo arquivos protegidos por DRM
- DRM 10 para dispositivos de rede, convertendo arquivos protegidos por DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644c1b4f7ede688434fbb1dde11b7051c6f644a5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640171"
---
# <a name="converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream"></a>Convertendo um arquivo de DRM-Protected em um fluxo do Windows Media DRM 10 para dispositivos de rede

Depois que um dispositivo é registrado e validado, você pode começar a processar mensagens de solicitação de licença dele. As mensagens de solicitação de licença são enviadas pelos dispositivos quando a ação do aplicativo é necessária. A única ação com suporte no momento é "Play", que é uma solicitação de dados seguros para reprodução.

Ao receber uma mensagem de solicitação de licença, você deve executar as seguintes etapas:

1.  Analise a mensagem de solicitação de licença chamando o método [**IWMDRMMessageParser::P arselicenserequestmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg) .
2.  Obtenha a interface [**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice) para o dispositivo chamando o método [**IWMDeviceRegistration:: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) , passando o certificado e o número de série obtidos na etapa 1.
3.  Verifique se o dispositivo está pronto para receber dados seguros:
    -   Chame [**IWMRegisteredDevice:: IsApproved**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved) para verificar se o dispositivo foi aprovado. A aprovação deve sempre ser baseada na preferência do usuário.
    -   Chame [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) para verificar se o dispositivo foi validado nas últimas 48 horas. Se o dispositivo não for válido, você precisará executar a detecção de proximidade. Para obter mais informações, consulte [executando a detecção de proximidade](performing-proximity-detection.md).
    -   Chame [**IWMRegisteredDevice:: Isopend**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened) para verificar se o dispositivo foi aberto. Se o dispositivo não estiver aberto, você poderá abri-lo chamando [**IWMRegisteredDevice:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open). Você só pode ter 10 dispositivos abertos no computador por vez. É possível que você precise fechar outro dispositivo antes de poder abrir aquele para o qual você está processando a solicitação. Para fechar um dispositivo, chame o método [**IWMRegisteredDevice:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close) .
4.  Crie uma instância do objeto de transcriptografador DRM chamando a função [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) .
5.  Chame o método [**IWMDRMTranscryptor:: Initialize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize) para inicializar o transcriptr. Esse método usa um ponteiro para a implementação da interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) , que ele usa para entregar mensagens de status. Esse método também retorna uma mensagem de solicitação de licença que deve ser enviada para o dispositivo antes de continuar.
6.  Quando o método [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) do seu aplicativo receber a \_ mensagem de status de inicialização do transcriptr do WMT \_ , chame o método [**IWMDRMTranscryptor:: Seek**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-seek) para buscar a posição inicial apropriada no arquivo. Para iniciar no início do arquivo, você deve chamar **Seek** com o tempo 0.
7.  O transcriptografador envia uma mensagem de descriptografia WMT \_ \_ quando está pronto para entregar dados do arquivo no novo horário de apresentação. Faça chamadas repetidas para o método [**IWMDRMTranscryptor:: Read**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read) para obter partes convertidas de dados de mídia. Cada chamada é assíncrona e não é concluída até que uma mensagem de leitura do transWMTn \_ \_ seja recebida. Ao receber a mensagem, você pode enviar os dados para o dispositivo receptor.
8.  Quando você recebe uma mensagem de leitura do transWMTer \_ \_ com o parâmetro *HR* definido como \_ EOF do \_ transcriptr NS S \_ , todo o arquivo foi lido. Neste ponto, chame o método [**IWMDRMTranscryptor:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-close) para fechar o arquivo e liberar recursos.
9.  Quando a mensagem de descriptografia de WMT \_ \_ fechada é recebida, você pode liberar a interface [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) .

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o protocolo Windows Media DRM 10 para dispositivos de rede**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




