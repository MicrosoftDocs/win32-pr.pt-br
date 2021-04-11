---
description: A \_ classe WMI de associação PrinterSetting do Win32 relaciona uma impressora e suas definições de configuração.
ms.assetid: 5d0f0724-0583-449b-a6da-336e7c8e526e
ms.tgt_platform: multiple
title: Classe Win32_PrinterSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterSetting
- Win32_PrinterSetting.Setting
- Win32_PrinterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90a77678e61b755550ebb1818c34ccdc3159a88c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164037"
---
# <a name="win32_printersetting-class"></a><span data-ttu-id="1c8ba-103">\_Classe Win32 PrinterSetting</span><span class="sxs-lookup"><span data-stu-id="1c8ba-103">Win32\_PrinterSetting class</span></span>

<span data-ttu-id="1c8ba-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ PrinterSetting do Win32** relaciona uma impressora e suas definições de configuração.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-104">The **Win32\_PrinterSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a printer and its configuration settings.</span></span>

<span data-ttu-id="1c8ba-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1c8ba-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c8ba-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c8ba-107">Syntax</span></span>

``` syntax
class Win32_PrinterSetting : Win32_DeviceSettings
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a><span data-ttu-id="1c8ba-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1c8ba-108">Members</span></span>

<span data-ttu-id="1c8ba-109">A classe **Win32 \_ PrinterSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1c8ba-109">The **Win32\_PrinterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="1c8ba-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1c8ba-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c8ba-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1c8ba-111">Properties</span></span>

<span data-ttu-id="1c8ba-112">A classe **Win32 \_ PrinterSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-112">The **Win32\_PrinterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c8ba-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c8ba-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c8ba-114">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="1c8ba-114">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="1c8ba-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c8ba-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c8ba-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="1c8ba-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="1c8ba-117">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que representa as propriedades do dispositivo lógico no qual as configurações podem ser aplicadas.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents properties of the logical device on which the settings can be applied.</span></span>

<span data-ttu-id="1c8ba-118">Esta propriedade é herdada do [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="1c8ba-118">This property is inherited from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c8ba-119">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="1c8ba-119">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c8ba-120">Tipo de dados **: \_ configuração de CIM**</span><span class="sxs-lookup"><span data-stu-id="1c8ba-120">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="1c8ba-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c8ba-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c8ba-122">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("configuração CIM CIM \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="1c8ba-122">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="1c8ba-123">Uma [**\_ configuração de CIM**](cim-setting.md) que representa as configurações que podem ser aplicadas ao dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-123">A [**CIM\_Setting**](cim-setting.md) that represents settings that can be applied to the logical device.</span></span>

<span data-ttu-id="1c8ba-124">Esta propriedade é herdada do [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="1c8ba-124">This property is inherited from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c8ba-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c8ba-125">Remarks</span></span>

<span data-ttu-id="1c8ba-126">A classe **Win32 \_ PrinterSetting** é derivada de [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="1c8ba-126">The **Win32\_PrinterSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c8ba-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c8ba-127">Requirements</span></span>



| <span data-ttu-id="1c8ba-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c8ba-128">Requirement</span></span> | <span data-ttu-id="1c8ba-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1c8ba-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c8ba-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c8ba-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1c8ba-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8ba-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="1c8ba-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c8ba-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1c8ba-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c8ba-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="1c8ba-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c8ba-134">Namespace</span></span><br/>                | <span data-ttu-id="1c8ba-135">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1c8ba-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="1c8ba-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1c8ba-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c8ba-137"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="1c8ba-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c8ba-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1c8ba-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c8ba-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c8ba-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="1c8ba-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c8ba-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c8ba-141">**\_DeviceSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="1c8ba-141">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="1c8ba-142">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="1c8ba-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
