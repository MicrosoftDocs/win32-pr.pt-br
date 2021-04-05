---
description: A \_ classe WMI de associação Win32 WMIElementSetting relaciona um serviço em execução no sistema Windows e as configurações de WMI que ele pode usar.
ms.assetid: 00e9f882-5f54-4042-a916-2f90ed9a37c0
ms.tgt_platform: multiple
title: Classe Win32_WMIElementSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMIElementSetting
- Win32_WMIElementSetting.Element
- Win32_WMIElementSetting.Setting
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 41f79614fd0931759d502bbd61c7f4143e9e7dc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826173"
---
# <a name="win32_wmielementsetting-class"></a><span data-ttu-id="20b29-103">\_Classe Win32 WMIElementSetting</span><span class="sxs-lookup"><span data-stu-id="20b29-103">Win32\_WMIElementSetting class</span></span>

<span data-ttu-id="20b29-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **Win32 \_ WMIElementSetting** relaciona um serviço em execução no sistema Windows e as configurações de WMI que ele pode usar.</span><span class="sxs-lookup"><span data-stu-id="20b29-104">The **Win32\_WMIElementSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a service running in the Windows system and the WMI settings it can use.</span></span>

<span data-ttu-id="20b29-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="20b29-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="20b29-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="20b29-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="20b29-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20b29-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("WBEMCORE"), UUID("{A83EF167-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMIElementSetting : CIM_ElementSetting
{
  Win32_Service    REF Element;
  Win32_WMISetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="20b29-108">Membros</span><span class="sxs-lookup"><span data-stu-id="20b29-108">Members</span></span>

<span data-ttu-id="20b29-109">A classe **Win32 \_ WMIElementSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="20b29-109">The **Win32\_WMIElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="20b29-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="20b29-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20b29-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="20b29-111">Properties</span></span>

<span data-ttu-id="20b29-112">A classe **Win32 \_ WMIElementSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="20b29-112">The **Win32\_WMIElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20b29-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="20b29-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20b29-114">Tipo de dados **: \_ serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="20b29-114">Data type: **Win32\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="20b29-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20b29-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20b29-116">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Service")</span><span class="sxs-lookup"><span data-stu-id="20b29-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Service")</span></span>
</dt> </dl>

<span data-ttu-id="20b29-117">Referência à instância que representa o serviço do Windows usando ou identificando propriedades WMI.</span><span class="sxs-lookup"><span data-stu-id="20b29-117">Reference to the instance representing the Windows service using or surfacing WMI properties.</span></span>

</dd> <dt>

<span data-ttu-id="20b29-118">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="20b29-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20b29-119">Tipo de dados: **Win32 \_ WMISetting**</span><span class="sxs-lookup"><span data-stu-id="20b29-119">Data type: **Win32\_WMISetting**</span></span>
</dt> <dt>

<span data-ttu-id="20b29-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20b29-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20b29-121">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("configuração"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ WMISetting")</span><span class="sxs-lookup"><span data-stu-id="20b29-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_WMISetting")</span></span>
</dt> </dl>

<span data-ttu-id="20b29-122">Referência à instância que representa as configurações de WMI disponíveis para o serviço do Windows.</span><span class="sxs-lookup"><span data-stu-id="20b29-122">Reference to the instance representing the WMI settings available to the Windows service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20b29-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="20b29-123">Remarks</span></span>

<span data-ttu-id="20b29-124">A classe **Win32 \_ WMIElementSetting** é derivada de [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="20b29-124">The **Win32\_WMIElementSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20b29-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20b29-125">Requirements</span></span>



| <span data-ttu-id="20b29-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="20b29-126">Requirement</span></span> | <span data-ttu-id="20b29-127">Valor</span><span class="sxs-lookup"><span data-stu-id="20b29-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20b29-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20b29-128">Minimum supported client</span></span><br/> | <span data-ttu-id="20b29-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20b29-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20b29-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20b29-130">Minimum supported server</span></span><br/> | <span data-ttu-id="20b29-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20b29-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20b29-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="20b29-132">Namespace</span></span><br/>                | <span data-ttu-id="20b29-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="20b29-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="20b29-134">MOF</span><span class="sxs-lookup"><span data-stu-id="20b29-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20b29-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20b29-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="20b29-136">DLL</span><span class="sxs-lookup"><span data-stu-id="20b29-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20b29-137"><dt>Wbemcore.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20b29-137"><dt>Wbemcore.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20b29-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="20b29-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20b29-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="20b29-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="20b29-140">Classes de gerenciamento de serviço WMI</span><span class="sxs-lookup"><span data-stu-id="20b29-140">WMI Service Management Classes</span></span>](./wmi-service-management-classes.md)
</dt> </dl>

 

 
