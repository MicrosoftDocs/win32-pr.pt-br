---
description: Contém um evento de plataforma corrigido (CPE). Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: b24a390e-293d-4dd4-b747-33c298a5d45f
title: Classe MSMCAInfo_RawCorrectedPlatformEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCorrectedPlatformEvent
- MSMCAInfo_RawCorrectedPlatformEvent.Active
- MSMCAInfo_RawCorrectedPlatformEvent.Count
- MSMCAInfo_RawCorrectedPlatformEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 906587ca9ee153eb93542c3e749e8164e6a5ee7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762170"
---
# <a name="msmcainfo_rawcorrectedplatformevent-class"></a><span data-ttu-id="70cb2-104">\_Classe MSMCAInfo RawCorrectedPlatformEvent</span><span class="sxs-lookup"><span data-stu-id="70cb2-104">MSMCAInfo\_RawCorrectedPlatformEvent class</span></span>

<span data-ttu-id="70cb2-105">A classe **MSMCAInfo \_ RawCorrectedPlatformEvent** contém um evento de plataforma corrigido (CPE).</span><span class="sxs-lookup"><span data-stu-id="70cb2-105">The **MSMCAInfo\_RawCorrectedPlatformEvent** class contains a Corrected Platform Event (CPE).</span></span> <span data-ttu-id="70cb2-106">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="70cb2-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="70cb2-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="70cb2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="70cb2-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="70cb2-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="70cb2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70cb2-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawCorrectedPlatformEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="70cb2-110">Membros</span><span class="sxs-lookup"><span data-stu-id="70cb2-110">Members</span></span>

<span data-ttu-id="70cb2-111">A classe **MSMCAInfo \_ RawCorrectedPlatformEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="70cb2-111">The **MSMCAInfo\_RawCorrectedPlatformEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="70cb2-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="70cb2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70cb2-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="70cb2-113">Properties</span></span>

<span data-ttu-id="70cb2-114">A classe **MSMCAInfo \_ RawCorrectedPlatformEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="70cb2-114">The **MSMCAInfo\_RawCorrectedPlatformEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70cb2-115">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="70cb2-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70cb2-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="70cb2-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70cb2-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="70cb2-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70cb2-118">TRUE, se esta instância da classe estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="70cb2-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="70cb2-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="70cb2-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70cb2-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70cb2-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="70cb2-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="70cb2-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70cb2-122">Número de registros de erro.</span><span class="sxs-lookup"><span data-stu-id="70cb2-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="70cb2-123">**Registros**</span><span class="sxs-lookup"><span data-stu-id="70cb2-123">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70cb2-124">Tipo de dados: matriz de **\_ entrada MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="70cb2-124">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="70cb2-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="70cb2-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70cb2-126">Matriz de registros de erro de MCA.</span><span class="sxs-lookup"><span data-stu-id="70cb2-126">Array of MCA error records.</span></span> <span data-ttu-id="70cb2-127">O número de registros de erro MCA na matriz é especificado pela propriedade **Count** .</span><span class="sxs-lookup"><span data-stu-id="70cb2-127">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70cb2-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="70cb2-128">Remarks</span></span>

<span data-ttu-id="70cb2-129">A classe **MSMCAInfo \_ RawCorrectedPlatformEvent** é derivada de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="70cb2-129">The **MSMCAInfo\_RawCorrectedPlatformEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70cb2-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70cb2-130">Requirements</span></span>



| <span data-ttu-id="70cb2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="70cb2-131">Requirement</span></span> | <span data-ttu-id="70cb2-132">Valor</span><span class="sxs-lookup"><span data-stu-id="70cb2-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70cb2-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70cb2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="70cb2-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="70cb2-134">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="70cb2-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70cb2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="70cb2-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="70cb2-136">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="70cb2-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="70cb2-137">Namespace</span></span><br/>                | <span data-ttu-id="70cb2-138">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="70cb2-138">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="70cb2-139">MOF</span><span class="sxs-lookup"><span data-stu-id="70cb2-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70cb2-140"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70cb2-140"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="70cb2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="70cb2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70cb2-142"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70cb2-142"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70cb2-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="70cb2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70cb2-144">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="70cb2-144">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="70cb2-145">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="70cb2-145">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

 




