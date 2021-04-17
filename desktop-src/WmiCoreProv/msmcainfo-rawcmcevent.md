---
description: Contém um evento de verificação de máquina corrigida (CMC). Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: e12efbf7-7d53-415a-bc48-90d33e4ce16d
title: Classe MSMCAInfo_RawCMCEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCMCEvent
- MSMCAInfo_RawCMCEvent.Active
- MSMCAInfo_RawCMCEvent.Count
- MSMCAInfo_RawCMCEvent.InstanceName
- MSMCAInfo_RawCMCEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 1bb60d5fbcf004b924a91e640d8cd8a8c5ad3c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790382"
---
# <a name="msmcainfo_rawcmcevent-class"></a><span data-ttu-id="ba7bd-104">\_Classe MSMCAInfo RawCMCEvent</span><span class="sxs-lookup"><span data-stu-id="ba7bd-104">MSMCAInfo\_RawCMCEvent class</span></span>

<span data-ttu-id="ba7bd-105">A classe **MSMCAInfo \_ RawCMCEvent** contém um evento de verificação de máquina corrigido (CMC).</span><span class="sxs-lookup"><span data-stu-id="ba7bd-105">The **MSMCAInfo\_RawCMCEvent** class contains a Corrected Machine Check (CMC) event.</span></span> <span data-ttu-id="ba7bd-106">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ba7bd-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="ba7bd-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ba7bd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ba7bd-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="ba7bd-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba7bd-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba7bd-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawCMCEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="ba7bd-110">Membros</span><span class="sxs-lookup"><span data-stu-id="ba7bd-110">Members</span></span>

<span data-ttu-id="ba7bd-111">A classe **MSMCAInfo \_ RawCMCEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ba7bd-111">The **MSMCAInfo\_RawCMCEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="ba7bd-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ba7bd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba7bd-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ba7bd-113">Properties</span></span>

<span data-ttu-id="ba7bd-114">A classe **MSMCAInfo \_ RawCMCEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ba7bd-114">The **MSMCAInfo\_RawCMCEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba7bd-115">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="ba7bd-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7bd-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ba7bd-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ba7bd-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ba7bd-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba7bd-118">TRUE, se esta instância da classe estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ba7bd-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ba7bd-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="ba7bd-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7bd-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba7bd-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba7bd-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ba7bd-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba7bd-122">Número de registros de erro.</span><span class="sxs-lookup"><span data-stu-id="ba7bd-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="ba7bd-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="ba7bd-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7bd-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ba7bd-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7bd-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ba7bd-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba7bd-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ba7bd-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ba7bd-127">Identificador exclusivo desta instância da classe.</span><span class="sxs-lookup"><span data-stu-id="ba7bd-127">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="ba7bd-128">**Registros**</span><span class="sxs-lookup"><span data-stu-id="ba7bd-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7bd-129">Tipo de dados: matriz de **\_ entrada MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="ba7bd-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="ba7bd-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ba7bd-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba7bd-131">Matriz de registros de erros da arquitetura de verificação de máquina (MCA).</span><span class="sxs-lookup"><span data-stu-id="ba7bd-131">Array of Machine Check Architecture (MCA) error records.</span></span> <span data-ttu-id="ba7bd-132">O número de registros de erro MCA na matriz é especificado pela propriedade **Count** .</span><span class="sxs-lookup"><span data-stu-id="ba7bd-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba7bd-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba7bd-133">Remarks</span></span>

<span data-ttu-id="ba7bd-134">A classe **MSMCAInfo \_ RawCMCEvent** é derivada de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="ba7bd-134">The **MSMCAInfo\_RawCMCEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba7bd-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba7bd-135">Requirements</span></span>



| <span data-ttu-id="ba7bd-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba7bd-136">Requirement</span></span> | <span data-ttu-id="ba7bd-137">Valor</span><span class="sxs-lookup"><span data-stu-id="ba7bd-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7bd-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba7bd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ba7bd-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ba7bd-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="ba7bd-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba7bd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ba7bd-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ba7bd-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="ba7bd-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba7bd-142">Namespace</span></span><br/>                | <span data-ttu-id="ba7bd-143">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="ba7bd-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="ba7bd-144">MOF</span><span class="sxs-lookup"><span data-stu-id="ba7bd-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba7bd-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba7bd-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba7bd-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ba7bd-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba7bd-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba7bd-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba7bd-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba7bd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba7bd-149">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="ba7bd-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="ba7bd-150">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="ba7bd-150">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

