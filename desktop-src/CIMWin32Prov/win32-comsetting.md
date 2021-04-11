---
description: A \_ classe WMI abstrata de configuração do Win32 representa as configurações associadas a um componente de Component Object Model (com) ou a um aplicativo com.
ms.assetid: e8cdbee8-41ab-4aff-b17b-707667138411
ms.tgt_platform: multiple
title: Classe Win32_COMSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMSetting
- Win32_COMSetting.Caption
- Win32_COMSetting.Description
- Win32_COMSetting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5ec7932117d1ff0bc058d2b9a131f77ff9e040bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163953"
---
# <a name="win32_comsetting-class"></a><span data-ttu-id="03b68-103">Classe de configuração do Win32 \_</span><span class="sxs-lookup"><span data-stu-id="03b68-103">Win32\_COMSetting class</span></span>

<span data-ttu-id="03b68-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstrata de **\_ configuração do Win32** representa as configurações associadas a um componente de Component Object Model (com) ou a um aplicativo com.</span><span class="sxs-lookup"><span data-stu-id="03b68-104">The **Win32\_COMSetting** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings associated with a Component Object Model (COM) component or COM application.</span></span>

<span data-ttu-id="03b68-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="03b68-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="03b68-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="03b68-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="03b68-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03b68-107">Syntax</span></span>

``` syntax
[abstract, UUID("{E5D8A560-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a><span data-ttu-id="03b68-108">Membros</span><span class="sxs-lookup"><span data-stu-id="03b68-108">Members</span></span>

<span data-ttu-id="03b68-109">A classe de **\_ configuração do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="03b68-109">The **Win32\_COMSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="03b68-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="03b68-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03b68-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="03b68-111">Properties</span></span>

<span data-ttu-id="03b68-112">A classe de **\_ configuração do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="03b68-112">The **Win32\_COMSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03b68-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="03b68-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b68-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03b68-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03b68-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03b68-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03b68-116">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="03b68-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="03b68-117">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="03b68-117">Short textual description of the current object.</span></span>

<span data-ttu-id="03b68-118">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="03b68-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="03b68-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="03b68-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b68-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03b68-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03b68-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03b68-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03b68-122">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="03b68-122">Textual description of the current object.</span></span>

<span data-ttu-id="03b68-123">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="03b68-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="03b68-124">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="03b68-124">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b68-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03b68-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03b68-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03b68-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03b68-127">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="03b68-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03b68-128">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="03b68-128">Identifier by which the current object is known.</span></span>

<span data-ttu-id="03b68-129">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="03b68-129">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03b68-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="03b68-130">Remarks</span></span>

<span data-ttu-id="03b68-131">A classe de **\_ configuração do Win32** é derivada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="03b68-131">The **Win32\_COMSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03b68-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03b68-132">Requirements</span></span>



| <span data-ttu-id="03b68-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="03b68-133">Requirement</span></span> | <span data-ttu-id="03b68-134">Valor</span><span class="sxs-lookup"><span data-stu-id="03b68-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03b68-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03b68-135">Minimum supported client</span></span><br/> | <span data-ttu-id="03b68-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03b68-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03b68-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03b68-137">Minimum supported server</span></span><br/> | <span data-ttu-id="03b68-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03b68-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03b68-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="03b68-139">Namespace</span></span><br/>                | <span data-ttu-id="03b68-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="03b68-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03b68-141">MOF</span><span class="sxs-lookup"><span data-stu-id="03b68-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03b68-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03b68-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03b68-143">DLL</span><span class="sxs-lookup"><span data-stu-id="03b68-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03b68-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03b68-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03b68-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="03b68-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03b68-146">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="03b68-146">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="03b68-147">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="03b68-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

