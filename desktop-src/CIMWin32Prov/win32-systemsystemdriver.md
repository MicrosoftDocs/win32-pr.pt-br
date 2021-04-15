---
description: A \_ classe WMI de associação SystemSystemDriver do Win32 relaciona um sistema de computador e um driver de sistema em execução nesse sistema de computador.
ms.assetid: 82638c29-6769-4410-90bc-b408b27adad4
ms.tgt_platform: multiple
title: Classe Win32_SystemSystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSystemDriver
- Win32_SystemSystemDriver.GroupComponent
- Win32_SystemSystemDriver.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b193d173fa0592a44ba437543659dec456e432ea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501095"
---
# <a name="win32_systemsystemdriver-class"></a><span data-ttu-id="a17ea-103">\_Classe Win32 SystemSystemDriver</span><span class="sxs-lookup"><span data-stu-id="a17ea-103">Win32\_SystemSystemDriver class</span></span>

<span data-ttu-id="a17ea-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemSystemDriver do Win32** relaciona um sistema de computador e um driver de sistema em execução nesse sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="a17ea-104">The **Win32\_SystemSystemDriver** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a system driver running on that computer system.</span></span>

<span data-ttu-id="a17ea-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a17ea-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a17ea-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="a17ea-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a17ea-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a17ea-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSystemDriver : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_SystemDriver   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a17ea-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a17ea-108">Members</span></span>

<span data-ttu-id="a17ea-109">A classe **Win32 \_ SystemSystemDriver** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a17ea-109">The **Win32\_SystemSystemDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="a17ea-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a17ea-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a17ea-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a17ea-111">Properties</span></span>

<span data-ttu-id="a17ea-112">A classe **Win32 \_ SystemSystemDriver** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a17ea-112">The **Win32\_SystemSystemDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a17ea-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a17ea-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a17ea-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="a17ea-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a17ea-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a17ea-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a17ea-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="a17ea-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="a17ea-117">Referência à instância que representa as propriedades do sistema de computador no qual o driver está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="a17ea-117">Reference to the instance representing the properties of the computer system upon which the driver is running.</span></span>

</dd> <dt>

<span data-ttu-id="a17ea-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a17ea-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a17ea-119">Tipo de dados **: \_ systemdrive do Win32**</span><span class="sxs-lookup"><span data-stu-id="a17ea-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="a17ea-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a17ea-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a17ea-121">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")</span><span class="sxs-lookup"><span data-stu-id="a17ea-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="a17ea-122">Referência à instância que representa o driver do sistema em execução no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="a17ea-122">Reference to the instance representing the system driver running on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a17ea-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a17ea-123">Remarks</span></span>

<span data-ttu-id="a17ea-124">A classe **Win32 \_ SystemSystemDriver** é derivada de [**CIM \_ Systemcomponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="a17ea-124">The **Win32\_SystemSystemDriver** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a17ea-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a17ea-125">Requirements</span></span>



| <span data-ttu-id="a17ea-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a17ea-126">Requirement</span></span> | <span data-ttu-id="a17ea-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a17ea-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a17ea-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a17ea-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a17ea-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a17ea-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a17ea-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a17ea-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a17ea-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a17ea-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a17ea-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="a17ea-132">Namespace</span></span><br/>                | <span data-ttu-id="a17ea-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a17ea-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a17ea-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a17ea-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a17ea-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a17ea-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a17ea-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a17ea-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a17ea-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a17ea-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a17ea-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a17ea-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a17ea-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="a17ea-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="a17ea-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="a17ea-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
