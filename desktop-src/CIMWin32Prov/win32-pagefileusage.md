---
description: O Win32 \_ PageFileUsage&\# 8194; A classe WMI representa o arquivo usado para lidar com a troca de arquivos de memória virtual em um sistema Win32. As informações contidas nos objetos instanciados nessa classe especificam o estado de tempo de execução do arquivo de paginação.
ms.assetid: 635d7bd0-3738-4092-8b76-5e9583e079a9
ms.tgt_platform: multiple
title: Classe Win32_PageFileUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileUsage
- Win32_PageFileUsage.Caption
- Win32_PageFileUsage.Description
- Win32_PageFileUsage.InstallDate
- Win32_PageFileUsage.Status
- Win32_PageFileUsage.AllocatedBaseSize
- Win32_PageFileUsage.CurrentUsage
- Win32_PageFileUsage.Name
- Win32_PageFileUsage.PeakUsage
- Win32_PageFileUsage.TempPageFile
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9885bea242a9f2b781ccb0dcac479248a9ccc538
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501061"
---
# <a name="win32_pagefileusage-class"></a><span data-ttu-id="b3cd9-104">\_Classe Win32 PageFileUsage</span><span class="sxs-lookup"><span data-stu-id="b3cd9-104">Win32\_PageFileUsage class</span></span>

<span data-ttu-id="b3cd9-105">A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PageFileUsage do Win32** representa o arquivo usado para lidar com a troca de arquivos de memória virtual em um sistema Win32.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-105">The **Win32\_PageFileUsage** [WMI class](../wmisdk/retrieving-a-class.md) represents the file used for handling virtual memory file swapping on a Win32 system.</span></span> <span data-ttu-id="b3cd9-106">As informações contidas nos objetos instanciados nessa classe especificam o estado de tempo de execução do arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-106">Information contained within objects instantiated from this class specify the run-time state of the page file.</span></span>

