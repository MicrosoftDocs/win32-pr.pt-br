---
description: A \_ classe WMI de associação SystemDriverPNPEntity do Win32 relaciona um dispositivo Plug and Play no sistema de computador que executa o Windows e o driver que dá suporte ao dispositivo Plug and Play.
ms.assetid: 2696c8e5-3bc3-42e3-807b-a387607c7c09
ms.tgt_platform: multiple
title: Classe Win32_SystemDriverPNPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriverPNPEntity
- Win32_SystemDriverPNPEntity.Antecedent
- Win32_SystemDriverPNPEntity.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b5a7eedfbd7a545e37cb9cda38c19cf61308761
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500958"
---
# <a name="win32_systemdriverpnpentity-class"></a><span data-ttu-id="2b27e-103">\_Classe Win32 SystemDriverPNPEntity</span><span class="sxs-lookup"><span data-stu-id="2b27e-103">Win32\_SystemDriverPNPEntity class</span></span>

<span data-ttu-id="2b27e-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemDriverPNPEntity do Win32** relaciona um dispositivo Plug and Play no sistema de computador que executa o Windows e o driver que dá suporte ao dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="2b27e-104">The **Win32\_SystemDriverPNPEntity** association [WMI class](../wmisdk/retrieving-a-class.md) relates a Plug and Play device on the computer system running Windows and the driver that supports the Plug and Play device.</span></span>

<span data-ttu-id="2b27e-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2b27e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2b27e-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="2b27e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b27e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b27e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0800F074-CB98-11d2-B35D-00104BC97924}"), AMENDMENT]
class Win32_SystemDriverPNPEntity : CIM_Dependency
{
  Win32_PNPEntity    REF Antecedent;
  Win32_SystemDriver REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2b27e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2b27e-108">Members</span></span>

<span data-ttu-id="2b27e-109">A classe **Win32 \_ SystemDriverPNPEntity** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2b27e-109">The **Win32\_SystemDriverPNPEntity** class has these types of members:</span></span>

-   [<span data-ttu-id="2b27e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2b27e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b27e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2b27e-111">Properties</span></span>

<span data-ttu-id="2b27e-112">A classe **Win32 \_ SystemDriverPNPEntity** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2b27e-112">The **Win32\_SystemDriverPNPEntity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b27e-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="2b27e-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b27e-114">Tipo de dados: **Win32 \_ PNPEntity**</span><span class="sxs-lookup"><span data-stu-id="2b27e-114">Data type: **Win32\_PNPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="2b27e-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2b27e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b27e-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PNPEntity")</span><span class="sxs-lookup"><span data-stu-id="2b27e-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PNPEntity")</span></span>
</dt> </dl>

<span data-ttu-id="2b27e-117">Representa o dispositivo Plug and Play controlado pelo driver.</span><span class="sxs-lookup"><span data-stu-id="2b27e-117">Represents the Plug and Play device controlled by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="2b27e-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="2b27e-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b27e-119">Tipo de dados **: \_ systemdrive do Win32**</span><span class="sxs-lookup"><span data-stu-id="2b27e-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="2b27e-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2b27e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b27e-121">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("dependente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")</span><span class="sxs-lookup"><span data-stu-id="2b27e-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="2b27e-122">Um [**\_ SystemDriver Win32**](win32-systemdriver.md) que representa o driver que dá suporte ao dispositivo de plug and Play.</span><span class="sxs-lookup"><span data-stu-id="2b27e-122">A [**Win32\_SystemDriver**](win32-systemdriver.md) that represents the driver that supports the Plug and Play device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b27e-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b27e-123">Remarks</span></span>

<span data-ttu-id="2b27e-124">A classe **Win32 \_ SystemDriverPNPEntity** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="2b27e-124">The **Win32\_SystemDriverPNPEntity** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b27e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b27e-125">Requirements</span></span>



| <span data-ttu-id="2b27e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b27e-126">Requirement</span></span> | <span data-ttu-id="2b27e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="2b27e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b27e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b27e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2b27e-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b27e-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2b27e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b27e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2b27e-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b27e-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2b27e-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b27e-132">Namespace</span></span><br/>                | <span data-ttu-id="2b27e-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2b27e-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2b27e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="2b27e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b27e-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b27e-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b27e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2b27e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b27e-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b27e-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b27e-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b27e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b27e-139">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="2b27e-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="2b27e-140">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="2b27e-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
