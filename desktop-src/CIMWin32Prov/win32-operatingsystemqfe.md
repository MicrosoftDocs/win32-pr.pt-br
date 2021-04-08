---
description: A \_ classe WMI de associação do Win32 OperatingSystemQFE relaciona um sistema operacional e as atualizações do produto são aplicadas conforme representado no Win32 \_ QuickFixEngineering.
ms.assetid: 71985759-7e45-44df-82a9-f9a93e3b923e
ms.tgt_platform: multiple
title: Classe Win32_OperatingSystemQFE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystemQFE
- Win32_OperatingSystemQFE.Antecedent
- Win32_OperatingSystemQFE.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3b357e3c6efb62217c137bc6c785185154ed984
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920523"
---
# <a name="win32_operatingsystemqfe-class"></a><span data-ttu-id="be86a-103">\_Classe Win32 OperatingSystemQFE</span><span class="sxs-lookup"><span data-stu-id="be86a-103">Win32\_OperatingSystemQFE class</span></span>

<span data-ttu-id="be86a-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação do **Win32 \_ OperatingSystemQFE** relaciona um sistema operacional e as atualizações do produto são aplicadas conforme representado no [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md).</span><span class="sxs-lookup"><span data-stu-id="be86a-104">The **Win32\_OperatingSystemQFE** association [WMI class](../wmisdk/retrieving-a-class.md) relates an operating system and the product updates applied as represented in [**Win32\_QuickFixEngineering**](win32-quickfixengineering.md).</span></span>

<span data-ttu-id="be86a-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="be86a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="be86a-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="be86a-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="be86a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be86a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{2CB2C452-C516-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_OperatingSystemQFE : CIM_Dependency
{
  Win32_OperatingSystem     REF Antecedent;
  Win32_QuickFixEngineering REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="be86a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="be86a-108">Members</span></span>

<span data-ttu-id="be86a-109">A classe **Win32 \_ OperatingSystemQFE** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="be86a-109">The **Win32\_OperatingSystemQFE** class has these types of members:</span></span>

-   [<span data-ttu-id="be86a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="be86a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be86a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="be86a-111">Properties</span></span>

<span data-ttu-id="be86a-112">A classe **Win32 \_ OperatingSystemQFE** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="be86a-112">The **Win32\_OperatingSystemQFE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be86a-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="be86a-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be86a-114">Tipo de dados: sistema **\_ operacional Win32**</span><span class="sxs-lookup"><span data-stu-id="be86a-114">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="be86a-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="be86a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be86a-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ OperatingSystem")</span><span class="sxs-lookup"><span data-stu-id="be86a-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_OperatingSystem")</span></span>
</dt> </dl>

<span data-ttu-id="be86a-117">Referência à instância que representa o sistema afetado pela atualização do produto nesta associação.</span><span class="sxs-lookup"><span data-stu-id="be86a-117">Reference to the instance representing the system affected by the product update in this association.</span></span>

</dd> <dt>

<span data-ttu-id="be86a-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="be86a-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be86a-119">Tipo de dados: **Win32 \_ QuickFixEngineering**</span><span class="sxs-lookup"><span data-stu-id="be86a-119">Data type: **Win32\_QuickFixEngineering**</span></span>
</dt> <dt>

<span data-ttu-id="be86a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="be86a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be86a-121">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**fraco**](../wmisdk/standard-qualifiers.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("dependente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ QuickFixEngineering")</span><span class="sxs-lookup"><span data-stu-id="be86a-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Weak**](../wmisdk/standard-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_QuickFixEngineering")</span></span>
</dt> </dl>

<span data-ttu-id="be86a-122">Referência à instância que representa a instância de objeto aplicada ao sistema operacional nessa associação.</span><span class="sxs-lookup"><span data-stu-id="be86a-122">Reference to the instance representing the object instance applied to the operating system in this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be86a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="be86a-123">Remarks</span></span>

<span data-ttu-id="be86a-124">A classe **Win32 \_ OperatingSystemQFE** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="be86a-124">The **Win32\_OperatingSystemQFE** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be86a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be86a-125">Requirements</span></span>



| <span data-ttu-id="be86a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="be86a-126">Requirement</span></span> | <span data-ttu-id="be86a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="be86a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be86a-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be86a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="be86a-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be86a-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be86a-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be86a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="be86a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be86a-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be86a-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="be86a-132">Namespace</span></span><br/>                | <span data-ttu-id="be86a-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="be86a-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="be86a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="be86a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be86a-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be86a-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="be86a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="be86a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be86a-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be86a-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be86a-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="be86a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be86a-139">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="be86a-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="be86a-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="be86a-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
