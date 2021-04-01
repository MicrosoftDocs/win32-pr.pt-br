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
# <a name="cim_nfs-class"></a><span data-ttu-id="87551-103">\_Classe NFS CIM</span><span class="sxs-lookup"><span data-stu-id="87551-103">CIM\_NFS class</span></span>

<span data-ttu-id="87551-104">A classe **CIM \_ NFS** representa um sistema de arquivos remoto que é montado, usando o protocolo NFS (sistema de arquivos de rede), de um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="87551-104">The **CIM\_NFS** class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span> <span data-ttu-id="87551-105">As propriedades do objeto NFS correspondem aos aspectos operacionais da montagem e representam a configuração do lado do cliente para acesso de NFS.</span><span class="sxs-lookup"><span data-stu-id="87551-105">The properties of the NFS object correspond to the operational aspects of the mount and represent the client-side configuration for NFS access.</span></span> <span data-ttu-id="87551-106">O tipo de sistema de arquivos deve ser definido para indicar o tipo de sistema de arquivos como ele aparece para o cliente.</span><span class="sxs-lookup"><span data-stu-id="87551-106">The file system type should be set to indicate the type of file system as it appears to the client.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87551-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="87551-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="87551-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="87551-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="87551-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="87551-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="87551-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="87551-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="87551-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87551-111">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="87551-112">Membros</span><span class="sxs-lookup"><span data-stu-id="87551-112">Members</span></span>

<span data-ttu-id="87551-113">A classe **CIM \_ NFS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="87551-113">The **CIM\_NFS** class has these types of members:</span></span>

