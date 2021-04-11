---
title: Classe Win32_RDCentralPublishedRemoteDesktop
description: Área de trabalho publicada em outro computador, para uso remoto por meio dos serviços de terminal.
ms.assetid: 2b28a2d3-048f-446f-9ce0-eb684b393eaa
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDCentralPublishedRemoteDesktop Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDCentralPublishedRemoteDesktop classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteDesktop
- Win32_RDCentralPublishedRemoteDesktop.Caption
- Win32_RDCentralPublishedRemoteDesktop.Description
- Win32_RDCentralPublishedRemoteDesktop.InstallDate
- Win32_RDCentralPublishedRemoteDesktop.Name
- Win32_RDCentralPublishedRemoteDesktop.Status
- Win32_RDCentralPublishedRemoteDesktop.PublishingFarm
- Win32_RDCentralPublishedRemoteDesktop.Alias
- Win32_RDCentralPublishedRemoteDesktop.IconContents
- Win32_RDCentralPublishedRemoteDesktop.ShowInPortal
- Win32_RDCentralPublishedRemoteDesktop.RDPFileContents
- Win32_RDCentralPublishedRemoteDesktop.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04696331b7027b7cc65d2202c29e6ce95bb3f4b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454977"
---
# <a name="win32_rdcentralpublishedremotedesktop-class"></a><span data-ttu-id="6667c-105">\_Classe Win32 RDCentralPublishedRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="6667c-105">Win32\_RDCentralPublishedRemoteDesktop class</span></span>

<span data-ttu-id="6667c-106">Área de trabalho publicada em outro computador, para uso remoto por meio dos serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="6667c-106">Desktop published on another computer, for remote use through Terminal Services</span></span>

<span data-ttu-id="6667c-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6667c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6667c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6667c-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a><span data-ttu-id="6667c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="6667c-109">Members</span></span>

<span data-ttu-id="6667c-110">A classe **Win32 \_ RDCentralPublishedRemoteDesktop** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6667c-110">The **Win32\_RDCentralPublishedRemoteDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="6667c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6667c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6667c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6667c-112">Properties</span></span>

<span data-ttu-id="6667c-113">A classe **Win32 \_ RDCentralPublishedRemoteDesktop** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6667c-113">The **Win32\_RDCentralPublishedRemoteDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6667c-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="6667c-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6667c-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6667c-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6667c-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6667c-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6667c-117">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6667c-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6667c-118">Alias da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6667c-118">Alias of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="6667c-119">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="6667c-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6667c-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6667c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6667c-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6667c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6667c-122">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6667c-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6667c-123">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="6667c-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="6667c-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6667c-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6667c-125">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6667c-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6667c-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6667c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6667c-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6667c-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6667c-128">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="6667c-128">Description of the object.</span></span>

<span data-ttu-id="6667c-129">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6667c-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6667c-130">**Pastas**</span><span class="sxs-lookup"><span data-stu-id="6667c-130">**Folders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6667c-131">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6667c-131">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6667c-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6667c-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6667c-133">Lista das pastas em que esse recurso deve ser exibido.</span><span class="sxs-lookup"><span data-stu-id="6667c-133">List of the folders where this resource should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="6667c-134">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="6667c-134">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6667c-135">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="6667c-135">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6667c-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6667c-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6667c-137">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6667c-137">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6667c-138">Conteúdo do ícone correspondente ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6667c-138">Contents of the icon corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="6667c-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6667c-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6667c-140">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6667c-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6667c-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6667c-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6667c-142">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="6667c-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="6667c-143">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="6667c-143">The date the object was installed.</span></span> <span data-ttu-id="6667c-144">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="6667c-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6667c-145">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6667c-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6667c-146">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6667c-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6667c-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6667c-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6667c-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6667c-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6667c-149">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="6667c-149">The name of the object.</span></span>

<span data-ttu-id="6667c-150">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6667c-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6667c-151">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="6667c-151">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6667c-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6667c-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6667c-153">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6667c-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6667c-154">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6667c-154">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6667c-155">Alias do farm que publicou a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6667c-155">Alias of the farm that published the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="6667c-156">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="6667c-156">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6667c-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6667c-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6667c-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6667c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6667c-159">Conteúdo do arquivo RDP correspondente à área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6667c-159">Contents of the RDP file corresponding to the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="6667c-160">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="6667c-160">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6667c-161">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6667c-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6667c-162">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6667c-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6667c-163">**true** se este aplicativo deve ser mostrado no TS acesso via Web; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="6667c-163">**true** if this application should be shown in the TS Web Access; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="6667c-164">**Status**</span><span class="sxs-lookup"><span data-stu-id="6667c-164">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6667c-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6667c-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6667c-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6667c-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6667c-167">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="6667c-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="6667c-168">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6667c-168">Current status of the object.</span></span> <span data-ttu-id="6667c-169">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="6667c-169">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6667c-170">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="6667c-170">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6667c-171">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="6667c-171">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6667c-172">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="6667c-172">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6667c-173">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="6667c-173">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6667c-174">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6667c-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="6667c-175">("OK")</span><span class="sxs-lookup"><span data-stu-id="6667c-175">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6667c-176">("Erro")</span><span class="sxs-lookup"><span data-stu-id="6667c-176">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6667c-177">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="6667c-177">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6667c-178">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="6667c-178">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6667c-179">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6667c-179">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6667c-180">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="6667c-180">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6667c-181">("Parando")</span><span class="sxs-lookup"><span data-stu-id="6667c-181">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6667c-182">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="6667c-182">("Service")</span></span>


<span data-ttu-id="6667c-183"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6667c-183"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="6667c-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6667c-184">Requirements</span></span>



| <span data-ttu-id="6667c-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="6667c-185">Requirement</span></span> | <span data-ttu-id="6667c-186">Valor</span><span class="sxs-lookup"><span data-stu-id="6667c-186">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6667c-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6667c-187">Minimum supported client</span></span><br/> | <span data-ttu-id="6667c-188">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6667c-188">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6667c-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6667c-189">Minimum supported server</span></span><br/> | <span data-ttu-id="6667c-190">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6667c-190">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="6667c-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="6667c-191">Namespace</span></span><br/>                | <span data-ttu-id="6667c-192">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="6667c-192">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6667c-193">MOF</span><span class="sxs-lookup"><span data-stu-id="6667c-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6667c-194"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6667c-194"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="6667c-195">DLL</span><span class="sxs-lookup"><span data-stu-id="6667c-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6667c-196"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6667c-196"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

