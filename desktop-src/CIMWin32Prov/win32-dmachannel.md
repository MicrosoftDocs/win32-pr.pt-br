---
description: A \_ classe WMI DMAChannel do Win32 representa um canal DMA (acesso direto à memória) em um sistema de computador executando o Windows.
ms.assetid: cc517aac-7bd4-4937-8b07-2597076fca2c
ms.tgt_platform: multiple
title: Classe Win32_DMAChannel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DMAChannel
- Win32_DMAChannel.AddressSize
- Win32_DMAChannel.Availability
- Win32_DMAChannel.BurstMode
- Win32_DMAChannel.ByteMode
- Win32_DMAChannel.Caption
- Win32_DMAChannel.ChannelTiming
- Win32_DMAChannel.CreationClassName
- Win32_DMAChannel.CSCreationClassName
- Win32_DMAChannel.CSName
- Win32_DMAChannel.Description
- Win32_DMAChannel.DMAChannel
- Win32_DMAChannel.InstallDate
- Win32_DMAChannel.MaxTransferSize
- Win32_DMAChannel.Name
- Win32_DMAChannel.Port
- Win32_DMAChannel.Status
- Win32_DMAChannel.TransferWidths
- Win32_DMAChannel.TypeCTiming
- Win32_DMAChannel.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0c2b36ff17931133d0dc4529e34f31ac24e00653
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826583"
---
# <a name="win32_dmachannel-class"></a><span data-ttu-id="51738-103">\_Classe Win32 DMAChannel</span><span class="sxs-lookup"><span data-stu-id="51738-103">Win32\_DMAChannel class</span></span>

<span data-ttu-id="51738-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DMAChannel do Win32** representa um canal DMA (acesso direto à memória) em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="51738-104">The **Win32\_DMAChannel** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a direct memory access (DMA) channel on a computer system running Windows.</span></span> <span data-ttu-id="51738-105">DMA é um método de mover dados de um dispositivo para uma memória (ou vice-versa) sem a ajuda do microprocessador.</span><span class="sxs-lookup"><span data-stu-id="51738-105">DMA is a method of moving data from a device to memory (or vice versa) without the help of the microprocessor.</span></span> <span data-ttu-id="51738-106">A placa do sistema usa um controlador DMA para lidar com um número fixo de canais, cada um dos quais pode ser usado por um único dispositivo (e apenas um) por vez.</span><span class="sxs-lookup"><span data-stu-id="51738-106">The system board uses a DMA controller to handle a fixed number of channels, each of which can be used by one (and only one) device at a time.</span></span>

<span data-ttu-id="51738-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="51738-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="51738-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="51738-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="51738-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51738-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DMAChannel : CIM_DMA
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
  uint32   Port;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a><span data-ttu-id="51738-110">Membros</span><span class="sxs-lookup"><span data-stu-id="51738-110">Members</span></span>

<span data-ttu-id="51738-111">A classe **Win32 \_ DMAChannel** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="51738-111">The **Win32\_DMAChannel** class has these types of members:</span></span>

