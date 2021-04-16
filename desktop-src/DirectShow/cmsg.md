---
description: A classe CMsgThread Fornece suporte para um thread de trabalho para o qual as solicitações podem ser postadas de forma assíncrona, em vez de enviadas diretamente.
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: Classe CMsg
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg
api_type:
- COM
api_location: ''
ms.openlocfilehash: a57a841b9c36a21895099c931acbf18a1e01ea0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105750472"
---
# <a name="cmsg-class"></a><span data-ttu-id="7725c-103">Classe CMsg</span><span class="sxs-lookup"><span data-stu-id="7725c-103">CMsg class</span></span>

<span data-ttu-id="7725c-104">A classe [**CMsgThread**](cmsgthread.md) fornece suporte para um thread de trabalho para o qual as solicitações podem ser postadas de forma assíncrona, em vez de enviadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="7725c-104">The [**CMsgThread**](cmsgthread.md) class provides support for a worker thread to which requests can be posted asynchronously instead of sent directly.</span></span> <span data-ttu-id="7725c-105">A classe [**CAMThread**](camthread.md) fornece um thread de trabalho para o qual podem ser enviadas solicitações únicas.</span><span class="sxs-lookup"><span data-stu-id="7725c-105">The [**CAMThread**](camthread.md) class provides a worker thread to which single requests can be sent.</span></span> <span data-ttu-id="7725c-106">Somente um cliente pode fazer uma solicitação por vez, e o cliente é bloqueado até que o thread de trabalho tenha concluído a solicitação.</span><span class="sxs-lookup"><span data-stu-id="7725c-106">Only one client can make a request at a time, and the client blocks until the worker thread has completed the request.</span></span> <span data-ttu-id="7725c-107">Por outro lado, a classe **CMsgThread** fornece um thread de trabalho para o qual qualquer número de solicitações pode ser lançada.</span><span class="sxs-lookup"><span data-stu-id="7725c-107">By contrast, the **CMsgThread** class provides a worker thread to which any number of requests can be posted.</span></span> <span data-ttu-id="7725c-108">As solicitações (na forma de um `CMsg` objeto) são enfileiradas e executadas em ordem, de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="7725c-108">The requests (in the form of a `CMsg` object) are queued and executed in order, asynchronously.</span></span> <span data-ttu-id="7725c-109">Nenhum valor de resposta ou retorno é recebido.</span><span class="sxs-lookup"><span data-stu-id="7725c-109">No reply or return value is received.</span></span>



| <span data-ttu-id="7725c-110">Membros de dados</span><span class="sxs-lookup"><span data-stu-id="7725c-110">Data Members</span></span>              | <span data-ttu-id="7725c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7725c-111">Description</span></span>                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7725c-112">dwFlags</span><span class="sxs-lookup"><span data-stu-id="7725c-112">dwFlags</span></span>                   | <span data-ttu-id="7725c-113">Sinalizador de parâmetro para o código de solicitação.</span><span class="sxs-lookup"><span data-stu-id="7725c-113">Flag parameter to the request code.</span></span>                                                                                                                                               |
| <span data-ttu-id="7725c-114">lpParam</span><span class="sxs-lookup"><span data-stu-id="7725c-114">lpParam</span></span>                   | <span data-ttu-id="7725c-115">Dados exigidos pelo thread de trabalho como valores de parâmetro ou retorno.</span><span class="sxs-lookup"><span data-stu-id="7725c-115">Data required by the worker thread as parameter or return values.</span></span> <span data-ttu-id="7725c-116">Esses dados não devem ser baseados em pilha, pois serão referenciados algum tempo após a conclusão da operação de enfileiramento.</span><span class="sxs-lookup"><span data-stu-id="7725c-116">This data should not be stack-based, as it will be referenced some time after completing the queuing operation.</span></span> |
| <span data-ttu-id="7725c-117">pEvent</span><span class="sxs-lookup"><span data-stu-id="7725c-117">pEvent</span></span>                    | <span data-ttu-id="7725c-118">Objeto de evento que um thread de trabalho pode sinalizar para indicar a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="7725c-118">Event object that a worker thread can signal to indicate the completion of the operation.</span></span>                                                                                         |
| <span data-ttu-id="7725c-119">uMsg</span><span class="sxs-lookup"><span data-stu-id="7725c-119">uMsg</span></span>                      | <span data-ttu-id="7725c-120">O código de solicitação que é definido pelo cliente da classe thread e compreendido pela função de thread de trabalho substituída.</span><span class="sxs-lookup"><span data-stu-id="7725c-120">Request code that is defined by the client of the thread class and understood by the overridden worker thread function.</span></span>                                                           |
| <span data-ttu-id="7725c-121">Funções de membro</span><span class="sxs-lookup"><span data-stu-id="7725c-121">Member Functions</span></span>          | <span data-ttu-id="7725c-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="7725c-122">Description</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="7725c-123">**CMsg**</span><span class="sxs-lookup"><span data-stu-id="7725c-123">**CMsg**</span></span>](cmsg-cmsg.md) | <span data-ttu-id="7725c-124">Constrói um objeto [**CMsg**](cmsg-cmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="7725c-124">Constructs a [**CMsg**](cmsg-cmsg.md) object.</span></span>                                                                                                                                    |



 

 

 



