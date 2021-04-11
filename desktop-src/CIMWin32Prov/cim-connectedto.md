---
description: A \_ classe CIM conectadoto representa uma associação que indica que dois ou mais conectores físicos estão conectados.
ms.assetid: fedd9227-8a3b-461a-995b-08cbceb81181
ms.tgt_platform: multiple
title: Classe CIM_ConnectedTo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectedTo
- CIM_ConnectedTo.Dependent
- CIM_ConnectedTo.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f1a507cb529f2040607024e1a6167ddcd5dc7c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010222"
---
# <a name="cim_connectedto-class"></a><span data-ttu-id="f2633-103">\_Classe conectada CIM</span><span class="sxs-lookup"><span data-stu-id="f2633-103">CIM\_ConnectedTo class</span></span>

<span data-ttu-id="f2633-104">A classe **CIM \_ conectadoto** representa uma associação que indica que dois ou mais conectores físicos estão conectados.</span><span class="sxs-lookup"><span data-stu-id="f2633-104">The **CIM\_ConnectedTo** class represents an association that indicates that two or more physical connectors are connected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2633-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="f2633-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f2633-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f2633-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f2633-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f2633-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f2633-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="f2633-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2633-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2633-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B85-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectedTo : CIM_Dependency
{
  CIM_PhysicalConnector REF Dependent;
  CIM_PhysicalConnector REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="f2633-110">Membros</span><span class="sxs-lookup"><span data-stu-id="f2633-110">Members</span></span>

<span data-ttu-id="f2633-111">A classe **CIM \_ conectadoto** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f2633-111">The **CIM\_ConnectedTo** class has these types of members:</span></span>

-   [<span data-ttu-id="f2633-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f2633-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2633-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f2633-113">Properties</span></span>

<span data-ttu-id="f2633-114">A classe **CIM \_ conectadoto** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f2633-114">The **CIM\_ConnectedTo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2633-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="f2633-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2633-116">Tipo de dados: **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="f2633-116">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="f2633-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2633-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2633-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="f2633-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f2633-119">Um [**\_ PhysicalConnector CIM**](cim-physicalconnector.md) que representa um conector físico que serve como uma extremidade da conexão.</span><span class="sxs-lookup"><span data-stu-id="f2633-119">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that represents a physical connector that serves as one end of the connection.</span></span>

</dd> <dt>

<span data-ttu-id="f2633-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="f2633-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2633-121">Tipo de dados: **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="f2633-121">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="f2633-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2633-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2633-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="f2633-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f2633-124">Um [**\_ PhysicalConnector CIM**](cim-physicalconnector.md) que representa outro conector físico que serve como a outra extremidade da conexão.</span><span class="sxs-lookup"><span data-stu-id="f2633-124">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that represents another physical connector that serves as the other end of the connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2633-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2633-125">Remarks</span></span>

<span data-ttu-id="f2633-126">A **classe \_ conectada ao CIM** é herdada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="f2633-126">The **CIM\_ConnectedTo** class is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="f2633-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="f2633-127">WMI does not implement this class.</span></span>

<span data-ttu-id="f2633-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="f2633-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f2633-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="f2633-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2633-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2633-130">Requirements</span></span>



| <span data-ttu-id="f2633-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2633-131">Requirement</span></span> | <span data-ttu-id="f2633-132">Valor</span><span class="sxs-lookup"><span data-stu-id="f2633-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2633-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2633-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f2633-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2633-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2633-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2633-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f2633-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2633-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2633-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2633-137">Namespace</span></span><br/>                | <span data-ttu-id="f2633-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f2633-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f2633-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f2633-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2633-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2633-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2633-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f2633-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2633-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2633-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2633-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2633-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2633-144">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="f2633-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

