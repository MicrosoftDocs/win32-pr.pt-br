---
description: A \_ associação CIM MediaPresent descreve uma relação em que uma extensão de armazenamento deve ser acessada por meio de um dispositivo de acesso à mídia.
ms.assetid: 84c4931c-1dc6-4fc1-b3b9-8252ecb627f5
ms.tgt_platform: multiple
title: Classe CIM_MediaPresent (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d033871a77a0433292c4a2ca1fae185df6aa5015
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837650"
---
# <a name="cim_mediapresent-class-cimwin32-wmi-providers"></a><span data-ttu-id="48db8-103">Classe CIM_MediaPresent (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="48db8-103">CIM_MediaPresent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="48db8-104">A associação **CIM \_ MediaPresent** descreve uma relação em que uma extensão de armazenamento deve ser acessada por meio de um dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="48db8-104">The **CIM\_MediaPresent** association describes a relationship where a storage extent must be accessed through a media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48db8-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="48db8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="48db8-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="48db8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="48db8-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="48db8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="48db8-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="48db8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="48db8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48db8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C540-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_StorageExtent     REF Dependent;
  CIM_MediaAccessDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="48db8-110">Membros</span><span class="sxs-lookup"><span data-stu-id="48db8-110">Members</span></span>

<span data-ttu-id="48db8-111">A classe **CIM \_ MediaPresent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="48db8-111">The **CIM\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="48db8-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="48db8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48db8-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="48db8-113">Properties</span></span>

<span data-ttu-id="48db8-114">A classe **CIM \_ MediaPresent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="48db8-114">The **CIM\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48db8-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="48db8-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db8-116">Tipo de dados: **CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="48db8-116">Data type: **CIM\_MediaAccessDevice**</span></span>
</dt> <dt>

<span data-ttu-id="48db8-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48db8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48db8-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="48db8-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="48db8-119">Um [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md) que descreve o dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="48db8-119">A [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) that describes the media access device.</span></span>

</dd> <dt>

<span data-ttu-id="48db8-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="48db8-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db8-121">Tipo de dados: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="48db8-121">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="48db8-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48db8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48db8-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="48db8-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="48db8-124">Um [**\_ StorageExtent CIM**](cim-storageextent.md) que descreve a extensão de armazenamento acessada usando o dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="48db8-124">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the storage extent accessed using the media access device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48db8-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="48db8-125">Remarks</span></span>

<span data-ttu-id="48db8-126">A classe **CIM \_ MediaPresent** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="48db8-126">The **CIM\_MediaPresent** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="48db8-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="48db8-127">WMI does not implement this class.</span></span> <span data-ttu-id="48db8-128">Para classes derivadas do **CIM \_ MediaPresent**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="48db8-128">For classes derived from **CIM\_MediaPresent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="48db8-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="48db8-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="48db8-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="48db8-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="48db8-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48db8-131">Requirements</span></span>



| <span data-ttu-id="48db8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="48db8-132">Requirement</span></span> | <span data-ttu-id="48db8-133">Valor</span><span class="sxs-lookup"><span data-stu-id="48db8-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48db8-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48db8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="48db8-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48db8-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48db8-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48db8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="48db8-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48db8-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48db8-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="48db8-138">Namespace</span></span><br/>                | <span data-ttu-id="48db8-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="48db8-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="48db8-140">MOF</span><span class="sxs-lookup"><span data-stu-id="48db8-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48db8-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48db8-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="48db8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="48db8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48db8-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48db8-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48db8-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="48db8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48db8-145">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="48db8-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

