---
title: Objeto de coletor de rede do gravador
description: Objeto de coletor de rede do gravador
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- SDK do Windows Media Format, objetos do coletor de rede do Writer
- ASF (Advanced Systems Format), objetos do coletor de rede do Writer
- ASF (formato de sistemas avançados), objetos de coletor de rede do gravador
- objetos, objetos do coletor de rede do gravador
- objetos do coletor de rede do gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85af356c1d326ddaaf3703ca87c3b7bdd1628b9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104084399"
---
# <a name="writer-network-sink-object"></a>Objeto de coletor de rede do gravador

O objeto de coletor de rede do gravador é usado para gravar mídia digital em uma rede.

O objeto de coletor de rede do gravador é criado pela função [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), que define um ponteiro para uma interface **IWMWriterNetworkSink** . As outras interfaces do objeto de coletor de rede do gravador podem ser obtidas chamando o método **QueryInterface** .



| Interface                                              | Descrição                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | Coleta informações sobre clientes conectados.                                                                                                                                                                      |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | Recupera informações avançadas do cliente.                                                                                                                                                                          |
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | Permite que o aplicativo obtenha mensagens de status do objeto.                                                                                                                                                 |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | Abre e fecha portas, define e recupera o número máximo de clientes que podem se conectar ao objeto do coletor, define o protocolo de rede a ser usado pelo objeto do gravador e executa outras funções avançadas. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | Aloca memória, determina se o coletor está operando em tempo real e manipula várias funções de retorno de chamada.                                                                                                |



 

A interface de retorno de chamada a seguir pode ser implementada pelo aplicativo para acompanhar o progresso de um objeto de coletor de rede do gravador.



| Interface                                      | Descrição                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Necessário quando as informações de status devem ser comunicadas ao aplicativo host. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Transmissão de dados ASF**](broadcasting-asf-data.md)
</dt> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Trabalhando com coletores de gravador**](working-with-writer-sinks.md)
</dt> </dl>

 

 




