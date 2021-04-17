---
description: A \_ classe WMI AutochkSetting do Win32 representa as configurações da operação de verificação de um disco.
ms.assetid: 637f4d5d-f2f0-4fe0-bbde-7804156979b7
ms.tgt_platform: multiple
title: Classe Win32_AutochkSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AutochkSetting
- Win32_AutochkSetting.Caption
- Win32_AutochkSetting.Description
- Win32_AutochkSetting.SettingID
- Win32_AutochkSetting.UserInputDelay
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea3da60cd4075aa2e36285d30950d3a105d59354
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762761"
---
# <a name="win32_autochksetting-class"></a><span data-ttu-id="abdd7-103">\_Classe Win32 AutochkSetting</span><span class="sxs-lookup"><span data-stu-id="abdd7-103">Win32\_AutochkSetting class</span></span>

<span data-ttu-id="abdd7-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ AutochkSetting do Win32** representa as configurações da operação de verificação de um disco.</span><span class="sxs-lookup"><span data-stu-id="abdd7-104">The **Win32\_AutochkSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings for the autocheck operation of a disk.</span></span>

<span data-ttu-id="abdd7-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="abdd7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="abdd7-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="abdd7-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="abdd7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abdd7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, AMENDMENT]
class Win32_AutochkSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 UserInputDelay;
};
```

## <a name="members"></a><span data-ttu-id="abdd7-108">Membros</span><span class="sxs-lookup"><span data-stu-id="abdd7-108">Members</span></span>

<span data-ttu-id="abdd7-109">A classe **Win32 \_ AutochkSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="abdd7-109">The **Win32\_AutochkSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="abdd7-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="abdd7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="abdd7-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="abdd7-111">Properties</span></span>

<span data-ttu-id="abdd7-112">A classe **Win32 \_ AutochkSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="abdd7-112">The **Win32\_AutochkSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abdd7-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="abdd7-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abdd7-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="abdd7-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abdd7-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="abdd7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abdd7-116">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="abdd7-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="abdd7-117">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="abdd7-117">Short textual description of the current object.</span></span>

<span data-ttu-id="abdd7-118">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="abdd7-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="abdd7-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="abdd7-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abdd7-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="abdd7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abdd7-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="abdd7-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abdd7-122">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="abdd7-122">Textual description of the current object.</span></span>

<span data-ttu-id="abdd7-123">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="abdd7-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="abdd7-124">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="abdd7-124">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abdd7-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="abdd7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abdd7-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="abdd7-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abdd7-127">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuraid"), [**chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="abdd7-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingId"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="abdd7-128">Uma ID que é usada como parte de uma chave para o objeto atual.</span><span class="sxs-lookup"><span data-stu-id="abdd7-128">An ID that is used as part of a key for the current object.</span></span>

</dd> <dt>

<span data-ttu-id="abdd7-129">**UserInputDelay**</span><span class="sxs-lookup"><span data-stu-id="abdd7-129">**UserInputDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abdd7-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="abdd7-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abdd7-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="abdd7-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="abdd7-132">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \| AutoChkTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Seconds")</span><span class="sxs-lookup"><span data-stu-id="abdd7-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM\\\\CurrentControlSet\\\\Control\\\\Session Manager \| AutoChkTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="abdd7-133">O atraso de entrada do usuário para AutoCheck.</span><span class="sxs-lookup"><span data-stu-id="abdd7-133">The user input delay for autocheck.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abdd7-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="abdd7-134">Remarks</span></span>

<span data-ttu-id="abdd7-135">A classe **Win32 \_ AutochkSetting** é derivada da [**\_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="abdd7-135">The **Win32\_AutochkSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abdd7-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abdd7-136">Requirements</span></span>



| <span data-ttu-id="abdd7-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="abdd7-137">Requirement</span></span> | <span data-ttu-id="abdd7-138">Valor</span><span class="sxs-lookup"><span data-stu-id="abdd7-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abdd7-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abdd7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="abdd7-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abdd7-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="abdd7-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abdd7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="abdd7-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abdd7-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="abdd7-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="abdd7-143">Namespace</span></span><br/>                | <span data-ttu-id="abdd7-144">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="abdd7-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="abdd7-145">MOF</span><span class="sxs-lookup"><span data-stu-id="abdd7-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abdd7-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abdd7-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="abdd7-147">DLL</span><span class="sxs-lookup"><span data-stu-id="abdd7-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abdd7-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abdd7-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abdd7-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="abdd7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abdd7-150">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="abdd7-150">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="abdd7-151">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="abdd7-151">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

