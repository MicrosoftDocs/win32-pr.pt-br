---
title: Classe MDM_VPNv2_DomainNameInformationList02_01
description: A \_ classe MDM VPNv2 \_ DomainNameInformationList02 \_ 01 descreve as regras de tabela de políticas de resolução de nomes (NRPT) para o perfil VPN.
ms.assetid: ed6863aa-f85e-4f65-9312-ddf60a8c0d5a
keywords:
- Classe MDM_VPNv2_DomainNameInformationList02_01
- Classe MDM_VPNv2_DomainNameInformationList02_01, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_DomainNameInformationList02_01
- MDM_VPNv2_DomainNameInformationList02_01.InstanceID
- MDM_VPNv2_DomainNameInformationList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec2fa2b6fd4216256a085caa23333bccc5f386d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919013"
---
# <a name="mdm_vpnv2_domainnameinformationlist02_01-class"></a><span data-ttu-id="bb46e-105">\_Classe MDM VPNv2 \_ DomainNameInformationList02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="bb46e-105">MDM\_VPNv2\_DomainNameInformationList02\_01 class</span></span>

<span data-ttu-id="bb46e-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="bb46e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bb46e-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="bb46e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bb46e-108">A classe **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** descreve as regras de tabela de políticas de resolução de nomes (NRPT) para o perfil VPN.</span><span class="sxs-lookup"><span data-stu-id="bb46e-108">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class describes the Name Resolution Policy Table (NRPT) rules for the VPN profile.</span></span>

<span data-ttu-id="bb46e-109">A Tabela de Políticas de Resolução de Nomes (NRPT) é uma tabela de namespaces e configurações correspondentes armazenadas no registro do Windows que determina o comportamento do cliente DNS ao emitir consultas e processar respostas.</span><span class="sxs-lookup"><span data-stu-id="bb46e-109">The Name Resolution Policy Table (NRPT) is a table of namespaces and corresponding settings stored in the Windows registry that determines the DNS client behavior when issuing queries and processing responses.</span></span> <span data-ttu-id="bb46e-110">Cada linha na NRPT representa uma regra para uma parte do namespace para o qual o cliente DNS emite consultas.</span><span class="sxs-lookup"><span data-stu-id="bb46e-110">Each row in the NRPT represents a rule for a portion of the namespace for which the DNS client issues queries.</span></span> <span data-ttu-id="bb46e-111">Antes de emitir consultas de resolução de nomes, o cliente DNS consulta a NRPT para determinar se qualquer sinalizador adicional deve ser definido na consulta.</span><span class="sxs-lookup"><span data-stu-id="bb46e-111">Before issuing name resolution queries, the DNS client consults the NRPT to determine if any additional flags must be set in the query.</span></span> <span data-ttu-id="bb46e-112">Depois de receber a resposta, o cliente consultará novamente o NRPT para verificar se há algum requisito especial de processamento ou política.</span><span class="sxs-lookup"><span data-stu-id="bb46e-112">After receiving the response, the client again consults the NRPT to check for any special processing or policy requirements.</span></span> <span data-ttu-id="bb46e-113">Na ausência da NRPT, o cliente opera com base nos servidores DNS e nos sufixos definidos na interface.</span><span class="sxs-lookup"><span data-stu-id="bb46e-113">In the absence of the NRPT, the client operates based on the DNS servers and suffixes set on the interface.</span></span>

<span data-ttu-id="bb46e-114">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bb46e-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb46e-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb46e-115">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DomainNameInformationList02_01
{
  string InstanceID;
  string ParentID;
  string DomainName;
  string DomainNameType;
  string DnsServers;
  string WebProxyServers;
};
```

## <a name="members"></a><span data-ttu-id="bb46e-116">Membros</span><span class="sxs-lookup"><span data-stu-id="bb46e-116">Members</span></span>

<span data-ttu-id="bb46e-117">A classe **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bb46e-117">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="bb46e-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bb46e-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb46e-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bb46e-119">Properties</span></span>

<span data-ttu-id="bb46e-120">A classe **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bb46e-120">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bb46e-121">DnsServers</span><span class="sxs-lookup"><span data-stu-id="bb46e-121">DnsServers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-dnsservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb46e-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb46e-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb46e-123">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bb46e-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bb46e-124">DomainName</span><span class="sxs-lookup"><span data-stu-id="bb46e-124">DomainName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb46e-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb46e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb46e-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bb46e-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bb46e-127">DomainNameType</span><span class="sxs-lookup"><span data-stu-id="bb46e-127">DomainNameType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainnametype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb46e-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb46e-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb46e-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bb46e-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bb46e-130">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bb46e-130">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb46e-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb46e-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb46e-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb46e-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb46e-133">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bb46e-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bb46e-134">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="bb46e-134">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="bb46e-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bb46e-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb46e-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb46e-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb46e-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb46e-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb46e-138">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bb46e-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bb46e-139">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="bb46e-139">Describes the full path to the parent node.</span></span> <span data-ttu-id="bb46e-140">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="bb46e-140">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="bb46e-141">WebProxyServers</span><span class="sxs-lookup"><span data-stu-id="bb46e-141">WebProxyServers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-webproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb46e-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb46e-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb46e-143">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bb46e-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb46e-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb46e-144">Requirements</span></span>



| <span data-ttu-id="bb46e-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb46e-145">Requirement</span></span> | <span data-ttu-id="bb46e-146">Valor</span><span class="sxs-lookup"><span data-stu-id="bb46e-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb46e-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb46e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="bb46e-148">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bb46e-148">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb46e-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb46e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="bb46e-150">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bb46e-150">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bb46e-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb46e-151">Namespace</span></span><br/>                | <span data-ttu-id="bb46e-152">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="bb46e-152">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bb46e-153">MOF</span><span class="sxs-lookup"><span data-stu-id="bb46e-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb46e-154"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb46e-154"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb46e-155">DLL</span><span class="sxs-lookup"><span data-stu-id="bb46e-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb46e-156"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb46e-156"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb46e-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb46e-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb46e-158">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="bb46e-158">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

