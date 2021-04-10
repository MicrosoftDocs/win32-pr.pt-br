---
description: A \_ classe WMI de aplicativo abstrato do Win32 representa um aplicativo de Component Object Model (com). Nesse contexto, um aplicativo COM é um agrupamento lógico de classes COM.
ms.assetid: a70939e2-5812-4ade-aa75-819c8d4b9173
ms.tgt_platform: multiple
title: Classe Win32_COMApplication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplication
- Win32_COMApplication.Caption
- Win32_COMApplication.Description
- Win32_COMApplication.InstallDate
- Win32_COMApplication.Name
- Win32_COMApplication.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 705f0f7b3c17ffca809de9a124748a74b5537f26
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010250"
---
# <a name="win32_comapplication-class"></a><span data-ttu-id="18da6-104">\_Classe de Comaplicativo Win32</span><span class="sxs-lookup"><span data-stu-id="18da6-104">Win32\_COMApplication class</span></span>

<span data-ttu-id="18da6-105">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ aplicativo** abstrato do Win32 representa um aplicativo de Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="18da6-105">The **Win32\_COMApplication** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a Component Object Model (COM) application.</span></span> <span data-ttu-id="18da6-106">Nesse contexto, um aplicativo COM é um agrupamento lógico de classes COM.</span><span class="sxs-lookup"><span data-stu-id="18da6-106">In this context, a COM application is a logical grouping of COM classes.</span></span>

<span data-ttu-id="18da6-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="18da6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="18da6-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="18da6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="18da6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18da6-109">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED4F-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="18da6-110">Membros</span><span class="sxs-lookup"><span data-stu-id="18da6-110">Members</span></span>

<span data-ttu-id="18da6-111">A classe do **\_ aplicativo Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="18da6-111">The **Win32\_COMApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="18da6-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="18da6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18da6-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="18da6-113">Properties</span></span>

<span data-ttu-id="18da6-114">A classe do **\_ aplicativo Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="18da6-114">The **Win32\_COMApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18da6-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="18da6-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18da6-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18da6-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18da6-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18da6-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18da6-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="18da6-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="18da6-119">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="18da6-119">A short textual description of the object.</span></span>

<span data-ttu-id="18da6-120">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18da6-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18da6-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="18da6-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18da6-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18da6-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18da6-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18da6-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18da6-124">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="18da6-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="18da6-125">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="18da6-125">A textual description of the object.</span></span>

<span data-ttu-id="18da6-126">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18da6-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18da6-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18da6-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18da6-128">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18da6-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18da6-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18da6-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18da6-130">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="18da6-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="18da6-131">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="18da6-131">Indicates when the object was installed.</span></span> <span data-ttu-id="18da6-132">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="18da6-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="18da6-133">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18da6-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18da6-134">**Nome**</span><span class="sxs-lookup"><span data-stu-id="18da6-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18da6-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18da6-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18da6-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18da6-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18da6-137">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="18da6-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="18da6-138">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="18da6-138">Label by which the object is known.</span></span> <span data-ttu-id="18da6-139">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="18da6-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="18da6-140">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18da6-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18da6-141">**Status**</span><span class="sxs-lookup"><span data-stu-id="18da6-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18da6-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18da6-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18da6-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18da6-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18da6-144">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="18da6-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="18da6-145">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="18da6-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="18da6-146">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="18da6-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="18da6-147">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="18da6-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="18da6-148">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="18da6-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="18da6-149">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="18da6-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="18da6-150">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="18da6-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="18da6-151">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="18da6-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="18da6-152">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18da6-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="18da6-153">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="18da6-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="18da6-154">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="18da6-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="18da6-155">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="18da6-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="18da6-156">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="18da6-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18da6-157">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="18da6-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="18da6-158">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="18da6-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="18da6-159">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="18da6-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="18da6-160">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="18da6-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="18da6-161">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="18da6-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="18da6-162">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="18da6-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="18da6-163">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="18da6-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="18da6-164">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="18da6-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="18da6-165">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="18da6-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="18da6-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="18da6-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="18da6-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="18da6-167">Remarks</span></span>

<span data-ttu-id="18da6-168">A classe do **\_ aplicativo Win32** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="18da6-168">The **Win32\_COMApplication** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18da6-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18da6-169">Requirements</span></span>



| <span data-ttu-id="18da6-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="18da6-170">Requirement</span></span> | <span data-ttu-id="18da6-171">Valor</span><span class="sxs-lookup"><span data-stu-id="18da6-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18da6-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18da6-172">Minimum supported client</span></span><br/> | <span data-ttu-id="18da6-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18da6-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18da6-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18da6-174">Minimum supported server</span></span><br/> | <span data-ttu-id="18da6-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18da6-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18da6-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="18da6-176">Namespace</span></span><br/>                | <span data-ttu-id="18da6-177">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="18da6-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="18da6-178">MOF</span><span class="sxs-lookup"><span data-stu-id="18da6-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18da6-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18da6-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="18da6-180">DLL</span><span class="sxs-lookup"><span data-stu-id="18da6-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18da6-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18da6-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18da6-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="18da6-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18da6-183">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="18da6-183">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="18da6-184">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18da6-184">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

