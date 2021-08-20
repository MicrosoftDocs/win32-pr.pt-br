---
title: Objeto do Sink de Rede do Writer
description: Objeto do Sink de Rede do Writer
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- Windows SDK de Formato de Mídia, objetos de sink de rede do writer
- FORMATO DE SISTEMAS Avançados (ASF), objetos de sink de rede de writer
- ASF (Formato de Sistemas Avançados), objetos de sink de rede de writer
- objetos, objetos de sink de rede de writer
- objetos do sink de rede do writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2011fd161fc4ac5e1cd03d955f06259e6499e343970cc309b1e8c41db051a32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843721"
---
# <a name="writer-network-sink-object"></a>Objeto do Sink de Rede do Writer

O objeto do sink de rede de gravação é usado para gravar mídia digital em uma rede.

O objeto do sink de rede do writer é criado pela função [**WMCreateWriterNetworkSink,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)que define um ponteiro para uma interface **IWMWriterNetworkSink.** As outras interfaces do objeto do sink de rede do autor podem ser obtidas chamando o **método QueryInterface.**



| Interface                                              | Descrição                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | Coleta informações sobre clientes conectados.                                                                                                                                                                      |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | Recupera informações avançadas do cliente.                                                                                                                                                                          |
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | Permite que o aplicativo receba mensagens de status do objeto .                                                                                                                                                 |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | Abre e fecha portas, define e recupera o número máximo de clientes que podem se conectar ao objeto de sink, define o protocolo de rede a ser usado pelo objeto writer e executa outras funções avançadas. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | Aloca memória, determina se o sink está operando em tempo real e lida com várias funções de retorno de chamada.                                                                                                |



 

A interface de retorno de chamada a seguir pode ser implementada pelo aplicativo para acompanhar o progresso de um objeto de sink de rede do writer.



| Interface                                      | Descrição                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Necessário quando as informações de status devem ser comunicadas ao aplicativo host. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Transmissão de dados ASF**](broadcasting-asf-data.md)
</dt> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Trabalhando com os sinks do Writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