-   [<span data-ttu-id="87551-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="87551-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87551-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="87551-115">Properties</span></span>

<span data-ttu-id="87551-116">A classe **CIM \_ NFS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="87551-116">The **CIM\_NFS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87551-117">**AttributeCaching**</span><span class="sxs-lookup"><span data-stu-id="87551-117">**AttributeCaching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-118">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="87551-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87551-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87551-120">Se **for true**, o cache de atributo de controle será habilitado.</span><span class="sxs-lookup"><span data-stu-id="87551-120">If **TRUE**, control attribute caching is enabled.</span></span> <span data-ttu-id="87551-121">Se **for false**, o cache de atributo de controle será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="87551-121">If **FALSE**, control attribute caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="87551-122">**AttributeCachingForDirectoriesMax**</span><span class="sxs-lookup"><span data-stu-id="87551-122">**AttributeCachingForDirectoriesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-123">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87551-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87551-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-125">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="87551-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="87551-126">Número máximo de segundos que os atributos armazenados em cache são mantidos após a atualização do diretório.</span><span class="sxs-lookup"><span data-stu-id="87551-126">Maximum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="87551-127">**AttributeCachingForDirectoriesMin**</span><span class="sxs-lookup"><span data-stu-id="87551-127">**AttributeCachingForDirectoriesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-128">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87551-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87551-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-130">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="87551-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="87551-131">Número mínimo de segundos que os atributos armazenados em cache são mantidos após a atualização do diretório.</span><span class="sxs-lookup"><span data-stu-id="87551-131">Minimum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="87551-132">**AttributeCachingForRegularFilesMax**</span><span class="sxs-lookup"><span data-stu-id="87551-132">**AttributeCachingForRegularFilesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-133">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87551-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87551-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-135">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="87551-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="87551-136">Número máximo de segundos em que os atributos armazenados em cache são mantidos após a modificação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="87551-136">Maximum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="87551-137">**AttributeCachingForRegularFilesMin**</span><span class="sxs-lookup"><span data-stu-id="87551-137">**AttributeCachingForRegularFilesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-138">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87551-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87551-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-140">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="87551-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="87551-141">Número mínimo de segundos em que os atributos armazenados em cache são mantidos após a modificação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="87551-141">Minimum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="87551-142">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="87551-142">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-143">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="87551-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="87551-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-145">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="87551-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="87551-146">Quantidade total de espaço livre, em bytes, para o sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="87551-146">Total amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="87551-147">Se for desconhecido, insira 0.</span><span class="sxs-lookup"><span data-stu-id="87551-147">If unknown, enter 0.</span></span>

<span data-ttu-id="87551-148">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-148">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="87551-149">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="87551-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="87551-150">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="87551-150">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-151">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="87551-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="87551-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-153">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="87551-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="87551-154">Os sistemas de arquivos podem ler ou gravar dados em blocos que são definidos independentemente das extensões de armazenamento subjacentes.</span><span class="sxs-lookup"><span data-stu-id="87551-154">File systems can read or write data in blocks that are defined independently of the underlying storage extents.</span></span> <span data-ttu-id="87551-155">Essa propriedade captura o tamanho do bloco do sistema de arquivos para o armazenamento e a recuperação de dados.</span><span class="sxs-lookup"><span data-stu-id="87551-155">This property captures the file system's block size for data storage and retrieval.</span></span>

<span data-ttu-id="87551-156">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-156">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="87551-157">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="87551-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="87551-158">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="87551-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87551-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87551-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-161">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="87551-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="87551-162">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="87551-162">Short textual description of the object.</span></span>

<span data-ttu-id="87551-163">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="87551-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="87551-164">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="87551-164">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-165">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="87551-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87551-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87551-167">Se **for true**, o caso dos nomes de arquivo será preservado.</span><span class="sxs-lookup"><span data-stu-id="87551-167">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="87551-168">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-168">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="87551-169">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="87551-169">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-170">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="87551-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87551-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87551-172">Se **verdadeiro**, os nomes de arquivo com diferenciação de maiúsculas e minúsculas têm suporte.</span><span class="sxs-lookup"><span data-stu-id="87551-172">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="87551-173">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="87551-174">**Código de**</span><span class="sxs-lookup"><span data-stu-id="87551-174">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-175">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87551-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="87551-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87551-177">Conjuntos de caracteres ou codificação com suporte no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="87551-177">Character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="87551-178">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-178">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="87551-179">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="87551-179">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="87551-180">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="87551-180">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="87551-181">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="87551-181">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="87551-182">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="87551-182">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="87551-183">**ISO2022** (4)</span><span class="sxs-lookup"><span data-stu-id="87551-183">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="87551-184">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="87551-184">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="87551-185">**Código UNIX estendido** (6)</span><span class="sxs-lookup"><span data-stu-id="87551-185">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="87551-186">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="87551-186">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="87551-187">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="87551-187">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="87551-188">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="87551-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87551-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87551-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-191">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,7 ")</span><span class="sxs-lookup"><span data-stu-id="87551-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="87551-192">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="87551-192">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="87551-193">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="87551-193">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="87551-194">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="87551-194">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="87551-195">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="87551-195">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="87551-196">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-196">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="87551-197">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="87551-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87551-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87551-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-200">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="87551-200">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="87551-201">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="87551-201">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="87551-202">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="87551-202">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="87551-203">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-203">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="87551-204">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="87551-204">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-205">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87551-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87551-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-207">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="87551-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="87551-208">Nome da classe de criação do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="87551-208">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="87551-209">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-209">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="87551-210">**CSName**</span><span class="sxs-lookup"><span data-stu-id="87551-210">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-211">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87551-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87551-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-213">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-computersystem.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="87551-213">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="87551-214">Nome do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="87551-214">Scoping computer system's name.</span></span>

<span data-ttu-id="87551-215">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-215">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="87551-216">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="87551-216">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87551-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87551-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-219">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="87551-219">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="87551-220">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="87551-220">Textual description of the object.</span></span>

<span data-ttu-id="87551-221">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="87551-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="87551-222">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="87551-222">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87551-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87551-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-225">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,8 ")</span><span class="sxs-lookup"><span data-stu-id="87551-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="87551-226">Cadeia de caracteres de forma livre que identifica o algoritmo ou a ferramenta usada para criptografar um arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="87551-226">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="87551-227">Se o esquema de criptografia não for indulged (por motivos de segurança, por exemplo), use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="87551-227">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="87551-228">Se o arquivo estiver criptografado, mas seu esquema de criptografia for desconhecido ou não for divulgado, use "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="87551-228">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="87551-229">Se o arquivo lógico não estiver criptografado, use "não criptografado".</span><span class="sxs-lookup"><span data-stu-id="87551-229">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="87551-230">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-230">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="87551-231">**Filesystemize**</span><span class="sxs-lookup"><span data-stu-id="87551-231">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-232">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="87551-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="87551-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-234">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="87551-234">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="87551-235">Tamanho total do sistema de arquivos, em bytes.</span><span class="sxs-lookup"><span data-stu-id="87551-235">Total size of the file system, in bytes.</span></span> <span data-ttu-id="87551-236">Se for desconhecido, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="87551-236">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="87551-237">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-237">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="87551-238">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="87551-238">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="87551-239">**ForegroundMount**</span><span class="sxs-lookup"><span data-stu-id="87551-239">**ForegroundMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-240">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="87551-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87551-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87551-242">Se **for true**, as repetições serão executadas em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="87551-242">If **TRUE**, retries are performed in the foreground.</span></span> <span data-ttu-id="87551-243">Se **for false**, e a primeira tentativa de montagem falhar, as novas tentativas serão executadas em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="87551-243">If **FALSE**, and the first mount attempt fails, retries are performed in the background.</span></span>

</dd> <dt>

<span data-ttu-id="87551-244">**HardMount**</span><span class="sxs-lookup"><span data-stu-id="87551-244">**HardMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-245">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="87551-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87551-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87551-247">Se **for true**, depois que o sistema de arquivos for montado, as solicitações de NFS serão repetidas até que o sistema de hospedagem responda.</span><span class="sxs-lookup"><span data-stu-id="87551-247">If **TRUE**, after the file system is mounted, NFS requests are retried until the hosting system responds.</span></span> <span data-ttu-id="87551-248">Se for **false**, depois que o sistema de arquivos for montado, um erro será retornado se o sistema de hospedagem não responder.</span><span class="sxs-lookup"><span data-stu-id="87551-248">If **FALSE**, after the file system is mounted, an error is returned if the hosting system does not respond.</span></span>

</dd> <dt>

<span data-ttu-id="87551-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="87551-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-250">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="87551-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="87551-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-252">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="87551-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="87551-253">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="87551-253">Date and time the object was installed.</span></span> <span data-ttu-id="87551-254">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="87551-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="87551-255">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="87551-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="87551-256">**Atividades**</span><span class="sxs-lookup"><span data-stu-id="87551-256">**Interrupt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-257">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="87551-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87551-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87551-259">Se **verdadeiro**, as interrupções são permitidas para montagens rígidas.</span><span class="sxs-lookup"><span data-stu-id="87551-259">If **TRUE**, interrupts are permitted for hard mounts.</span></span> <span data-ttu-id="87551-260">Se **for false**, as interrupções serão ignoradas para montagens físicas.</span><span class="sxs-lookup"><span data-stu-id="87551-260">If **FALSE**, interrupts are ignored for hard mounts.</span></span>

</dd> <dt>

<span data-ttu-id="87551-261">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="87551-261">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-262">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87551-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87551-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87551-264">Comprimento máximo de um nome de arquivo dentro do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="87551-264">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="87551-265">Um valor de 0 (zero) indica que não há limite para o comprimento do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="87551-265">A value of 0 (zero)indicates that there is no limit for file name length.</span></span>

<span data-ttu-id="87551-266">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-266">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="87551-267">**MountFailureRetries**</span><span class="sxs-lookup"><span data-stu-id="87551-267">**MountFailureRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-268">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87551-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87551-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87551-270">Número máximo de tentativas de falha de montagem permitidas.</span><span class="sxs-lookup"><span data-stu-id="87551-270">Maximum number of mount failure retries that are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="87551-271">**Nome**</span><span class="sxs-lookup"><span data-stu-id="87551-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-272">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87551-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87551-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-274">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="87551-274">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="87551-275">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="87551-275">Label by which the object is known.</span></span> <span data-ttu-id="87551-276">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="87551-276">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="87551-277">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="87551-277">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="87551-278">**ReadBufferSize**</span><span class="sxs-lookup"><span data-stu-id="87551-278">**ReadBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-279">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="87551-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="87551-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-281">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="87551-281">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="87551-282">Tamanho do buffer de leitura, em bytes.</span><span class="sxs-lookup"><span data-stu-id="87551-282">Read buffer size, in bytes.</span></span>

<span data-ttu-id="87551-283">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="87551-283">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="87551-284">**ReadOnly (somente-leitura)**</span><span class="sxs-lookup"><span data-stu-id="87551-284">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-285">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="87551-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87551-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-287">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="87551-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="87551-288">Se **for true**, o sistema de arquivos será designado como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="87551-288">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="87551-289">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-289">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="87551-290">**RetransmissionAttempts**</span><span class="sxs-lookup"><span data-stu-id="87551-290">**RetransmissionAttempts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-291">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87551-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87551-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87551-293">Número máximo de retransmissões de NFS permitidas.</span><span class="sxs-lookup"><span data-stu-id="87551-293">Maximum number of NFS retransmissions allowed.</span></span>

</dd> <dt>

<span data-ttu-id="87551-294">**RetransmissionTimeout**</span><span class="sxs-lookup"><span data-stu-id="87551-294">**RetransmissionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-295">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87551-295">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87551-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-297">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("décimos de segundos")</span><span class="sxs-lookup"><span data-stu-id="87551-297">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of seconds")</span></span>
</dt> </dl>

