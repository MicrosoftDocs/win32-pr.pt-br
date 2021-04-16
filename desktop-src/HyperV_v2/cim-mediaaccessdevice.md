---
description: Representa um dispositivo que pode usar a mídia para armazenar e recuperar dados.
ms.assetid: c63b1731-dbc0-4e5e-acb8-cd91b5569dd2
title: Classe CIM_MediaAccessDevice (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.NumberOfMediaSupported
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.MediaIsLocked
- CIM_MediaAccessDevice.Security
- CIM_MediaAccessDevice.LastCleaned
- CIM_MediaAccessDevice.MaxAccessTime
- CIM_MediaAccessDevice.UncompressedDataRate
- CIM_MediaAccessDevice.LoadTime
- CIM_MediaAccessDevice.UnloadTime
- CIM_MediaAccessDevice.MountCount
- CIM_MediaAccessDevice.TimeOfLastMount
- CIM_MediaAccessDevice.TotalMountTime
- CIM_MediaAccessDevice.UnitsDescription
- CIM_MediaAccessDevice.MaxUnitsBeforeCleaning
- CIM_MediaAccessDevice.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 616148f6749f3ec00d019a903e8f9046d3aba602
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105758036"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a><span data-ttu-id="3f31a-103">Classe CIM_MediaAccessDevice (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="3f31a-103">CIM_MediaAccessDevice class (Hyper-V management)</span></span>

<span data-ttu-id="3f31a-104">Representa um dispositivo que pode usar a mídia para armazenar e recuperar dados.</span><span class="sxs-lookup"><span data-stu-id="3f31a-104">Represents a device that can use media to store and retrieve data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f31a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f31a-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
{
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology;
  string   CompressionMethod;
  uint32   NumberOfMediaSupported;
  uint64   MaxMediaSize;
  uint64   DefaultBlockSize;
  uint64   MaxBlockSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  boolean  MediaIsLocked;
  uint16   Security;
  datetime LastCleaned;
  uint64   MaxAccessTime;
  uint32   UncompressedDataRate;
  uint64   LoadTime;
  uint64   UnloadTime;
  uint64   MountCount;
  datetime TimeOfLastMount;
  uint64   TotalMountTime;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning;
  uint64   UnitsUsed;
};
```

## <a name="members"></a><span data-ttu-id="3f31a-106">Membros</span><span class="sxs-lookup"><span data-stu-id="3f31a-106">Members</span></span>

<span data-ttu-id="3f31a-107">A classe **CIM \_ MediaAccessDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3f31a-107">The **CIM\_MediaAccessDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="3f31a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="3f31a-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="3f31a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3f31a-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3f31a-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="3f31a-110">Methods</span></span>

<span data-ttu-id="3f31a-111">A classe **CIM \_ MediaAccessDevice** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3f31a-111">The **CIM\_MediaAccessDevice** class has these methods.</span></span>



| <span data-ttu-id="3f31a-112">Método</span><span class="sxs-lookup"><span data-stu-id="3f31a-112">Method</span></span>                                               | <span data-ttu-id="3f31a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f31a-113">Description</span></span>                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="3f31a-114">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="3f31a-114">**LockMedia**</span></span>](cim-mediaaccessdevice-lockmedia.md) | <span data-ttu-id="3f31a-115">Bloqueia e desbloqueia a mídia removível em um dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="3f31a-115">Locks and unlocks removable media in a media access device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3f31a-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3f31a-116">Properties</span></span>

<span data-ttu-id="3f31a-117">A classe **CIM \_ MediaAccessDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3f31a-117">The **CIM\_MediaAccessDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f31a-118">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="3f31a-118">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-119">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f31a-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-121">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de armazenamento DMTF \| 1,9 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,11 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,12 "," MIF. \|Discos DMTF \| 3,7 "," MIF. \|Disco do host DMTF \| 1,2 "," MIF. \|Disco do host DMTF \| 1,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="3f31a-121">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7", "MIF.DMTF\|Host Disk\|001.2", "MIF.DMTF\|Host Disk\|001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-122">Uma matriz que contém os recursos do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="3f31a-122">An array that contains the capabilities of the media access device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3f31a-123">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3f31a-123">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3f31a-124">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="3f31a-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="3f31a-125">**Acesso sequencial** (2)</span><span class="sxs-lookup"><span data-stu-id="3f31a-125">**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="3f31a-126">**Acesso aleatório** (3)</span><span class="sxs-lookup"><span data-stu-id="3f31a-126">**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="3f31a-127">**Dá suporte à gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="3f31a-127">**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="3f31a-128">**Criptografia** (5)</span><span class="sxs-lookup"><span data-stu-id="3f31a-128">**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="3f31a-129">**Compactação** (6)</span><span class="sxs-lookup"><span data-stu-id="3f31a-129">**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="3f31a-130">**Dá suporte à mídia removida** (7)</span><span class="sxs-lookup"><span data-stu-id="3f31a-130">**Supports Removeable Media** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="3f31a-131">**Limpeza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="3f31a-131">**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="3f31a-132">**Limpeza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="3f31a-132">**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="3f31a-133">**Notificação inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="3f31a-133">**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="3f31a-134">**Dá suporte à mídia de dois lados** (11)</span><span class="sxs-lookup"><span data-stu-id="3f31a-134">**Supports Dual Sided Media** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="3f31a-135">**Ejeção de desmontagem não necessária** (12)</span><span class="sxs-lookup"><span data-stu-id="3f31a-135">**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3f31a-136">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3f31a-136">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-137">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3f31a-137">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-139">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM MediaAccessDevice**.**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="3f31a-139">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-140">Uma matriz de descrições de recursos para os itens na matriz de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="3f31a-140">An array of feature descriptions for the items in the **Capabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-141">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="3f31a-141">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3f31a-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-144">O nome do algoritmo ou da ferramenta usada pelo dispositivo para dar suporte à compactação.</span><span class="sxs-lookup"><span data-stu-id="3f31a-144">The name of the algorithm or tool used by the device to support compression.</span></span>

<span data-ttu-id="3f31a-145">Se um tipo de compactação não for especificado, um dos seguintes valores poderá ser usado:</span><span class="sxs-lookup"><span data-stu-id="3f31a-145">If a compression type is not specified, one of the following values can be used:</span></span>

-   <span data-ttu-id="3f31a-146">O suporte à compactação "desconhecida" é desconhecido ou não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="3f31a-146">"Unknown"   compression support is unknown or not specified.</span></span>
-   <span data-ttu-id="3f31a-147">Há suporte para compactação "compactada", mas o tipo é desconhecido ou não especificado.</span><span class="sxs-lookup"><span data-stu-id="3f31a-147">"Compressed"   compression is supported but the type is unknown or unspecified.</span></span>
-   <span data-ttu-id="3f31a-148">"Não compactado" o dispositivo não oferece suporte a recursos de compactação.</span><span class="sxs-lookup"><span data-stu-id="3f31a-148">"Not Compressed"   the device does not support compression capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-149">**Defaultblockize**</span><span class="sxs-lookup"><span data-stu-id="3f31a-149">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-150">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f31a-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-152">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **PUnit** ("byte")</span><span class="sxs-lookup"><span data-stu-id="3f31a-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-153">O tamanho do bloco padrão, em bytes, para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-153">The default block size, in bytes, for the device.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-154">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="3f31a-154">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3f31a-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-157">O tipo de detecção de erros e correção com suporte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-157">The type of error detection and correction supported by the device.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-158">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="3f31a-158">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-159">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3f31a-159">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-161">A data e a hora da última limpeza do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-161">The date and time when the device was last cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-162">**Loadtime**</span><span class="sxs-lookup"><span data-stu-id="3f31a-162">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-163">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f31a-163">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-165">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos"), **PUnit** ("segundo \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="3f31a-165">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-166">O tempo necessário, em milissegundos, para que o dispositivo possa ler ou gravar uma mídia depois que o dispositivo começar a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="3f31a-166">The time it takes, in milliseconds, for the device to be able to read or write a media after the device starts loading.</span></span> <span data-ttu-id="3f31a-167">Por exemplo, para unidades de disco, esse é o intervalo entre um disco que não está girando para o disco relatando que está pronto para operações de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3f31a-167">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write operations.</span></span> <span data-ttu-id="3f31a-168">Para unidades de fita, isso é iniciado quando a mídia é inserida e termina quando a unidade relata que está pronta para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-168">For tape drives, this starts when media is inserted and ends when the drive reports that it is ready for an application.</span></span> <span data-ttu-id="3f31a-169">Isso geralmente está na área de BOT (início de fita) da fita.</span><span class="sxs-lookup"><span data-stu-id="3f31a-169">This is usually at the tape's beginning-of-tape (BOT) area.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-170">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="3f31a-170">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-171">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f31a-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-173">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos"), **PUnit** ("segundo \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="3f31a-173">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-174">O tempo de acesso máximo da mídia, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="3f31a-174">The maximum access time of the media, in milliseconds.</span></span> <span data-ttu-id="3f31a-175">Para uma unidade de disco, isso representa a busca completa e o atraso de rotação completo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-175">For a disk drive, this represents full seek and full rotational delay.</span></span> <span data-ttu-id="3f31a-176">Para unidades de fita, isso representa uma pesquisa desde o início da fita até o ponto distante fisicamente.</span><span class="sxs-lookup"><span data-stu-id="3f31a-176">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-177">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="3f31a-177">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-178">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f31a-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-180">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **PUnit** ("byte")</span><span class="sxs-lookup"><span data-stu-id="3f31a-180">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-181">O tamanho máximo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-181">The maximum block size, in bytes, for media accessed by the device.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-182">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="3f31a-182">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-183">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f31a-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-185">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acesso sequencial DMTF \| 1,2 "," MIF. \|Disco do host DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="3f31a-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2", "MIF.DMTF\|Host Disk\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-186">O tamanho máximo, em kilobytes, da mídia com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-186">The maximum size, in kilobytes, of media supported by this device.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-187">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="3f31a-187">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-188">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f31a-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-190">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**")</span><span class="sxs-lookup"><span data-stu-id="3f31a-190">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**UnitsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-191">O número máximo de unidades que podem ser usadas antes de o dispositivo ser limpo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-191">The maximum number of units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="3f31a-192">**UnitsDescription** define como o tipo de unidade.</span><span class="sxs-lookup"><span data-stu-id="3f31a-192">**UnitsDescription** defines how the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-193">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="3f31a-193">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-194">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3f31a-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-196">**true** se a mídia estiver bloqueada no dispositivo e não puder ser ejetada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3f31a-196">**true** if the media is locked in the device and can not be ejected; otherwise, **false**.</span></span> <span data-ttu-id="3f31a-197">Para dispositivos não removíveis, esse valor deve ser **true**.</span><span class="sxs-lookup"><span data-stu-id="3f31a-197">For non-removable devices, this value should be **true**.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-198">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="3f31a-198">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-199">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f31a-199">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-201">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **PUnit** ("byte")</span><span class="sxs-lookup"><span data-stu-id="3f31a-201">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-202">O tamanho mínimo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-202">The minimum block size, in bytes, for media accessed by the device.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-203">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="3f31a-203">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-204">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f31a-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-206">Qualificadores: **contador**</span><span class="sxs-lookup"><span data-stu-id="3f31a-206">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-207">O número de vezes que a mídia foi montada para transferência de dados ou para limpar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-207">The number of times that media has been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="3f31a-208">Se o dispositivo não oferecer suporte a mídia removível, essa propriedade deverá ser definida como zero.</span><span class="sxs-lookup"><span data-stu-id="3f31a-208">If the device does not support removable media, this property should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-209">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="3f31a-209">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-210">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3f31a-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-212">**true** se o dispositivo precisar de limpeza; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3f31a-212">**true** if the device needs cleaning; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="3f31a-213">A propriedade **Capabilities** indica se a limpeza manual ou automática é possível.</span><span class="sxs-lookup"><span data-stu-id="3f31a-213">The **Capabilities** property indicates whether manual or automatic cleaning is possible.</span></span>

 

</dd> <dt>

<span data-ttu-id="3f31a-214">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="3f31a-214">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-215">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f31a-215">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-217">Se o dispositivo der suporte a várias mídias individuais, essa propriedade definirá o número máximo que pode ser suportado ou inserido.</span><span class="sxs-lookup"><span data-stu-id="3f31a-217">If the device supports multiple individual media, this property defines the maximum number which can be supported or inserted.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-218">**Segurança**</span><span class="sxs-lookup"><span data-stu-id="3f31a-218">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-219">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f31a-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-221">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Discos DMTF \| 3,22 ")</span><span class="sxs-lookup"><span data-stu-id="3f31a-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Disks\|003.22")</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-222">A segurança operacional para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-222">The operational security for the device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3f31a-223">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="3f31a-223">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3f31a-224">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="3f31a-224">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="3f31a-225">**Nenhum** (3)</span><span class="sxs-lookup"><span data-stu-id="3f31a-225">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Only"></span><span id="read_only"></span><span id="READ_ONLY"></span>

<span data-ttu-id="3f31a-226">**Somente leitura** (4)</span><span class="sxs-lookup"><span data-stu-id="3f31a-226">**Read Only** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

<span data-ttu-id="3f31a-227">**Bloqueado** (5)</span><span class="sxs-lookup"><span data-stu-id="3f31a-227">**Locked Out** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

<span data-ttu-id="3f31a-228">**Bypass de inicialização** (6)</span><span class="sxs-lookup"><span data-stu-id="3f31a-228">**Boot Bypass** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

<span data-ttu-id="3f31a-229">**Bypass de inicialização e somente leitura** (7)</span><span class="sxs-lookup"><span data-stu-id="3f31a-229">**Boot Bypass and Read Only** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3f31a-230">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="3f31a-230">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-231">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3f31a-231">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-233">A data e a hora mais recentes quando a mídia foi montada no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-233">The most recent date and time when media was mounted on the device.</span></span> <span data-ttu-id="3f31a-234">Essa propriedade só é usada por dispositivos que oferecem suporte a mídia removível.</span><span class="sxs-lookup"><span data-stu-id="3f31a-234">This property is only used by devices that support removable media.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-235">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="3f31a-235">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-236">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f31a-236">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-238">O tempo, em segundos, que a mídia foi montada para transferência de dados ou para limpar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-238">The time, in seconds, that media has been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="3f31a-239">Se o dispositivo não oferecer suporte a mídia removível, essa propriedade deverá ser definida como zero.</span><span class="sxs-lookup"><span data-stu-id="3f31a-239">If the device does not support removable media, this property should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-240">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="3f31a-240">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-241">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f31a-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-243">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes por segundo"), **PUnit** ("byte/segundo \* 10 ^ 3")</span><span class="sxs-lookup"><span data-stu-id="3f31a-243">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes per Second"), **PUnit** ("byte / second \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-244">A taxa de transferência de dados sustentada em kilobytes na qual o dispositivo pode ler e gravar em uma mídia.</span><span class="sxs-lookup"><span data-stu-id="3f31a-244">The sustained data transfer rate in kilobytes at which the device can read and write to a media.</span></span> <span data-ttu-id="3f31a-245">Essa é uma taxa de dados bruta e prolongada.</span><span class="sxs-lookup"><span data-stu-id="3f31a-245">This is a sustained, raw data rate.</span></span> <span data-ttu-id="3f31a-246">Taxas ou taxas máximas com compactação não devem ser relatadas nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="3f31a-246">Maximum rates or rates with compression should not be reported in this property.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-247">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="3f31a-247">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-248">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3f31a-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-250">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**","**CIM \_ MediaAccessDevice**.**UnitsUsed**")</span><span class="sxs-lookup"><span data-stu-id="3f31a-250">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**MaxUnitsBeforeCleaning**", "**CIM\_MediaAccessDevice**.**UnitsUsed**")</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-251">Descreve o tipo de unidade das propriedades **MaxUnitsBeforeCleaning** e **UnitsUsed** .</span><span class="sxs-lookup"><span data-stu-id="3f31a-251">Describes the unit type of the **MaxUnitsBeforeCleaning** and **UnitsUsed** properties.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-252">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="3f31a-252">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-253">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f31a-253">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-255">Qualificadores: [**medidor**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**","**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**")</span><span class="sxs-lookup"><span data-stu-id="3f31a-255">Qualifiers: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**UnitsDescription**", "**CIM\_MediaAccessDevice**.**MaxUnitsBeforeCleaning**")</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-256">O número de unidades usadas pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-256">The number of units used by the device.</span></span> <span data-ttu-id="3f31a-257">Essa propriedade é usada para determinar quando o dispositivo deve ser limpo.</span><span class="sxs-lookup"><span data-stu-id="3f31a-257">This property is used to determine when the device should be cleaned.</span></span> <span data-ttu-id="3f31a-258">**UnitsDescription** define como o tipo de unidade.</span><span class="sxs-lookup"><span data-stu-id="3f31a-258">**UnitsDescription** defines how the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-259">**Descarregar**</span><span class="sxs-lookup"><span data-stu-id="3f31a-259">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-260">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f31a-260">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f31a-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-262">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos"), **PUnit** ("segundo \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="3f31a-262">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-263">O tempo necessário, em milissegundos, para o dispositivo fazer a transição da leitura ou gravação de mídia para descarregamento.</span><span class="sxs-lookup"><span data-stu-id="3f31a-263">The time it takes, in milliseconds, for the device to transition from reading or writing media to unloading.</span></span> <span data-ttu-id="3f31a-264">Por exemplo, para unidades de disco, esse é o intervalo entre um disco girando em velocidades nominais e um disco não está girando.</span><span class="sxs-lookup"><span data-stu-id="3f31a-264">For example, for disk drives, this is the interval between a disk spinning at nominal speeds and a disk not spinning.</span></span> <span data-ttu-id="3f31a-265">Para unidades de fita, esse é o momento de uma mídia passar de seu BOT para ser totalmente ejetado e acessível a um elemento selecionador ou a um operador humano.</span><span class="sxs-lookup"><span data-stu-id="3f31a-265">For tape drives, this is the time for a media to go from its BOT to being fully ejected and accessible to a picker element or human operator.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f31a-266">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f31a-266">Requirements</span></span>



| <span data-ttu-id="3f31a-267">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f31a-267">Requirement</span></span> | <span data-ttu-id="3f31a-268">Valor</span><span class="sxs-lookup"><span data-stu-id="3f31a-268">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f31a-269">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f31a-269">Minimum supported client</span></span><br/> | <span data-ttu-id="3f31a-270">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3f31a-270">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3f31a-271">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f31a-271">Minimum supported server</span></span><br/> | <span data-ttu-id="3f31a-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3f31a-272">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3f31a-273">Namespace</span><span class="sxs-lookup"><span data-stu-id="3f31a-273">Namespace</span></span><br/>                | <span data-ttu-id="3f31a-274">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3f31a-274">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3f31a-275">MOF</span><span class="sxs-lookup"><span data-stu-id="3f31a-275">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f31a-276"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f31a-276"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f31a-277">DLL</span><span class="sxs-lookup"><span data-stu-id="3f31a-277">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f31a-278"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3f31a-278"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3f31a-279">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f31a-279">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f31a-280">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3f31a-280">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

