---
description: Além de habilitar o monitoramento de dígitos e ser notificado de dígitos um de cada vez, um aplicativo também pode solicitar que vários dígitos sejam coletados em um buffer.
ms.assetid: db83c48a-5178-40ed-90a9-e7c8e1886fe0
title: Coleta de dígitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5eab4185882b86a5a8e5dcb1444f39c9db2b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789873"
---
# <a name="digit-gathering"></a><span data-ttu-id="b6c4e-103">Coleta de dígitos</span><span class="sxs-lookup"><span data-stu-id="b6c4e-103">Digit Gathering</span></span>

<span data-ttu-id="b6c4e-104">Além de habilitar o monitoramento de dígitos e ser notificado de dígitos um de cada vez, um aplicativo também pode solicitar que vários dígitos sejam coletados em um buffer.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-104">Besides enabling digit monitoring and being notified of digits one at a time, an application can also request that multiple digits be collected in a buffer.</span></span> <span data-ttu-id="b6c4e-105">Somente quando o buffer estiver cheio ou quando alguma outra condição de encerramento for atendida, o aplicativo será notificado.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-105">Only when the buffer is full or when some other termination condition is met is the application notified.</span></span> <span data-ttu-id="b6c4e-106">A coleta de dígitos é útil para funções como coleção de números de cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-106">Digit gathering is useful for functions such as credit card number collection.</span></span> <span data-ttu-id="b6c4e-107">Ele é executado quando um aplicativo chama [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), especificando um buffer para preencher com dígitos.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-107">It is performed when an application calls [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), specifying a buffer to fill with digits.</span></span> <span data-ttu-id="b6c4e-108">A coleta de dígitos é encerrada quando uma das seguintes condições é verdadeira:</span><span class="sxs-lookup"><span data-stu-id="b6c4e-108">Digit gathering terminates when one of the following conditions is true:</span></span>

-   <span data-ttu-id="b6c4e-109">O número de dígitos solicitado foi coletado.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-109">The requested number of digits has been collected.</span></span>
-   <span data-ttu-id="b6c4e-110">Um dos vários dígitos de encerramento é detectado.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-110">One of multiple termination digits is detected.</span></span> <span data-ttu-id="b6c4e-111">Os dígitos de terminação são especificados para [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), e o dígito de término também é colocado no buffer.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-111">The termination digits are specified to [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), and the termination digit is placed in the buffer as well.</span></span>
-   <span data-ttu-id="b6c4e-112">Um dos dois tempos limite expira.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-112">One of two timeouts expires.</span></span> <span data-ttu-id="b6c4e-113">Os tempos limites são um tempo limite de primeiro dígito, especificando a duração máxima antes que o primeiro dígito deve ser coletado e um tempo limite entre dígitos, especificando a duração máxima entre dígitos sucessivos.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-113">The timeouts are a first digit timeout, specifying the maximum duration before the first digit must be collected, and an inter-digit timeout, specifying the maximum duration between successive digits.</span></span>
-   <span data-ttu-id="b6c4e-114">A coleta de dígitos é cancelada explicitamente por [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) novamente com um outro conjunto de parâmetros para iniciar uma nova solicitação de coleta ou usando um parâmetro de buffer de dígito **nulo** para cancelar.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-114">Digit gathering is canceled explicitly by [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) again with either another set of parameters to start a new gathering request or by using a **NULL** digit buffer parameter to cancel.</span></span>

<span data-ttu-id="b6c4e-115">Quando a coleta de dígitos é encerrada por qualquer motivo, uma mensagem de [**\_ GATHERDIGITS de linha**](line-gatherdigits.md) é enviada ao aplicativo que solicitou a coleta de dígitos.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-115">When digit gathering terminates for any reason, a [**LINE\_GATHERDIGITS**](line-gatherdigits.md) message is sent to the application that requested the digit gathering.</span></span> <span data-ttu-id="b6c4e-116">Apenas uma solicitação de coleta de dígito único pode estar pendente em uma chamada a qualquer momento em todos os aplicativos que são proprietários da chamada.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-116">Only a single digit gathering request can be outstanding on a call at any given time across all applications that are owners of the call.</span></span>

<span data-ttu-id="b6c4e-117">A coleta de dígitos e o monitoramento de dígitos podem ser habilitados na mesma chamada ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-117">Digit gathering and digit monitoring can be enabled on the same call at the same time.</span></span> <span data-ttu-id="b6c4e-118">Nesse caso, o aplicativo receberá uma mensagem [**de \_ MONITORDIGITS de linha**](line-monitordigits.md) para cada dígito detectado e uma mensagem de GATHERDIGITS de linha separada \_ quando o buffer for enviado de volta.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-118">In that case, the application will receive a [**LINE\_MONITORDIGITS**](line-monitordigits.md) message for each detected digit and a separate LINE\_GATHERDIGITS message when the buffer is sent back.</span></span>

 

 



