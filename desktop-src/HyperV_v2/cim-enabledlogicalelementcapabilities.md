---
description: Descreve as restrições nas propriedades de um \_ objeto CIM EnabledLogicalElement associado.
ms.assetid: debce40c-9a0e-43a7-88fa-9336afd52e17
title: Classe CIM_EnabledLogicalElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElementCapabilities
- CIM_EnabledLogicalElementCapabilities.ElementNameEditSupported
- CIM_EnabledLogicalElementCapabilities.MaxElementNameLen
- CIM_EnabledLogicalElementCapabilities.RequestedStatesSupported
- CIM_EnabledLogicalElementCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35f400643e01821667c999342603fd402a3ae419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753297"
---
# <a name="cim_enabledlogicalelementcapabilities-class"></a><span data-ttu-id="92c2e-103">\_Classe CIM EnabledLogicalElementCapabilities</span><span class="sxs-lookup"><span data-stu-id="92c2e-103">CIM\_EnabledLogicalElementCapabilities class</span></span>

<span data-ttu-id="92c2e-104">Descreve as restrições nas propriedades de um objeto [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md) associado.</span><span class="sxs-lookup"><span data-stu-id="92c2e-104">Describes the restrictions on the properties of an associated [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c2e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92c2e-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_EnabledLogicalElementCapabilities : CIM_Capabilities
{
  boolean ElementNameEditSupported;
  uint16  MaxElementNameLen;
  uint16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a><span data-ttu-id="92c2e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="92c2e-106">Members</span></span>

<span data-ttu-id="92c2e-107">A classe **CIM \_ EnabledLogicalElementCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="92c2e-107">The **CIM\_EnabledLogicalElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="92c2e-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="92c2e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92c2e-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="92c2e-109">Properties</span></span>

<span data-ttu-id="92c2e-110">A classe **CIM \_ EnabledLogicalElementCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="92c2e-110">The **CIM\_EnabledLogicalElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92c2e-111">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="92c2e-111">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c2e-112">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="92c2e-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92c2e-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92c2e-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c2e-114">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI. INCITS-T11 \| SWAPI \_ unidade \_ config \_ Caps \_ T \| editname "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ managedelement**](cim-managedelement.md).**ElementName**")</span><span class="sxs-lookup"><span data-stu-id="92c2e-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI.INCITS-T11\|SWAPI\_UNIT\_CONFIG\_CAPS\_T\|EditName"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ManagedElement**](cim-managedelement.md).**ElementName**")</span></span>
</dt> </dl>

<span data-ttu-id="92c2e-115">**true** se a propriedade **ElementName** do elemento lógico habilitado puder ser modificada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="92c2e-115">**true** if the **ElementName** property of the enabled logical element can be modified; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="92c2e-116">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="92c2e-116">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c2e-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="92c2e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c2e-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92c2e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c2e-119">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElementCapabilities**.**MaxElementNameLen**")</span><span class="sxs-lookup"><span data-stu-id="92c2e-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElementCapabilities**.**MaxElementNameLen**")</span></span>
</dt> </dl>

<span data-ttu-id="92c2e-120">Uma expressão regular que indica as restrições na propriedade **ElementName** do elemento lógico Enable.</span><span class="sxs-lookup"><span data-stu-id="92c2e-120">A regular expression that indicates the restrictions on the **ElementName** property of the enable logical element.</span></span> <span data-ttu-id="92c2e-121">Confira *ABNF padrão da DMTF com o guia de uso da especificação do perfil de gerenciamento*, o Apêndice C para a sintaxe permitida.</span><span class="sxs-lookup"><span data-stu-id="92c2e-121">See *DMTF standard ABNF with the Management Profile Specification Usage Guide*, appendix C for the permitted syntax.</span></span>

> [!Note]  
> <span data-ttu-id="92c2e-122">Se essa propriedade e a propriedade **ElementNameMask** do elemento lógico Enable descreverem o comprimento máximo de **ElementName**, o valor menor será usado.</span><span class="sxs-lookup"><span data-stu-id="92c2e-122">If this property and the **ElementNameMask** property of the enable logical element describe the maximum length of **ElementName**, the smaller value is used.</span></span>

 

</dd> <dt>

<span data-ttu-id="92c2e-123">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="92c2e-123">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c2e-124">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92c2e-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92c2e-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92c2e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c2e-126">Qualificadores: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI. INCITS-T11 \| \_ configi da unidade de permuta \_ \_ Caps \_ T \| MaxNameChars "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ FCSwitchCapabilities. ElementNameEditSupported ","**CIM \_ EnabledLogicalElementCapabilities**.**ElementNameMask**")</span><span class="sxs-lookup"><span data-stu-id="92c2e-126">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI.INCITS-T11\|SWAPI\_UNIT\_CONFIG\_CAPS\_T\|MaxNameChars"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_FCSwitchCapabilities.ElementNameEditSupported", "**CIM\_EnabledLogicalElementCapabilities**.**ElementNameMask**")</span></span>
</dt> </dl>

<span data-ttu-id="92c2e-127">O comprimento máximo com suporte da propriedade **ElementName** do elemento lógico habilitado.</span><span class="sxs-lookup"><span data-stu-id="92c2e-127">The maximum supported length of the **ElementName** property of the enabled logical element.</span></span>

</dd> <dt>

<span data-ttu-id="92c2e-128">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="92c2e-128">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c2e-129">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92c2e-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="92c2e-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92c2e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c2e-131">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**")</span><span class="sxs-lookup"><span data-stu-id="92c2e-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**")</span></span>
</dt> </dl>

<span data-ttu-id="92c2e-132">Os possíveis Estados que podem ser solicitados no elemento lógico habilitado pelo método [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="92c2e-132">The possible states that can be requested on the enabled logical element by the [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) method.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="92c2e-133">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="92c2e-133">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="92c2e-134">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="92c2e-134">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="92c2e-135">**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="92c2e-135">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="92c2e-136">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="92c2e-136">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="92c2e-137">**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="92c2e-137">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="92c2e-138">**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="92c2e-138">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="92c2e-139">**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="92c2e-139">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="92c2e-140">**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="92c2e-140">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="92c2e-141">**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="92c2e-141">**Reset** (11)</span></span>


<span data-ttu-id="92c2e-142"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="92c2e-142"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="92c2e-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92c2e-143">Requirements</span></span>



| <span data-ttu-id="92c2e-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="92c2e-144">Requirement</span></span> | <span data-ttu-id="92c2e-145">Valor</span><span class="sxs-lookup"><span data-stu-id="92c2e-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92c2e-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92c2e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="92c2e-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="92c2e-147">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="92c2e-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92c2e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="92c2e-149">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92c2e-149">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="92c2e-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="92c2e-150">Namespace</span></span><br/>                | <span data-ttu-id="92c2e-151">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="92c2e-151">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="92c2e-152">MOF</span><span class="sxs-lookup"><span data-stu-id="92c2e-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92c2e-153"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92c2e-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="92c2e-154">DLL</span><span class="sxs-lookup"><span data-stu-id="92c2e-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92c2e-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="92c2e-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="92c2e-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="92c2e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c2e-157">**Recursos de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="92c2e-157">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

