---
description: A \_ classe CIM NFS representa um sistema de arquivos remoto que é montado, usando o protocolo NFS (sistema de arquivos de rede), de um sistema de computador.
ms.assetid: 24eba28f-fbd5-4aa3-a7c7-a611269d55ac
ms.tgt_platform: multiple
title: Classe CIM_NFS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NFS
- CIM_NFS.AttributeCaching
- CIM_NFS.AttributeCachingForDirectoriesMax
- CIM_NFS.AttributeCachingForDirectoriesMin
- CIM_NFS.AttributeCachingForRegularFilesMax
- CIM_NFS.AttributeCachingForRegularFilesMin
- CIM_NFS.AvailableSpace
- CIM_NFS.BlockSize
- CIM_NFS.Caption
- CIM_NFS.CasePreserved
- CIM_NFS.CaseSensitive
- CIM_NFS.CodeSet
- CIM_NFS.CompressionMethod
- CIM_NFS.CreationClassName
- CIM_NFS.CSCreationClassName
- CIM_NFS.CSName
- CIM_NFS.Description
- CIM_NFS.EncryptionMethod
- CIM_NFS.FileSystemSize
- CIM_NFS.ForegroundMount
- CIM_NFS.HardMount
- CIM_NFS.InstallDate
- CIM_NFS.Interrupt
- CIM_NFS.MaxFileNameLength
- CIM_NFS.MountFailureRetries
- CIM_NFS.Name
- CIM_NFS.ReadBufferSize
- CIM_NFS.ReadOnly
- CIM_NFS.RetransmissionAttempts
- CIM_NFS.RetransmissionTimeout
- CIM_NFS.Root
- CIM_NFS.ServerCommunicationPort
- CIM_NFS.Status
- CIM_NFS.WriteBufferSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0dcfb44fdcd035ca47cbe3056da2a081ef2ae07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646421"
---
# <a name="cim_nfs-class"></a><span data-ttu-id="86ecd-103">\_Classe NFS CIM</span><span class="sxs-lookup"><span data-stu-id="86ecd-103">CIM\_NFS class</span></span>

