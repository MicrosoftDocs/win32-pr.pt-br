---
title: Objeto do sink push do writer
description: Objeto do sink push do writer
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- Windows SDK de Formato de Mídia, objetos do sink de push do autor
- FORMATO DE SISTEMAS Avançados (ASF), objetos de sink de push do autor
- ASF (Formato de Sistemas Avançados), objetos de sink de push do autor
- objetos, objetos de sink de push do autor
- objetos do sink push do writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859e4d2d5cf2530e655b74705b1d6f9ef93960d28f523c00e0da7a7336ab258d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006326"
---
# <a name="writer-push-sink-object"></a>Objeto do sink push do writer

O objeto do sink de push do autor distribui mídia digital para pontos de publicação. Por exemplo, um show ao vivo pode ser codificado por um único servidor e, em seguida, entregue ou enviado por e/ou enviado por *e/ou* para vários outros servidores que realmente transmitirão o conteúdo para os usuários.

Um objeto de sink de push do autor é criado pela função [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), que define um ponteiro para uma interface **IWMWriterPushSink.** As outras interfaces com suporte pelo objeto , listadas na tabela a seguir, podem ser obtidas chamando o **método QueryInterface.**



| Interface                                          | Descrição                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Permite que o aplicativo receba mensagens de status do objeto .                                                  |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | Gerencia uma sessão de distribuição por push.                                                                             |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Aloca memória, determina se o sink está operando em tempo real e expõe várias funções de retorno de chamada. |



 

A interface de retorno de chamada a seguir pode ser implementada pelo aplicativo para acompanhar o progresso de um objeto de sink de push do autor.



| Interface                                      | Descrição                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Necessário quando as informações de status devem ser comunicadas ao aplicativo host. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Enviando dados ASF para um ponto de publicação**](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[**Trabalhando com os sinks do Writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




