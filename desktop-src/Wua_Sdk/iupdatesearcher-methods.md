---
description: A interface IUpdateSearcher define os métodos a seguir.
ms.assetid: 82735555-b23a-43b0-bf5b-a8cf72dc40d4
title: Métodos IUpdateSearcher
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 462cbd371546743bab836ed1cdc2479e30f13612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769263"
---
# <a name="iupdatesearcher-methods"></a><span data-ttu-id="85f48-103">Métodos IUpdateSearcher</span><span class="sxs-lookup"><span data-stu-id="85f48-103">IUpdateSearcher Methods</span></span>

<span data-ttu-id="85f48-104">A interface [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) define os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="85f48-104">The [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) interface defines the following methods.</span></span>



| <span data-ttu-id="85f48-105">Método</span><span class="sxs-lookup"><span data-stu-id="85f48-105">Method</span></span>                                                              | <span data-ttu-id="85f48-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="85f48-106">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85f48-107">**BeginSearch**</span><span class="sxs-lookup"><span data-stu-id="85f48-107">**BeginSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)                   | <span data-ttu-id="85f48-108">Inicia a execução de uma pesquisa assíncrona para atualizações.</span><span class="sxs-lookup"><span data-stu-id="85f48-108">Begins execution of an asynchronous search for updates.</span></span> <span data-ttu-id="85f48-109">A pesquisa usa as opções de pesquisa que estão configuradas no momento.</span><span class="sxs-lookup"><span data-stu-id="85f48-109">The search uses the search options that are currently configured.</span></span> |
| [<span data-ttu-id="85f48-110">**Endsearch**</span><span class="sxs-lookup"><span data-stu-id="85f48-110">**EndSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)                       | <span data-ttu-id="85f48-111">Conclui uma pesquisa assíncrona de atualizações.</span><span class="sxs-lookup"><span data-stu-id="85f48-111">Completes an asynchronous search for updates.</span></span>                                                                             |
| [<span data-ttu-id="85f48-112">**EscapeString**</span><span class="sxs-lookup"><span data-stu-id="85f48-112">**EscapeString**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-escapestring)                 | <span data-ttu-id="85f48-113">Converte uma cadeia de caracteres em uma cadeia de caracteres que pode ser usada como um valor literal em uma cadeia de caracteres de critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="85f48-113">Converts a string into a string that can be used as a literal value in a search criteria string.</span></span>                          |
| [<span data-ttu-id="85f48-114">**GetTotalHistoryCount**</span><span class="sxs-lookup"><span data-stu-id="85f48-114">**GetTotalHistoryCount**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-gettotalhistorycount) | <span data-ttu-id="85f48-115">Retorna o número de eventos de atualização no computador.</span><span class="sxs-lookup"><span data-stu-id="85f48-115">Returns the number of update events on the computer.</span></span>                                                                      |
| [<span data-ttu-id="85f48-116">**QueryHistory**</span><span class="sxs-lookup"><span data-stu-id="85f48-116">**QueryHistory**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-queryhistory)                | <span data-ttu-id="85f48-117">Consulta de forma síncrona o computador para o histórico de eventos de atualização.</span><span class="sxs-lookup"><span data-stu-id="85f48-117">Synchronously queries the computer for the history of update events.</span></span>                                                      |
| [<span data-ttu-id="85f48-118">**Search**</span><span class="sxs-lookup"><span data-stu-id="85f48-118">**Search**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search)                             | <span data-ttu-id="85f48-119">Executa uma pesquisa síncrona para atualizações.</span><span class="sxs-lookup"><span data-stu-id="85f48-119">Performs a synchronous search for updates.</span></span> <span data-ttu-id="85f48-120">A pesquisa usa as opções de pesquisa que estão configuradas no momento.</span><span class="sxs-lookup"><span data-stu-id="85f48-120">The search uses the search options that are currently configured.</span></span>              |



 

 

 



