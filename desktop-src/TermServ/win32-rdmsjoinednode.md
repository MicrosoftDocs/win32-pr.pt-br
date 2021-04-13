---
title: Classe Win32_RDMSJoinedNode
description: Representa um nó de servidor gerenciado por serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 8751f3f7-dfb5-45bd-a6b1-758aa22a3569
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSJoinedNode Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSJoinedNode classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode.FQDN
- Win32_RDMSJoinedNode.SID
- Win32_RDMSJoinedNode.OSVersion
- Win32_RDMSJoinedNode.IsRdcb
- Win32_RDMSJoinedNode.IsRdg
- Win32_RDMSJoinedNode.IsRdls
- Win32_RDMSJoinedNode.IsRdvh
- Win32_RDMSJoinedNode.IsRdwa
- Win32_RDMSJoinedNode.IsRdsh
- Win32_RDMSJoinedNode.IsWebAccessCertificateInstalled
- Win32_RDMSJoinedNode.IsGatewayCertificateInstalled
- Win32_RDMSJoinedNode.IsRedirectorCertificateInstalled
- Win32_RDMSJoinedNode.IsPublishingCertificateInstalled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cabf1cf7ff98b698624285b2877412c4323259b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369268"
---
# <a name="win32_rdmsjoinednode-class"></a><span data-ttu-id="ac1c1-105">\_Classe Win32 RDMSJoinedNode</span><span class="sxs-lookup"><span data-stu-id="ac1c1-105">Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="ac1c1-106">Representa um nó de servidor gerenciado por serviços de gerenciamento de Área de Trabalho Remota (RDMS).</span><span class="sxs-lookup"><span data-stu-id="ac1c1-106">Represents a server node that is managed by Remote Desktop Management Services (RDMS).</span></span>

