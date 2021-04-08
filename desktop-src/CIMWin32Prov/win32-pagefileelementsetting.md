---
description: A \_ classe WMI de associação do Win32 PageFileElementSetting relaciona as configurações iniciais de um arquivo de paginação e o estado dessas configurações durante o uso normal.
ms.assetid: efc1f20d-166e-4e27-9767-f6ec0bbd6c14
ms.tgt_platform: multiple
title: Classe Win32_PageFileElementSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileElementSetting
- Win32_PageFileElementSetting.Element
- Win32_PageFileElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfc1087225894cef2895cf41af5e5297769a4041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920520"
---
# <a name="win32_pagefileelementsetting-class"></a><span data-ttu-id="2aed4-103">\_Classe Win32 PageFileElementSetting</span><span class="sxs-lookup"><span data-stu-id="2aed4-103">Win32\_PageFileElementSetting class</span></span>

<span data-ttu-id="2aed4-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação do **Win32 \_ PageFileElementSetting** relaciona as configurações iniciais de um arquivo de paginação e o estado dessas configurações durante o uso normal.</span><span class="sxs-lookup"><span data-stu-id="2aed4-104">The **Win32\_PageFileElementSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates the initial settings of a page file and the state of those settings during normal use.</span></span>

<span data-ttu-id="2aed4-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2aed4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2aed4-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="2aed4-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aed4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2aed4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8E7F70E8-C856-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileElementSetting : CIM_ElementSetting
{
  Win32_PageFileUsage   REF Element;
  Win32_PageFileSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="2aed4-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2aed4-108">Members</span></span>

<span data-ttu-id="2aed4-109">A classe **Win32 \_ PageFileElementSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2aed4-109">The **Win32\_PageFileElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="2aed4-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2aed4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2aed4-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2aed4-111">Properties</span></span>

<span data-ttu-id="2aed4-112">A classe **Win32 \_ PageFileElementSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2aed4-112">The **Win32\_PageFileElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2aed4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2aed4-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aed4-114">Tipo de dados: **Win32 \_ PageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="2aed4-114">Data type: **Win32\_PageFileUsage**</span></span>
</dt> <dt>

<span data-ttu-id="2aed4-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aed4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2aed4-116">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("elemento"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PageFileUsage")</span><span class="sxs-lookup"><span data-stu-id="2aed4-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PageFileUsage")</span></span>
</dt> </dl>

<span data-ttu-id="2aed4-117">Referência à instância que representa as propriedades de um arquivo de paginação enquanto o sistema Win32 está em uso.</span><span class="sxs-lookup"><span data-stu-id="2aed4-117">Reference to the instance representing the properties of a page file while the Win32 system is in use.</span></span>

</dd> <dt>

<span data-ttu-id="2aed4-118">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="2aed4-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aed4-119">Tipo de dados: **Win32 \_ PageFileSetting**</span><span class="sxs-lookup"><span data-stu-id="2aed4-119">Data type: **Win32\_PageFileSetting**</span></span>
</dt> <dt>

<span data-ttu-id="2aed4-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aed4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2aed4-121">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("configuração"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PageFileSetting")</span><span class="sxs-lookup"><span data-stu-id="2aed4-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PageFileSetting")</span></span>
</dt> </dl>

<span data-ttu-id="2aed4-122">Referência à instância que representa as configurações iniciais de um arquivo de paginação quando o sistema Win32 está sendo inicializado.</span><span class="sxs-lookup"><span data-stu-id="2aed4-122">Reference to the instance representing the initial settings of a page file when the Win32 system is starting up.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2aed4-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="2aed4-123">Remarks</span></span>

<span data-ttu-id="2aed4-124">A classe **Win32 \_ PageFileElementSetting** é derivada de [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="2aed4-124">The **Win32\_PageFileElementSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2aed4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2aed4-125">Requirements</span></span>



| <span data-ttu-id="2aed4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2aed4-126">Requirement</span></span> | <span data-ttu-id="2aed4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="2aed4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2aed4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2aed4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2aed4-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2aed4-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2aed4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2aed4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2aed4-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2aed4-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2aed4-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="2aed4-132">Namespace</span></span><br/>                | <span data-ttu-id="2aed4-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2aed4-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2aed4-134">MOF</span><span class="sxs-lookup"><span data-stu-id="2aed4-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2aed4-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2aed4-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2aed4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2aed4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2aed4-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2aed4-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2aed4-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="2aed4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aed4-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="2aed4-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="2aed4-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="2aed4-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
