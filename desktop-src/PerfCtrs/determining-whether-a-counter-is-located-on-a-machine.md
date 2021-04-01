---
description: Para determinar se um contador está instalado em um computador específico, chame PdhValidatePath com o caminho do contador totalmente qualificado. A função retornará êxito de erro \_ se o contador estiver localizado no computador especificado.
ms.assetid: 5533a8d8-3621-4ce7-984c-c3895adef531
title: Determinando se um contador está localizado em um computador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795878e2f9c97989fe924737ec7f8e7f14bdc67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921746"
---
# <a name="determining-whether-a-counter-is-located-on-a-computer"></a><span data-ttu-id="59e68-104">Determinando se um contador está localizado em um computador</span><span class="sxs-lookup"><span data-stu-id="59e68-104">Determining Whether a Counter Is Located on a Computer</span></span>

<span data-ttu-id="59e68-105">Para determinar se um contador está instalado em um computador específico, chame [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) com o caminho do contador totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="59e68-105">To determine if a counter is installed on a particular computer, call [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) with the fully qualified counter path.</span></span> <span data-ttu-id="59e68-106">A função retornará êxito de erro \_ se o contador estiver localizado no computador especificado.</span><span class="sxs-lookup"><span data-stu-id="59e68-106">The function returns ERROR\_SUCCESS if the counter is located on the specified computer.</span></span>

<span data-ttu-id="59e68-107">[**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) valida o caminho inteiro; Portanto, se qualquer objeto, instância ou contador no caminho não existir, o valor de retorno indicará isso.</span><span class="sxs-lookup"><span data-stu-id="59e68-107">[**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) validates the entire path; therefore, if any object, instance, or counter in the path does not exist, the return value indicates so.</span></span> <span data-ttu-id="59e68-108">**PdhValidatePath** verifica o caminho do contador especificado nesta ordem: computador, objeto de desempenho, instância e contador.</span><span class="sxs-lookup"><span data-stu-id="59e68-108">**PdhValidatePath** verifies the specified counter path in this order: computer, performance object, instance, and counter.</span></span>

 

 



