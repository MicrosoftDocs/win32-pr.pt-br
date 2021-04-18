---
description: A \_ classe WMI ClassicCOMClass do Win32 representa as propriedades de um componente com.
ms.assetid: 49b10991-cc2e-40a1-bbb3-a816a52d1a91
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClass
- Win32_ClassicCOMClass.Caption
- Win32_ClassicCOMClass.Description
- Win32_ClassicCOMClass.InstallDate
- Win32_ClassicCOMClass.Status
- Win32_ClassicCOMClass.ComponentId
- Win32_ClassicCOMClass.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 92299b46c3942b2a8a3304da3b1c41b8ec985e6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756432"
---
# <a name="win32_classiccomclass-class"></a><span data-ttu-id="55936-103">\_Classe Win32 ClassicCOMClass</span><span class="sxs-lookup"><span data-stu-id="55936-103">Win32\_ClassicCOMClass class</span></span>

<span data-ttu-id="55936-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ClassicCOMClass do Win32** representa as propriedades de um componente com.</span><span class="sxs-lookup"><span data-stu-id="55936-104">The **Win32\_ClassicCOMClass** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a COM component.</span></span>

<span data-ttu-id="55936-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="55936-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="55936-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="55936-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="55936-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55936-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED53-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClass : Win32_COMClass
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   ComponentId;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="55936-108">Membros</span><span class="sxs-lookup"><span data-stu-id="55936-108">Members</span></span>

<span data-ttu-id="55936-109">A classe **Win32 \_ ClassicCOMClass** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="55936-109">The **Win32\_ClassicCOMClass** class has these types of members:</span></span>

-   [<span data-ttu-id="55936-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="55936-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55936-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="55936-111">Properties</span></span>

<span data-ttu-id="55936-112">A classe **Win32 \_ ClassicCOMClass** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="55936-112">The **Win32\_ClassicCOMClass** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55936-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="55936-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55936-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55936-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55936-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55936-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55936-116">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="55936-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="55936-117">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="55936-117">A short textual description of the object.</span></span>

<span data-ttu-id="55936-118">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55936-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55936-119">**ComponentId**</span><span class="sxs-lookup"><span data-stu-id="55936-119">**ComponentId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55936-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55936-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55936-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55936-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55936-122">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="55936-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="55936-123">GUID (identificador global exclusivo) dessa classe COM.</span><span class="sxs-lookup"><span data-stu-id="55936-123">Globally unique identifier (GUID) of this COM class.</span></span>

</dd> <dt>

<span data-ttu-id="55936-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="55936-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55936-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55936-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55936-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55936-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55936-127">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="55936-127">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="55936-128">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="55936-128">A textual description of the object.</span></span>

<span data-ttu-id="55936-129">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55936-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55936-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="55936-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55936-131">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="55936-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="55936-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55936-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55936-133">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="55936-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="55936-134">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="55936-134">Indicates when the object was installed.</span></span> <span data-ttu-id="55936-135">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="55936-135">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="55936-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55936-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55936-137">**Nome**</span><span class="sxs-lookup"><span data-stu-id="55936-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55936-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55936-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55936-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55936-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55936-140">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="55936-140">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="55936-141">A propriedade Name contém o nome legível para a classe COM.</span><span class="sxs-lookup"><span data-stu-id="55936-141">The Name property contains the human-readable name for the COM class.</span></span>

</dd> <dt>

<span data-ttu-id="55936-142">**Status**</span><span class="sxs-lookup"><span data-stu-id="55936-142">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55936-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55936-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55936-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55936-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55936-145">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="55936-145">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="55936-146">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="55936-146">String that indicates the current status of the object.</span></span> <span data-ttu-id="55936-147">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="55936-147">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="55936-148">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="55936-148">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="55936-149">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="55936-149">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="55936-150">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="55936-150">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="55936-151">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="55936-151">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="55936-152">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="55936-152">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="55936-153">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55936-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="55936-154">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="55936-154">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="55936-155">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="55936-155">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="55936-156">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="55936-156">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="55936-157">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="55936-157">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55936-158">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="55936-158">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="55936-159">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="55936-159">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="55936-160">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="55936-160">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="55936-161">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="55936-161">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="55936-162">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="55936-162">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="55936-163">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="55936-163">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="55936-164">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="55936-164">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="55936-165">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="55936-165">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="55936-166">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="55936-166">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="55936-167"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="55936-167"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="55936-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="55936-168">Remarks</span></span>

<span data-ttu-id="55936-169">A classe **Win32 \_ ClassicCOMClass** é derivada de [**Win32 \_ COMClass**](win32-comclass.md).</span><span class="sxs-lookup"><span data-stu-id="55936-169">The **Win32\_ClassicCOMClass** class is derived from [**Win32\_COMClass**](win32-comclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55936-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55936-170">Requirements</span></span>



| <span data-ttu-id="55936-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="55936-171">Requirement</span></span> | <span data-ttu-id="55936-172">Valor</span><span class="sxs-lookup"><span data-stu-id="55936-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55936-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55936-173">Minimum supported client</span></span><br/> | <span data-ttu-id="55936-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55936-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55936-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55936-175">Minimum supported server</span></span><br/> | <span data-ttu-id="55936-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55936-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55936-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="55936-177">Namespace</span></span><br/>                | <span data-ttu-id="55936-178">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="55936-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55936-179">MOF</span><span class="sxs-lookup"><span data-stu-id="55936-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55936-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55936-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55936-181">DLL</span><span class="sxs-lookup"><span data-stu-id="55936-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55936-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55936-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55936-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="55936-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55936-184">**\_COMClass Win32**</span><span class="sxs-lookup"><span data-stu-id="55936-184">**Win32\_COMClass**</span></span>](win32-comclass.md)
</dt> <dt>

<span data-ttu-id="55936-185">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="55936-185">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

