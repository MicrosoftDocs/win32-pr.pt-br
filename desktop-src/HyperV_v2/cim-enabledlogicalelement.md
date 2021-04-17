---
description: Representa um elemento lógico que pode ser habilitado e desabilitado.
ms.assetid: 52eed77e-f3f1-4489-8eff-a8ebebd5e1a8
title: Classe CIM_EnabledLogicalElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElement
- CIM_EnabledLogicalElement.EnabledState
- CIM_EnabledLogicalElement.OtherEnabledState
- CIM_EnabledLogicalElement.RequestedState
- CIM_EnabledLogicalElement.EnabledDefault
- CIM_EnabledLogicalElement.TimeOfLastStateChange
- CIM_EnabledLogicalElement.AvailableRequestedStates
- CIM_EnabledLogicalElement.TransitioningToState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e2d7043653b219bc0d54ac7bee3393275dab673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760866"
---
# <a name="cim_enabledlogicalelement-class"></a><span data-ttu-id="e08cd-103">\_Classe CIM EnabledLogicalElement</span><span class="sxs-lookup"><span data-stu-id="e08cd-103">CIM\_EnabledLogicalElement class</span></span>

<span data-ttu-id="e08cd-104">Representa um elemento lógico que pode ser habilitado e desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e08cd-104">Represents a logical element that can be enabled and disabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="e08cd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e08cd-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_EnabledLogicalElement : CIM_LogicalElement
{
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
};
```

## <a name="members"></a><span data-ttu-id="e08cd-106">Membros</span><span class="sxs-lookup"><span data-stu-id="e08cd-106">Members</span></span>

<span data-ttu-id="e08cd-107">A classe **CIM \_ EnabledLogicalElement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e08cd-107">The **CIM\_EnabledLogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="e08cd-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e08cd-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="e08cd-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e08cd-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e08cd-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e08cd-110">Methods</span></span>

<span data-ttu-id="e08cd-111">A classe **CIM \_ EnabledLogicalElement** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e08cd-111">The **CIM\_EnabledLogicalElement** class has these methods.</span></span>



| <span data-ttu-id="e08cd-112">Método</span><span class="sxs-lookup"><span data-stu-id="e08cd-112">Method</span></span>                                                                     | <span data-ttu-id="e08cd-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="e08cd-113">Description</span></span>                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="e08cd-114">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e08cd-114">**RequestStateChange**</span></span>](cim-enabledlogicalelement-requeststatechange.md) | <span data-ttu-id="e08cd-115">Solicita que o estado do elemento seja alterado para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="e08cd-115">Requests that the state of the element be changed to the specified value.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e08cd-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e08cd-116">Properties</span></span>

<span data-ttu-id="e08cd-117">A classe **CIM \_ EnabledLogicalElement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e08cd-117">The **CIM\_EnabledLogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e08cd-118">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="e08cd-118">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08cd-119">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e08cd-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e08cd-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e08cd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e08cd-121">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**RequestStateChange**","[**CIM \_ EnabledLogicalElementCapabilities**](cim-enabledlogicalelementcapabilities.md).**RequestedStatesSupported**")</span><span class="sxs-lookup"><span data-stu-id="e08cd-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**RequestStateChange**", "[**CIM\_EnabledLogicalElementCapabilities**](cim-enabledlogicalelementcapabilities.md).**RequestedStatesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="e08cd-122">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="e08cd-122">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) method.</span></span>

<span data-ttu-id="e08cd-123">Os valores listados devem ser um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância **\_ EnabledLogicalElementCapabilities do CIM** associada.</span><span class="sxs-lookup"><span data-stu-id="e08cd-123">The listed values must be a subset of the values that are contained in the **RequestedStatesSupported** property of the associated **CIM\_EnabledLogicalElementCapabilities** instance.</span></span> <span data-ttu-id="e08cd-124">Essa propriedade será **nula** se a implementação não puder determinar o conjunto de valores possíveis para o estado atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="e08cd-124">This property is **NULL** if the implementation cannot determine the set of possible values for the current state of the element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e08cd-125">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="e08cd-125">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e08cd-126">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e08cd-126">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="e08cd-127">**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="e08cd-127">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="e08cd-128">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e08cd-128">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="e08cd-129">**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="e08cd-129">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="e08cd-130">**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="e08cd-130">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="e08cd-131">**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="e08cd-131">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="e08cd-132">**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="e08cd-132">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="e08cd-133">**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="e08cd-133">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e08cd-134">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e08cd-134">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e08cd-135">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="e08cd-135">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08cd-136">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e08cd-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e08cd-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e08cd-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e08cd-138">Indica a configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="e08cd-138">Indicates an administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e08cd-139">O valor padrão **habilitado** (2).</span><span class="sxs-lookup"><span data-stu-id="e08cd-139">The default value **Enabled** (2).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e08cd-140">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="e08cd-140">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e08cd-141">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e08cd-141">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e08cd-142">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="e08cd-142">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="e08cd-143">**Habilitado, mas offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e08cd-143">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Default"></span><span id="no_default"></span><span id="NO_DEFAULT"></span>

<span data-ttu-id="e08cd-144">**Nenhum padrão** (7)</span><span class="sxs-lookup"><span data-stu-id="e08cd-144">**No Default** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="e08cd-145">**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="e08cd-145">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e08cd-146">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e08cd-146">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e08cd-147">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e08cd-147">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e08cd-148">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e08cd-148">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08cd-149">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e08cd-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e08cd-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e08cd-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e08cd-151">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**OtherEnabledState**")</span><span class="sxs-lookup"><span data-stu-id="e08cd-151">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**OtherEnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="e08cd-152">Indica o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="e08cd-152">Indicates the enabled state of an element.</span></span> <span data-ttu-id="e08cd-153">Os valores possíveis incluem as transições entre Estados.</span><span class="sxs-lookup"><span data-stu-id="e08cd-153">Possible values include the transitions between states.</span></span> <span data-ttu-id="e08cd-154">Por exemplo, **desligar** (4) e **Iniciar** (10) são estados transitórios entre **habilitado** e **desabilitado**.</span><span class="sxs-lookup"><span data-stu-id="e08cd-154">For example, **Shutting Down** (4) and **Starting** (10) are transient states between **Enabled** and **Disabled**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e08cd-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e08cd-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e08cd-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e08cd-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e08cd-157"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="e08cd-157"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-158">O elemento é ou pode estar executando comandos, processará qualquer comando na fila e enfileirará novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="e08cd-158">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e08cd-159"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e08cd-159"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-160">o elemento não executará comandos e descartará as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="e08cd-160">the element will not execute commands and will drop any new requests.</span></span>

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="e08cd-161"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (4)</span><span class="sxs-lookup"><span data-stu-id="e08cd-161"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-162">O elemento está no processo de ir para um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e08cd-162">The element is in the process of going to a Disabled state.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e08cd-163"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="e08cd-163"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-164">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e08cd-164">The element does not support being enabled or disabled.</span></span>

</dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="e08cd-165"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitado, mas offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e08cd-165"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-166">O elemento pode estar concluindo comandos e removerá novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="e08cd-166">The element might be completing commands, and will drop any new requests.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e08cd-167"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (7)</span><span class="sxs-lookup"><span data-stu-id="e08cd-167"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-168">O elemento está em um estado de teste.</span><span class="sxs-lookup"><span data-stu-id="e08cd-168">The element is in a test state.</span></span>

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="e08cd-169"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Adiado** (8)</span><span class="sxs-lookup"><span data-stu-id="e08cd-169"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-170">O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.</span><span class="sxs-lookup"><span data-stu-id="e08cd-170">The element might be completing commands, but will queue any new requests.</span></span>

</dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="e08cd-171"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="e08cd-171"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-172">Se o elemento está habilitado, mas em um modo restrito.</span><span class="sxs-lookup"><span data-stu-id="e08cd-172">That the element is enabled but in a restricted mode.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e08cd-173"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (10)</span><span class="sxs-lookup"><span data-stu-id="e08cd-173"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-174">O elemento está no processo de ir para um estado habilitado.</span><span class="sxs-lookup"><span data-stu-id="e08cd-174">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="e08cd-175">Novas solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="e08cd-175">New requests are queued.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e08cd-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (11.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e08cd-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (11..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e08cd-177"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e08cd-177"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e08cd-178">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="e08cd-178">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08cd-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e08cd-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e08cd-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e08cd-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e08cd-181">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**Enabledstate**")</span><span class="sxs-lookup"><span data-stu-id="e08cd-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="e08cd-182">Descreve o estado do elemento quando o valor da propriedade **enabledstate** é **outro**.</span><span class="sxs-lookup"><span data-stu-id="e08cd-182">Describes the state of the element when the value of the **EnabledState** property is **Other**.</span></span> <span data-ttu-id="e08cd-183">Essa propriedade deve ser definida como **NULL** quando **enabledstate** não for **outra**.</span><span class="sxs-lookup"><span data-stu-id="e08cd-183">This property must be set to **NULL** when **EnabledState** is not **Other**.</span></span>

</dd> <dt>

<span data-ttu-id="e08cd-184">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e08cd-184">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08cd-185">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e08cd-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e08cd-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e08cd-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e08cd-187">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**Enabledstate**")</span><span class="sxs-lookup"><span data-stu-id="e08cd-187">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="e08cd-188">Indica o último estado solicitado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="e08cd-188">Indicates the last requested state for the element.</span></span> <span data-ttu-id="e08cd-189">O estado atual é indicado pela propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="e08cd-189">The current state is indicated by the **EnabledState** property.</span></span> <span data-ttu-id="e08cd-190">Essa propriedade permite que você compare os últimos Estados solicitados e atuais.</span><span class="sxs-lookup"><span data-stu-id="e08cd-190">This property enables you to compare the last requested and current states.</span></span>

> [!Note]  
> <span data-ttu-id="e08cd-191">Quando o valor da propriedade **enabledstate** não é **aplicável**, essa propriedade não tem significado.</span><span class="sxs-lookup"><span data-stu-id="e08cd-191">When the value of the **EnabledState** property is **Not Applicable**, this property has no meaning.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e08cd-192"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e08cd-192"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-193">O último estado solicitado para o elemento é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e08cd-193">The last requested state for the element is unknown.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e08cd-194"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="e08cd-194"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e08cd-195"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e08cd-195"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-196">Solicita uma desabilitação imediata do elemento, de modo que ele não executará ou aceitará comandos ou solicitações de processamento.</span><span class="sxs-lookup"><span data-stu-id="e08cd-196">Requests an immediate disabling of the element, such that it will not execute or accept any commands or processing requests.</span></span>

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="e08cd-197"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="e08cd-197"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-198">Solicita uma transição ordenada para o estado desabilitado e pode envolver a remoção de energia, para apagar completamente qualquer estado existente.</span><span class="sxs-lookup"><span data-stu-id="e08cd-198">Requests an orderly transition to the Disabled state, and might involve removing power, to completely erase any existing state.</span></span>

</dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="e08cd-199"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**Nenhuma alteração** (5)</span><span class="sxs-lookup"><span data-stu-id="e08cd-199"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**No Change** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-200">Preterido em vez de indicar que o último estado solicitado é "desconhecido" (0).</span><span class="sxs-lookup"><span data-stu-id="e08cd-200">Deprecated in lieu of indicating the last requested state is "Unknown" (0).</span></span> <span data-ttu-id="e08cd-201">Se o último estado solicitado ou desejado for desconhecido, **solicitstate** deverá ter o valor "Unknown" (0), mas poderá ter o valor "no Change" (5).</span><span class="sxs-lookup"><span data-stu-id="e08cd-201">If the last requested or desired state is unknown, **RequestedState** should have the value "Unknown" (0), but may have the value "No Change" (5).</span></span>

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="e08cd-202"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e08cd-202"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-203">O elemento foi solicitado a fazer a transição para o habilitado, mas Offlinestate **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="e08cd-203">The element has been requested to transition to the Enabled but Offline **EnabledState**.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="e08cd-204"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="e08cd-204"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="e08cd-205"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Adiado** (8)</span><span class="sxs-lookup"><span data-stu-id="e08cd-205"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="e08cd-206"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="e08cd-206"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="e08cd-207"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="e08cd-207"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-208">Refere-se a fazer um "desligamento" e, em seguida, mover para um estado "habilitado".</span><span class="sxs-lookup"><span data-stu-id="e08cd-208">Refers to doing a "Shut Down" and then moving to an "Enabled" state.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="e08cd-209"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="e08cd-209"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>


</dt> <dd>

<span data-ttu-id="e08cd-210">Indica que o elemento é primeiro "desabilitado" e, em seguida, "habilitado".</span><span class="sxs-lookup"><span data-stu-id="e08cd-210">Indicates that the element is first "Disabled" and then "Enabled".</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e08cd-211"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (12)</span><span class="sxs-lookup"><span data-stu-id="e08cd-211"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e08cd-212"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e08cd-212"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e08cd-213"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e08cd-213"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e08cd-214">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="e08cd-214">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08cd-215">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e08cd-215">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e08cd-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e08cd-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e08cd-217">Indica quando o estado da última alteração do elemento.</span><span class="sxs-lookup"><span data-stu-id="e08cd-217">Indicates when the element last changed state.</span></span> <span data-ttu-id="e08cd-218">Se o estado do elemento não tiver sido alterado e essa propriedade for populada, ela deverá ser definida como um valor de intervalo de zero.</span><span class="sxs-lookup"><span data-stu-id="e08cd-218">If the state of the element has not changed and this property is populated, then it must be set to a zero interval value.</span></span> <span data-ttu-id="e08cd-219">Se uma alteração de estado foi solicitada, mas foi rejeitada ou ainda não foi processada, a propriedade não deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="e08cd-219">If a state change was requested, but was rejected or is not yet processed, the property must not be updated.</span></span>

</dd> <dt>

<span data-ttu-id="e08cd-220">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="e08cd-220">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08cd-221">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e08cd-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e08cd-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e08cd-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e08cd-223">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**RequestStateChange**","**CIM \_ EnabledLogicalElement**.**Requestedstate**","**CIM \_ EnabledLogicalElement**.**Enabledstate**")</span><span class="sxs-lookup"><span data-stu-id="e08cd-223">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**RequestStateChange**", "**CIM\_EnabledLogicalElement**.**RequestedState**", "**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="e08cd-224">Indica o estado de destino para o qual a instância está sendo alterada.</span><span class="sxs-lookup"><span data-stu-id="e08cd-224">Indicates the target state to which the instance is changing.</span></span>

<span data-ttu-id="e08cd-225">Um valor **sem alteração** indica que nenhuma transição está em andamento.</span><span class="sxs-lookup"><span data-stu-id="e08cd-225">A value of **No Change** indicates that no transition is in progress.</span></span> <span data-ttu-id="e08cd-226">Um valor **não aplicável** indica que a implementação não relata transições contínuas.</span><span class="sxs-lookup"><span data-stu-id="e08cd-226">A value of **Not Applicable** indicates that the implementation does not report ongoing transitions.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e08cd-227">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e08cd-227">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e08cd-228">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="e08cd-228">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e08cd-229">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e08cd-229">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="e08cd-230">**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="e08cd-230">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="e08cd-231">**Nenhuma alteração** (5)</span><span class="sxs-lookup"><span data-stu-id="e08cd-231">**No Change** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="e08cd-232">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e08cd-232">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="e08cd-233">**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="e08cd-233">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="e08cd-234">**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="e08cd-234">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="e08cd-235">**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="e08cd-235">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="e08cd-236">**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="e08cd-236">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="e08cd-237">**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="e08cd-237">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e08cd-238">**Não aplicável** (12)</span><span class="sxs-lookup"><span data-stu-id="e08cd-238">**Not Applicable** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e08cd-239">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e08cd-239">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="e08cd-240"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e08cd-240"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e08cd-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e08cd-241">Requirements</span></span>



| <span data-ttu-id="e08cd-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="e08cd-242">Requirement</span></span> | <span data-ttu-id="e08cd-243">Valor</span><span class="sxs-lookup"><span data-stu-id="e08cd-243">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e08cd-244">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e08cd-244">Minimum supported client</span></span><br/> | <span data-ttu-id="e08cd-245">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e08cd-245">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e08cd-246">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e08cd-246">Minimum supported server</span></span><br/> | <span data-ttu-id="e08cd-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e08cd-247">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e08cd-248">Namespace</span><span class="sxs-lookup"><span data-stu-id="e08cd-248">Namespace</span></span><br/>                | <span data-ttu-id="e08cd-249">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e08cd-249">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e08cd-250">MOF</span><span class="sxs-lookup"><span data-stu-id="e08cd-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e08cd-251"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e08cd-251"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e08cd-252">DLL</span><span class="sxs-lookup"><span data-stu-id="e08cd-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e08cd-253"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e08cd-253"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e08cd-254">Confira também</span><span class="sxs-lookup"><span data-stu-id="e08cd-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e08cd-255">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="e08cd-255">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

