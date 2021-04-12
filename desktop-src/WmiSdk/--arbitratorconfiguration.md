---
description: Limita os recursos internos que são usados por operações iniciadas por clientes WMI.
ms.assetid: e877899d-2f5e-4468-8c47-055fd4d16f56
ms.tgt_platform: multiple
title: Classe __ArbitratorConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ArbitratorConfiguration
- Root.__ArbitratorConfiguration.OutstandingTasksTotal
- Root.__ArbitratorConfiguration.OutstandingTasksPerUser
- Root.__ArbitratorConfiguration.TaskThreadsTotal
- Root.__ArbitratorConfiguration.TaskThreadsPerUser
- Root.__ArbitratorConfiguration.QuotaRetryCount
- Root.__ArbitratorConfiguration.QuotaRetryWaitInterval
- Root.__ArbitratorConfiguration.TotalUsers
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerTask
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerUser
- Root.__ArbitratorConfiguration.TotalCacheMemory
- Root.__ArbitratorConfiguration.TotalCacheDiskPerTask
- Root.__ArbitratorConfiguration.TotalCacheDiskPerUser
- Root.__ArbitratorConfiguration.TotalCacheDisk
- Root.__ArbitratorConfiguration.TemporarySubscriptionsPerUser
- Root.__ArbitratorConfiguration.PermanentSubscriptionsPerUser
- Root.__ArbitratorConfiguration.PollingInstructionsPerUser
- Root.__ArbitratorConfiguration.PollingMemoryPerUser
- Root.__ArbitratorConfiguration.TemporarySubscriptionsTotal
- Root.__ArbitratorConfiguration.PermanentSubscriptionsTotal
- Root.__ArbitratorConfiguration.PollingInstructionsTotal
- Root.__ArbitratorConfiguration.PollingMemoryTotal
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 906164d6d715ed70bccecf61fba767ada622c74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170196"
---
# <a name="__arbitratorconfiguration-class"></a><span data-ttu-id="02c75-103">\_\_Classe ArbitratorConfiguration</span><span class="sxs-lookup"><span data-stu-id="02c75-103">\_\_ArbitratorConfiguration class</span></span>

<span data-ttu-id="02c75-104">A classe **\_ \_ ArbitratorConfiguration** é uma classe de configuração que limita os recursos internos que são usados por operações iniciadas por clientes WMI.</span><span class="sxs-lookup"><span data-stu-id="02c75-104">The **\_\_ArbitratorConfiguration** class is a configuration class that limits the internal resources that are used by operations initiated by WMI clients.</span></span> <span data-ttu-id="02c75-105">Essa é uma classe singleton que reside no \\ namespace raiz.</span><span class="sxs-lookup"><span data-stu-id="02c75-105">This is a singleton class that resides in the \\root namespace.</span></span> <span data-ttu-id="02c75-106">A classe é gerada internamente para que não haja nenhum arquivo MOF para ela.</span><span class="sxs-lookup"><span data-stu-id="02c75-106">The class is internally generated so there is no MOF file for it.</span></span>

<span data-ttu-id="02c75-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="02c75-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="02c75-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="02c75-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="02c75-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02c75-109">Syntax</span></span>

``` syntax
[singleton]
class __ArbitratorConfiguration : __SystemClass
{
  uint32 OutstandingTasksTotal;
  uint32 OutstandingTasksPerUser;
  uint32 TaskThreadsTotal;
  uint32 TaskThreadsPerUser;
  uint32 QuotaRetryCount;
  uint32 QuotaRetryWaitInterval;
  uint32 TotalUsers;
  uint32 TotalCacheMemoryPerTask;
  uint32 TotalCacheMemoryPerUser;
  uint32 TotalCacheMemory;
  uint32 TotalCacheDiskPerTask;
  uint32 TotalCacheDiskPerUser;
  uint32 TotalCacheDisk;
  uint32 TemporarySubscriptionsPerUser;
  uint32 PermanentSubscriptionsPerUser;
  uint32 PollingInstructionsPerUser;
  uint32 PollingMemoryPerUser;
  uint32 TemporarySubscriptionsTotal;
  uint32 PermanentSubscriptionsTotal;
  uint32 PollingInstructionsTotal;
  uint32 PollingMemoryTotal;
};
```

## <a name="members"></a><span data-ttu-id="02c75-110">Membros</span><span class="sxs-lookup"><span data-stu-id="02c75-110">Members</span></span>