<span data-ttu-id="86ecd-104">A classe **CIM \_ NFS** representa um sistema de arquivos remoto que é montado, usando o protocolo NFS (sistema de arquivos de rede), de um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="86ecd-104">The **CIM\_NFS** class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span> <span data-ttu-id="86ecd-105">As propriedades do objeto NFS correspondem aos aspectos operacionais da montagem e representam a configuração do lado do cliente para acesso de NFS.</span><span class="sxs-lookup"><span data-stu-id="86ecd-105">The properties of the NFS object correspond to the operational aspects of the mount and represent the client-side configuration for NFS access.</span></span> <span data-ttu-id="86ecd-106">O tipo de sistema de arquivos deve ser definido para indicar o tipo de sistema de arquivos como ele aparece para o cliente.</span><span class="sxs-lookup"><span data-stu-id="86ecd-106">The file system type should be set to indicate the type of file system as it appears to the client.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="86ecd-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="86ecd-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="86ecd-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="86ecd-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="86ecd-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="86ecd-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="86ecd-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="86ecd-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="86ecd-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86ecd-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4FB-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_NFS : CIM_RemoteFileSystem
{
  boolean  AttributeCaching;
  uint16   AttributeCachingForDirectoriesMax;
  uint16   AttributeCachingForDirectoriesMin;
  uint16   AttributeCachingForRegularFilesMax;
  uint16   AttributeCachingForRegularFilesMin;
  uint64   AvailableSpace;
  uint64   BlockSize;
  string   Caption;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  boolean  ForegroundMount;
  boolean  HardMount;
  datetime InstallDate;
  boolean  Interrupt;
  uint32   MaxFileNameLength;
  uint16   MountFailureRetries;
  string   Name;
  uint64   ReadBufferSize;
  boolean  ReadOnly;
  uint16   RetransmissionAttempts;
  uint32   RetransmissionTimeout;
  string   Root;
  uint32   ServerCommunicationPort;
  string   Status;
  uint64   WriteBufferSize;
};
```

## <a name="members"></a><span data-ttu-id="86ecd-112">Membros</span><span class="sxs-lookup"><span data-stu-id="86ecd-112">Members</span></span>

<span data-ttu-id="86ecd-113">A classe **CIM \_ NFS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="86ecd-113">The **CIM\_NFS** class has these types of members:</span></span>

-   [<span data-ttu-id="86ecd-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="86ecd-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="86ecd-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="86ecd-115">Properties</span></span>

<span data-ttu-id="86ecd-116">A classe **CIM \_ NFS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="86ecd-116">The **CIM\_NFS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="86ecd-117">**AttributeCaching**</span><span class="sxs-lookup"><span data-stu-id="86ecd-117">**AttributeCaching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-118">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="86ecd-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-120">Se **for true**, o cache de atributo de controle será habilitado.</span><span class="sxs-lookup"><span data-stu-id="86ecd-120">If **TRUE**, control attribute caching is enabled.</span></span> <span data-ttu-id="86ecd-121">Se **for false**, o cache de atributo de controle será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="86ecd-121">If **FALSE**, control attribute caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-122">**AttributeCachingForDirectoriesMax**</span><span class="sxs-lookup"><span data-stu-id="86ecd-122">**AttributeCachingForDirectoriesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-123">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ecd-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-125">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="86ecd-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-126">Número máximo de segundos que os atributos armazenados em cache são mantidos após a atualização do diretório.</span><span class="sxs-lookup"><span data-stu-id="86ecd-126">Maximum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-127">**AttributeCachingForDirectoriesMin**</span><span class="sxs-lookup"><span data-stu-id="86ecd-127">**AttributeCachingForDirectoriesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-128">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ecd-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-130">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="86ecd-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-131">Número mínimo de segundos que os atributos armazenados em cache são mantidos após a atualização do diretório.</span><span class="sxs-lookup"><span data-stu-id="86ecd-131">Minimum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-132">**AttributeCachingForRegularFilesMax**</span><span class="sxs-lookup"><span data-stu-id="86ecd-132">**AttributeCachingForRegularFilesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-133">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ecd-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-135">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="86ecd-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-136">Número máximo de segundos em que os atributos armazenados em cache são mantidos após a modificação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="86ecd-136">Maximum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-137">**AttributeCachingForRegularFilesMin**</span><span class="sxs-lookup"><span data-stu-id="86ecd-137">**AttributeCachingForRegularFilesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-138">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ecd-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-140">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="86ecd-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-141">Número mínimo de segundos em que os atributos armazenados em cache são mantidos após a modificação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="86ecd-141">Minimum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-142">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="86ecd-142">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-143">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="86ecd-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-145">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="86ecd-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-146">Quantidade total de espaço livre, em bytes, para o sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="86ecd-146">Total amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="86ecd-147">Se for desconhecido, insira 0.</span><span class="sxs-lookup"><span data-stu-id="86ecd-147">If unknown, enter 0.</span></span>

<span data-ttu-id="86ecd-148">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-148">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="86ecd-149">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="86ecd-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-150">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="86ecd-150">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-151">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="86ecd-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-153">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="86ecd-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-154">Os sistemas de arquivos podem ler ou gravar dados em blocos que são definidos independentemente das extensões de armazenamento subjacentes.</span><span class="sxs-lookup"><span data-stu-id="86ecd-154">File systems can read or write data in blocks that are defined independently of the underlying storage extents.</span></span> <span data-ttu-id="86ecd-155">Essa propriedade captura o tamanho do bloco do sistema de arquivos para o armazenamento e a recuperação de dados.</span><span class="sxs-lookup"><span data-stu-id="86ecd-155">This property captures the file system's block size for data storage and retrieval.</span></span>

<span data-ttu-id="86ecd-156">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-156">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="86ecd-157">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="86ecd-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-158">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="86ecd-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="86ecd-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-161">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="86ecd-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-162">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="86ecd-162">Short textual description of the object.</span></span>

<span data-ttu-id="86ecd-163">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-164">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="86ecd-164">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-165">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="86ecd-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-167">Se **for true**, o caso dos nomes de arquivo será preservado.</span><span class="sxs-lookup"><span data-stu-id="86ecd-167">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="86ecd-168">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-168">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-169">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="86ecd-169">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-170">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="86ecd-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-172">Se **verdadeiro**, os nomes de arquivo com diferenciação de maiúsculas e minúsculas têm suporte.</span><span class="sxs-lookup"><span data-stu-id="86ecd-172">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="86ecd-173">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-174">**Código de**</span><span class="sxs-lookup"><span data-stu-id="86ecd-174">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-175">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ecd-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-177">Conjuntos de caracteres ou codificação com suporte no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="86ecd-177">Character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="86ecd-178">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-178">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="86ecd-179">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="86ecd-179">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="86ecd-180">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="86ecd-180">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="86ecd-181">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="86ecd-181">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="86ecd-182">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="86ecd-182">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="86ecd-183">**ISO2022** (4)</span><span class="sxs-lookup"><span data-stu-id="86ecd-183">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="86ecd-184">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="86ecd-184">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="86ecd-185">**Código UNIX estendido** (6)</span><span class="sxs-lookup"><span data-stu-id="86ecd-185">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="86ecd-186">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="86ecd-186">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="86ecd-187">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="86ecd-187">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="86ecd-188">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="86ecd-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="86ecd-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-191">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,7 ")</span><span class="sxs-lookup"><span data-stu-id="86ecd-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-192">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="86ecd-192">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="86ecd-193">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="86ecd-193">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="86ecd-194">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="86ecd-194">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="86ecd-195">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="86ecd-195">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="86ecd-196">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-196">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-197">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="86ecd-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="86ecd-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-200">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="86ecd-200">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-201">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="86ecd-201">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="86ecd-202">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="86ecd-202">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="86ecd-203">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-203">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-204">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="86ecd-204">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-205">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="86ecd-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-207">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="86ecd-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-208">Nome da classe de criação do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="86ecd-208">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="86ecd-209">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-209">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-210">**CSName**</span><span class="sxs-lookup"><span data-stu-id="86ecd-210">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-211">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="86ecd-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-213">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-computersystem.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="86ecd-213">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-214">Nome do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="86ecd-214">Scoping computer system's name.</span></span>

<span data-ttu-id="86ecd-215">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-215">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-216">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="86ecd-216">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="86ecd-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-219">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="86ecd-219">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-220">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="86ecd-220">Textual description of the object.</span></span>

<span data-ttu-id="86ecd-221">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-222">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="86ecd-222">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="86ecd-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-225">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,8 ")</span><span class="sxs-lookup"><span data-stu-id="86ecd-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-226">Cadeia de caracteres de forma livre que identifica o algoritmo ou a ferramenta usada para criptografar um arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="86ecd-226">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="86ecd-227">Se o esquema de criptografia não for indulged (por motivos de segurança, por exemplo), use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="86ecd-227">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="86ecd-228">Se o arquivo estiver criptografado, mas seu esquema de criptografia for desconhecido ou não for divulgado, use "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="86ecd-228">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="86ecd-229">Se o arquivo lógico não estiver criptografado, use "não criptografado".</span><span class="sxs-lookup"><span data-stu-id="86ecd-229">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="86ecd-230">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-230">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-231">**Filesystemize**</span><span class="sxs-lookup"><span data-stu-id="86ecd-231">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-232">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="86ecd-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-234">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="86ecd-234">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-235">Tamanho total do sistema de arquivos, em bytes.</span><span class="sxs-lookup"><span data-stu-id="86ecd-235">Total size of the file system, in bytes.</span></span> <span data-ttu-id="86ecd-236">Se for desconhecido, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="86ecd-236">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="86ecd-237">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-237">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="86ecd-238">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="86ecd-238">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-239">**ForegroundMount**</span><span class="sxs-lookup"><span data-stu-id="86ecd-239">**ForegroundMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-240">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="86ecd-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-242">Se **for true**, as repetições serão executadas em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="86ecd-242">If **TRUE**, retries are performed in the foreground.</span></span> <span data-ttu-id="86ecd-243">Se **for false**, e a primeira tentativa de montagem falhar, as novas tentativas serão executadas em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="86ecd-243">If **FALSE**, and the first mount attempt fails, retries are performed in the background.</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-244">**HardMount**</span><span class="sxs-lookup"><span data-stu-id="86ecd-244">**HardMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-245">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="86ecd-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-247">Se **for true**, depois que o sistema de arquivos for montado, as solicitações de NFS serão repetidas até que o sistema de hospedagem responda.</span><span class="sxs-lookup"><span data-stu-id="86ecd-247">If **TRUE**, after the file system is mounted, NFS requests are retried until the hosting system responds.</span></span> <span data-ttu-id="86ecd-248">Se for **false**, depois que o sistema de arquivos for montado, um erro será retornado se o sistema de hospedagem não responder.</span><span class="sxs-lookup"><span data-stu-id="86ecd-248">If **FALSE**, after the file system is mounted, an error is returned if the hosting system does not respond.</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="86ecd-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-250">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="86ecd-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-252">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="86ecd-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-253">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="86ecd-253">Date and time the object was installed.</span></span> <span data-ttu-id="86ecd-254">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="86ecd-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="86ecd-255">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-256">**Atividades**</span><span class="sxs-lookup"><span data-stu-id="86ecd-256">**Interrupt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-257">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="86ecd-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-259">Se **verdadeiro**, as interrupções são permitidas para montagens rígidas.</span><span class="sxs-lookup"><span data-stu-id="86ecd-259">If **TRUE**, interrupts are permitted for hard mounts.</span></span> <span data-ttu-id="86ecd-260">Se **for false**, as interrupções serão ignoradas para montagens físicas.</span><span class="sxs-lookup"><span data-stu-id="86ecd-260">If **FALSE**, interrupts are ignored for hard mounts.</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-261">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="86ecd-261">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-262">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86ecd-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-264">Comprimento máximo de um nome de arquivo dentro do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="86ecd-264">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="86ecd-265">Um valor de 0 (zero) indica que não há limite para o comprimento do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="86ecd-265">A value of 0 (zero)indicates that there is no limit for file name length.</span></span>

<span data-ttu-id="86ecd-266">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-266">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-267">**MountFailureRetries**</span><span class="sxs-lookup"><span data-stu-id="86ecd-267">**MountFailureRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-268">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ecd-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-270">Número máximo de tentativas de falha de montagem permitidas.</span><span class="sxs-lookup"><span data-stu-id="86ecd-270">Maximum number of mount failure retries that are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-271">**Nome**</span><span class="sxs-lookup"><span data-stu-id="86ecd-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-272">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="86ecd-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-274">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="86ecd-274">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-275">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="86ecd-275">Label by which the object is known.</span></span> <span data-ttu-id="86ecd-276">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="86ecd-276">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="86ecd-277">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-277">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-278">**ReadBufferSize**</span><span class="sxs-lookup"><span data-stu-id="86ecd-278">**ReadBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-279">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="86ecd-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-281">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="86ecd-281">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-282">Tamanho do buffer de leitura, em bytes.</span><span class="sxs-lookup"><span data-stu-id="86ecd-282">Read buffer size, in bytes.</span></span>

<span data-ttu-id="86ecd-283">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="86ecd-283">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-284">**ReadOnly (somente-leitura)**</span><span class="sxs-lookup"><span data-stu-id="86ecd-284">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-285">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="86ecd-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-287">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="86ecd-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-288">Se **for true**, o sistema de arquivos será designado como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="86ecd-288">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="86ecd-289">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-289">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-290">**RetransmissionAttempts**</span><span class="sxs-lookup"><span data-stu-id="86ecd-290">**RetransmissionAttempts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-291">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ecd-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-293">Número máximo de retransmissões de NFS permitidas.</span><span class="sxs-lookup"><span data-stu-id="86ecd-293">Maximum number of NFS retransmissions allowed.</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-294">**RetransmissionTimeout**</span><span class="sxs-lookup"><span data-stu-id="86ecd-294">**RetransmissionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-295">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86ecd-295">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-297">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("décimos de segundos")</span><span class="sxs-lookup"><span data-stu-id="86ecd-297">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of seconds")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-298">Tempo limite do NFS, em décimos de segundo.</span><span class="sxs-lookup"><span data-stu-id="86ecd-298">NFS time-out, in tenths of a second.</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-299">**Básica**</span><span class="sxs-lookup"><span data-stu-id="86ecd-299">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="86ecd-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-302">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="86ecd-302">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-303">Nome do caminho ou outras informações que definem a raiz do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="86ecd-303">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="86ecd-304">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-304">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-305">**ServerCommunicationPort**</span><span class="sxs-lookup"><span data-stu-id="86ecd-305">**ServerCommunicationPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-306">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86ecd-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-308">Número da porta UDP do sistema do computador remoto.</span><span class="sxs-lookup"><span data-stu-id="86ecd-308">Remote computer system's UDP port number.</span></span>

</dd> <dt>

<span data-ttu-id="86ecd-309">**Status**</span><span class="sxs-lookup"><span data-stu-id="86ecd-309">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-310">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="86ecd-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-312">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="86ecd-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-313">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="86ecd-313">Current status of the object.</span></span>

<span data-ttu-id="86ecd-314">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="86ecd-315">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="86ecd-315">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="86ecd-316">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="86ecd-316">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="86ecd-317">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="86ecd-317">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="86ecd-318">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="86ecd-318">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="86ecd-319">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="86ecd-319">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="86ecd-320">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="86ecd-320">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="86ecd-321">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="86ecd-321">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="86ecd-322">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="86ecd-322">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="86ecd-323">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="86ecd-323">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="86ecd-324">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="86ecd-324">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="86ecd-325">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="86ecd-325">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="86ecd-326">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="86ecd-326">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="86ecd-327">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="86ecd-327">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="86ecd-328">**WriteBufferSize**</span><span class="sxs-lookup"><span data-stu-id="86ecd-328">**WriteBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ecd-329">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="86ecd-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86ecd-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ecd-331">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="86ecd-331">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="86ecd-332">Tamanho do buffer de gravação, em bytes.</span><span class="sxs-lookup"><span data-stu-id="86ecd-332">Write buffer size, in bytes.</span></span>

<span data-ttu-id="86ecd-333">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="86ecd-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86ecd-334">Comentários</span><span class="sxs-lookup"><span data-stu-id="86ecd-334">Remarks</span></span>

<span data-ttu-id="86ecd-335">A classe **CIM \_ NFS** é derivada do [**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md).</span><span class="sxs-lookup"><span data-stu-id="86ecd-335">The **CIM\_NFS** class is derived from [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md).</span></span>

<span data-ttu-id="86ecd-336">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="86ecd-336">WMI does not implement this class.</span></span>

<span data-ttu-id="86ecd-337">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="86ecd-337">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="86ecd-338">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="86ecd-338">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="86ecd-339">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86ecd-339">Requirements</span></span>



| <span data-ttu-id="86ecd-340">Requisito</span><span class="sxs-lookup"><span data-stu-id="86ecd-340">Requirement</span></span> | <span data-ttu-id="86ecd-341">Valor</span><span class="sxs-lookup"><span data-stu-id="86ecd-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86ecd-342">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86ecd-342">Minimum supported client</span></span><br/> | <span data-ttu-id="86ecd-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86ecd-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86ecd-344">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86ecd-344">Minimum supported server</span></span><br/> | <span data-ttu-id="86ecd-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86ecd-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86ecd-346">Namespace</span><span class="sxs-lookup"><span data-stu-id="86ecd-346">Namespace</span></span><br/>                | <span data-ttu-id="86ecd-347">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="86ecd-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="86ecd-348">MOF</span><span class="sxs-lookup"><span data-stu-id="86ecd-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86ecd-349"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86ecd-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="86ecd-350">DLL</span><span class="sxs-lookup"><span data-stu-id="86ecd-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86ecd-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86ecd-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86ecd-352">Confira também</span><span class="sxs-lookup"><span data-stu-id="86ecd-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86ecd-353">**\_REMOTEFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="86ecd-353">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> </dl>

 

