---
description: Essa classe representa a associação entre um sistema operacional e as configurações de Autochk que se aplicam aos discos no computador. Observe que a configuração está associada ao sistema operacional, e não ao sistema de computador, pois pode haver um ou mais sistemas operacionais instalados no computador, cada um com suas próprias configurações de autochk.
ms.assetid: 11178459-85c2-41c0-83b3-5b967e3311cf
ms.tgt_platform: multiple
title: Classe Win32_OperatingSystemAutochkSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 905ffc92273b46bb36b7b3e2909afea32e6baeff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089529"
---
# <a name="win32_operatingsystemautochksetting-class"></a><span data-ttu-id="18856-103">\_Classe Win32 OperatingSystemAutochkSetting</span><span class="sxs-lookup"><span data-stu-id="18856-103">Win32\_OperatingSystemAutochkSetting class</span></span>

<span data-ttu-id="18856-104">Essa classe representa a associação entre um sistema operacional e as configurações de Autochk que se aplicam aos discos no computador. Observe que a configuração está associada ao sistema operacional, e não ao sistema de computador, pois pode haver um ou mais sistemas operacionais instalados no computador, cada um com suas próprias configurações de autochk.</span><span class="sxs-lookup"><span data-stu-id="18856-104">This class represents the association between an operating system and the autochk settings that apply to the disks on the machine.Note that the setting is associated to operating system rather than computer system since there can be one or more operating systems installed on the machine, each with its own autochk settings.</span></span>

<span data-ttu-id="18856-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="18856-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18856-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18856-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_OperatingSystemAutochkSetting : CIM_ElementSetting
{
  Win32_OperatingSystem REF Element;
  Win32_AutochkSetting  REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="18856-107">Membros</span><span class="sxs-lookup"><span data-stu-id="18856-107">Members</span></span>

<span data-ttu-id="18856-108">A classe **Win32 \_ OperatingSystemAutochkSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="18856-108">The **Win32\_OperatingSystemAutochkSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="18856-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="18856-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18856-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="18856-110">Properties</span></span>

<span data-ttu-id="18856-111">A classe **Win32 \_ OperatingSystemAutochkSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="18856-111">The **Win32\_OperatingSystemAutochkSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18856-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="18856-112">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18856-113">Tipo de dados: sistema **\_ operacional Win32**</span><span class="sxs-lookup"><span data-stu-id="18856-113">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="18856-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18856-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18856-115">Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) ("element"), [**Key**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="18856-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="18856-116">TBD</span><span class="sxs-lookup"><span data-stu-id="18856-116">TBD</span></span>

</dd> <dt>

<span data-ttu-id="18856-117">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="18856-117">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18856-118">Tipo de dados: **Win32 \_ AutochkSetting**</span><span class="sxs-lookup"><span data-stu-id="18856-118">Data type: **Win32\_AutochkSetting**</span></span>
</dt> <dt>

<span data-ttu-id="18856-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18856-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18856-120">Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) ("Setting"), [**Key**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="18856-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="18856-121">TBD</span><span class="sxs-lookup"><span data-stu-id="18856-121">TBD</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18856-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18856-122">Requirements</span></span>



| <span data-ttu-id="18856-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="18856-123">Requirement</span></span> | <span data-ttu-id="18856-124">Valor</span><span class="sxs-lookup"><span data-stu-id="18856-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18856-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18856-125">Minimum supported client</span></span><br/> | <span data-ttu-id="18856-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18856-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18856-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18856-127">Minimum supported server</span></span><br/> | <span data-ttu-id="18856-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18856-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18856-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="18856-129">Namespace</span></span><br/>                | <span data-ttu-id="18856-130">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="18856-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="18856-131">MOF</span><span class="sxs-lookup"><span data-stu-id="18856-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18856-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18856-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="18856-133">DLL</span><span class="sxs-lookup"><span data-stu-id="18856-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18856-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18856-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18856-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="18856-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18856-136">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="18856-136">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

 
