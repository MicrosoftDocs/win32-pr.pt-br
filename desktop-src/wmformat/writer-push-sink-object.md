---
title: Objeto de coletor de push do gravador
description: Objeto de coletor de push do gravador
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- SDK do Windows Media Format, objetos do coletor de push do Writer
- ASF (Advanced Systems Format), objetos do coletor push do Writer
- ASF (formato de sistemas avançados), objetos do coletor de push de gravador
- objetos, objetos de coletor de push de gravador
- objetos do coletor de push de gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19ea9855219dcb4572ef187ad93e03696b88492
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916983"
---
# <a name="writer-push-sink-object"></a>Objeto de coletor de push do gravador

O objeto de coletor de push de gravador distribui mídia digital para pontos de publicação. Por exemplo, um concerto ao vivo pode ser codificado por um único servidor e, em seguida, entregue, ou *enviado por push*, a vários outros servidores que, de fato, transmitirão o conteúdo aos usuários.

Um objeto de coletor de push de gravador é criado pela função [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), que define um ponteiro para uma interface **IWMWriterPushSink** . As outras interfaces com suporte do objeto, listadas na tabela a seguir, podem ser obtidas chamando o método **QueryInterface** .



| Interface                                          | Descrição                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Permite que o aplicativo obtenha mensagens de status do objeto.                                                  |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | Gerencia uma sessão de distribuição por push.                                                                             |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Aloca memória, determina se o coletor está operando em tempo real e expõe várias funções de retorno de chamada. |



 

A interface de retorno de chamada a seguir pode ser implementada pelo aplicativo para acompanhar o progresso de um objeto de coletor de push de gravador.



| Interface                                      | Descrição                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Necessário quando as informações de status devem ser comunicadas ao aplicativo host. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Enviando dados ASF para um ponto de publicação**](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[**Trabalhando com coletores de gravador**](working-with-writer-sinks.md)
</dt> </dl>

 

 




