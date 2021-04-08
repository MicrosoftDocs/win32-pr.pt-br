---
description: A \_ classe WMI COMClass abstrato do Win32 representa as propriedades de um componente de Component Object Model (com).
ms.assetid: 0e1d3930-1499-423a-96b0-89b2f05a1191
ms.tgt_platform: multiple
title: Classe Win32_COMClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMClass
- Win32_COMClass.Caption
- Win32_COMClass.Description
- Win32_COMClass.InstallDate
- Win32_COMClass.Name
- Win32_COMClass.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 685b0b1f869d159df12dfcf12f3a61fed8d76ad8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920496"
---
# <a name="win32_comclass-class"></a><span data-ttu-id="ca825-103">\_Classe COMClass Win32</span><span class="sxs-lookup"><span data-stu-id="ca825-103">Win32\_COMClass class</span></span>

<span data-ttu-id="ca825-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ COMClass** abstrato do Win32 representa as propriedades de um componente de Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="ca825-104">The **Win32\_COMClass** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a Component Object Model (COM) component.</span></span>

<span data-ttu-id="ca825-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ca825-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ca825-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="ca825-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca825-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca825-107">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED50-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMClass : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="ca825-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ca825-108">Members</span></span>

<span data-ttu-id="ca825-109">A **classe \_ COMClass do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ca825-109">The **Win32\_COMClass** class has these types of members:</span></span>

-   [<span data-ttu-id="ca825-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ca825-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca825-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ca825-111">Properties</span></span>

<span data-ttu-id="ca825-112">A **classe \_ COMClass do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ca825-112">The **Win32\_COMClass** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca825-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="ca825-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca825-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca825-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca825-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca825-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca825-116">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ca825-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ca825-117">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca825-117">A short textual description of the object.</span></span>

<span data-ttu-id="ca825-118">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca825-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca825-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ca825-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca825-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca825-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca825-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca825-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca825-122">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="ca825-122">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ca825-123">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca825-123">A textual description of the object.</span></span>

<span data-ttu-id="ca825-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca825-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca825-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ca825-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca825-126">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ca825-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ca825-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca825-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca825-128">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="ca825-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ca825-129">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="ca825-129">Indicates when the object was installed.</span></span> <span data-ttu-id="ca825-130">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="ca825-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ca825-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca825-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca825-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ca825-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca825-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca825-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca825-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca825-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca825-135">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="ca825-135">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ca825-136">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="ca825-136">Label by which the object is known.</span></span> <span data-ttu-id="ca825-137">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="ca825-137">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="ca825-138">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca825-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca825-139">**Status**</span><span class="sxs-lookup"><span data-stu-id="ca825-139">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca825-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca825-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca825-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca825-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca825-142">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="ca825-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ca825-143">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca825-143">String that indicates the current status of the object.</span></span> <span data-ttu-id="ca825-144">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="ca825-144">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="ca825-145">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="ca825-145">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ca825-146">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="ca825-146">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ca825-147">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="ca825-147">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ca825-148">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="ca825-148">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ca825-149">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="ca825-149">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ca825-150">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca825-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ca825-151">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ca825-151">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ca825-152">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ca825-152">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ca825-153">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="ca825-153">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ca825-154">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="ca825-154">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca825-155">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="ca825-155">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ca825-156">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ca825-156">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ca825-157">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="ca825-157">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ca825-158">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="ca825-158">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ca825-159">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="ca825-159">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ca825-160">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="ca825-160">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ca825-161">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="ca825-161">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ca825-162">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="ca825-162">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ca825-163">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="ca825-163">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="ca825-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ca825-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="ca825-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca825-165">Remarks</span></span>

<span data-ttu-id="ca825-166">A **classe \_ COMClass do Win32** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca825-166">The **Win32\_COMClass** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca825-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca825-167">Requirements</span></span>



| <span data-ttu-id="ca825-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca825-168">Requirement</span></span> | <span data-ttu-id="ca825-169">Valor</span><span class="sxs-lookup"><span data-stu-id="ca825-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca825-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca825-170">Minimum supported client</span></span><br/> | <span data-ttu-id="ca825-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca825-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca825-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca825-172">Minimum supported server</span></span><br/> | <span data-ttu-id="ca825-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca825-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca825-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca825-174">Namespace</span></span><br/>                | <span data-ttu-id="ca825-175">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ca825-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ca825-176">MOF</span><span class="sxs-lookup"><span data-stu-id="ca825-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca825-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca825-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca825-178">DLL</span><span class="sxs-lookup"><span data-stu-id="ca825-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca825-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca825-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca825-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca825-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca825-181">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="ca825-181">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="ca825-182">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca825-182">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