<span data-ttu-id="ac1c1-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1c1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac1c1-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSJoinedNode
{
  string  FQDN;
  string  SID;
  String  OSVersion;
  boolean IsRdcb;
  boolean IsRdg;
  boolean IsRdls;
  boolean IsRdvh;
  boolean IsRdwa;
  boolean IsRdsh;
  boolean IsWebAccessCertificateInstalled;
  boolean IsGatewayCertificateInstalled;
  boolean IsRedirectorCertificateInstalled;
  boolean IsPublishingCertificateInstalled;
};
```

## <a name="members"></a><span data-ttu-id="ac1c1-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ac1c1-109">Members</span></span>

<span data-ttu-id="ac1c1-110">A classe **Win32 \_ RDMSJoinedNode** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ac1c1-110">The **Win32\_RDMSJoinedNode** class has these types of members:</span></span>

-   [<span data-ttu-id="ac1c1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ac1c1-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ac1c1-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ac1c1-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ac1c1-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ac1c1-113">Methods</span></span>

<span data-ttu-id="ac1c1-114">A classe **Win32 \_ RDMSJoinedNode** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-114">The **Win32\_RDMSJoinedNode** class has these methods.</span></span>



| <span data-ttu-id="ac1c1-115">Método</span><span class="sxs-lookup"><span data-stu-id="ac1c1-115">Method</span></span>                                                                | <span data-ttu-id="ac1c1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac1c1-116">Description</span></span>                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac1c1-117">**GetJoinedNodeCount**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-117">**GetJoinedNodeCount**</span></span>](win32-rdmsjoinednode-getjoinednodecount.md) | <span data-ttu-id="ac1c1-118">**Windows server 2012 R2 e Windows server 2012:** Esse método não está disponível antes do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-118">**Windows Server 2012 R2 and Windows Server 2012:** This method is unavailable prior to Windows Server 2016.</span></span><br/> <span data-ttu-id="ac1c1-119">Obtém o número de servidores que têm a função especificada instalada.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-119">Gets the number of servers that have the specified role installed.</span></span><br/> |
| [<span data-ttu-id="ac1c1-120">**Join**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-120">**Join**</span></span>](join-win32-rdmsjoinednode.md)                             | <span data-ttu-id="ac1c1-121">Adiciona um nó a RDMS.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-121">Adds a node to RDMS.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="ac1c1-122">**Sair**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-122">**Unjoin**</span></span>](unjoin-win32-rdmsjoinednode.md)                         | <span data-ttu-id="ac1c1-123">Remove um nó de RDMS.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-123">Removes a node from RDMS.</span></span><br/>                                                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="ac1c1-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ac1c1-124">Properties</span></span>

<span data-ttu-id="ac1c1-125">A classe **Win32 \_ RDMSJoinedNode** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-125">The **Win32\_RDMSJoinedNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac1c1-126">**FQDN**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-126">**FQDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1c1-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac1c1-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-129">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ac1c1-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ac1c1-130">Obtém o nome de domínio totalmente qualificado do nó.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-130">Gets the fully qualified domain name of the node.</span></span>

</dd> <dt>

<span data-ttu-id="ac1c1-131">**IsGatewayCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-131">**IsGatewayCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1c1-132">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac1c1-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac1c1-134">Obtém e define um valor que indica se o servidor tem um certificado para executar a autenticação para conexões Área de Trabalho Remota gateway.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-134">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop gateway connections.</span></span> <span data-ttu-id="ac1c1-135">**True** se o certificado estiver instalado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-135">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ac1c1-136">**IsPublishingCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-136">**IsPublishingCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1c1-137">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac1c1-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac1c1-139">Obtém e define um valor que indica se o servidor tem um certificado para assinar protocolo RDP arquivos de publicação.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-139">Gets and sets a value that indicates whether the server has a certificate to sign Remote Desktop Protocol publishing files.</span></span> <span data-ttu-id="ac1c1-140">**True** se o certificado estiver instalado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-140">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ac1c1-141">**IsRdcb**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-141">**IsRdcb**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1c1-142">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-143">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac1c1-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac1c1-144">Obtém e define um valor que indica se o servidor está Conexão de Área de Trabalho Remota Agente.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-144">Gets and sets a value that indicates whether the server is Remote Desktop Connection Broker.</span></span> <span data-ttu-id="ac1c1-145">**True** se o servidor for um agente de conexão de área de trabalho remota; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-145">**TRUE** if the server is a Remote Desktop Connection Broker; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ac1c1-146">**IsRdg**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-146">**IsRdg**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1c1-147">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac1c1-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac1c1-149">Obtém e define um valor que indica se o servidor está Área de Trabalho Remota servidor de gateway.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-149">Gets and sets a value that indicates whether the server is Remote Desktop gateway server.</span></span> <span data-ttu-id="ac1c1-150">**True** se o servidor for um servidor de gateway área de trabalho remota; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-150">**TRUE** if the server is a Remote Desktop gateway server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ac1c1-151">**IsRdls**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-151">**IsRdls**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1c1-152">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-153">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac1c1-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac1c1-154">Obtém e define um valor que indica se o servidor está Área de Trabalho Remota servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-154">Gets and sets a value that indicates whether the server is Remote Desktop license server.</span></span> <span data-ttu-id="ac1c1-155">**True** se o servidor for um servidor de licença área de trabalho remota; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-155">**TRUE** if the server is a Remote Desktop license server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ac1c1-156">**IsRdsh**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-156">**IsRdsh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1c1-157">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac1c1-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac1c1-159">Obtém e define um valor que indica se o servidor está Área de Trabalho Remota servidor host de sessão.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-159">Gets and sets a value that indicates whether the server is Remote Desktop session host server.</span></span> <span data-ttu-id="ac1c1-160">**True** se o servidor for um servidor host de sessão área de trabalho remota; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-160">**TRUE** if the server is a Remote Desktop session host server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ac1c1-161">**IsRdvh**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-161">**IsRdvh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1c1-162">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac1c1-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac1c1-164">Obtém e define um valor que indica se o servidor está Área de Trabalho Remota host de virtualização.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-164">Gets and sets a value that indicates whether the server is Remote Desktop virtualization host.</span></span> <span data-ttu-id="ac1c1-165">**True** se o servidor for um host de virtualização área de trabalho remota; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-165">**TRUE** if the server is a Remote Desktop virtualization host; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ac1c1-166">**IsRdwa**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-166">**IsRdwa**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1c1-167">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-167">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-168">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac1c1-168">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac1c1-169">Obtém e define um valor que indica se o servidor é Área de Trabalho Remota servidor de acesso à Web.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-169">Gets and sets a value that indicates whether the server is Remote Desktop web access server.</span></span> <span data-ttu-id="ac1c1-170">**True** se o servidor for um servidor de acesso via Web à área de trabalho remota; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-170">**TRUE** if the server is a Remote Desktop Web Access server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ac1c1-171">**IsRedirectorCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-171">**IsRedirectorCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1c1-172">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-173">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac1c1-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac1c1-174">Obtém e define um valor que indica se o servidor tem um certificado para executar a autenticação para Serviços de Área de Trabalho Remota implantação.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-174">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop Services deployment.</span></span> <span data-ttu-id="ac1c1-175">**True** se o certificado estiver instalado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-175">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ac1c1-176">**IsWebAccessCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-176">**IsWebAccessCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1c1-177">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac1c1-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac1c1-179">Obtém e define um valor que indica se o servidor tem um certificado para executar a autenticação para Acesso via Web à Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-179">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop Web Access.</span></span> <span data-ttu-id="ac1c1-180">**True** se o certificado estiver instalado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-180">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ac1c1-181">**OSVersion**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-181">**OSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1c1-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-182">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-183">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac1c1-183">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-184">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ac1c1-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ac1c1-185">Obtém e define a versão dos sistemas operacionais no nó.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-185">Gets and sets the version of the operating systems on the node.</span></span>

</dd> <dt>

<span data-ttu-id="ac1c1-186">**SID**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-186">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1c1-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac1c1-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac1c1-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac1c1-189">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ac1c1-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ac1c1-190">Obtém o identificador de segurança (SID) do nó.</span><span class="sxs-lookup"><span data-stu-id="ac1c1-190">Gets the security identifier (SID) of the node.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac1c1-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac1c1-191">Requirements</span></span>



| <span data-ttu-id="ac1c1-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac1c1-192">Requirement</span></span> | <span data-ttu-id="ac1c1-193">Valor</span><span class="sxs-lookup"><span data-stu-id="ac1c1-193">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac1c1-194">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac1c1-194">Minimum supported client</span></span><br/> | <span data-ttu-id="ac1c1-195">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ac1c1-195">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ac1c1-196">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac1c1-196">Minimum supported server</span></span><br/> | <span data-ttu-id="ac1c1-197">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac1c1-197">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="ac1c1-198">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac1c1-198">Namespace</span></span><br/>                | <span data-ttu-id="ac1c1-199">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="ac1c1-199">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="ac1c1-200">MOF</span><span class="sxs-lookup"><span data-stu-id="ac1c1-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac1c1-201"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac1c1-201"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac1c1-202">DLL</span><span class="sxs-lookup"><span data-stu-id="ac1c1-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac1c1-203"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac1c1-203"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="ac1c1-204">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac1c1-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac1c1-205">Provedor de serviços de gerenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="ac1c1-205">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

