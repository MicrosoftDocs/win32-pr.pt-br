---
description: Permite que os limites sejam definidos no uso do processo de host de recursos do sistema.
ms.assetid: 5f5ed1c6-bd1a-406d-a682-7a52059d9450
ms.tgt_platform: multiple
title: Classe __ProviderHostQuotaConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderHostQuotaConfiguration
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 443d66c8e508346444e98a92b341f1e7d67d8cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169811"
---
# <a name="__providerhostquotaconfiguration-class"></a><span data-ttu-id="94e8c-103">\_\_Classe ProviderHostQuotaConfiguration</span><span class="sxs-lookup"><span data-stu-id="94e8c-103">\_\_ProviderHostQuotaConfiguration class</span></span>

<span data-ttu-id="94e8c-104">A classe de sistema **\_ \_ ProviderHostQuotaConfiguration** é uma classe de configuração para processos de provedor de host.</span><span class="sxs-lookup"><span data-stu-id="94e8c-104">The **\_\_ProviderHostQuotaConfiguration** system class is a configuration class for host provider processes.</span></span> <span data-ttu-id="94e8c-105">Essa classe reside no namespace raiz e permite que os limites sejam definidos no uso do processo de host dos recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="94e8c-105">This class resides in the root namespace and allows limits to be set on host process usage of system resources.</span></span>

<span data-ttu-id="94e8c-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="94e8c-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="94e8c-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="94e8c-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="94e8c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94e8c-108">Syntax</span></span>

``` syntax
class __ProviderHostQuotaConfiguration : __SystemClass
{
  uint32 ThreadsPerHost;
  uint32 HandlesPerHost;
  uint32 ProcessLimitAllHosts;
  uint64 MemoryPerHost;
  uint64 MemoryAllHosts;
};
```

## <a name="members"></a><span data-ttu-id="94e8c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="94e8c-109">Members</span></span>

<span data-ttu-id="94e8c-110">A classe **\_ \_ ProviderHostQuotaConfiguration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="94e8c-110">The **\_\_ProviderHostQuotaConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="94e8c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="94e8c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94e8c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="94e8c-112">Properties</span></span>

<span data-ttu-id="94e8c-113">A classe **\_ \_ ProviderHostQuotaConfiguration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="94e8c-113">The **\_\_ProviderHostQuotaConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94e8c-114">**HandlesPerHost**</span><span class="sxs-lookup"><span data-stu-id="94e8c-114">**HandlesPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e8c-115">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94e8c-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94e8c-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94e8c-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94e8c-117">Número de identificadores de objeto de kernel que cada host pode ter.</span><span class="sxs-lookup"><span data-stu-id="94e8c-117">Number of kernel object handles each host can have.</span></span>

</dd> <dt>

<span data-ttu-id="94e8c-118">**MemoryAllHosts**</span><span class="sxs-lookup"><span data-stu-id="94e8c-118">**MemoryAllHosts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e8c-119">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94e8c-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94e8c-120">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94e8c-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94e8c-121">Quantidade combinada de memória privada em bytes que pode ser mantida por todos os hosts.</span><span class="sxs-lookup"><span data-stu-id="94e8c-121">Combined amount of private memory in bytes that can be held by all hosts.</span></span>

<span data-ttu-id="94e8c-122">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="94e8c-122">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="94e8c-123">**MemoryPerHost**</span><span class="sxs-lookup"><span data-stu-id="94e8c-123">**MemoryPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e8c-124">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94e8c-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94e8c-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94e8c-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94e8c-126">Quantidade de memória privada que pode ser mantida por cada host.</span><span class="sxs-lookup"><span data-stu-id="94e8c-126">Amount of private memory that can be held by each host.</span></span>

<span data-ttu-id="94e8c-127">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="94e8c-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="94e8c-128">**ProcessLimitAllHosts**</span><span class="sxs-lookup"><span data-stu-id="94e8c-128">**ProcessLimitAllHosts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e8c-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94e8c-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94e8c-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94e8c-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94e8c-131">Número total de processos de host que podem ser executados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="94e8c-131">Total number of host processes that can be executing concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="94e8c-132">**ThreadsPerHost**</span><span class="sxs-lookup"><span data-stu-id="94e8c-132">**ThreadsPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e8c-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94e8c-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94e8c-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94e8c-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94e8c-135">Número de threads pertencentes a um host.</span><span class="sxs-lookup"><span data-stu-id="94e8c-135">Number of threads owned by any one host.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94e8c-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="94e8c-136">Remarks</span></span>

<span data-ttu-id="94e8c-137">As propriedades que representam os limites podem ser alteradas, mas como a classe é singleton, todos os hosts do provedor compartilham os mesmos limites.</span><span class="sxs-lookup"><span data-stu-id="94e8c-137">The properties that represent limits can be changed but because the class is a singleton, all the provider hosts share the same limits.</span></span>

<span data-ttu-id="94e8c-138">Os parâmetros a seguir são usados ao configurar os limites de objeto de trabalho para o objeto de trabalho do host:</span><span class="sxs-lookup"><span data-stu-id="94e8c-138">The following parameters are used when configuring the job object limits for the host job object:</span></span>

-   <span data-ttu-id="94e8c-139">**MemoryAllHosts**</span><span class="sxs-lookup"><span data-stu-id="94e8c-139">**MemoryAllHosts**</span></span>
-   <span data-ttu-id="94e8c-140">**MemoryPerHost**</span><span class="sxs-lookup"><span data-stu-id="94e8c-140">**MemoryPerHost**</span></span>
-   <span data-ttu-id="94e8c-141">**ProcessLimitAllHosts**</span><span class="sxs-lookup"><span data-stu-id="94e8c-141">**ProcessLimitAllHosts**</span></span>
-   <span data-ttu-id="94e8c-142">**ThreadsPerHost**</span><span class="sxs-lookup"><span data-stu-id="94e8c-142">**ThreadsPerHost**</span></span>

<span data-ttu-id="94e8c-143">O processo de host pesquisa o uso do identificador e sai do processo se a cota de **HandlesPerHost** for violada.</span><span class="sxs-lookup"><span data-stu-id="94e8c-143">The host process polls handle usage and exits the process if the **HandlesPerHost** quota is violated.</span></span> <span data-ttu-id="94e8c-144">As alterações nesses valores entrarão em vigor depois que o computador for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="94e8c-144">Changes to these values take effect after the computer is restarted.</span></span>

## <a name="requirements"></a><span data-ttu-id="94e8c-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94e8c-145">Requirements</span></span>



| <span data-ttu-id="94e8c-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="94e8c-146">Requirement</span></span> | <span data-ttu-id="94e8c-147">Valor</span><span class="sxs-lookup"><span data-stu-id="94e8c-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="94e8c-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94e8c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="94e8c-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94e8c-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="94e8c-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94e8c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="94e8c-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94e8c-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="94e8c-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="94e8c-152">Namespace</span></span><br/>                | <span data-ttu-id="94e8c-153">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="94e8c-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="94e8c-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="94e8c-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94e8c-155">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="94e8c-155">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="94e8c-156">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="94e8c-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

