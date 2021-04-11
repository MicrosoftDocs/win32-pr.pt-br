---
description: O \_ abstrato DeviceSettings do Win32, a classe WMI de associação relaciona um dispositivo lógico e uma configuração que pode ser aplicada a ele.
ms.assetid: 4f6c4c26-8da9-4e2c-8b8c-cec658ac08d4
ms.tgt_platform: multiple
title: Classe Win32_DeviceSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceSettings
- Win32_DeviceSettings.Setting
- Win32_DeviceSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1cd9cae29cfa608c9f3c0c36ebfe3ca7f903c809
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164124"
---
# <a name="win32_devicesettings-class"></a><span data-ttu-id="12b05-103">\_Classe Win32 DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="12b05-103">Win32\_DeviceSettings class</span></span>

<span data-ttu-id="12b05-104">O **abstrato \_ DeviceSettings do Win32** , a [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação relaciona um dispositivo lógico e uma configuração que pode ser aplicada a ele.</span><span class="sxs-lookup"><span data-stu-id="12b05-104">The **Win32\_DeviceSettings** abstract, association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical device and a setting that can be applied to it.</span></span>

<span data-ttu-id="12b05-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="12b05-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="12b05-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="12b05-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="12b05-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12b05-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4FD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceSettings : CIM_ElementSetting
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a><span data-ttu-id="12b05-108">Membros</span><span class="sxs-lookup"><span data-stu-id="12b05-108">Members</span></span>

<span data-ttu-id="12b05-109">A classe **Win32 \_ DeviceSettings** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="12b05-109">The **Win32\_DeviceSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="12b05-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="12b05-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12b05-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="12b05-111">Properties</span></span>

<span data-ttu-id="12b05-112">A classe **Win32 \_ DeviceSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="12b05-112">The **Win32\_DeviceSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12b05-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="12b05-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12b05-114">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="12b05-114">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="12b05-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12b05-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12b05-116">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="12b05-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="12b05-117">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que representa as propriedades do dispositivo lógico no qual as configurações podem ser aplicadas.</span><span class="sxs-lookup"><span data-stu-id="12b05-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents properties of the logical device on which the settings can be applied.</span></span>

</dd> <dt>

<span data-ttu-id="12b05-118">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="12b05-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12b05-119">Tipo de dados **: \_ configuração de CIM**</span><span class="sxs-lookup"><span data-stu-id="12b05-119">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="12b05-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12b05-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12b05-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuração"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuração CIM CIM \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="12b05-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="12b05-122">Uma [**\_ configuração de CIM**](cim-setting.md) que representa as configurações que podem ser aplicadas ao dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="12b05-122">A [**CIM\_Setting**](cim-setting.md) that represents settings that can be applied to the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12b05-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="12b05-123">Remarks</span></span>

<span data-ttu-id="12b05-124">A classe **Win32 \_ DeviceSettings** é derivada de [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="12b05-124">The **Win32\_DeviceSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12b05-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12b05-125">Requirements</span></span>



| <span data-ttu-id="12b05-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="12b05-126">Requirement</span></span> | <span data-ttu-id="12b05-127">Valor</span><span class="sxs-lookup"><span data-stu-id="12b05-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12b05-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12b05-128">Minimum supported client</span></span><br/> | <span data-ttu-id="12b05-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12b05-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12b05-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12b05-130">Minimum supported server</span></span><br/> | <span data-ttu-id="12b05-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12b05-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12b05-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="12b05-132">Namespace</span></span><br/>                | <span data-ttu-id="12b05-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="12b05-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="12b05-134">MOF</span><span class="sxs-lookup"><span data-stu-id="12b05-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12b05-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12b05-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="12b05-136">DLL</span><span class="sxs-lookup"><span data-stu-id="12b05-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12b05-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12b05-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12b05-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="12b05-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12b05-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="12b05-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="12b05-140">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="12b05-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

