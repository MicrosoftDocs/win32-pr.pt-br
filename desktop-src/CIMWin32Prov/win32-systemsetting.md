---
description: A \_ classe WMI de associação abstrata SystemSetting do Win32 relaciona um sistema de computador e uma configuração geral nesse sistema.
ms.assetid: 796ee263-2526-43f8-bd3d-23442b6bd4ca
ms.tgt_platform: multiple
title: Classe Win32_SystemSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSetting
- Win32_SystemSetting.Element
- Win32_SystemSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e29b752d769cd347ce1cfdb729bf8c0c3959a4f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457168"
---
# <a name="win32_systemsetting-class"></a><span data-ttu-id="dca70-103">\_Classe Win32 SystemSetting</span><span class="sxs-lookup"><span data-stu-id="dca70-103">Win32\_SystemSetting class</span></span>

<span data-ttu-id="dca70-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação abstrata **\_ SystemSetting do Win32** relaciona um sistema de computador e uma configuração geral nesse sistema.</span><span class="sxs-lookup"><span data-stu-id="dca70-104">The **Win32\_SystemSetting** abstract association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a general setting on that system.</span></span>

<span data-ttu-id="dca70-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="dca70-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dca70-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="dca70-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dca70-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dca70-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C501-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSetting : CIM_ElementSetting
{
  Win32_ComputerSystem REF Element;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="dca70-108">Membros</span><span class="sxs-lookup"><span data-stu-id="dca70-108">Members</span></span>

<span data-ttu-id="dca70-109">A classe **Win32 \_ SystemSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dca70-109">The **Win32\_SystemSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="dca70-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dca70-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dca70-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dca70-111">Properties</span></span>

<span data-ttu-id="dca70-112">A classe **Win32 \_ SystemSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dca70-112">The **Win32\_SystemSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dca70-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="dca70-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dca70-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="dca70-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="dca70-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dca70-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dca70-116">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("elemento"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="dca70-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="dca70-117">Referência à instância que representa as propriedades de um sistema de computador em que essa configuração pode ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="dca70-117">Reference to the instance representing the properties of a computer system where this setting can be applied.</span></span>

</dd> <dt>

<span data-ttu-id="dca70-118">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="dca70-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dca70-119">Tipo de dados **: \_ configuração de CIM**</span><span class="sxs-lookup"><span data-stu-id="dca70-119">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="dca70-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dca70-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dca70-121">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("configuração"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("configuração CIM CIM \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="dca70-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="dca70-122">Referência à instância que representa as propriedades da configuração que pode ser aplicada ao sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="dca70-122">Reference to the instance representing the properties of the setting that can be applied to the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dca70-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="dca70-123">Remarks</span></span>

<span data-ttu-id="dca70-124">A classe **Win32 \_ SystemSetting** é derivada de [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="dca70-124">The **Win32\_SystemSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dca70-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dca70-125">Requirements</span></span>



| <span data-ttu-id="dca70-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dca70-126">Requirement</span></span> | <span data-ttu-id="dca70-127">Valor</span><span class="sxs-lookup"><span data-stu-id="dca70-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dca70-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dca70-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dca70-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dca70-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dca70-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dca70-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dca70-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dca70-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dca70-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="dca70-132">Namespace</span></span><br/>                | <span data-ttu-id="dca70-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dca70-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dca70-134">MOF</span><span class="sxs-lookup"><span data-stu-id="dca70-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dca70-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dca70-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dca70-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dca70-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dca70-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dca70-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dca70-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="dca70-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dca70-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="dca70-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="dca70-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="dca70-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