-   [<span data-ttu-id="51738-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="51738-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51738-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="51738-113">Properties</span></span>

<span data-ttu-id="51738-114">A classe **Win32 \_ DMAChannel** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="51738-114">The **Win32\_DMAChannel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51738-115">**AddressSize**</span><span class="sxs-lookup"><span data-stu-id="51738-115">**AddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-116">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51738-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51738-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-118">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,3 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="51738-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="51738-119">Tamanho do endereço do canal de DMA em bits.</span><span class="sxs-lookup"><span data-stu-id="51738-119">DMA channel address size in bits.</span></span> <span data-ttu-id="51738-120">Os valores permitidos são 8, 16, 32 ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="51738-120">Permissible values are 8, 16, 32, or 64 bits.</span></span> <span data-ttu-id="51738-121">Se for desconhecido, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="51738-121">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="51738-122">Essa propriedade é herdada do [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="51738-122">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>



 <span data-ttu-id="51738-123"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="51738-123">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51738-124">(8)</span><span class="sxs-lookup"><span data-stu-id="51738-124">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51738-125">(16)</span><span class="sxs-lookup"><span data-stu-id="51738-125">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51738-126">(32)</span><span class="sxs-lookup"><span data-stu-id="51738-126">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51738-127">(64)</span><span class="sxs-lookup"><span data-stu-id="51738-127">(64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="51738-128">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="51738-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51738-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51738-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-131">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="51738-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="51738-132">Disponibilidade do DMA.</span><span class="sxs-lookup"><span data-stu-id="51738-132">Availability of the DMA.</span></span> <span data-ttu-id="51738-133">Essa propriedade é herdada do [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="51738-133">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="51738-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="51738-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="51738-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="51738-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="51738-136"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponível** (3)</span><span class="sxs-lookup"><span data-stu-id="51738-136"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="51738-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**Em uso/não disponível** (4)</span><span class="sxs-lookup"><span data-stu-id="51738-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="51738-138">Em uso ou não disponível</span><span class="sxs-lookup"><span data-stu-id="51738-138">In Use or Not Available</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="51738-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**Em uso e disponível/compartilhável** (5)</span><span class="sxs-lookup"><span data-stu-id="51738-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="51738-140">Em uso e disponível ou compartilhável</span><span class="sxs-lookup"><span data-stu-id="51738-140">In Use and Available or Sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="51738-141">**Intermitênciamode**</span><span class="sxs-lookup"><span data-stu-id="51738-141">**BurstMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-142">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="51738-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51738-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-144">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="51738-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="51738-145">Indica se o canal DMA dá suporte ou não ao modo de intermitência.</span><span class="sxs-lookup"><span data-stu-id="51738-145">Indicates whether or not the DMA channel supports burst mode.</span></span>

<span data-ttu-id="51738-146">Essa propriedade é herdada do [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="51738-146">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="51738-147">**Bytemode**</span><span class="sxs-lookup"><span data-stu-id="51738-147">**ByteMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-148">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51738-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51738-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-150">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,7 ")</span><span class="sxs-lookup"><span data-stu-id="51738-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="51738-151">Modo de execução DMA.</span><span class="sxs-lookup"><span data-stu-id="51738-151">DMA execution mode.</span></span>

<span data-ttu-id="51738-152">Essa propriedade é herdada do [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="51738-152">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="51738-153"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="51738-153"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="51738-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="51738-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="51738-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Não executar no modo ' contagem por byte '** (3)</span><span class="sxs-lookup"><span data-stu-id="51738-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Not execute in 'count by byte' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="51738-156">Não é executado no modo "contagem por byte"</span><span class="sxs-lookup"><span data-stu-id="51738-156">Does not execute in "count by byte" mode</span></span>

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="51738-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Executar no modo ' contagem por byte '** (4)</span><span class="sxs-lookup"><span data-stu-id="51738-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Execute in 'count by byte' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="51738-158">Executar no modo "contagem por byte"</span><span class="sxs-lookup"><span data-stu-id="51738-158">Execute in "count by byte" mode</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="51738-159">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="51738-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51738-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51738-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-162">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="51738-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="51738-163">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="51738-163">Short description of the object a one-line string.</span></span>

<span data-ttu-id="51738-164">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51738-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="51738-165">**ChannelTiming**</span><span class="sxs-lookup"><span data-stu-id="51738-165">**ChannelTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-166">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51738-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51738-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-168">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="51738-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="51738-169">Tempo de canal de DMA.</span><span class="sxs-lookup"><span data-stu-id="51738-169">DMA channel timing.</span></span>

<span data-ttu-id="51738-170">Essa propriedade é herdada do [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="51738-170">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="51738-171">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="51738-171">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="51738-172">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="51738-172">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="51738-173">**Compatível com ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="51738-173">**ISA Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span data-ttu-id="51738-174">**Digite A** (4)</span><span class="sxs-lookup"><span data-stu-id="51738-174">**Type A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span data-ttu-id="51738-175">**Tipo B** (5)</span><span class="sxs-lookup"><span data-stu-id="51738-175">**Type B** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span data-ttu-id="51738-176">**Digite F** (6)</span><span class="sxs-lookup"><span data-stu-id="51738-176">**Type F** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="51738-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="51738-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51738-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51738-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-180">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="51738-180">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="51738-181">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="51738-181">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="51738-182">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="51738-182">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="51738-183">Essa propriedade é herdada do [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="51738-183">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="51738-184">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="51738-184">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51738-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51738-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-187">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="51738-187">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="51738-188">Nome da classe de criação do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="51738-188">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="51738-189">Essa propriedade é herdada do [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="51738-189">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="51738-190">**CSName**</span><span class="sxs-lookup"><span data-stu-id="51738-190">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51738-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51738-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-193">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="51738-193">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="51738-194">Nome do sistema de computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="51738-194">Name of the scoping computer system.</span></span>

<span data-ttu-id="51738-195">Essa propriedade é herdada do [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="51738-195">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="51738-196">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="51738-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51738-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51738-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-199">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="51738-199">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="51738-200">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="51738-200">Description of the object.</span></span>

<span data-ttu-id="51738-201">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51738-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="51738-202">**DMAChannel**</span><span class="sxs-lookup"><span data-stu-id="51738-202">**DMAChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-203">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51738-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51738-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-205">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 1,1 ")</span><span class="sxs-lookup"><span data-stu-id="51738-205">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="51738-206">Número de canal DMA, parte do valor de chave do objeto.</span><span class="sxs-lookup"><span data-stu-id="51738-206">DMA channel number, part of the object's key value.</span></span>

<span data-ttu-id="51738-207">Essa propriedade é herdada do [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="51738-207">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="51738-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="51738-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-209">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="51738-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="51738-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-211">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="51738-211">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="51738-212">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="51738-212">Date and time the object was installed.</span></span> <span data-ttu-id="51738-213">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="51738-213">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="51738-214">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51738-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="51738-215">**MaxTransferSize**</span><span class="sxs-lookup"><span data-stu-id="51738-215">**MaxTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-216">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51738-216">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51738-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-218">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="51738-218">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="51738-219">Número máximo de bytes que podem ser transferidos por este canal DMA.</span><span class="sxs-lookup"><span data-stu-id="51738-219">Maximum number of bytes that can be transferred by this DMA channel.</span></span> <span data-ttu-id="51738-220">Se for desconhecido, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="51738-220">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="51738-221">Essa propriedade é herdada do [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="51738-221">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="51738-222">**Nome**</span><span class="sxs-lookup"><span data-stu-id="51738-222">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51738-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51738-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-225">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="51738-225">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="51738-226">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="51738-226">Label by which the object is known.</span></span> <span data-ttu-id="51738-227">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="51738-227">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="51738-228">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51738-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="51738-229">**Porta**</span><span class="sxs-lookup"><span data-stu-id="51738-229">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-230">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51738-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51738-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-232">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| estruturas do sistema \| cm/porta DMA do [**\_ \_ \_ descritor de recursos parciais**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor) \| \| ")</span><span class="sxs-lookup"><span data-stu-id="51738-232">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|[**CM\_PARTIAL\_RESOURCE\_DESCRIPTOR**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)\|Dma\|Port")</span></span>
</dt> </dl>

<span data-ttu-id="51738-233">Porta DMA usada pelo adaptador de barramento de host.</span><span class="sxs-lookup"><span data-stu-id="51738-233">DMA port used by the host bus adapter.</span></span> <span data-ttu-id="51738-234">Isso é significativo para barramentos de tipo MCA.</span><span class="sxs-lookup"><span data-stu-id="51738-234">This is meaningful for MCA-type buses.</span></span>

<span data-ttu-id="51738-235">Exemplo: 12</span><span class="sxs-lookup"><span data-stu-id="51738-235">Example: 12</span></span>

</dd> <dt>

<span data-ttu-id="51738-236">**Status**</span><span class="sxs-lookup"><span data-stu-id="51738-236">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51738-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51738-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-239">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="51738-239">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="51738-240">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="51738-240">Current status of the object.</span></span> <span data-ttu-id="51738-241">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="51738-241">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="51738-242">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="51738-242">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="51738-243">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="51738-243">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="51738-244">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="51738-244">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="51738-245">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="51738-245">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="51738-246">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51738-246">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="51738-247">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="51738-247">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="51738-248">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="51738-248">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="51738-249">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="51738-249">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="51738-250">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="51738-250">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="51738-251">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="51738-251">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="51738-252">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="51738-252">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="51738-253">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="51738-253">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="51738-254">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="51738-254">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="51738-255">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="51738-255">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="51738-256">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="51738-256">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="51738-257">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="51738-257">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="51738-258">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="51738-258">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="51738-259">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="51738-259">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="51738-260">**TransferWidths**</span><span class="sxs-lookup"><span data-stu-id="51738-260">**TransferWidths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-261">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51738-261">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="51738-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-263">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="51738-263">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="51738-264">Matriz de todas as larguras de transferência (em bits) com suporte por este canal de DMA.</span><span class="sxs-lookup"><span data-stu-id="51738-264">Array of all the transfer widths (in bits) supported by this DMA channel.</span></span> <span data-ttu-id="51738-265">Se for desconhecido, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="51738-265">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="51738-266">Essa propriedade é herdada do [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="51738-266">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>



 <span data-ttu-id="51738-267"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="51738-267">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51738-268">(8)</span><span class="sxs-lookup"><span data-stu-id="51738-268">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51738-269">(16)</span><span class="sxs-lookup"><span data-stu-id="51738-269">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51738-270">(32)</span><span class="sxs-lookup"><span data-stu-id="51738-270">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51738-271">(64)</span><span class="sxs-lookup"><span data-stu-id="51738-271">(64)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51738-272">(128)</span><span class="sxs-lookup"><span data-stu-id="51738-272">(128)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="51738-273">**TypeCTiming**</span><span class="sxs-lookup"><span data-stu-id="51738-273">**TypeCTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-274">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51738-274">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51738-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-276">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,10 ")</span><span class="sxs-lookup"><span data-stu-id="51738-276">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="51738-277">Suporte para tempo de tipo C (intermitência).</span><span class="sxs-lookup"><span data-stu-id="51738-277">Support for C type (burst) timing.</span></span>

<span data-ttu-id="51738-278">Essa propriedade é herdada do [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="51738-278">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="51738-279">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="51738-279">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="51738-280">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="51738-280">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="51738-281">**Compatível com ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="51738-281">**ISA Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="51738-282">**Sem suporte** (4)</span><span class="sxs-lookup"><span data-stu-id="51738-282">**Not Supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="51738-283">**Com suporte** (5)</span><span class="sxs-lookup"><span data-stu-id="51738-283">**Supported** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="51738-284">**WordMode**</span><span class="sxs-lookup"><span data-stu-id="51738-284">**WordMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51738-285">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51738-285">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51738-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51738-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51738-287">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,8 ")</span><span class="sxs-lookup"><span data-stu-id="51738-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="51738-288">Modo de execução DMA.</span><span class="sxs-lookup"><span data-stu-id="51738-288">DMA execution mode.</span></span>

<span data-ttu-id="51738-289">Essa propriedade é herdada do [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="51738-289">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="51738-290"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="51738-290"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="51738-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="51738-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="51738-292"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Não executar no modo ' contagem por palavra '** (3)</span><span class="sxs-lookup"><span data-stu-id="51738-292"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Not execute in 'count by word' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="51738-293">Não é executado no modo "contagem por palavra"</span><span class="sxs-lookup"><span data-stu-id="51738-293">Does not execute in "count by word" mode</span></span>

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="51738-294"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Executar no modo ' contagem por palavra '** (4)</span><span class="sxs-lookup"><span data-stu-id="51738-294"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Execute in 'count by word' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="51738-295">Executar no modo "contagem por palavra"</span><span class="sxs-lookup"><span data-stu-id="51738-295">Execute in "count by word" mode</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51738-296">Comentários</span><span class="sxs-lookup"><span data-stu-id="51738-296">Remarks</span></span>

<span data-ttu-id="51738-297">A classe **Win32 \_ DMAChannel** é derivada do [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="51738-297">The **Win32\_DMAChannel** class is derived from [**CIM\_DMA**](cim-dma.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51738-298">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51738-298">Requirements</span></span>



| <span data-ttu-id="51738-299">Requisito</span><span class="sxs-lookup"><span data-stu-id="51738-299">Requirement</span></span> | <span data-ttu-id="51738-300">Valor</span><span class="sxs-lookup"><span data-stu-id="51738-300">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51738-301">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51738-301">Minimum supported client</span></span><br/> | <span data-ttu-id="51738-302">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51738-302">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="51738-303">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51738-303">Minimum supported server</span></span><br/> | <span data-ttu-id="51738-304">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51738-304">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="51738-305">Namespace</span><span class="sxs-lookup"><span data-stu-id="51738-305">Namespace</span></span><br/>                | <span data-ttu-id="51738-306">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="51738-306">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="51738-307">MOF</span><span class="sxs-lookup"><span data-stu-id="51738-307">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51738-308"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51738-308"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="51738-309">DLL</span><span class="sxs-lookup"><span data-stu-id="51738-309">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51738-310"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51738-310"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51738-311">Confira também</span><span class="sxs-lookup"><span data-stu-id="51738-311">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51738-312">**DMA de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="51738-312">**CIM\_DMA**</span></span>](cim-dma.md)
</dt> <dt>

[<span data-ttu-id="51738-313">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="51738-313">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

