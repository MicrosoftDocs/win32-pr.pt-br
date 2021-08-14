---
title: Enviando dados ASF para um ponto de publicação
description: Enviando dados ASF para um ponto de publicação
ms.assetid: 8f01beae-4270-4cf5-afff-3f7014cae90f
keywords:
- Windows SDK de Formato de Mídia, enviando dados ASF
- Windows SDK de Formato de Mídia, pontos de publicação
- ASF (Advanced Systems Format), enviando dados
- ASF (Formato de Sistemas Avançados), enviando dados
- FORMATO DE SISTEMAS Avançados (ASF), pontos de publicação
- ASF (Formato de Sistemas Avançados), pontos de publicação
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

Você pode usar o SDK Windows Formato de Mídia para efetuar push de dados ASF para um ponto de publicação em um Windows De mídia. Em seguida, o servidor transmite os dados desse ponto de publicação. Esse cenário será útil se você estiver capturando ou codificando conteúdo em um computador e desejar distribuir o conteúdo de outro computador (ou vários computadores). Também será útil se você precisar mover o conteúdo de um computador dentro de um firewall para um servidor de mídia Windows para fora do firewall, pois a distribuição por push usa o protocolo HTTP.

> [!Note]  
> Um *ponto de publicação atua* essencialmente como um redirecionador. O cliente especifica o ponto de publicação na URL (por exemplo, mms://MyServer/MyPublishingPoint) e o servidor converte isso em uma solicitação de conteúdo.

 

Para fazer push de dados para o ponto de publicação, anexe o objeto de sink push ao objeto writer. O sink push é usado para abrir a conexão com o servidor e gerenciar a sessão de push. O objeto writer trata todos os outros aspectos da criação do arquivo.

Execute as seguintes etapas:

1.  Crie o objeto writer chamando a [**função WMCreateWriter,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) que retorna um [**ponteiro IWMWriter.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
2.  Crie o objeto do sink push chamando a [**função WMCreateWriterPushSink,**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) que retorna um ponteiro [**IWMWriterPushSink.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)
3.  Anexe o sink de rede ao autor chamando [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) no autor, com um ponteiro para a interface **IWMWriterPushSink** do sink de rede.
4.  Conexão ao servidor chamando [**IWMWriterPushSink::Conexão**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect).
5.  Escreva o fluxo. Esta etapa envolve a configuração do perfil no objeto writer, o envio de exemplos para o autor e, possivelmente, outras tarefas. Para obter mais informações, consulte [Escrevendo arquivos ASF](writing-asf-files.md). Tarefas adicionais podem incluir a configuração de atributos de metadados (conforme descrito em Trabalhando com metadados [)](working-with-metadata.md)ou a configuração de DRM ao vivo no fluxo (conforme descrito em Habilitando o [suporte a DRM).](enabling-drm-support.md) Essas tarefas são executadas exatamente como são para a escrita de arquivo ASF.
6.  Depois de terminar de escrever, chame [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) no autor para desconectar o objeto do sink push.
7.  Chame [**IWMWriterPushSink::EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) no sink push para encerrar a sessão com o servidor.

Essas etapas são ilustradas no aplicativo de exemplo WMVNetWrite.

> [!Note]  
> Se você estiver enviando um arquivo somente vídeo de taxa de bits muito baixa, ele poderá não começar a ser gravado no ponto de publicação por vários segundos. Isso pode acontecer em vários casos, por exemplo, quando um único pacote contém muitos quadros de vídeo pequenos e nenhum áudio ou quando há uma lacuna de tempo longa entre o primeiro pacote e o segundo pacote em um arquivo somente vídeo de taxa de bits baixa. Para evitar esse problema, insira um fluxo de áudio silencioso no arquivo.

 

## <a name="authentication"></a>Autenticação

A autenticação no servidor é manipulada automaticamente pelo objeto do sink push. No entanto, o aplicativo pode precisar fornecer credenciais. Isso é feito por meio da interface de retorno de chamada **IWMCredentialCallback,** da seguinte forma:

1.  Implemente a interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) [**e IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) em seu aplicativo.
2.  Consulte o objeto do sink push para a interface [**IWMRegisterCallback.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)
3.  Chame [**IWMRegisterCallback::Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) com um ponteiro para a interface **IWMStatusCallback** do aplicativo.
4.  Se o sink push precisar obter credenciais do aplicativo, ele consultará o ponteiro **IWMStatusCallback** para a interface **IWMCredentialCallback** e [**chamará IWMCredentialCallback::AcquireCredentials**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials). Para obter informações sobre esse método, consulte [Autenticação](authentication.md).
5.  Quando terminar, chame [**IWMRegisterCallback::Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) para parar de receber notificações de eventos do sink push.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Enviando dados ASF por uma rede**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Trabalhando com os sinks do Writer**](working-with-writer-sinks.md)
</dt> <dt>

[**Objeto do sink push do writer**](writer-push-sink-object.md)
</dt> </dl>

 

 




