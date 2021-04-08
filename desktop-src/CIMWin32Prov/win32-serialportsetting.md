---
description: A \_ classe WMI de associação do Win32 SerialPortSetting relaciona uma porta serial e suas definições de configuração.
ms.assetid: 57856207-abe5-4d93-9a34-acfe30ccd80c
ms.tgt_platform: multiple
title: Classe Win32_SerialPortSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortSetting
- Win32_SerialPortSetting.Setting
- Win32_SerialPortSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 713cdb57b5ed7135529959d3c17f7453924ce1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920180"
---
# <a name="win32_serialportsetting-class"></a><span data-ttu-id="dd355-103">\_Classe Win32 SerialPortSetting</span><span class="sxs-lookup"><span data-stu-id="dd355-103">Win32\_SerialPortSetting class</span></span>

<span data-ttu-id="dd355-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação do **Win32 \_ SerialPortSetting** relaciona uma porta serial e suas definições de configuração.</span><span class="sxs-lookup"><span data-stu-id="dd355-104">The **Win32\_SerialPortSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a serial port and its configuration settings.</span></span>

<span data-ttu-id="dd355-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="dd355-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dd355-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="dd355-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd355-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd355-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortSetting : Win32_DeviceSettings
{
  Win32_SerialPortConfiguration REF Setting;
  Win32_SerialPort              REF Element;
};
```

## <a name="members"></a><span data-ttu-id="dd355-108">Membros</span><span class="sxs-lookup"><span data-stu-id="dd355-108">Members</span></span>

<span data-ttu-id="dd355-109">A classe **Win32 \_ SerialPortSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dd355-109">The **Win32\_SerialPortSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="dd355-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dd355-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd355-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dd355-111">Properties</span></span>

<span data-ttu-id="dd355-112">A classe **Win32 \_ SerialPortSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dd355-112">The **Win32\_SerialPortSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd355-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd355-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd355-114">Tipo de dados **: \_ SerialPort do Win32**</span><span class="sxs-lookup"><span data-stu-id="dd355-114">Data type: **Win32\_SerialPort**</span></span>
</dt> <dt>

<span data-ttu-id="dd355-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd355-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd355-116">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")</span><span class="sxs-lookup"><span data-stu-id="dd355-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPort")</span></span>
</dt> </dl>

<span data-ttu-id="dd355-117">Uma [**\_ SerialPort do Win32**](win32-serialport.md) que contém as propriedades de uma porta serial no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="dd355-117">A [**Win32\_SerialPort**](win32-serialport.md) that contains the properties of a serial port on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="dd355-118">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="dd355-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd355-119">Tipo de dados: **Win32 \_ SerialPortConfiguration**</span><span class="sxs-lookup"><span data-stu-id="dd355-119">Data type: **Win32\_SerialPortConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="dd355-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd355-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd355-121">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPortConfiguration")</span><span class="sxs-lookup"><span data-stu-id="dd355-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPortConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="dd355-122">Um [**\_ SerialPortConfiguration Win32**](win32-serialportconfiguration.md) que contém a definição de configuração para a porta serial.</span><span class="sxs-lookup"><span data-stu-id="dd355-122">A [**Win32\_SerialPortConfiguration**](win32-serialportconfiguration.md) that contains the configuration setting for the serial port.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd355-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd355-123">Remarks</span></span>

<span data-ttu-id="dd355-124">A classe **Win32 \_ SerialPortSetting** é derivada de [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="dd355-124">The **Win32\_SerialPortSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd355-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd355-125">Requirements</span></span>



| <span data-ttu-id="dd355-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd355-126">Requirement</span></span> | <span data-ttu-id="dd355-127">Valor</span><span class="sxs-lookup"><span data-stu-id="dd355-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd355-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd355-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dd355-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd355-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd355-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd355-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dd355-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd355-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd355-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd355-132">Namespace</span></span><br/>                | <span data-ttu-id="dd355-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dd355-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dd355-134">MOF</span><span class="sxs-lookup"><span data-stu-id="dd355-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd355-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd355-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd355-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dd355-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd355-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd355-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd355-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd355-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd355-139">**\_DeviceSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="dd355-139">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="dd355-140">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="dd355-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
