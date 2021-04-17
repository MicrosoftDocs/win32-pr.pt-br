---
description: A \_ classe WMI de associação NetworkAdapterSetting do Win32 relaciona um adaptador de rede e suas definições de configuração.
ms.assetid: 6fc646c3-05f9-4c92-8598-07ea20fffaca
ms.tgt_platform: multiple
title: Classe Win32_NetworkAdapterSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterSetting
- Win32_NetworkAdapterSetting.Setting
- Win32_NetworkAdapterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c51ef9ed790c902a6a662dc3ebc45df97fa29721
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755431"
---
# <a name="win32_networkadaptersetting-class"></a><span data-ttu-id="658e3-103">\_Classe Win32 NetworkAdapterSetting</span><span class="sxs-lookup"><span data-stu-id="658e3-103">Win32\_NetworkAdapterSetting class</span></span>

<span data-ttu-id="658e3-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ NetworkAdapterSetting do Win32** relaciona um adaptador de rede e suas definições de configuração.</span><span class="sxs-lookup"><span data-stu-id="658e3-104">The **Win32\_NetworkAdapterSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a network adapter and its configuration settings.</span></span>

<span data-ttu-id="658e3-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="658e3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="658e3-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="658e3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="658e3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="658e3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterSetting : Win32_DeviceSettings
{
  Win32_NetworkAdapterConfiguration REF Setting;
  Win32_NetworkAdapter              REF Element;
};
```

## <a name="members"></a><span data-ttu-id="658e3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="658e3-108">Members</span></span>

<span data-ttu-id="658e3-109">A classe **Win32 \_ NetworkAdapterSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="658e3-109">The **Win32\_NetworkAdapterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="658e3-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="658e3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="658e3-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="658e3-111">Properties</span></span>

<span data-ttu-id="658e3-112">A classe **Win32 \_ NetworkAdapterSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="658e3-112">The **Win32\_NetworkAdapterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="658e3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="658e3-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e3-114">Tipo de dados: **Win32 \_ adaptador**</span><span class="sxs-lookup"><span data-stu-id="658e3-114">Data type: **Win32\_NetworkAdapter**</span></span>
</dt> <dt>

<span data-ttu-id="658e3-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="658e3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658e3-116">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ adaptador")</span><span class="sxs-lookup"><span data-stu-id="658e3-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="658e3-117">Um [**\_ adaptador Win32**](win32-networkadapter.md) que descreve as propriedades do adaptador de rede que está usando uma configuração de adaptador de rede específica.</span><span class="sxs-lookup"><span data-stu-id="658e3-117">A [**Win32\_NetworkAdapter**](win32-networkadapter.md) that describes the properties of the network adapter that is using a particular network adapter setting.</span></span>

</dd> <dt>

<span data-ttu-id="658e3-118">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="658e3-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e3-119">Tipo de dados: **Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="658e3-119">Data type: **Win32\_NetworkAdapterConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="658e3-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="658e3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658e3-121">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration")</span><span class="sxs-lookup"><span data-stu-id="658e3-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapterConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="658e3-122">Um [**\_ NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md) que descreve as definições de configuração usadas no adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="658e3-122">A [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) that describes the configuration settings used on the network adapter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="658e3-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="658e3-123">Remarks</span></span>

<span data-ttu-id="658e3-124">A classe **Win32 \_ NetworkAdapterSetting** é derivada de [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="658e3-124">The **Win32\_NetworkAdapterSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

<span data-ttu-id="658e3-125">Para obter informações sobre como usar classes de associação, consulte [associars of Statement](../wmisdk/associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="658e3-125">For information on how to use association classes, see [ASSOCIATORS OF Statement](../wmisdk/associators-of-statement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="658e3-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="658e3-126">Examples</span></span>

<span data-ttu-id="658e3-127">O exemplo de VBScript a seguir usa o **Win32 \_ NetworkAdapterSetting** para identificar o endereço IP na conexão de área local.</span><span class="sxs-lookup"><span data-stu-id="658e3-127">The following VBScript sample uses **Win32\_NetworkAdapterSetting** to identify the IP Address on the Local Area Connection.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colNics = objWMIService.ExecQuery _
    ("Select * From Win32_NetworkAdapter " _
        & "Where NetConnectionID = " & _
        "'Local Area Connection'")
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      ("ASSOCIATORS OF " _
          & "{Win32_NetworkAdapter.DeviceID='" & _
      objNic.DeviceID & "'}" & _
      " WHERE AssocClass=Win32_NetworkAdapterSetting")
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo "IP Address: " &  strIPAddress
        Next
    Next
Next
```



## <a name="requirements"></a><span data-ttu-id="658e3-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="658e3-128">Requirements</span></span>



| <span data-ttu-id="658e3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="658e3-129">Requirement</span></span> | <span data-ttu-id="658e3-130">Valor</span><span class="sxs-lookup"><span data-stu-id="658e3-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="658e3-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="658e3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="658e3-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="658e3-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="658e3-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="658e3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="658e3-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="658e3-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="658e3-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="658e3-135">Namespace</span></span><br/>                | <span data-ttu-id="658e3-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="658e3-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="658e3-137">MOF</span><span class="sxs-lookup"><span data-stu-id="658e3-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="658e3-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="658e3-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="658e3-139">DLL</span><span class="sxs-lookup"><span data-stu-id="658e3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="658e3-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="658e3-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="658e3-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="658e3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="658e3-142">**\_DeviceSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="658e3-142">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="658e3-143">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="658e3-143">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="658e3-144">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="658e3-144">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> </dl>

 

 
