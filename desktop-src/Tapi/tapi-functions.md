---
description: As seções a seguir contêm uma lista alfabética de funções agrupadas por área. As informações de cada função incluem uma lista dos Estados de chamada válidos na entrada da função e transições de estado de chamada típicas quando a solicitação é concluída.
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: Funções TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38532fa1c0b978e3e59e54b08fbc43152fa0bd64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505914"
---
# <a name="tapi-functions"></a><span data-ttu-id="ebb5d-104">Funções TAPI</span><span class="sxs-lookup"><span data-stu-id="ebb5d-104">TAPI Functions</span></span>

<span data-ttu-id="ebb5d-105">As seções a seguir contêm uma lista alfabética de funções agrupadas por área.</span><span class="sxs-lookup"><span data-stu-id="ebb5d-105">The following sections contain an alphabetic list of functions grouped by area.</span></span> <span data-ttu-id="ebb5d-106">As informações de cada função incluem uma lista dos Estados de chamada válidos na entrada da função e transições de estado de chamada típicas quando a solicitação é concluída.</span><span class="sxs-lookup"><span data-stu-id="ebb5d-106">The information for each function includes a list of the valid call states on entry of the function and typical call state transitions when the request is complete.</span></span>

-   [<span data-ttu-id="ebb5d-107">Funções de telefonia assistidas</span><span class="sxs-lookup"><span data-stu-id="ebb5d-107">Assisted Telephony Functions</span></span>](assisted-telephony-functions.md)
-   [<span data-ttu-id="ebb5d-108">Funções do Call Center</span><span class="sxs-lookup"><span data-stu-id="ebb5d-108">Call Center Functions</span></span>](call-center-functions.md)
-   [<span data-ttu-id="ebb5d-109">Funções de dispositivo de linha</span><span class="sxs-lookup"><span data-stu-id="ebb5d-109">Line Device Functions</span></span>](line-device-functions.md)
-   [<span data-ttu-id="ebb5d-110">Funções de dispositivo de telefone</span><span class="sxs-lookup"><span data-stu-id="ebb5d-110">Phone Device Functions</span></span>](phone-device-functions.md)

<span data-ttu-id="ebb5d-111">Para funções TAPI categorizadas por nível de serviço e tarefa, consulte [referência de função rápida TAPI](tapi-quick-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ebb5d-111">For TAPI functions categorized by service level and task, see [TAPI Quick Function Reference](tapi-quick-function-reference.md).</span></span>

<span data-ttu-id="ebb5d-112">Observe que as limitações do provedor de serviços podem existir em relação aos Estados reais em que uma função pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="ebb5d-112">Please note that service provider limitations may exist concerning the actual states in which a function can be performed.</span></span> <span data-ttu-id="ebb5d-113">Os aplicativos devem verificar o membro **dwCallFeatures** na estrutura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , o membro **dwAddressFeatures** na estrutura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) e o membro **dwLineFeatures** na estrutura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) para determinar se uma função é permitida ou não no estado de chamada atual.</span><span class="sxs-lookup"><span data-stu-id="ebb5d-113">Applications must check the **dwCallFeatures** member in the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure, the **dwAddressFeatures** member in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure, and the **dwLineFeatures** member in the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) structure to determine whether or not a function is permitted within the current call state.</span></span>

 

 