<span data-ttu-id="87551-298">Tempo limite do NFS, em décimos de segundo.</span><span class="sxs-lookup"><span data-stu-id="87551-298">NFS time-out, in tenths of a second.</span></span>

</dd> <dt>

<span data-ttu-id="87551-299">**Básica**</span><span class="sxs-lookup"><span data-stu-id="87551-299">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87551-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87551-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-302">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="87551-302">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="87551-303">Nome do caminho ou outras informações que definem a raiz do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="87551-303">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="87551-304">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-304">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="87551-305">**ServerCommunicationPort**</span><span class="sxs-lookup"><span data-stu-id="87551-305">**ServerCommunicationPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-306">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87551-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87551-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87551-308">Número da porta UDP do sistema do computador remoto.</span><span class="sxs-lookup"><span data-stu-id="87551-308">Remote computer system's UDP port number.</span></span>

</dd> <dt>

<span data-ttu-id="87551-309">**Status**</span><span class="sxs-lookup"><span data-stu-id="87551-309">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-310">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87551-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87551-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-312">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="87551-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="87551-313">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="87551-313">Current status of the object.</span></span>

<span data-ttu-id="87551-314">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="87551-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="87551-315">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="87551-315">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="87551-316">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="87551-316">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="87551-317">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="87551-317">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="87551-318">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="87551-318">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="87551-319">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="87551-319">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="87551-320">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="87551-320">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="87551-321">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="87551-321">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="87551-322">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="87551-322">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="87551-323">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="87551-323">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="87551-324">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="87551-324">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="87551-325">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="87551-325">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="87551-326">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="87551-326">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="87551-327">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="87551-327">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="87551-328">**WriteBufferSize**</span><span class="sxs-lookup"><span data-stu-id="87551-328">**WriteBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87551-329">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="87551-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="87551-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87551-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87551-331">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="87551-331">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="87551-332">Tamanho do buffer de gravação, em bytes.</span><span class="sxs-lookup"><span data-stu-id="87551-332">Write buffer size, in bytes.</span></span>

