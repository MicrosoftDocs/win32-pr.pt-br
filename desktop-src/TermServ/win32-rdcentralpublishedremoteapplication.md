---
title: Classe Win32_RDCentralPublishedRemoteApplication
description: Descreve um aplicativo publicado em outro computador, para uso remoto por meio dos serviços de terminal.
ms.assetid: 8605bd1e-e825-4fd9-b14f-9d3bdac489f1
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDCentralPublishedRemoteApplication Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDCentralPublishedRemoteApplication classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteApplication
- Win32_RDCentralPublishedRemoteApplication.Caption
- Win32_RDCentralPublishedRemoteApplication.Description
- Win32_RDCentralPublishedRemoteApplication.InstallDate
- Win32_RDCentralPublishedRemoteApplication.Name
- Win32_RDCentralPublishedRemoteApplication.Status
- Win32_RDCentralPublishedRemoteApplication.PublishingFarm
- Win32_RDCentralPublishedRemoteApplication.Alias
- Win32_RDCentralPublishedRemoteApplication.SecurityDescriptor
- Win32_RDCentralPublishedRemoteApplication.Path
- Win32_RDCentralPublishedRemoteApplication.VPath
- Win32_RDCentralPublishedRemoteApplication.IconContents
- Win32_RDCentralPublishedRemoteApplication.CommandLineSetting
- Win32_RDCentralPublishedRemoteApplication.RequiredCommandLine
- Win32_RDCentralPublishedRemoteApplication.ShowInPortal
- Win32_RDCentralPublishedRemoteApplication.AppID
- Win32_RDCentralPublishedRemoteApplication.RDPFileContents
- Win32_RDCentralPublishedRemoteApplication.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd837f62d8d0787d992e8eed7316ed1ef3f199ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918313"
---
# <a name="win32_rdcentralpublishedremoteapplication-class"></a><span data-ttu-id="e9c1f-105">\_Classe Win32 RDCentralPublishedRemoteApplication</span><span class="sxs-lookup"><span data-stu-id="e9c1f-105">Win32\_RDCentralPublishedRemoteApplication class</span></span>

<span data-ttu-id="e9c1f-106">Descreve um aplicativo publicado em outro computador, para uso remoto por meio dos serviços de terminal.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-106">Describes an application published on another computer, for remote use through Terminal Services.</span></span>

<span data-ttu-id="e9c1f-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9c1f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9c1f-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  string   VPath;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   AppID;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a><span data-ttu-id="e9c1f-109">Membros</span><span class="sxs-lookup"><span data-stu-id="e9c1f-109">Members</span></span>

<span data-ttu-id="e9c1f-110">A classe **Win32 \_ RDCentralPublishedRemoteApplication** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e9c1f-110">The **Win32\_RDCentralPublishedRemoteApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="e9c1f-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e9c1f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9c1f-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e9c1f-112">Properties</span></span>

<span data-ttu-id="e9c1f-113">A classe **Win32 \_ RDCentralPublishedRemoteApplication** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-113">The **Win32\_RDCentralPublishedRemoteApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9c1f-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e9c1f-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-117">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e9c1f-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-118">Alias do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-118">Alias of the application.</span></span>

</dd> <dt>

<span data-ttu-id="e9c1f-119">**AppID**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-119">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e9c1f-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-122">AppID é usado para fixação nos clientes.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-122">AppID is used for pinning on the clients.</span></span>

</dd> <dt>

<span data-ttu-id="e9c1f-123">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9c1f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-126">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e9c1f-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-127">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-127">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="e9c1f-128">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9c1f-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9c1f-129">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-129">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e9c1f-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-132">Se argumentos de linha de comando são necessários para este aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-132">Whether command-line arguments are required for this application.</span></span>

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span data-ttu-id="e9c1f-133"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span><span class="sxs-lookup"><span data-stu-id="e9c1f-133"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e9c1f-134">Não permitir</span><span class="sxs-lookup"><span data-stu-id="e9c1f-134">Do not allow</span></span>

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="e9c1f-135"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Permitir** (1)</span><span class="sxs-lookup"><span data-stu-id="e9c1f-135"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span data-ttu-id="e9c1f-136"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Exigir** (2)</span><span class="sxs-lookup"><span data-stu-id="e9c1f-136"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Require** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9c1f-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9c1f-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-140">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-140">Description of the object.</span></span>

