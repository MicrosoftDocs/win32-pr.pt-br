---
description: Indica que uma página de memória foi removida do uso do sistema devido a erros excessivos de verificação de erro de hardware e correção (ECC). Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: 364a2520-8d7c-44f2-95f6-eea9a5531975
title: Classe MSMCAEvent_MemoryPageRemoved
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryPageRemoved
- MSMCAEvent_MemoryPageRemoved.Active
- MSMCAEvent_MemoryPageRemoved.InstanceName
- MSMCAEvent_MemoryPageRemoved.PhysicalAddress
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: dc29c5b51531e204ab50f062dd08ef8d5abf1bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763985"
---
# <a name="msmcaevent_memorypageremoved-class"></a><span data-ttu-id="89d15-104">\_Classe MSMCAEvent MemoryPageRemoved</span><span class="sxs-lookup"><span data-stu-id="89d15-104">MSMCAEvent\_MemoryPageRemoved class</span></span>

<span data-ttu-id="89d15-105">A classe **MSMCAEvent \_ MemoryPageRemoved** indica que uma página de memória foi removida do uso do sistema devido a erros excessivos de verificação de erros de hardware e correção (ECC).</span><span class="sxs-lookup"><span data-stu-id="89d15-105">The **MSMCAEvent\_MemoryPageRemoved** class indicates that a memory page has been removed from system use due to excessive hardware Error Checking and Correcting (ECC) errors.</span></span> <span data-ttu-id="89d15-106">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="89d15-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="89d15-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="89d15-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="89d15-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="89d15-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d15-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89d15-109">Syntax</span></span>

``` syntax
class MSMCAEvent_MemoryPageRemoved : WmiEvent
{
  boolean Active;
  string  InstanceName;
  uint64  PhysicalAddress;
};
```

## <a name="members"></a><span data-ttu-id="89d15-110">Membros</span><span class="sxs-lookup"><span data-stu-id="89d15-110">Members</span></span>

<span data-ttu-id="89d15-111">A classe **MSMCAEvent \_ MemoryPageRemoved** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="89d15-111">The **MSMCAEvent\_MemoryPageRemoved** class has these types of members:</span></span>

-   [<span data-ttu-id="89d15-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="89d15-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89d15-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="89d15-113">Properties</span></span>

<span data-ttu-id="89d15-114">A classe **MSMCAEvent \_ MemoryPageRemoved** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="89d15-114">The **MSMCAEvent\_MemoryPageRemoved** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89d15-115">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="89d15-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89d15-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="89d15-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89d15-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89d15-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89d15-118">**True**, se esta instância da classe estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="89d15-118">**TRUE**, if this instance of the class is active; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89d15-119">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="89d15-119">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89d15-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="89d15-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89d15-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89d15-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89d15-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="89d15-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="89d15-123">Identificador exclusivo para esta instância da classe.</span><span class="sxs-lookup"><span data-stu-id="89d15-123">Unique identifier for this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="89d15-124">**PhysicalAddress**</span><span class="sxs-lookup"><span data-stu-id="89d15-124">**PhysicalAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89d15-125">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89d15-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89d15-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89d15-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89d15-127">Endereço da página de memória que foi removida.</span><span class="sxs-lookup"><span data-stu-id="89d15-127">Address of the page of memory that has been removed.</span></span>

<span data-ttu-id="89d15-128">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="89d15-128">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89d15-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="89d15-129">Remarks</span></span>

<span data-ttu-id="89d15-130">A classe **MSMCAEvent \_ MemoryPageRemoved** é derivada de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="89d15-130">The **MSMCAEvent\_MemoryPageRemoved** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89d15-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89d15-131">Requirements</span></span>



| <span data-ttu-id="89d15-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="89d15-132">Requirement</span></span> | <span data-ttu-id="89d15-133">Valor</span><span class="sxs-lookup"><span data-stu-id="89d15-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89d15-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89d15-134">Minimum supported client</span></span><br/> | <span data-ttu-id="89d15-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="89d15-135">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="89d15-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89d15-136">Minimum supported server</span></span><br/> | <span data-ttu-id="89d15-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="89d15-137">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="89d15-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="89d15-138">Namespace</span></span><br/>                | <span data-ttu-id="89d15-139">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="89d15-139">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="89d15-140">MOF</span><span class="sxs-lookup"><span data-stu-id="89d15-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89d15-141"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89d15-141"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="89d15-142">DLL</span><span class="sxs-lookup"><span data-stu-id="89d15-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89d15-143"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89d15-143"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89d15-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="89d15-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89d15-145">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="89d15-145">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="89d15-146">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="89d15-146">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

