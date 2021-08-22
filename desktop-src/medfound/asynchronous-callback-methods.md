---
description: Métodos de retorno de chamada assíncrono
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Métodos de retorno de chamada assíncrono
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e59fec2423d6bc1b02a3f5ce05855419596bc92ea54062303ebd1315d087e489
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606706"
---
# <a name="asynchronous-callback-methods"></a>Métodos de retorno de chamada assíncrono

Media Foundation fornece uma maneira consistente de implementar métodos assíncronos, usando uma interface de retorno de chamada.

Esta seção descreve como implementar a interface de retorno de chamada e como escrever métodos assíncronos que usam essa interface. Ele contém os tópicos a seguir.



| Tópico                                                                                | Descrição                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Chamando métodos assíncronos](calling-asynchronous-methods.md)                     | Como chamar métodos assíncronos no Media Foundation.                                               |
| [Implementando o retorno de chamada assíncrono](implementing-the-asynchronous-callback.md) | Como implementar o método de retorno de chamada na interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . |
| [Dando suporte a vários retornos de chamada](supporting-multiple-callbacks.md)                   | Como dar suporte a vários retornos de chamada dentro da mesma classe C++.                                        |
| [Filas de trabalho](work-queues.md)                                                       | As filas de trabalho fornecem uma maneira eficiente de executar operações assíncronas em outro thread.          |
| [Escrevendo um método assíncrono](writing-an-asynchronous-method.md)                 | Como implementar métodos assíncronos no Media Foundation.                                          |
| [Objetos de resultados assíncronos personalizados](custom-asynchronous-result-objects.md)         | Como fornecer uma implementação personalizada da interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[**Interface IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[APIs da plataforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



