---
title: Para interromper a indexação em andamento
description: Para interromper a indexação em andamento
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- SDK do Windows Media Format, parando a indexação em andamento
- ASF (Advanced Systems Format), parando a indexação em andamento
- ASF (formato de sistemas avançados), parando a indexação em andamento
- índices, parando a indexação em andamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea40cbf020182250e0fb982af5b5f84327d5d9a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007134"
---
# <a name="to-stop-indexing-in-progress"></a>Para interromper a indexação em andamento

Depois de começar a indexação com uma chamada para [**IWMIndexer:: startIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), o indexador normalmente continuará até que o arquivo seja indexado. Você pode parar a indexação de operações chamando o método [**IWMIndexer:: Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) . Depois de ter cancelado a indexação, você **pode chamar de** forma diferente, mas o indexador começará a partir do início do arquivo, em vez de retomar a partir do ponto de cancelamento.

Como o **startIndex** é uma chamada assíncrona, normalmente você precisará chamar **Cancel** de algum outro thread ou manipulador de eventos em seu aplicativo. Normalmente, o **cancelamento** será chamado a partir de um procedimento de evento associado a um controle de botão de um aplicativo do Windows.

Quando a indexação for cancelada, o indexador passará uma mensagem de status de WMT \_ fechada, assim como se o arquivo tivesse sido indexado corretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> </dl>

 

 




