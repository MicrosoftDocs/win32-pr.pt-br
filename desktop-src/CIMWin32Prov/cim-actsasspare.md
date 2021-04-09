---
description: A \_ associação CIM ActsAsSpare indica quais elementos podem ser sobressalentes ou substituir outros elementos agregados. Um sobressalente pode operar no \# modo &0034; hot-standby&\# 0034;, conforme especificado em uma base elemento a elemento.
ms.assetid: bed8c552-f782-4af9-9441-ff3268182c3b
ms.tgt_platform: multiple
title: Classe CIM_ActsAsSpare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActsAsSpare
- CIM_ActsAsSpare.Group
- CIM_ActsAsSpare.HotStandby
- CIM_ActsAsSpare.Spare
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 975c6317a78789938ea9d34e062d84fe3435498a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920466"
---
# <a name="cim_actsasspare-class"></a><span data-ttu-id="a8aae-104">\_Classe CIM ActsAsSpare</span><span class="sxs-lookup"><span data-stu-id="a8aae-104">CIM\_ActsAsSpare class</span></span>

<span data-ttu-id="a8aae-105">A associação **CIM \_ ActsAsSpare** indica quais elementos podem ser sobressalentes ou substituir outros elementos agregados.</span><span class="sxs-lookup"><span data-stu-id="a8aae-105">The **CIM\_ActsAsSpare** association indicates which elements can be spares or replace other aggregated elements.</span></span> <span data-ttu-id="a8aae-106">Um sobressalente pode operar no modo "hot-standby", conforme especificado de acordo com o elemento.</span><span class="sxs-lookup"><span data-stu-id="a8aae-106">A spare can operate in "hot-standby" mode as specified on an element-by-element basis.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a8aae-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="a8aae-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a8aae-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a8aae-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a8aae-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a8aae-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a8aae-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a8aae-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8aae-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8aae-111">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{64C1726E-DB21-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ActsAsSpare
{
  CIM_SpareGroup           REF Group;
  boolean                      HotStandby;
  CIM_ManagedSystemElement REF Spare;
};
```

## <a name="members"></a><span data-ttu-id="a8aae-112">Membros</span><span class="sxs-lookup"><span data-stu-id="a8aae-112">Members</span></span>

<span data-ttu-id="a8aae-113">A classe **CIM \_ ActsAsSpare** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a8aae-113">The **CIM\_ActsAsSpare** class has these types of members:</span></span>

-   [<span data-ttu-id="a8aae-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a8aae-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8aae-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a8aae-115">Properties</span></span>

<span data-ttu-id="a8aae-116">A classe **CIM \_ ActsAsSpare** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a8aae-116">The **CIM\_ActsAsSpare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8aae-117">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="a8aae-117">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8aae-118">Tipo de dados **: \_ Respare CIM**</span><span class="sxs-lookup"><span data-stu-id="a8aae-118">Data type: **CIM\_SpareGroup**</span></span>
</dt> <dt>

<span data-ttu-id="a8aae-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8aae-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8aae-120">Referência à propriedade de **grupo** que representa a classe de [**\_ reserva de CIM**](cim-sparegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="a8aae-120">Reference to the **Group** property that represents the [**CIM\_SpareGroup**](cim-sparegroup.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="a8aae-121">**HotStandby**</span><span class="sxs-lookup"><span data-stu-id="a8aae-121">**HotStandby**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8aae-122">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a8aae-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a8aae-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8aae-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8aae-124">Se for **true**, o sobressalente estará operando como uma espera ativa.</span><span class="sxs-lookup"><span data-stu-id="a8aae-124">If **TRUE**, the spare is operating as a hot standby.</span></span>

</dd> <dt>

<span data-ttu-id="a8aae-125">**Livre**</span><span class="sxs-lookup"><span data-stu-id="a8aae-125">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8aae-126">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="a8aae-126">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="a8aae-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8aae-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8aae-128">Referência a um elemento do sistema gerenciado atuando como um sobressalente e participando do grupo sobressalente.</span><span class="sxs-lookup"><span data-stu-id="a8aae-128">Reference to a managed system element acting as a spare and participating in the spare group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8aae-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8aae-129">Remarks</span></span>

<span data-ttu-id="a8aae-130">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="a8aae-130">WMI does not implement this class.</span></span>

<span data-ttu-id="a8aae-131">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="a8aae-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a8aae-132">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="a8aae-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8aae-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8aae-133">Requirements</span></span>



| <span data-ttu-id="a8aae-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8aae-134">Requirement</span></span> | <span data-ttu-id="a8aae-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a8aae-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8aae-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8aae-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a8aae-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8aae-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8aae-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8aae-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a8aae-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8aae-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8aae-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8aae-140">Namespace</span></span><br/>                | <span data-ttu-id="a8aae-141">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a8aae-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a8aae-142">MOF</span><span class="sxs-lookup"><span data-stu-id="a8aae-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8aae-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8aae-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8aae-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a8aae-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8aae-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8aae-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8aae-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8aae-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8aae-147">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="a8aae-147">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

