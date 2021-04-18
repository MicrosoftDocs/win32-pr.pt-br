---
description: Como uma ação personalizada pode ser agendada na interface do usuário e executar tabelas de sequência e pode ser executada no processo do serviço ou do cliente, uma ação personalizada pode potencialmente ser executada várias vezes.
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: Opções de agendamento de execução de ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa5aee44f3ad357eefc6f9dd9c5ee5ae45797c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755086"
---
# <a name="custom-action-execution-scheduling-options"></a><span data-ttu-id="2fa9e-103">Opções de agendamento de execução de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="2fa9e-103">Custom Action Execution Scheduling Options</span></span>

<span data-ttu-id="2fa9e-104">Como uma ação personalizada pode ser agendada na interface do usuário e executar tabelas de sequência e pode ser executada no processo do serviço ou do cliente, uma ação personalizada pode potencialmente ser executada várias vezes.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-104">Because a custom action can be scheduled in both the UI and execute sequence tables, and can be executed either in the service or client process, a custom action can potentially execute multiple times.</span></span>

<span data-ttu-id="2fa9e-105">Observe que o instalador:</span><span class="sxs-lookup"><span data-stu-id="2fa9e-105">Note that the installer:</span></span>

-   <span data-ttu-id="2fa9e-106">Executa ações em uma tabela de sequência imediatamente por padrão.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-106">Executes actions in a sequence table immediately by default.</span></span>
-   <span data-ttu-id="2fa9e-107">Não executará uma ação se o campo expressão condicional da tabela de sequência for avaliado como false.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-107">Does not execute an action if the conditional expression field of the sequence table evaluates to False.</span></span>
-   <span data-ttu-id="2fa9e-108">Processa a tabela de sequências da interface do usuário no processo do cliente se o nível da interface dos usuários internos estiver definido como o modo de interface de usuário completo (consulte [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) para obter uma descrição dos níveis de IU).</span><span class="sxs-lookup"><span data-stu-id="2fa9e-108">Processes the UI sequence table in the client process if the internal user's interface level is set to the full UI mode (see [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) for a description of UI levels).</span></span>
-   <span data-ttu-id="2fa9e-109">É um serviço registrado por padrão ao usar o Windows 2000 e, nesse caso, a tabela de sequências de execução é processada no serviço do instalador.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-109">Is a service registered by default when using Windows 2000 and, in this case, the execute sequence table is processed in the installer service.</span></span>

<span data-ttu-id="2fa9e-110">Você pode usar os seguintes sinalizadores de opção para controlar várias execuções imediatas de ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-110">You can use the following option flags to control multiple immediate execution of custom actions.</span></span> <span data-ttu-id="2fa9e-111">Para definir uma opção, adicione o valor nessa tabela ao valor no campo tipo da [tabela CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="2fa9e-111">To set an option, add the value in this table to the value in the Type field of the [CustomAction table](customaction-table.md).</span></span> <span data-ttu-id="2fa9e-112">Nenhum dos sinalizadores a seguir deve ser usado com [ações personalizadas de execução adiada](deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="2fa9e-112">None of the following flags should be used with [deferred execution custom actions](deferred-execution-custom-actions.md).</span></span>

<dl> <dt>

<span data-ttu-id="2fa9e-113"><span id="_default_"></span><span id="_DEFAULT_"></span>os</span><span class="sxs-lookup"><span data-stu-id="2fa9e-113"><span id="_default_"></span><span id="_DEFAULT_"></span>(default)</span></span>
</dt> <dd>

<span data-ttu-id="2fa9e-114">Hexadecimal: 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2fa9e-114">Hexadecimal: 0x00000000</span></span>

<span data-ttu-id="2fa9e-115">Decimal: 0</span><span class="sxs-lookup"><span data-stu-id="2fa9e-115">Decimal: 0</span></span>

<span data-ttu-id="2fa9e-116">Sempre executar.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-116">Always execute.</span></span> <span data-ttu-id="2fa9e-117">A ação pode ser executada duas vezes se estiver presente em ambas as tabelas de sequência.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-117">Action may run twice if present in both sequence tables.</span></span>

</dd> <dt>

<span data-ttu-id="2fa9e-118"><span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence**</span><span class="sxs-lookup"><span data-stu-id="2fa9e-118"><span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence**</span></span> 
</dt> <dd>

<span data-ttu-id="2fa9e-119">Hexadecimal: 0x00000100</span><span class="sxs-lookup"><span data-stu-id="2fa9e-119">Hexadecimal: 0x00000100</span></span>

<span data-ttu-id="2fa9e-120">Decimal: 256</span><span class="sxs-lookup"><span data-stu-id="2fa9e-120">Decimal: 256</span></span>