<span data-ttu-id="e9c1f-141">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9c1f-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9c1f-142">**Pastas**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-142">**Folders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-143">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e9c1f-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-145">Lista das pastas em que esse recurso deve ser exibido.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-145">List of the folders where this resource should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="e9c1f-146">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-146">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-147">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-147">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e9c1f-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-149">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e9c1f-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-150">Conteúdo do ícone correspondente ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-150">Contents of the icon corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="e9c1f-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-152">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9c1f-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-154">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="e9c1f-154">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-155">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-155">The date the object was installed.</span></span> <span data-ttu-id="e9c1f-156">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-156">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e9c1f-157">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9c1f-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9c1f-158">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9c1f-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-161">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-161">The name of the object.</span></span>

<span data-ttu-id="e9c1f-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9c1f-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9c1f-163">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-163">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e9c1f-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-166">Caminho para o aplicativo</span><span class="sxs-lookup"><span data-stu-id="e9c1f-166">Path to the application</span></span>

</dd> <dt>

<span data-ttu-id="e9c1f-167">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-167">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e9c1f-169">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-170">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e9c1f-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-171">Alias do farm que publicou o aplicativo</span><span class="sxs-lookup"><span data-stu-id="e9c1f-171">Alias of the farm that published the Application</span></span>

</dd> <dt>

<span data-ttu-id="e9c1f-172">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-172">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9c1f-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-175">Conteúdo do arquivo RDP correspondente ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-175">Contents of the RDP file corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="e9c1f-176">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-176">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e9c1f-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-179">Argumentos de linha de comando necessários para este aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-179">Command-line arguments required for this application.</span></span>

</dd> <dt>

<span data-ttu-id="e9c1f-180">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-180">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-182">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e9c1f-182">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-183">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e9c1f-183">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-184">Descritor de segurança que controla o acesso ao aplicativo, no formato SDDL.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-184">Security Descriptor controlling access to the application, in SDDL Format.</span></span> <span data-ttu-id="e9c1f-185">A cadeia de caracteres vazia implica permitir todo o acesso.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-185">Empty string implies allow all access.</span></span>

</dd> <dt>

<span data-ttu-id="e9c1f-186">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-186">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-187">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-188">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e9c1f-188">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-189">**true** se este aplicativo deve ser mostrado no TS acesso via Web; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-189">**true** if this application should be shown in the TS Web Access; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="e9c1f-190">**Status**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9c1f-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-193">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="e9c1f-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-194">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-194">Current status of the object.</span></span> <span data-ttu-id="e9c1f-195">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-195">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e9c1f-196">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="e9c1f-196">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e9c1f-197">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="e9c1f-197">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e9c1f-198">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-198">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e9c1f-199">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-199">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e9c1f-200">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9c1f-200">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="e9c1f-201">("OK")</span><span class="sxs-lookup"><span data-stu-id="e9c1f-201">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e9c1f-202">("Erro")</span><span class="sxs-lookup"><span data-stu-id="e9c1f-202">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e9c1f-203">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="e9c1f-203">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e9c1f-204">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="e9c1f-204">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e9c1f-205">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="e9c1f-205">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e9c1f-206">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="e9c1f-206">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e9c1f-207">("Parando")</span><span class="sxs-lookup"><span data-stu-id="e9c1f-207">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e9c1f-208">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="e9c1f-208">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9c1f-209">**VPath**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-209">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c1f-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9c1f-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c1f-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e9c1f-211">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9c1f-212">Caminho virtual para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e9c1f-212">Virtual Path to the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9c1f-213">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9c1f-213">Requirements</span></span>



| <span data-ttu-id="e9c1f-214">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9c1f-214">Requirement</span></span> | <span data-ttu-id="e9c1f-215">Valor</span><span class="sxs-lookup"><span data-stu-id="e9c1f-215">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c1f-216">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9c1f-216">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c1f-217">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e9c1f-217">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e9c1f-218">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9c1f-218">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c1f-219">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9c1f-219">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="e9c1f-220">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9c1f-220">Namespace</span></span><br/>                | <span data-ttu-id="e9c1f-221">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="e9c1f-221">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e9c1f-222">MOF</span><span class="sxs-lookup"><span data-stu-id="e9c1f-222">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9c1f-223"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9c1f-223"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="e9c1f-224">DLL</span><span class="sxs-lookup"><span data-stu-id="e9c1f-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9c1f-225"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9c1f-225"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

