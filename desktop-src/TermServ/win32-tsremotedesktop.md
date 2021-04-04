---
title: Classe Win32_TSRemoteDesktop
description: Descreve uma conexão de área de trabalho remota que está disponível por meio de Acesso via Web à Área de Trabalho Remota (RD Acesso via Web).
ms.assetid: 40c7d8f1-cc45-4f0a-8c07-8215342ca02e
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSRemoteDesktop Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSRemoteDesktop classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSRemoteDesktop
- Win32_TSRemoteDesktop.Caption
- Win32_TSRemoteDesktop.Description
- Win32_TSRemoteDesktop.InstallDate
- Win32_TSRemoteDesktop.Name
- Win32_TSRemoteDesktop.Status
- Win32_TSRemoteDesktop.Alias
- Win32_TSRemoteDesktop.SecurityDescriptor
- Win32_TSRemoteDesktop.IconPath
- Win32_TSRemoteDesktop.IconIndex
- Win32_TSRemoteDesktop.IconContents
- Win32_TSRemoteDesktop.ShowInPortal
- Win32_TSRemoteDesktop.RDPFileContents
- Win32_TSRemoteDesktop.IsVmFarm
- Win32_TSRemoteDesktop.VmFarmSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3a23e63d5c79313933b7ce6951265a85740bc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085226"
---
# <a name="win32_tsremotedesktop-class"></a><span data-ttu-id="ddc66-105">\_Classe Win32 TSRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="ddc66-105">Win32\_TSRemoteDesktop class</span></span>

<span data-ttu-id="ddc66-106">Descreve uma conexão de área de trabalho remota que está disponível por meio de Acesso via Web à Área de Trabalho Remota (RD Acesso via Web).</span><span class="sxs-lookup"><span data-stu-id="ddc66-106">Describes a remote desktop connection that is available through Remote Desktop Web Access (RD Web Access).</span></span>

## <a name="syntax"></a><span data-ttu-id="ddc66-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ddc66-107">Syntax</span></span>

``` syntax
class Win32_TSRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  boolean  IsVmFarm;
  string   VmFarmSettings;
};
```

## <a name="members"></a><span data-ttu-id="ddc66-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ddc66-108">Members</span></span>

<span data-ttu-id="ddc66-109">A classe **Win32 \_ TSRemoteDesktop** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ddc66-109">The **Win32\_TSRemoteDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="ddc66-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ddc66-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ddc66-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ddc66-111">Properties</span></span>

<span data-ttu-id="ddc66-112">A classe **Win32 \_ TSRemoteDesktop** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ddc66-112">The **Win32\_TSRemoteDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ddc66-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="ddc66-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc66-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ddc66-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ddc66-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-116">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="ddc66-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ddc66-117">O alias da conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="ddc66-117">The alias of the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="ddc66-118">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="ddc66-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc66-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ddc66-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ddc66-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-121">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ddc66-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ddc66-122">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="ddc66-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="ddc66-123">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddc66-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddc66-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ddc66-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc66-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ddc66-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ddc66-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddc66-127">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="ddc66-127">Description of the object.</span></span>

<span data-ttu-id="ddc66-128">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddc66-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddc66-129">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="ddc66-129">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc66-130">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="ddc66-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ddc66-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddc66-132">O conteúdo em bytes do ícone que corresponde à conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="ddc66-132">The byte contents of the icon that corresponds to the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="ddc66-133">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="ddc66-133">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc66-134">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddc66-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ddc66-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ddc66-136">O índice ou a ID do ícone para a conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="ddc66-136">The index or ID of the icon for the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="ddc66-137">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="ddc66-137">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc66-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ddc66-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ddc66-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ddc66-140">Caminho do ícone para a conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="ddc66-140">Path of the icon for the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="ddc66-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ddc66-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc66-142">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ddc66-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ddc66-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-144">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="ddc66-144">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ddc66-145">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="ddc66-145">The date the object was installed.</span></span> <span data-ttu-id="ddc66-146">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="ddc66-146">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ddc66-147">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddc66-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddc66-148">**IsVmFarm**</span><span class="sxs-lookup"><span data-stu-id="ddc66-148">**IsVmFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc66-149">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ddc66-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ddc66-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ddc66-151">Indica se esta conexão de área de trabalho remota faz parte de um farm de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="ddc66-151">Indicates if this remote desktop connection is part of a virtual machine farm.</span></span>

</dd> <dt>

<span data-ttu-id="ddc66-152">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ddc66-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc66-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ddc66-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ddc66-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddc66-155">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="ddc66-155">The name of the object.</span></span>