<span data-ttu-id="02c75-111">A classe **\_ \_ ArbitratorConfiguration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="02c75-111">The **\_\_ArbitratorConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="02c75-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="02c75-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02c75-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="02c75-113">Properties</span></span>

<span data-ttu-id="02c75-114">A classe **\_ \_ ArbitratorConfiguration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="02c75-114">The **\_\_ArbitratorConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02c75-115">**OutstandingTasksPerUser**</span><span class="sxs-lookup"><span data-stu-id="02c75-115">**OutstandingTasksPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-116">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-118">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="02c75-118">Unused.</span></span> <span data-ttu-id="02c75-119">Número de tarefas de usuário pendentes iniciadas a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-119">Number of outstanding user initiated tasks at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-120">**OutstandingTasksTotal**</span><span class="sxs-lookup"><span data-stu-id="02c75-120">**OutstandingTasksTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-121">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-123">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="02c75-123">Unused.</span></span> <span data-ttu-id="02c75-124">Número total de tarefas pendentes a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-124">Total number of outstanding tasks at any time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-125">**PermanentSubscriptionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="02c75-125">**PermanentSubscriptionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-126">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-128">Número de assinaturas permanentes permitidas para um usuário específico a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-128">Number of permanent subscriptions allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-129">**PermanentSubscriptionsTotal**</span><span class="sxs-lookup"><span data-stu-id="02c75-129">**PermanentSubscriptionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-132">Número total de assinaturas permanentes permitidas para todos os usuários a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-132">Total number of permanent subscriptions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-133">**PollingInstructionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="02c75-133">**PollingInstructionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-136">Número de consultas de evento de sondagem permitidas para um usuário específico a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-136">Number of polling event queries allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-137">**PollingInstructionsTotal**</span><span class="sxs-lookup"><span data-stu-id="02c75-137">**PollingInstructionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-138">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-140">Número total de instruções de sondagem permitidas para todos os usuários a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-140">Total number of polling instructions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-141">**PollingMemoryPerUser**</span><span class="sxs-lookup"><span data-stu-id="02c75-141">**PollingMemoryPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-144">A quantidade de consultas de eventos de sondagem de memória, emitidas por um usuário específico, pode consumir a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-144">Amount of memory polling event queries, issued by a particular user, can consume at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-145">**PollingMemoryTotal**</span><span class="sxs-lookup"><span data-stu-id="02c75-145">**PollingMemoryTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-148">A quantidade total de memória que sonda consultas de eventos, para todos os usuários combinados, pode ser consumidora a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-148">Total amount of memory that polling event queries, for all users combined, can consumer at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-149">**QuotaRetryCount**</span><span class="sxs-lookup"><span data-stu-id="02c75-149">**QuotaRetryCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-150">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-152">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="02c75-152">Unused.</span></span> <span data-ttu-id="02c75-153">Número de violações de cota permitidas antes que uma tarefa seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="02c75-153">Number of quota violations permitted before a task is canceled.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-154">**QuotaRetryWaitInterval**</span><span class="sxs-lookup"><span data-stu-id="02c75-154">**QuotaRetryWaitInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-155">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-157">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="02c75-157">Unused.</span></span> <span data-ttu-id="02c75-158">Atraso introduzido na execução da tarefa em cada violação de cota.</span><span class="sxs-lookup"><span data-stu-id="02c75-158">Delay introduced into the task execution on each quota violation.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-159">**TaskThreadsPerUser**</span><span class="sxs-lookup"><span data-stu-id="02c75-159">**TaskThreadsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-160">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-162">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="02c75-162">Unused.</span></span> <span data-ttu-id="02c75-163">Número máximo de threads de tarefa associados a um usuário específico t qualquer vez.</span><span class="sxs-lookup"><span data-stu-id="02c75-163">Maximum number of task threads associated with a particular user t any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-164">**TaskThreadsTotal**</span><span class="sxs-lookup"><span data-stu-id="02c75-164">**TaskThreadsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-165">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-167">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="02c75-167">Unused.</span></span> <span data-ttu-id="02c75-168">Número máximo de threads de tarefa.</span><span class="sxs-lookup"><span data-stu-id="02c75-168">Maximum number of task threads.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-169">**TemporarySubscriptionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="02c75-169">**TemporarySubscriptionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-170">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-172">Número de assinaturas temporárias permitidas para um usuário específico a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-172">Number of temporary subscriptions allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-173">**TemporarySubscriptionsTotal**</span><span class="sxs-lookup"><span data-stu-id="02c75-173">**TemporarySubscriptionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-174">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-176">Número total de assinaturas temporárias permitidas para todos os usuários a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-176">Total number of temporary subscriptions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-177">**TotalCacheDisk**</span><span class="sxs-lookup"><span data-stu-id="02c75-177">**TotalCacheDisk**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-178">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-180">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="02c75-180">Unused.</span></span> <span data-ttu-id="02c75-181">Total de cache de disco associado a todos os usuários a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-181">Total disk cache associated with all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-182">**TotalCacheDiskPerTask**</span><span class="sxs-lookup"><span data-stu-id="02c75-182">**TotalCacheDiskPerTask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-183">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-185">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="02c75-185">Unused.</span></span> <span data-ttu-id="02c75-186">Total de cache de disco associado a uma tarefa específica a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-186">Total disk cache associated with a particular task at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-187">**TotalCacheDiskPerUser**</span><span class="sxs-lookup"><span data-stu-id="02c75-187">**TotalCacheDiskPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-188">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-190">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="02c75-190">Unused.</span></span> <span data-ttu-id="02c75-191">Total de cache de disco associado a um usuário específico a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-191">Total disk cache associated with a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-192">**TotalCacheMemory**</span><span class="sxs-lookup"><span data-stu-id="02c75-192">**TotalCacheMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-193">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-195">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="02c75-195">Unused.</span></span> <span data-ttu-id="02c75-196">Total de cache de memória associado a todos os usuários de uma vez.</span><span class="sxs-lookup"><span data-stu-id="02c75-196">Total memory cache associated with all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-197">**TotalCacheMemoryPerTask**</span><span class="sxs-lookup"><span data-stu-id="02c75-197">**TotalCacheMemoryPerTask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-198">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-200">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="02c75-200">Unused.</span></span> <span data-ttu-id="02c75-201">Cache de memória total associado a uma tarefa específica a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-201">Total memory cache associated with a particular task at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-202">**TotalCacheMemoryPerUser**</span><span class="sxs-lookup"><span data-stu-id="02c75-202">**TotalCacheMemoryPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-203">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-205">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="02c75-205">Unused.</span></span> <span data-ttu-id="02c75-206">Total de cache de memória associado a um usuário específico em qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="02c75-206">Total memory cache associated with a particular user at anyone time.</span></span>