<span data-ttu-id="87551-333">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="87551-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87551-334">Comentários</span><span class="sxs-lookup"><span data-stu-id="87551-334">Remarks</span></span>

<span data-ttu-id="87551-335">A classe **CIM \_ NFS** é derivada do [**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md).</span><span class="sxs-lookup"><span data-stu-id="87551-335">The **CIM\_NFS** class is derived from [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md).</span></span>

<span data-ttu-id="87551-336">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="87551-336">WMI does not implement this class.</span></span>

<span data-ttu-id="87551-337">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="87551-337">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="87551-338">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="87551-338">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="87551-339">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87551-339">Requirements</span></span>



| <span data-ttu-id="87551-340">Requisito</span><span class="sxs-lookup"><span data-stu-id="87551-340">Requirement</span></span> | <span data-ttu-id="87551-341">Valor</span><span class="sxs-lookup"><span data-stu-id="87551-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87551-342">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87551-342">Minimum supported client</span></span><br/> | <span data-ttu-id="87551-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87551-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87551-344">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87551-344">Minimum supported server</span></span><br/> | <span data-ttu-id="87551-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87551-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87551-346">Namespace</span><span class="sxs-lookup"><span data-stu-id="87551-346">Namespace</span></span><br/>                | <span data-ttu-id="87551-347">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="87551-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="87551-348">MOF</span><span class="sxs-lookup"><span data-stu-id="87551-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87551-349"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87551-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="87551-350">DLL</span><span class="sxs-lookup"><span data-stu-id="87551-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87551-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87551-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87551-352">Confira também</span><span class="sxs-lookup"><span data-stu-id="87551-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87551-353">**\_REMOTEFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="87551-353">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> </dl>

 