<span data-ttu-id="ddc66-156">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddc66-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddc66-157">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="ddc66-157">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc66-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ddc66-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-159">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ddc66-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ddc66-160">Conteúdo do arquivo RDP que corresponde à conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="ddc66-160">Contents of the RDP file that correspond to the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="ddc66-161">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ddc66-161">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc66-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ddc66-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ddc66-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ddc66-164">Um descritor de segurança que controla o acesso à conexão de área de trabalho remota, no formato SDDL.</span><span class="sxs-lookup"><span data-stu-id="ddc66-164">A security descriptor that controls access to the remote desktop connection, in SDDL format.</span></span> <span data-ttu-id="ddc66-165">Uma cadeia de caracteres vazia implica permitir todo o acesso.</span><span class="sxs-lookup"><span data-stu-id="ddc66-165">An empty string implies allow all access.</span></span> <span data-ttu-id="ddc66-166">Este descritor de segurança não oferece suporte a ACEs DENY ou ACEs que se referem a usuários ou grupos que não são de domínio.</span><span class="sxs-lookup"><span data-stu-id="ddc66-166">This security descriptor does not support DENY ACEs, or ACEs that refer to nondomain users or groups.</span></span>

</dd> <dt>

<span data-ttu-id="ddc66-167">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="ddc66-167">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc66-168">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ddc66-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ddc66-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ddc66-170">Indica se a conexão de área de trabalho remota deve ser mostrada no Acesso via Web RD.</span><span class="sxs-lookup"><span data-stu-id="ddc66-170">Indicates whether the remote desktop connection should be shown in RD Web Access.</span></span>

</dd> <dt>

<span data-ttu-id="ddc66-171">**Status**</span><span class="sxs-lookup"><span data-stu-id="ddc66-171">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc66-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ddc66-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ddc66-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-174">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="ddc66-174">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="ddc66-175">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ddc66-175">Current status of the object.</span></span> <span data-ttu-id="ddc66-176">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="ddc66-176">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ddc66-177">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="ddc66-177">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ddc66-178">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="ddc66-178">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ddc66-179">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="ddc66-179">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ddc66-180">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="ddc66-180">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ddc66-181">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddc66-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="ddc66-182">("OK")</span><span class="sxs-lookup"><span data-stu-id="ddc66-182">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ddc66-183">("Erro")</span><span class="sxs-lookup"><span data-stu-id="ddc66-183">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ddc66-184">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="ddc66-184">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ddc66-185">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="ddc66-185">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ddc66-186">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ddc66-186">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ddc66-187">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="ddc66-187">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ddc66-188">("Parando")</span><span class="sxs-lookup"><span data-stu-id="ddc66-188">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ddc66-189">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="ddc66-189">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ddc66-190">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="ddc66-190">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc66-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ddc66-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddc66-192">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ddc66-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ddc66-193">Configurações do farm de máquinas virtuais para a conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="ddc66-193">Virtual machine farm settings for the remote desktop connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddc66-194">Comentários</span><span class="sxs-lookup"><span data-stu-id="ddc66-194">Remarks</span></span>

<span data-ttu-id="ddc66-195">Você deve ser um membro do grupo Administradores para definir propriedades usando essa classe.</span><span class="sxs-lookup"><span data-stu-id="ddc66-195">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="ddc66-196">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="ddc66-196">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="ddc66-197">Para chamadas C/C++, esse é um nível de autenticação **de \_ \_ privacidade do \_ PCT no \_ nível \_** de autenticado RPC C, que pode ser definido usando a função com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="ddc66-197">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="ddc66-198">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="ddc66-198">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="ddc66-199">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="ddc66-199">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="ddc66-200">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ddc66-200">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ddc66-201">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ddc66-201">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ddc66-202">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="ddc66-202">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ddc66-203">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ddc66-203">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddc66-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddc66-204">Requirements</span></span>



| <span data-ttu-id="ddc66-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddc66-205">Requirement</span></span> | <span data-ttu-id="ddc66-206">Valor</span><span class="sxs-lookup"><span data-stu-id="ddc66-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddc66-207">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ddc66-207">Minimum supported client</span></span><br/> | <span data-ttu-id="ddc66-208">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ddc66-208">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ddc66-209">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ddc66-209">Minimum supported server</span></span><br/> | <span data-ttu-id="ddc66-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddc66-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ddc66-211">Namespace</span><span class="sxs-lookup"><span data-stu-id="ddc66-211">Namespace</span></span><br/>                | <span data-ttu-id="ddc66-212">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="ddc66-212">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ddc66-213">MOF</span><span class="sxs-lookup"><span data-stu-id="ddc66-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddc66-214"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ddc66-214"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="ddc66-215">DLL</span><span class="sxs-lookup"><span data-stu-id="ddc66-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddc66-216"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddc66-216"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

