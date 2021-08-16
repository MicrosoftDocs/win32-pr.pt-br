---
title: Enviando dados ASF para um ponto de publicação
description: Enviando dados ASF para um ponto de publicação
ms.assetid: 8f01beae-4270-4cf5-afff-3f7014cae90f
keywords:
- Windows SDK do formato de mídia, enviando dados do ASF
- Windows SDK do formato de mídia, pontos de publicação
- ASF (Advanced Systems Format), enviando dados
- ASF (formato de sistemas avançados), enviando dados
- ASF (Advanced Systems Format), pontos de publicação
- ASF (formato de sistemas avançados), pontos de publicação
- pontos de publicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f70c1a49ea7ff6272d0eef9f1a51ff79ec216ed9af445c3078d59dd19841dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197534"
---
# <a name="sending-asf-data-to-a-publishing-point"></a>Enviando dados ASF para um ponto de publicação

você pode usar o SDK do formato de mídia Windows para enviar dados ASF para um ponto de publicação em um servidor de mídia Windows. Em seguida, o servidor transmite os dados desse ponto de publicação. Esse cenário será útil se você estiver capturando ou recodificando o conteúdo em um computador e desejar distribuir o conteúdo de outro computador (ou vários computadores). ele também será útil se você precisar mover o conteúdo de um computador dentro de um firewall para um Windows servidor de mídia fora do firewall, pois a distribuição por push usa o protocolo HTTP.

> [!Note]  
> Um *ponto de publicação* funciona basicamente como um redirecionador. O cliente especifica o ponto de publicação na URL (por exemplo, mms://MyServer/MyPublishingPoint) e o servidor converte isso em uma solicitação de conteúdo.

 

Para enviar dados por push ao ponto de publicação, anexe o objeto de coletor de push ao objeto gravador. O coletor de Push é usado para abrir a conexão com o servidor e gerenciar a sessão de push. O objeto gravador manipula todos os outros aspectos da criação do arquivo.

Execute as seguintes etapas:

1.  Crie o objeto gravador chamando a função [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) , que retorna um ponteiro [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) .
2.  Crie o objeto de coletor de push chamando a função [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) , que retorna um ponteiro [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) .
3.  Anexe o coletor de rede ao gravador chamando [**IWMWriterAdvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) no gravador, com um ponteiro para a interface **IWMWriterPushSink** do coletor de rede.
4.  Conexão ao servidor chamando [**IWMWriterPushSink:: Conexão**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect).
5.  Grave o fluxo. Esta etapa envolve a definição do perfil no objeto do gravador, o envio de amostras ao gravador e, possivelmente, outras tarefas. Para obter mais informações, consulte [Writing ASF files](writing-asf-files.md). Tarefas adicionais podem incluir atributos de metadados de configuração (conforme descrito em [trabalhando com metadados](working-with-metadata.md)) ou configurar o DRM ao vivo no fluxo (conforme descrito em [habilitando o suporte a DRM](enabling-drm-support.md)). Essas tarefas são executadas exatamente como são para gravação de arquivo ASF.
6.  Depois de terminar de escrever, chame [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) no gravador para desanexar o objeto do coletor de push.
7.  Chame [**IWMWriterPushSink:: EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) no coletor de push para encerrar a sessão com o servidor.

Essas etapas são ilustradas no aplicativo de exemplo WMVNetWrite.

> [!Note]  
> Se você estiver enviando um arquivo somente de vídeo de taxa de bits muito baixa, ele poderá não começar a ser reproduzido no ponto de publicação por vários segundos. Isso pode acontecer em vários casos, por exemplo, quando um único pacote contém muitos quadros de vídeo pequenos e sem áudio, ou quando há uma lacuna de tempo longa entre o primeiro pacote e o segundo pacote em um arquivo somente de vídeo de taxa de bits baixa. Para evitar esse problema, insira um fluxo de áudio silencioso no arquivo.

 

## <a name="authentication"></a>Autenticação

A autenticação para o servidor é manipulada automaticamente pelo objeto de coletor de push. No entanto, o aplicativo pode precisar fornecer credenciais. Isso é feito por meio da interface de retorno de chamada do **IWMCredentialCallback** , da seguinte maneira:

1.  Implemente a interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) e [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) em seu aplicativo.
2.  Consulte o objeto de coletor de push para a interface [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) .
3.  Chame [**IWMRegisterCallback:: Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) com um ponteiro para a interface **IWMStatusCallback** do seu aplicativo.
4.  Se o coletor de push precisar obter credenciais do aplicativo, ele consultará o ponteiro **IWMStatusCallback** para a interface **IWMCredentialCallback** e chamará [**IWMCredentialCallback:: AcquireCredentials**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials). Para obter informações sobre esse método, consulte [autenticação](authentication.md).
5.  Quando terminar, chame [**IWMRegisterCallback:: Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) para parar de obter notificações de eventos do coletor de push.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Enviando dados ASF por meio de uma rede**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Trabalhando com coletores de gravador**](working-with-writer-sinks.md)
</dt> <dt>

[**Objeto de coletor de push do gravador**](writer-push-sink-object.md)
</dt> </dl>

 

 




