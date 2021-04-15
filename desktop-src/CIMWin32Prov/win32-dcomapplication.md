---
description: A \_ classe WMI DCOMApplication do Win32 representa as propriedades de um aplicativo DCOM.
ms.assetid: 11856834-6774-4262-bac4-e0265d4ba7e3
ms.tgt_platform: multiple
title: Classe Win32_DCOMApplication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplication
- Win32_DCOMApplication.Caption
- Win32_DCOMApplication.Description
- Win32_DCOMApplication.InstallDate
- Win32_DCOMApplication.Name
- Win32_DCOMApplication.Status
- Win32_DCOMApplication.AppID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a90ddaab9565557b5bbc83f52d0dce82447ab15d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753802"
---
# <a name="win32_dcomapplication-class"></a><span data-ttu-id="40b22-103">\_Classe Win32 DCOMApplication</span><span class="sxs-lookup"><span data-stu-id="40b22-103">Win32\_DCOMApplication class</span></span>

<span data-ttu-id="40b22-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DCOMApplication do Win32** representa as propriedades de um aplicativo DCOM.</span><span class="sxs-lookup"><span data-stu-id="40b22-104">The **Win32\_DCOMApplication** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a DCOM application.</span></span>

<span data-ttu-id="40b22-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="40b22-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="40b22-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="40b22-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="40b22-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40b22-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED52-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplication : Win32_COMApplication
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   AppID;
};
```

## <a name="members"></a><span data-ttu-id="40b22-108">Membros</span><span class="sxs-lookup"><span data-stu-id="40b22-108">Members</span></span>

<span data-ttu-id="40b22-109">A classe **Win32 \_ DCOMApplication** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="40b22-109">The **Win32\_DCOMApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="40b22-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="40b22-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40b22-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="40b22-111">Properties</span></span>

<span data-ttu-id="40b22-112">A classe **Win32 \_ DCOMApplication** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="40b22-112">The **Win32\_DCOMApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40b22-113">**AppID**</span><span class="sxs-lookup"><span data-stu-id="40b22-113">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b22-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40b22-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40b22-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40b22-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b22-116">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="40b22-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="40b22-117">GUID (identificador global exclusivo) para o aplicativo DCOM.</span><span class="sxs-lookup"><span data-stu-id="40b22-117">Globally unique identifier (GUID) for the DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="40b22-118">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="40b22-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b22-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40b22-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40b22-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40b22-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b22-121">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="40b22-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="40b22-122">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="40b22-122">A short textual description of the object.</span></span>

<span data-ttu-id="40b22-123">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40b22-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40b22-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="40b22-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b22-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40b22-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40b22-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40b22-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b22-127">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="40b22-127">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="40b22-128">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="40b22-128">A textual description of the object.</span></span>

<span data-ttu-id="40b22-129">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40b22-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40b22-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="40b22-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b22-131">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="40b22-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="40b22-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40b22-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b22-133">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="40b22-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="40b22-134">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="40b22-134">Indicates when the object was installed.</span></span> <span data-ttu-id="40b22-135">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="40b22-135">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="40b22-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40b22-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40b22-137">**Nome**</span><span class="sxs-lookup"><span data-stu-id="40b22-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b22-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40b22-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40b22-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40b22-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b22-140">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="40b22-140">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="40b22-141">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="40b22-141">Label by which the object is known.</span></span> <span data-ttu-id="40b22-142">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="40b22-142">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="40b22-143">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40b22-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40b22-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="40b22-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b22-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40b22-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40b22-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40b22-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b22-147">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="40b22-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="40b22-148">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="40b22-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="40b22-149">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="40b22-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="40b22-150">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="40b22-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="40b22-151">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="40b22-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="40b22-152">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="40b22-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="40b22-153">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="40b22-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="40b22-154">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="40b22-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="40b22-155">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40b22-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="40b22-156">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="40b22-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="40b22-157">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="40b22-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="40b22-158">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="40b22-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="40b22-159">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="40b22-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40b22-160">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="40b22-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="40b22-161">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="40b22-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="40b22-162">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="40b22-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="40b22-163">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="40b22-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="40b22-164">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="40b22-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="40b22-165">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="40b22-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="40b22-166">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="40b22-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="40b22-167">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="40b22-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="40b22-168">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="40b22-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="40b22-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="40b22-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="40b22-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="40b22-170">Remarks</span></span>

<span data-ttu-id="40b22-171">A classe **Win32 \_ DCOMApplication** é derivada do [**\_ aplicativo Win32**](win32-comapplication.md).</span><span class="sxs-lookup"><span data-stu-id="40b22-171">The **Win32\_DCOMApplication** class is derived from [**Win32\_COMApplication**](win32-comapplication.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40b22-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40b22-172">Requirements</span></span>



| <span data-ttu-id="40b22-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="40b22-173">Requirement</span></span> | <span data-ttu-id="40b22-174">Valor</span><span class="sxs-lookup"><span data-stu-id="40b22-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40b22-175">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40b22-175">Minimum supported client</span></span><br/> | <span data-ttu-id="40b22-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40b22-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40b22-177">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40b22-177">Minimum supported server</span></span><br/> | <span data-ttu-id="40b22-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40b22-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40b22-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="40b22-179">Namespace</span></span><br/>                | <span data-ttu-id="40b22-180">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="40b22-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="40b22-181">MOF</span><span class="sxs-lookup"><span data-stu-id="40b22-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40b22-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40b22-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="40b22-183">DLL</span><span class="sxs-lookup"><span data-stu-id="40b22-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40b22-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40b22-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40b22-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="40b22-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40b22-186">**\_Aplicativo Win32**</span><span class="sxs-lookup"><span data-stu-id="40b22-186">**Win32\_COMApplication**</span></span>](win32-comapplication.md)
</dt> <dt>

<span data-ttu-id="40b22-187">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="40b22-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

