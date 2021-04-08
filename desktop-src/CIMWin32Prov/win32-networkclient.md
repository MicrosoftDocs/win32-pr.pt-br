---
description: A \_ classe WMI vinculado do Win32 representa um cliente de rede em um sistema Windows. Qualquer sistema de computador na rede com uma relação de cliente com o sistema é um descendente (ou membro) dessa classe.
ms.assetid: f0cc2cef-be23-42f4-a592-2c292aa5085f
ms.tgt_platform: multiple
title: Classe Win32_NetworkClient
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkClient
- Win32_NetworkClient.Caption
- Win32_NetworkClient.Description
- Win32_NetworkClient.InstallDate
- Win32_NetworkClient.Status
- Win32_NetworkClient.Manufacturer
- Win32_NetworkClient.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54579073b3974a6c4954ef95b1da3fe2e9fd8348
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920525"
---
# <a name="win32_networkclient-class"></a><span data-ttu-id="09526-104">\_Classe Win32 vinculado</span><span class="sxs-lookup"><span data-stu-id="09526-104">Win32\_NetworkClient class</span></span>

<span data-ttu-id="09526-105">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ vinculado do Win32** representa um cliente de rede em um sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="09526-105">The **Win32\_NetworkClient** [WMI class](../wmisdk/retrieving-a-class.md) represents a network client on a Windows system.</span></span> <span data-ttu-id="09526-106">Qualquer sistema de computador na rede com uma relação de cliente com o sistema é um descendente (ou membro) dessa classe.</span><span class="sxs-lookup"><span data-stu-id="09526-106">Any computer system on the network with a client relationship to the system is a descendant (or member) of this class.</span></span>

<span data-ttu-id="09526-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="09526-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="09526-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="09526-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="09526-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09526-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkClient : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Manufacturer;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="09526-110">Membros</span><span class="sxs-lookup"><span data-stu-id="09526-110">Members</span></span>

<span data-ttu-id="09526-111">A classe **Win32 \_ vinculado** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="09526-111">The **Win32\_NetworkClient** class has these types of members:</span></span>

-   [<span data-ttu-id="09526-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="09526-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09526-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="09526-113">Properties</span></span>

<span data-ttu-id="09526-114">A classe **Win32 \_ vinculado** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="09526-114">The **Win32\_NetworkClient** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09526-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="09526-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09526-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09526-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09526-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09526-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09526-118">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="09526-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="09526-119">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="09526-119">A short textual description of the object.</span></span>

<span data-ttu-id="09526-120">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="09526-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09526-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="09526-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09526-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09526-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09526-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09526-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09526-124">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="09526-124">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="09526-125">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="09526-125">A textual description of the object.</span></span>

<span data-ttu-id="09526-126">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="09526-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09526-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="09526-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09526-128">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="09526-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="09526-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09526-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09526-130">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="09526-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="09526-131">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="09526-131">Indicates when the object was installed.</span></span> <span data-ttu-id="09526-132">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="09526-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="09526-133">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="09526-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09526-134">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="09526-134">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09526-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09526-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09526-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09526-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09526-137">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ LanmanWorkstation \\ \\ NetworkProvider \| manufatura")</span><span class="sxs-lookup"><span data-stu-id="09526-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanWorkstation\\\\NetworkProvider\|Mfg")</span></span>
</dt> </dl>

<span data-ttu-id="09526-138">Nome do fabricante do cliente de rede em execução no sistema de computador que executa o Windows.</span><span class="sxs-lookup"><span data-stu-id="09526-138">Name of the manufacturer of the network client running on the computer system running Windows.</span></span>

<span data-ttu-id="09526-139">Exemplo: "Microsoft Corporation"</span><span class="sxs-lookup"><span data-stu-id="09526-139">Example: "Microsoft Corporation"</span></span>

</dd> <dt>

<span data-ttu-id="09526-140">**Nome**</span><span class="sxs-lookup"><span data-stu-id="09526-140">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09526-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09526-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09526-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09526-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09526-143">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("nome"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Serviços \\ \\ LanmanWorkstation \\ \\ NetworkProvider \| nome")</span><span class="sxs-lookup"><span data-stu-id="09526-143">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanWorkstation\\\\NetworkProvider\|Name")</span></span>
</dt> </dl>

<span data-ttu-id="09526-144">Nome de rede do cliente de rede em execução no sistema de computador que executa o Windows.</span><span class="sxs-lookup"><span data-stu-id="09526-144">Network name of the network client running on the computer system running Windows.</span></span>

<span data-ttu-id="09526-145">Exemplo: "rede do Microsoft Windows"</span><span class="sxs-lookup"><span data-stu-id="09526-145">Example: "Microsoft Windows Network"</span></span>

</dd> <dt>

<span data-ttu-id="09526-146">**Status**</span><span class="sxs-lookup"><span data-stu-id="09526-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09526-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09526-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09526-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09526-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09526-149">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="09526-149">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="09526-150">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="09526-150">String that indicates the current status of the object.</span></span> <span data-ttu-id="09526-151">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="09526-151">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="09526-152">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="09526-152">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="09526-153">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="09526-153">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="09526-154">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="09526-154">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="09526-155">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="09526-155">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="09526-156">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="09526-156">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="09526-157">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="09526-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="09526-158">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="09526-158">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="09526-159">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="09526-159">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="09526-160">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="09526-160">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="09526-161">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="09526-161">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="09526-162">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="09526-162">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="09526-163">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="09526-163">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="09526-164">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="09526-164">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="09526-165">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="09526-165">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="09526-166">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="09526-166">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="09526-167">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="09526-167">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="09526-168">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="09526-168">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="09526-169">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="09526-169">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="09526-170">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="09526-170">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="09526-171"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="09526-171"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="09526-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="09526-172">Remarks</span></span>

<span data-ttu-id="09526-173">A classe **Win32 \_ vinculado** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="09526-173">The **Win32\_NetworkClient** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="09526-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09526-174">Requirements</span></span>



| <span data-ttu-id="09526-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="09526-175">Requirement</span></span> | <span data-ttu-id="09526-176">Valor</span><span class="sxs-lookup"><span data-stu-id="09526-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09526-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09526-177">Minimum supported client</span></span><br/> | <span data-ttu-id="09526-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09526-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="09526-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09526-179">Minimum supported server</span></span><br/> | <span data-ttu-id="09526-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09526-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="09526-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="09526-181">Namespace</span></span><br/>                | <span data-ttu-id="09526-182">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="09526-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="09526-183">MOF</span><span class="sxs-lookup"><span data-stu-id="09526-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09526-184"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09526-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="09526-185">DLL</span><span class="sxs-lookup"><span data-stu-id="09526-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09526-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09526-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09526-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="09526-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09526-188">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="09526-188">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="09526-189">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="09526-189">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
