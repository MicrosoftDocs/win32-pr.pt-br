---
title: Modelo de Data-Pull e modelo de Data-Push
description: Modelo de Data-Pull e modelo de Data-Push
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f6607e9b466c439859a99b857e7ce3fe6d8acd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366789"
---
# <a name="data-pull-model-and-data-push-model"></a><span data-ttu-id="7c9db-103">Modelo de Data-Pull e modelo de Data-Push</span><span class="sxs-lookup"><span data-stu-id="7c9db-103">Data-Pull Model and Data-Push Model</span></span>

<span data-ttu-id="7c9db-104">Um cliente de um moniker assíncrono pode escolher entre um modelo de pull de dados e de envio de dados para conduzir uma operação assíncrona [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) e receber notificações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="7c9db-104">A client of an asynchronous moniker can choose between a data-pull and data-push model for driving an asynchronous [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) operation and receiving asynchronous notifications.</span></span> <span data-ttu-id="7c9db-105">No modelo de pull de dados, o cliente orienta a operação de associação e o moniker fornece dados para o cliente somente quando ele é lido.</span><span class="sxs-lookup"><span data-stu-id="7c9db-105">In the data-pull model, the client drives the bind operation and the moniker provides data to the client only as it is read.</span></span> <span data-ttu-id="7c9db-106">Em outras palavras, após a primeira chamada para [**IBindStatusCallback:: OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), o moniker não fornece nenhum dado para o cliente, a menos que o cliente tenha consumido todos os dados que já estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7c9db-106">In other words, after the first call to [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), the moniker does not provide any data to the client unless the client has consumed all of the data that is already available.</span></span>

<span data-ttu-id="7c9db-107">Como os dados são baixados apenas conforme solicitado, os clientes que escolhem o modelo de pull de dados devem certificar-se de ler esses dados em tempo hábil.</span><span class="sxs-lookup"><span data-stu-id="7c9db-107">Because data is downloaded only as it is requested, clients that choose the data-pull model must make sure to read this data in a timely manner.</span></span> <span data-ttu-id="7c9db-108">No caso de downloads da Internet com [monikers de URL](url-monikers.md), a operação de associação poderá falhar se um cliente aguardar muito tempo antes de solicitar mais dados.</span><span class="sxs-lookup"><span data-stu-id="7c9db-108">In the case of Internet downloads with [URL monikers](url-monikers.md), the bind operation may fail if a client waits too long before requesting more data.</span></span>

<span data-ttu-id="7c9db-109">No modelo de envio de dados por push, o moniker orienta a operação de vinculação assíncrona e notifica continuamente o cliente sempre que novos dados estiverem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7c9db-109">In the data-push model, the moniker drives the asynchronous bind operation and continuously notifies the client whenever new data is available.</span></span> <span data-ttu-id="7c9db-110">O cliente pode escolher se deseja ler os dados a qualquer momento durante a operação de associação, mas o moniker orientará a operação de associação a ser concluída, independentemente.</span><span class="sxs-lookup"><span data-stu-id="7c9db-110">The client may choose whether to read the data at any point during the bind operation, but the moniker will drive the bind operation to completion regardless.</span></span>

<span data-ttu-id="7c9db-111">Além disso, você precisa se lembrar de seguir as regras COM para alocação de memória ao usar monikers assíncronos, especificamente o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7c9db-111">Also, you need to remember to follow the COM rules for memory allocation when using asynchronous monikers, specifically the following:</span></span>

-   <span data-ttu-id="7c9db-112">Sempre que uma interface COM ou chamada de função retorna um buffer (cadeia de caracteres ou outro) para seu cliente, o cliente é responsável por liberar a memória chamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="7c9db-112">Whenever a COM interface or function call returns a buffer (string or other) to its client, the client is responsible for freeing the memory by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>
-   <span data-ttu-id="7c9db-113">Sempre que uma interface COM ou função requer um buffer de seu cliente, o cliente deve alocar esse buffer usando [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) e o receptor deve liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="7c9db-113">Whenever a COM interface or function requires a buffer from its client, the client must allocate that buffer using [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) and the callee must free it.</span></span>

<span data-ttu-id="7c9db-114">Certifique-se de seguir essas regras ao alocar cadeias de caracteres ou buffers que são passados para monikers assíncronos e lembre-se de liberar memória retornada por monikers assíncronos.</span><span class="sxs-lookup"><span data-stu-id="7c9db-114">Be sure to follow these rules when allocating strings or buffers that are passed to asynchronous monikers, and remember to free memory returned by asynchronous monikers.</span></span> <span data-ttu-id="7c9db-115">Consulte [Gerenciando alocação de memória](the-com-library.md) e tópicos relacionados para obter detalhes completos.</span><span class="sxs-lookup"><span data-stu-id="7c9db-115">See [Managing Memory Allocation](the-com-library.md) and related topics for complete details.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c9db-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c9db-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c9db-117">Monikers assíncronos</span><span class="sxs-lookup"><span data-stu-id="7c9db-117">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 