</dd> <dt>

<span data-ttu-id="02c75-207">**TotalUsers**</span><span class="sxs-lookup"><span data-stu-id="02c75-207">**TotalUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02c75-208">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c75-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02c75-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02c75-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02c75-210">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="02c75-210">Unused.</span></span> <span data-ttu-id="02c75-211">Número máximo de usuários conectados.</span><span class="sxs-lookup"><span data-stu-id="02c75-211">Maximum number of connected users.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02c75-212">Comentários</span><span class="sxs-lookup"><span data-stu-id="02c75-212">Remarks</span></span>

<span data-ttu-id="02c75-213">**\_ \_ ArbitratorConfiguration** é herdado de [**\_ \_ SystemClass**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="02c75-213">**\_\_ArbitratorConfiguration** is inherited from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02c75-214">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02c75-214">Requirements</span></span>



| <span data-ttu-id="02c75-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="02c75-215">Requirement</span></span> | <span data-ttu-id="02c75-216">Valor</span><span class="sxs-lookup"><span data-stu-id="02c75-216">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="02c75-217">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02c75-217">Minimum supported client</span></span><br/> | <span data-ttu-id="02c75-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02c75-218">Windows Vista</span></span><br/>       |
| <span data-ttu-id="02c75-219">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02c75-219">Minimum supported server</span></span><br/> | <span data-ttu-id="02c75-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02c75-220">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="02c75-221">Namespace</span><span class="sxs-lookup"><span data-stu-id="02c75-221">Namespace</span></span><br/>                | <span data-ttu-id="02c75-222">Root</span><span class="sxs-lookup"><span data-stu-id="02c75-222">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="02c75-223">Confira também</span><span class="sxs-lookup"><span data-stu-id="02c75-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c75-224">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="02c75-224">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="02c75-225">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="02c75-225">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

