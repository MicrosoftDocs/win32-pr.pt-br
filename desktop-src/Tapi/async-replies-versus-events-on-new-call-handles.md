---
description: O TSPI inclui várias operações que iniciam o tempo de vida de um identificador de chamada.
ms.assetid: 28e171a3-db47-40fd-9c5a-d7b76d834a99
title: Respostas assíncronas versus eventos em novos identificadores de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02511a083c318afb227e3e172191d3ab84a69fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829131"
---
# <a name="async-replies-versus-events-on-new-call-handles"></a><span data-ttu-id="00999-103">Respostas assíncronas versus eventos em novos identificadores de chamada</span><span class="sxs-lookup"><span data-stu-id="00999-103">Async Replies versus Events on New Call Handles</span></span>

<span data-ttu-id="00999-104">O TSPI inclui várias operações que iniciam o tempo de vida de um identificador de chamada.</span><span class="sxs-lookup"><span data-stu-id="00999-104">TSPI includes a number of operations that start the lifetime of a call handle.</span></span> <span data-ttu-id="00999-105">Se o provedor de serviços retornar o sucesso para tal operação, ele deverá preencher o identificador opaco do tipo **HDRVCALL**, que ele usa para a nova chamada antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="00999-105">If the service provider returns SUCCESS for such an operation, it must fill in the opaque handle of type **HDRVCALL**, which it uses for the new call before it returns.</span></span> <span data-ttu-id="00999-106">A TAPI nunca executa operações na chamada antes que o [*\_ procedimento de conclusão*](/windows/win32/api/tspi/nc-tspi-async_completion) correspondente seja recebido.</span><span class="sxs-lookup"><span data-stu-id="00999-106">TAPI never performs operations on the call before the matching [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) has been received.</span></span> <span data-ttu-id="00999-107">Se o provedor de serviços retornar uma falha, o identificador se tornará automaticamente inválido (ou seja, sem [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)).</span><span class="sxs-lookup"><span data-stu-id="00999-107">If the service provider returns FAILURE, the handle automatically becomes invalid (that is, without [**TSPI\_lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)).</span></span> <span data-ttu-id="00999-108">Na verdade, a TAPI trata o identificador como "ainda não válido" até a conclusão assíncrona.</span><span class="sxs-lookup"><span data-stu-id="00999-108">In effect, TAPI treats the handle as "not yet valid" until the asynchronous completion.</span></span>

<span data-ttu-id="00999-109">O provedor de serviços também deve tratar o identificador como "ainda não válido" até que o [*\_ procedimento de conclusão*](/windows/win32/api/tspi/nc-tspi-async_completion) correspondente seja recebido.</span><span class="sxs-lookup"><span data-stu-id="00999-109">The service provider must also treat the handle as "not yet valid" until after the matching [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) is received.</span></span> <span data-ttu-id="00999-110">Em outras palavras, ele não deve emitir nenhuma função de [*\_ evento de linha*](/windows/win32/api/tspi/nc-tspi-lineevent) para a nova chamada ou incluí-lo em contagens de chamadas em mensagens ou estruturas de dados de status para a linha.</span><span class="sxs-lookup"><span data-stu-id="00999-110">In other words, it must not issue any [*Line\_Event*](/windows/win32/api/tspi/nc-tspi-lineevent) functions for the new call or include it in call counts in messages or status data structures for the line.</span></span>

<span data-ttu-id="00999-111">O nível de TAPI também está em conformidade com essas restrições de ciclo de vida; um novo identificador de chamada não é retornado ou válido até a mensagem de [**\_ resposta de linha**](./line-reply.md) correspondente, e nenhum evento para a nova chamada é entregue ao aplicativo até depois da mensagem de resposta de linha \_ .</span><span class="sxs-lookup"><span data-stu-id="00999-111">The TAPI level also conforms to these life cycle restrictions; a new call handle is not returned or valid until the matching [**LINE\_REPLY**](./line-reply.md) message, and no events for the new call are delivered to the application until after the LINE\_REPLY message.</span></span>

<span data-ttu-id="00999-112">As operações de TSPI para as quais esse princípio de "tempo de vida de início" aplicam-se são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="00999-112">The TSPI operations to which this "start lifetime" principle applies are the following:</span></span>

-   [<span data-ttu-id="00999-113">**TSPI \_ lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="00999-113">**TSPI\_lineCompleteTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [<span data-ttu-id="00999-114">**TSPI \_ lineForward**</span><span class="sxs-lookup"><span data-stu-id="00999-114">**TSPI\_lineForward**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [<span data-ttu-id="00999-115">**TSPI \_ lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="00999-115">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [<span data-ttu-id="00999-116">**TSPI \_ linePickup**</span><span class="sxs-lookup"><span data-stu-id="00999-116">**TSPI\_linePickup**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [<span data-ttu-id="00999-117">**TSPI \_ linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="00999-117">**TSPI\_linePrepareAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [<span data-ttu-id="00999-118">**TSPI \_ lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="00999-118">**TSPI\_lineSetupConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [<span data-ttu-id="00999-119">**TSPI \_ lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="00999-119">**TSPI\_lineSetupTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [<span data-ttu-id="00999-120">**TSPI \_ lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="00999-120">**TSPI\_lineUnpark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