<span data-ttu-id="b3cd9-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b3cd9-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3cd9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3cd9-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{9B3AC16A-EEE5-11d2-B13B-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileUsage : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AllocatedBaseSize;
  uint32   CurrentUsage;
  string   Name;
  uint32   PeakUsage;
  boolean  TempPageFile;
};
```

## <a name="members"></a><span data-ttu-id="b3cd9-110">Membros</span><span class="sxs-lookup"><span data-stu-id="b3cd9-110">Members</span></span>

<span data-ttu-id="b3cd9-111">A classe **Win32 \_ PageFileUsage** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b3cd9-111">The **Win32\_PageFileUsage** class has these types of members:</span></span>

-   [<span data-ttu-id="b3cd9-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b3cd9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3cd9-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b3cd9-113">Properties</span></span>

<span data-ttu-id="b3cd9-114">A classe **Win32 \_ PageFileUsage** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-114">The **Win32\_PageFileUsage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3cd9-115">**AllocatedBaseSize**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-115">**AllocatedBaseSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3cd9-116">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3cd9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-118">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwTotalPageFile"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="b3cd9-119">Quantidade real de espaço em disco alocada para uso com este arquivo de página.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-119">Actual amount of disk space allocated for use with this page file.</span></span> <span data-ttu-id="b3cd9-120">Esse valor corresponde ao intervalo estabelecido no [**Win32 \_ PageFileSetting**](win32-pagefilesetting.md) nas propriedades **initialSize** e **MaximumSize** , definido na inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-120">This value corresponds to the range established in [**Win32\_PageFileSetting**](win32-pagefilesetting.md) under the **InitialSize** and **MaximumSize** properties, set at system startup.</span></span>

<span data-ttu-id="b3cd9-121">Exemplo: 178</span><span class="sxs-lookup"><span data-stu-id="b3cd9-121">Example: 178</span></span>

</dd> <dt>

<span data-ttu-id="b3cd9-122">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3cd9-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3cd9-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-125">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b3cd9-126">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-126">A short textual description of the object.</span></span>

<span data-ttu-id="b3cd9-127">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3cd9-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3cd9-128">**CurrentUsage**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-128">**CurrentUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3cd9-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3cd9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-131">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="b3cd9-132">Quantidade de espaço em disco usada atualmente pelo arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-132">Amount of disk space currently used by the page file.</span></span>

</dd> <dt>

<span data-ttu-id="b3cd9-133">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3cd9-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3cd9-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-136">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-136">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b3cd9-137">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-137">A textual description of the object.</span></span>

<span data-ttu-id="b3cd9-138">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3cd9-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3cd9-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3cd9-140">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3cd9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-142">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b3cd9-143">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-143">Indicates when the object was installed.</span></span> <span data-ttu-id="b3cd9-144">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-144">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b3cd9-145">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3cd9-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3cd9-146">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3cd9-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3cd9-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-149">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-149">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b3cd9-150">Nome do arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-150">Name of the page file.</span></span>

<span data-ttu-id="b3cd9-151">Exemplo: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="b3cd9-151">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="b3cd9-152">**PeakUsage**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-152">**PeakUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3cd9-153">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3cd9-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-155">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="b3cd9-156">Arquivo de página de uso mais alto.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-156">Highest use page file.</span></span>

</dd> <dt>

<span data-ttu-id="b3cd9-157">**Status**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-157">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3cd9-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3cd9-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-160">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-160">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b3cd9-161">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-161">String that indicates the current status of the object.</span></span> <span data-ttu-id="b3cd9-162">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-162">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b3cd9-163">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="b3cd9-163">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b3cd9-164">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="b3cd9-164">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b3cd9-165">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="b3cd9-165">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b3cd9-166">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-166">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b3cd9-167">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-167">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b3cd9-168">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3cd9-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b3cd9-169">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b3cd9-169">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b3cd9-170">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-170">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b3cd9-171">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-171">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b3cd9-172">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-172">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b3cd9-173">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-173">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b3cd9-174">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-174">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b3cd9-175">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-175">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b3cd9-176">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-176">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b3cd9-177">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-177">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b3cd9-178">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-178">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b3cd9-179">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-179">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b3cd9-180">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-180">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b3cd9-181">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-181">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b3cd9-182">**TempPageFile**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-182">**TempPageFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3cd9-183">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3cd9-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3cd9-185">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| TempPageFile")</span><span class="sxs-lookup"><span data-stu-id="b3cd9-185">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|TempPageFile")</span></span>
</dt> </dl>

<span data-ttu-id="b3cd9-186">Se for **true**, um arquivo de paginação temporário foi criado, geralmente porque não há nenhum arquivo de paginação permanente no sistema de computador atual.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-186">If **true**, a temporary page file has been created, usually because there is no permanent page file on the current computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3cd9-187">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3cd9-187">Remarks</span></span>

<span data-ttu-id="b3cd9-188">A classe **Win32 \_ PageFileUsage** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3cd9-188">The **Win32\_PageFileUsage** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3cd9-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3cd9-189">Requirements</span></span>



| <span data-ttu-id="b3cd9-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3cd9-190">Requirement</span></span> | <span data-ttu-id="b3cd9-191">Valor</span><span class="sxs-lookup"><span data-stu-id="b3cd9-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3cd9-192">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3cd9-192">Minimum supported client</span></span><br/> | <span data-ttu-id="b3cd9-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3cd9-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b3cd9-194">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3cd9-194">Minimum supported server</span></span><br/> | <span data-ttu-id="b3cd9-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3cd9-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b3cd9-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3cd9-196">Namespace</span></span><br/>                | <span data-ttu-id="b3cd9-197">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b3cd9-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b3cd9-198">MOF</span><span class="sxs-lookup"><span data-stu-id="b3cd9-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3cd9-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3cd9-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3cd9-200">DLL</span><span class="sxs-lookup"><span data-stu-id="b3cd9-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3cd9-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3cd9-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3cd9-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3cd9-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3cd9-203">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-203">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="b3cd9-204">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="b3cd9-204">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
