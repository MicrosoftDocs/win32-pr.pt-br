---
title: Modelo de Data-Pull e modelo de Data-Push
description: Modelo de Data-Pull e modelo de Data-Push
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab89f61301f9116a7e826f1965bd54f75004a3a90af8c9d1a1bc13acb1fc9c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048444"
---
# <a name="data-pull-model-and-data-push-model"></a>Modelo de Data-Pull e modelo de Data-Push

Um cliente de um moniker assíncrono pode escolher entre um modelo de pull de dados e de envio de dados para conduzir uma operação assíncrona [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) e receber notificações assíncronas. No modelo de pull de dados, o cliente orienta a operação de associação e o moniker fornece dados para o cliente somente quando ele é lido. Em outras palavras, após a primeira chamada para [**IBindStatusCallback:: OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), o moniker não fornece nenhum dado para o cliente, a menos que o cliente tenha consumido todos os dados que já estão disponíveis.

Como os dados são baixados apenas conforme solicitado, os clientes que escolhem o modelo de pull de dados devem certificar-se de ler esses dados em tempo hábil. No caso de downloads da Internet com [monikers de URL](url-monikers.md), a operação de associação poderá falhar se um cliente aguardar muito tempo antes de solicitar mais dados.

No modelo de envio de dados por push, o moniker orienta a operação de vinculação assíncrona e notifica continuamente o cliente sempre que novos dados estiverem disponíveis. O cliente pode escolher se deseja ler os dados a qualquer momento durante a operação de associação, mas o moniker orientará a operação de associação a ser concluída, independentemente.

Além disso, você precisa se lembrar de seguir as regras COM para alocação de memória ao usar monikers assíncronos, especificamente o seguinte:

-   Sempre que uma interface COM ou chamada de função retorna um buffer (cadeia de caracteres ou outro) para seu cliente, o cliente é responsável por liberar a memória chamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).
-   Sempre que uma interface COM ou função requer um buffer de seu cliente, o cliente deve alocar esse buffer usando [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) e o receptor deve liberá-lo.

Certifique-se de seguir essas regras ao alocar cadeias de caracteres ou buffers que são passados para monikers assíncronos e lembre-se de liberar memória retornada por monikers assíncronos. Consulte [Gerenciando alocação de memória](the-com-library.md) e tópicos relacionados para obter detalhes completos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monikers assíncronos](asynchronous-monikers.md)
</dt> </dl>

 

 