<span data-ttu-id="2fa9e-121">Execute não mais de uma vez se estiver presente em ambas as tabelas de sequência.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-121">Execute no more than once if present in both sequence tables.</span></span> <span data-ttu-id="2fa9e-122">Sempre ignora a ação na sequência de execução se a sequência da interface do usuário tiver sido executada.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-122">Always skips action in execute sequence if UI sequence has run.</span></span> <span data-ttu-id="2fa9e-123">Nenhum efeito na sequência da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-123">No effect in UI sequence.</span></span> <span data-ttu-id="2fa9e-124">A ação não precisa estar presente ou ser executada na sequência da interface do usuário para ser ignorada na sequência de execução.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-124">The action is not required to be present or run in the UI sequence to be skipped in the execute sequence.</span></span> <span data-ttu-id="2fa9e-125">Não afetado pelo registro do serviço de instalação.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-125">Not affected by install service registration.</span></span>

</dd> <dt>

<span data-ttu-id="2fa9e-126"><span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**</span><span class="sxs-lookup"><span data-stu-id="2fa9e-126"><span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**</span></span>
</dt> <dd>

<span data-ttu-id="2fa9e-127">Hexadecimal: 0x00000200</span><span class="sxs-lookup"><span data-stu-id="2fa9e-127">Hexadecimal: 0x00000200</span></span>

<span data-ttu-id="2fa9e-128">Decimal: 512</span><span class="sxs-lookup"><span data-stu-id="2fa9e-128">Decimal: 512</span></span>

<span data-ttu-id="2fa9e-129">Execute uma vez por processo se estiver em ambas as tabelas de sequência.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-129">Execute once per process if in both sequence tables.</span></span> <span data-ttu-id="2fa9e-130">Ignora a ação na sequência de execução se a sequência da interface do usuário foi executada no mesmo processo, por exemplo, ambas são executadas no processo do cliente.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-130">Skips action in execute sequence if UI sequence has been run in same process, for example both run in the client process.</span></span> <span data-ttu-id="2fa9e-131">Usado para impedir que as ações que modificam o estado da sessão, como dados de propriedade e de Database, sejam executadas duas vezes.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-131">Used to prevent actions that modify the session state, such as property and database data, from running twice.</span></span>

</dd> <dt>

<span data-ttu-id="2fa9e-132"><span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**</span><span class="sxs-lookup"><span data-stu-id="2fa9e-132"><span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**</span></span>
</dt> <dd>

<span data-ttu-id="2fa9e-133">Hexadecimal: 0x00000300</span><span class="sxs-lookup"><span data-stu-id="2fa9e-133">Hexadecimal: 0x00000300</span></span>

<span data-ttu-id="2fa9e-134">Decimal: 768</span><span class="sxs-lookup"><span data-stu-id="2fa9e-134">Decimal: 768</span></span>

<span data-ttu-id="2fa9e-135">Execute somente se estiver executando no cliente após a execução da sequência da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-135">Execute only if running on client after UI sequence has run.</span></span> <span data-ttu-id="2fa9e-136">A ação será executada somente se a sequência de execução for executada no cliente após a sequência de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-136">The action runs only if the execute sequence is run on the client following UI sequence.</span></span> <span data-ttu-id="2fa9e-137">Pode ser usado para fornecer ou/ou lógica, ou para suprimir o processamento relacionado à interface do usuário, se já tiver feito para a sessão do cliente.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-137">May be used to provide either/or logic, or to suppress the UI-related processing if already done for the client session.</span></span>

</dd> </dl>

<span data-ttu-id="2fa9e-138">Observe que, para executar uma ação personalizada durante dois modos de execução diferentes, crie duas entradas na [tabela CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2fa9e-138">Note that to run a custom action during two different run modes, author two entries into the [CustomAction table](customaction-table.md) .</span></span> <span data-ttu-id="2fa9e-139">Por exemplo, para ter uma ação personalizada que chama uma DLL (biblioteca de vínculo dinâmico) do C/C++ ( [tipo de ação personalizada 1](custom-action-type-1.md)) quando o modo for MSIRUNMODE \_ agendado e MSIRUNMODE \_ Rollback, coloque duas entradas na tabela CustomAction que chamam a mesma DLL, mas que têm tipos numéricos diferentes.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-139">For example, to have a custom action that calls a C/C++ dynamic link library (DLL) ( [Custom Action Type 1](custom-action-type-1.md)) both when the mode is MSIRUNMODE\_SCHEDULED and MSIRUNMODE\_ROLLBACK, put two entries in the CustomAction table that call the same DLL but that have different numeric types.</span></span> <span data-ttu-id="2fa9e-140">Inclua o código que chama [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) para determinar quando executar qual ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="2fa9e-140">Include code that calls [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) to determine when to run which custom action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fa9e-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2fa9e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fa9e-142">Referência de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="2fa9e-142">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="2fa9e-143">Sobre ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="2fa9e-143">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="2fa9e-144">Usando ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="2fa9e-144">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 



