---
description: A \_ classe CIM DMA representa o DMA (acesso direto à memória) da arquitetura do computador.
ms.assetid: 101fa9f3-a403-487d-8482-b1e8e9f957d6
ms.tgt_platform: multiple
title: Classe CIM_DMA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DMA
- CIM_DMA.AddressSize
- CIM_DMA.Availability
- CIM_DMA.BurstMode
- CIM_DMA.ByteMode
- CIM_DMA.Caption
- CIM_DMA.ChannelTiming
- CIM_DMA.CreationClassName
- CIM_DMA.CSCreationClassName
- CIM_DMA.CSName
- CIM_DMA.Description
- CIM_DMA.DMAChannel
- CIM_DMA.InstallDate
- CIM_DMA.MaxTransferSize
- CIM_DMA.Name
- CIM_DMA.Status
- CIM_DMA.TransferWidths
- CIM_DMA.TypeCTiming
- CIM_DMA.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71fe9c0ad29afa7be20df6fbf05c5d1183d23d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920395"
---
# <a name="cim_dma-class"></a><span data-ttu-id="db5d3-103">\_Classe DMA de CIM</span><span class="sxs-lookup"><span data-stu-id="db5d3-103">CIM\_DMA class</span></span>

<span data-ttu-id="db5d3-104">A classe **CIM \_ DMA** representa o DMA (acesso direto à memória) da arquitetura do computador.</span><span class="sxs-lookup"><span data-stu-id="db5d3-104">The **CIM\_DMA** class represents computer architecture direct memory access (DMA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db5d3-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="db5d3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="db5d3-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="db5d3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="db5d3-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="db5d3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="db5d3-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="db5d3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="db5d3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db5d3-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C523-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DMA : CIM_SystemResource
{
  uint16   AddressSize;
  uint16   Availability;
  boolean  BurstMode;
  uint16   ByteMode;
  string   Caption;
  uint16   ChannelTiming;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint32   DMAChannel;
  datetime InstallDate;
  uint32   MaxTransferSize;
  string   Name;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a><span data-ttu-id="db5d3-110">Membros</span><span class="sxs-lookup"><span data-stu-id="db5d3-110">Members</span></span>

<span data-ttu-id="db5d3-111">A classe de **\_ DMA do CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="db5d3-111">The **CIM\_DMA** class has these types of members:</span></span>

-   [<span data-ttu-id="db5d3-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="db5d3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="db5d3-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="db5d3-113">Properties</span></span>

<span data-ttu-id="db5d3-114">A classe de **\_ DMA do CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="db5d3-114">The **CIM\_DMA** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="db5d3-115">**AddressSize**</span><span class="sxs-lookup"><span data-stu-id="db5d3-115">**AddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-116">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="db5d3-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-118">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,3 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="db5d3-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-119">Tamanho do endereço do canal DMA, em bits.</span><span class="sxs-lookup"><span data-stu-id="db5d3-119">DMA channel address size, in bits.</span></span> <span data-ttu-id="db5d3-120">Os valores permitidos são 8, 16, 32 e 64.</span><span class="sxs-lookup"><span data-stu-id="db5d3-120">Permissible values are 8, 16, 32, and 64.</span></span> <span data-ttu-id="db5d3-121">Se for desconhecido, insira 0.</span><span class="sxs-lookup"><span data-stu-id="db5d3-121">If unknown, enter 0.</span></span>

<dt>



 <span data-ttu-id="db5d3-122"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="db5d3-122">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="db5d3-123">(8)</span><span class="sxs-lookup"><span data-stu-id="db5d3-123">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="db5d3-124">(16)</span><span class="sxs-lookup"><span data-stu-id="db5d3-124">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="db5d3-125">(32)</span><span class="sxs-lookup"><span data-stu-id="db5d3-125">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="db5d3-126">(64)</span><span class="sxs-lookup"><span data-stu-id="db5d3-126">(64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="db5d3-127">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="db5d3-127">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-128">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="db5d3-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-130">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="db5d3-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-131">Disponibilidade do DMA.</span><span class="sxs-lookup"><span data-stu-id="db5d3-131">Availability of the DMA.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="db5d3-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="db5d3-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="db5d3-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="db5d3-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-134">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="db5d3-134">Unknown.</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="db5d3-135"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponível** (3)</span><span class="sxs-lookup"><span data-stu-id="db5d3-135"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-136">Disponível.</span><span class="sxs-lookup"><span data-stu-id="db5d3-136">Available.</span></span>

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="db5d3-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**Em uso/não disponível** (4)</span><span class="sxs-lookup"><span data-stu-id="db5d3-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-138">Em uso (não disponível).</span><span class="sxs-lookup"><span data-stu-id="db5d3-138">In use (not available).</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="db5d3-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**Em uso e disponível/compartilhável** (5)</span><span class="sxs-lookup"><span data-stu-id="db5d3-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-140">Em uso, mas disponível (compartilhável).</span><span class="sxs-lookup"><span data-stu-id="db5d3-140">In use, but available (sharable).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db5d3-141">**Intermitênciamode**</span><span class="sxs-lookup"><span data-stu-id="db5d3-141">**BurstMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-142">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="db5d3-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-144">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="db5d3-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-145">Se **for true**, o canal DMA dará suporte ao modo de intermitência.</span><span class="sxs-lookup"><span data-stu-id="db5d3-145">If **TRUE**, the DMA channel supports burst mode.</span></span>

</dd> <dt>

<span data-ttu-id="db5d3-146">**Bytemode**</span><span class="sxs-lookup"><span data-stu-id="db5d3-146">**ByteMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-147">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="db5d3-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-149">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,7 ")</span><span class="sxs-lookup"><span data-stu-id="db5d3-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-150">Indica se o DMA pode ser executado no modo de contagem por byte.</span><span class="sxs-lookup"><span data-stu-id="db5d3-150">Indicates whether DMA can execute in count-by-byte mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="db5d3-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="db5d3-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-152">Outros.</span><span class="sxs-lookup"><span data-stu-id="db5d3-152">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="db5d3-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="db5d3-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-154">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="db5d3-154">Unknown.</span></span>

</dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="db5d3-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Não executar no modo ' contagem por byte '** (3)</span><span class="sxs-lookup"><span data-stu-id="db5d3-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Not execute in 'count by byte' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-156">Não é possível executar no modo de contagem por byte.</span><span class="sxs-lookup"><span data-stu-id="db5d3-156">Cannot execute in count-by-byte mode.</span></span>

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="db5d3-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Executar no modo ' contagem por byte '** (4)</span><span class="sxs-lookup"><span data-stu-id="db5d3-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Execute in 'count by byte' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-158">Capaz de executar em modo de contagem por byte.</span><span class="sxs-lookup"><span data-stu-id="db5d3-158">Able to execute in count-by-byte mode.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db5d3-159">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="db5d3-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="db5d3-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-162">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="db5d3-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-163">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="db5d3-163">Short textual description of the object.</span></span>

<span data-ttu-id="db5d3-164">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="db5d3-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db5d3-165">**ChannelTiming**</span><span class="sxs-lookup"><span data-stu-id="db5d3-165">**ChannelTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-166">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="db5d3-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-168">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="db5d3-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-169">Tempo de canal de DMA.</span><span class="sxs-lookup"><span data-stu-id="db5d3-169">DMA channel timing.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="db5d3-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="db5d3-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-171">Outros.</span><span class="sxs-lookup"><span data-stu-id="db5d3-171">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="db5d3-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="db5d3-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-173">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="db5d3-173">Unknown.</span></span>

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="db5d3-174"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**Compatível com ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="db5d3-174"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA Compatible** (3)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-175">Compatível com ISA.</span><span class="sxs-lookup"><span data-stu-id="db5d3-175">ISA-compatible.</span></span>

</dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span data-ttu-id="db5d3-176"><span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**Digite A** (4)</span><span class="sxs-lookup"><span data-stu-id="db5d3-176"><span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**Type A** (4)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-177">Digite A.</span><span class="sxs-lookup"><span data-stu-id="db5d3-177">Type A.</span></span>

</dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span data-ttu-id="db5d3-178"><span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**Tipo B** (5)</span><span class="sxs-lookup"><span data-stu-id="db5d3-178"><span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**Type B** (5)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-179">Digite B.</span><span class="sxs-lookup"><span data-stu-id="db5d3-179">Type B.</span></span>

</dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span data-ttu-id="db5d3-180"><span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**Digite F** (6)</span><span class="sxs-lookup"><span data-stu-id="db5d3-180"><span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**Type F** (6)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-181">Digite F.</span><span class="sxs-lookup"><span data-stu-id="db5d3-181">Type F.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db5d3-182">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="db5d3-182">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="db5d3-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-185">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="db5d3-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-186">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="db5d3-186">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="db5d3-187">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="db5d3-187">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="db5d3-188">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="db5d3-188">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="db5d3-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-191">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="db5d3-191">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-192">Nome da classe de criação do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="db5d3-192">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="db5d3-193">**CSName**</span><span class="sxs-lookup"><span data-stu-id="db5d3-193">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="db5d3-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-196">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="db5d3-196">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-197">Nome do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="db5d3-197">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="db5d3-198">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="db5d3-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="db5d3-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-201">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="db5d3-201">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-202">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="db5d3-202">Textual description of the object.</span></span>

<span data-ttu-id="db5d3-203">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="db5d3-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db5d3-204">**DMAChannel**</span><span class="sxs-lookup"><span data-stu-id="db5d3-204">**DMAChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-205">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db5d3-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 1,1 ")</span><span class="sxs-lookup"><span data-stu-id="db5d3-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-208">Número do canal DMA.</span><span class="sxs-lookup"><span data-stu-id="db5d3-208">DMA channel number.</span></span> <span data-ttu-id="db5d3-209">Esse número é parte do valor de chave do objeto.</span><span class="sxs-lookup"><span data-stu-id="db5d3-209">This number is part of the object's key value.</span></span>

</dd> <dt>

<span data-ttu-id="db5d3-210">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="db5d3-210">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-211">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="db5d3-211">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-213">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="db5d3-213">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-214">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="db5d3-214">Date and time the object was installed.</span></span> <span data-ttu-id="db5d3-215">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="db5d3-215">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="db5d3-216">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="db5d3-216">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db5d3-217">**MaxTransferSize**</span><span class="sxs-lookup"><span data-stu-id="db5d3-217">**MaxTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-218">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db5d3-218">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-220">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="db5d3-220">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-221">Número máximo de bytes que podem ser transferidos por este canal DMA.</span><span class="sxs-lookup"><span data-stu-id="db5d3-221">Maximum number of bytes that can be transferred by this DMA channel.</span></span> <span data-ttu-id="db5d3-222">Se for desconhecido, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="db5d3-222">If unknown, enter 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="db5d3-223">**Nome**</span><span class="sxs-lookup"><span data-stu-id="db5d3-223">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-224">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="db5d3-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-226">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="db5d3-226">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-227">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="db5d3-227">Label by which the object is known.</span></span> <span data-ttu-id="db5d3-228">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="db5d3-228">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="db5d3-229">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="db5d3-229">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db5d3-230">**Status**</span><span class="sxs-lookup"><span data-stu-id="db5d3-230">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-231">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="db5d3-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-233">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="db5d3-233">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-234">Indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="db5d3-234">Indicates the current status of the object.</span></span>

<span data-ttu-id="db5d3-235">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="db5d3-235">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="db5d3-236">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="db5d3-236">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="db5d3-237">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="db5d3-237">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="db5d3-238">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="db5d3-238">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="db5d3-239">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="db5d3-239">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="db5d3-240">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="db5d3-240">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="db5d3-241">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="db5d3-241">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="db5d3-242">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="db5d3-242">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="db5d3-243">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="db5d3-243">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="db5d3-244">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="db5d3-244">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="db5d3-245">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="db5d3-245">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="db5d3-246">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="db5d3-246">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="db5d3-247">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="db5d3-247">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="db5d3-248">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="db5d3-248">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="db5d3-249">**TransferWidths**</span><span class="sxs-lookup"><span data-stu-id="db5d3-249">**TransferWidths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-250">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="db5d3-250">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-252">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="db5d3-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-253">Matriz que indica todas as larguras de transferência, em bits, para as quais este canal DMA dá suporte.</span><span class="sxs-lookup"><span data-stu-id="db5d3-253">Array that indicates all of the transfer widths, in bits, supported by this DMA channel.</span></span> <span data-ttu-id="db5d3-254">Os valores permitidos são 8, 16, 32, 64 e 128 bits.</span><span class="sxs-lookup"><span data-stu-id="db5d3-254">Permissible values are 8, 16, 32, 64, and 128 bits.</span></span> <span data-ttu-id="db5d3-255">Se for desconhecido, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="db5d3-255">If unknown, enter 0 (zero).</span></span>

<dt>



 <span data-ttu-id="db5d3-256"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="db5d3-256">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="db5d3-257">(8)</span><span class="sxs-lookup"><span data-stu-id="db5d3-257">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="db5d3-258">(16)</span><span class="sxs-lookup"><span data-stu-id="db5d3-258">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="db5d3-259">(32)</span><span class="sxs-lookup"><span data-stu-id="db5d3-259">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="db5d3-260">(64)</span><span class="sxs-lookup"><span data-stu-id="db5d3-260">(64)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="db5d3-261">(128)</span><span class="sxs-lookup"><span data-stu-id="db5d3-261">(128)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="db5d3-262">**TypeCTiming**</span><span class="sxs-lookup"><span data-stu-id="db5d3-262">**TypeCTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-263">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="db5d3-263">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-265">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,10 ")</span><span class="sxs-lookup"><span data-stu-id="db5d3-265">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-266">Indica se há suporte para o tempo de tipo C (intermitência).</span><span class="sxs-lookup"><span data-stu-id="db5d3-266">Indicates whether Type C (burst) timing is supported.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="db5d3-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="db5d3-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-268">Outros.</span><span class="sxs-lookup"><span data-stu-id="db5d3-268">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="db5d3-269"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="db5d3-269"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-270">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="db5d3-270">Unknown.</span></span>

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="db5d3-271"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**Compatível com ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="db5d3-271"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA Compatible** (3)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-272">Compatível com ISA.</span><span class="sxs-lookup"><span data-stu-id="db5d3-272">ISA-compatible.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="db5d3-273"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (4)</span><span class="sxs-lookup"><span data-stu-id="db5d3-273"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-274">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="db5d3-274">Not supported.</span></span>

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="db5d3-275"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**Com suporte** (5)</span><span class="sxs-lookup"><span data-stu-id="db5d3-275"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**Supported** (5)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-276">Com suporte.</span><span class="sxs-lookup"><span data-stu-id="db5d3-276">Supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db5d3-277">**WordMode**</span><span class="sxs-lookup"><span data-stu-id="db5d3-277">**WordMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5d3-278">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="db5d3-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db5d3-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5d3-280">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,8 ")</span><span class="sxs-lookup"><span data-stu-id="db5d3-280">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="db5d3-281">Indica se o DMA pode ser executado no modo de contagem por palavra.</span><span class="sxs-lookup"><span data-stu-id="db5d3-281">Indicates whether DMA can execute in count-by-word mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="db5d3-282"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="db5d3-282"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-283">Outros.</span><span class="sxs-lookup"><span data-stu-id="db5d3-283">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="db5d3-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="db5d3-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-285">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="db5d3-285">Unknown.</span></span>

</dd> <dt>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="db5d3-286"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Não executar no modo ' contagem por palavra '** (3)</span><span class="sxs-lookup"><span data-stu-id="db5d3-286"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Not execute in 'count by word' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-287">Não é possível executar no modo de contagem por palavra.</span><span class="sxs-lookup"><span data-stu-id="db5d3-287">Cannot execute in count-by-word mode.</span></span>

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="db5d3-288"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Executar no modo ' contagem por palavra '** (4)</span><span class="sxs-lookup"><span data-stu-id="db5d3-288"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Execute in 'count by word' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="db5d3-289">Capaz de executar em modo de contagem por palavra.</span><span class="sxs-lookup"><span data-stu-id="db5d3-289">Able to execute in count-by-word mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db5d3-290">Comentários</span><span class="sxs-lookup"><span data-stu-id="db5d3-290">Remarks</span></span>

<span data-ttu-id="db5d3-291">A classe **CIM \_ DMA** é derivada do [**CIM \_ SystemResource**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="db5d3-291">The **CIM\_DMA** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span>

<span data-ttu-id="db5d3-292">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="db5d3-292">WMI does not implement this class.</span></span> <span data-ttu-id="db5d3-293">Para classes derivadas do **\_ DMA do CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="db5d3-293">For classes derived from **CIM\_DMA**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="db5d3-294">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="db5d3-294">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="db5d3-295">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="db5d3-295">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="db5d3-296">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db5d3-296">Requirements</span></span>



| <span data-ttu-id="db5d3-297">Requisito</span><span class="sxs-lookup"><span data-stu-id="db5d3-297">Requirement</span></span> | <span data-ttu-id="db5d3-298">Valor</span><span class="sxs-lookup"><span data-stu-id="db5d3-298">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db5d3-299">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db5d3-299">Minimum supported client</span></span><br/> | <span data-ttu-id="db5d3-300">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db5d3-300">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="db5d3-301">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db5d3-301">Minimum supported server</span></span><br/> | <span data-ttu-id="db5d3-302">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db5d3-302">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="db5d3-303">Namespace</span><span class="sxs-lookup"><span data-stu-id="db5d3-303">Namespace</span></span><br/>                | <span data-ttu-id="db5d3-304">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="db5d3-304">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="db5d3-305">MOF</span><span class="sxs-lookup"><span data-stu-id="db5d3-305">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db5d3-306"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db5d3-306"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="db5d3-307">DLL</span><span class="sxs-lookup"><span data-stu-id="db5d3-307">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db5d3-308"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db5d3-308"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db5d3-309">Confira também</span><span class="sxs-lookup"><span data-stu-id="db5d3-309">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db5d3-310">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="db5d3-310">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

