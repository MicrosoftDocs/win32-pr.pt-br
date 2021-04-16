---
description: A \_ classe WMI de associação PnPDevice do Win32 relaciona um dispositivo (conhecido por Configuration Manager como um PNPEntity) e a função que ele executa.
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Classe Win32_PnPDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c17dc6d4169854469d630e2a622eacc85e8a587c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753798"
---
# <a name="win32_pnpdevice-class"></a><span data-ttu-id="5098d-103">\_Classe Win32 PnPDevice</span><span class="sxs-lookup"><span data-stu-id="5098d-103">Win32\_PnPDevice class</span></span>

<span data-ttu-id="5098d-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ PnPDevice do Win32** relaciona um dispositivo (conhecido por Configuration Manager como um PNPEntity) e a função que ele executa.</span><span class="sxs-lookup"><span data-stu-id="5098d-104">The **Win32\_PnPDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a device (known to Configuration Manager as a PNPEntity) and the function it performs.</span></span> <span data-ttu-id="5098d-105">Sua função é representada por uma subclasse do dispositivo lógico que descreve seu uso.</span><span class="sxs-lookup"><span data-stu-id="5098d-105">Its function is represented by a subclass of the logical device that describes its use.</span></span> <span data-ttu-id="5098d-106">Por exemplo, uma instância do Win32 [**\_ Keyboard**](win32-keyboard.md) ou [**Win32 \_ DiskDrive**](win32-diskdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="5098d-106">For example, a [**Win32\_Keyboard**](win32-keyboard.md) or [**Win32\_DiskDrive**](win32-diskdrive.md) instance.</span></span> <span data-ttu-id="5098d-107">Ambos os objetos referenciados representam o mesmo dispositivo de sistema subjacente; as alterações na alocação de recursos no lado do PNPEntity afetarão o dispositivo associado.</span><span class="sxs-lookup"><span data-stu-id="5098d-107">Both referenced objects represent the same underlying system device; changes to resource allocation on the PNPEntity side will effect the associated device.</span></span>

<span data-ttu-id="5098d-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5098d-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5098d-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5098d-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5098d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5098d-110">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="5098d-111">Membros</span><span class="sxs-lookup"><span data-stu-id="5098d-111">Members</span></span>

<span data-ttu-id="5098d-112">A classe **Win32 \_ PnPDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5098d-112">The **Win32\_PnPDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="5098d-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5098d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5098d-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5098d-114">Properties</span></span>

<span data-ttu-id="5098d-115">A classe **Win32 \_ PnPDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5098d-115">The **Win32\_PnPDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5098d-116">**Mesmoelement**</span><span class="sxs-lookup"><span data-stu-id="5098d-116">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5098d-117">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="5098d-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="5098d-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5098d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5098d-119">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="5098d-119">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="5098d-120">Referência à instância [**CIM \_ LogicalDevice**](cim-logicaldevice.md) que representa as propriedades de dispositivo lógico associadas ao dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="5098d-120">Reference to the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance representing the logical device properties associated with the Plug and Play device.</span></span>

</dd> <dt>

<span data-ttu-id="5098d-121">**Sistema de**</span><span class="sxs-lookup"><span data-stu-id="5098d-121">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5098d-122">Tipo de dados: **Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="5098d-122">Data type: **Win32\_PnPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="5098d-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5098d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5098d-124">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PnPEntity")</span><span class="sxs-lookup"><span data-stu-id="5098d-124">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PnPEntity")</span></span>
</dt> </dl>

<span data-ttu-id="5098d-125">Referência à instância do [**Win32 \_ PnPEntity**](win32-pnpentity.md) que representa o dispositivo Plug and Play associado ao dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5098d-125">Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance representing the Plug and Play device associated with the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5098d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5098d-126">Requirements</span></span>



| <span data-ttu-id="5098d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5098d-127">Requirement</span></span> | <span data-ttu-id="5098d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5098d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5098d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5098d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5098d-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5098d-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5098d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5098d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5098d-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5098d-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5098d-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="5098d-133">Namespace</span></span><br/>                | <span data-ttu-id="5098d-134">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5098d-134">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5098d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="5098d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5098d-136"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5098d-136"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5098d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5098d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5098d-138"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5098d-138"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5098d-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="5098d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5098d-140">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="5098d-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
