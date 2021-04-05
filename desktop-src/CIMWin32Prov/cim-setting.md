---
description: A \_ classe de configuração CIM representa parâmetros operacionais e relacionados à configuração para um ou mais elementos do sistema gerenciado.
ms.assetid: 57c46b00-96c4-4df1-82ad-01f7b4f75ced
ms.tgt_platform: multiple
title: Classe CIM_Setting (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f1081bd93c95dfa90b6a4dfa6a87339e8e3172a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826340"
---
# <a name="cim_setting-class-cimwin32-wmi-providers"></a><span data-ttu-id="65789-103">Classe CIM_Setting (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="65789-103">CIM_Setting class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="65789-104">A classe de **\_ configuração CIM** representa parâmetros operacionais e relacionados à configuração para um ou mais elementos do sistema gerenciado.</span><span class="sxs-lookup"><span data-stu-id="65789-104">The **CIM\_Setting** class represents configuration-related and operational parameters for one or more managed system elements.</span></span> <span data-ttu-id="65789-105">Um elemento de sistema gerenciado pode ter vários objetos de configuração associados a ele.</span><span class="sxs-lookup"><span data-stu-id="65789-105">A managed system element can have multiple setting objects associated with it.</span></span> <span data-ttu-id="65789-106">Os valores operacionais atuais para os parâmetros de um elemento são refletidos pelas propriedades no próprio elemento ou por propriedades em suas associações.</span><span class="sxs-lookup"><span data-stu-id="65789-106">The current operational values for an element's parameters are reflected by properties in the element itself or by properties in its associations.</span></span> <span data-ttu-id="65789-107">Essas propriedades não precisam ter os mesmos valores presentes no objeto Setting.</span><span class="sxs-lookup"><span data-stu-id="65789-107">These properties do not have to be the same values present in the setting object.</span></span> <span data-ttu-id="65789-108">Por exemplo, um modem pode ter uma taxa de baud de configuração de 56 quilobytes por segundo, mas operando a 19,2 quilobytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="65789-108">For example, a modem may have a setting baud rate of 56 kilobytes per second, but be operating at 19.2 kilobytes per second.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65789-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="65789-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="65789-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="65789-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="65789-111">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="65789-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="65789-112">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="65789-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="65789-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65789-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C572-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a><span data-ttu-id="65789-114">Membros</span><span class="sxs-lookup"><span data-stu-id="65789-114">Members</span></span>

<span data-ttu-id="65789-115">A classe de **\_ configuração CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="65789-115">The **CIM\_Setting** class has these types of members:</span></span>

-   [<span data-ttu-id="65789-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="65789-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65789-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="65789-117">Properties</span></span>

<span data-ttu-id="65789-118">A classe de **\_ configuração CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="65789-118">The **CIM\_Setting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65789-119">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="65789-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65789-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="65789-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65789-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="65789-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65789-122">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="65789-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="65789-123">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="65789-123">Short textual description of the current object.</span></span>

</dd> <dt>

<span data-ttu-id="65789-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="65789-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65789-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="65789-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65789-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="65789-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65789-127">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="65789-127">Textual description of the current object.</span></span>

</dd> <dt>

<span data-ttu-id="65789-128">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="65789-128">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65789-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="65789-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65789-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="65789-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65789-131">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="65789-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="65789-132">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="65789-132">Identifier by which the current object is known.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65789-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="65789-133">Remarks</span></span>

<span data-ttu-id="65789-134">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="65789-134">WMI does not implement this class.</span></span> <span data-ttu-id="65789-135">Para classes WMI derivadas da **\_ configuração de CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="65789-135">For WMI classes derived from **CIM\_Setting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="65789-136">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="65789-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="65789-137">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="65789-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="65789-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65789-138">Requirements</span></span>



| <span data-ttu-id="65789-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="65789-139">Requirement</span></span> | <span data-ttu-id="65789-140">Valor</span><span class="sxs-lookup"><span data-stu-id="65789-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65789-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65789-141">Minimum supported client</span></span><br/> | <span data-ttu-id="65789-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65789-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65789-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65789-143">Minimum supported server</span></span><br/> | <span data-ttu-id="65789-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65789-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65789-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="65789-145">Namespace</span></span><br/>                | <span data-ttu-id="65789-146">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="65789-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="65789-147">MOF</span><span class="sxs-lookup"><span data-stu-id="65789-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65789-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65789-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="65789-149">DLL</span><span class="sxs-lookup"><span data-stu-id="65789-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65789-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65789-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

