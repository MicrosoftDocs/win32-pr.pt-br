---
title: Classe MDM_ClientCertificateInstall_SCEP01_01
description: A \_ classe MDM ClientCertificateInstall \_ SCEP01 \_ 01 habilita o acesso ao nó para instalação do certificado SCEP, usando IDs exclusivas para diferenciar solicitações de instalação de certificado diferentes.
ms.assetid: 273e6ef7-fd00-4049-bb8b-b9900b3d250b
keywords:
- Classe MDM_ClientCertificateInstall_SCEP01_01
- Classe MDM_ClientCertificateInstall_SCEP01_01, descrita
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_SCEP01_01
- MDM_ClientCertificateInstall_SCEP01_01.InstanceID
- MDM_ClientCertificateInstall_SCEP01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f8db7decb2e3ae0674381b2f17df10f82ee38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824609"
---
# <a name="mdm_clientcertificateinstall_scep01_01-class"></a><span data-ttu-id="19f02-105">\_Classe MDM ClientCertificateInstall \_ SCEP01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="19f02-105">MDM\_ClientCertificateInstall\_SCEP01\_01 class</span></span>

<span data-ttu-id="19f02-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="19f02-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="19f02-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="19f02-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="19f02-108">A classe **MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** habilita o acesso ao nó para instalação do certificado SCEP, usando IDs exclusivas para diferenciar solicitações de instalação de certificado diferentes.</span><span class="sxs-lookup"><span data-stu-id="19f02-108">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class enables access to the node for SCEP certificate installation, using unique IDs to differentiate different certificate install requests.</span></span>

<span data-ttu-id="19f02-109">Necessário para a instalação do certificado SCEP.</span><span class="sxs-lookup"><span data-stu-id="19f02-109">Required for SCEP certificate installation.</span></span>

<span data-ttu-id="19f02-110">As operações com suporte são obter, adicionar e excluir.</span><span class="sxs-lookup"><span data-stu-id="19f02-110">Supported operations are Get, Add and Delete.</span></span>

<span data-ttu-id="19f02-111">Chamar Delete no nó deve excluir o certificado SCEP correspondente.</span><span class="sxs-lookup"><span data-stu-id="19f02-111">Calling Delete on the this node should delete the corresponding SCEP certificate.</span></span>

<span data-ttu-id="19f02-112">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="19f02-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="19f02-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19f02-113">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_SCEP01_01
{
  string InstanceID;
  string ParentID;
  string CertThumbprint;
  sint32 Status;
  sint32 ErrorCode;
  string RespondentServerUrl;
};
```

## <a name="members"></a><span data-ttu-id="19f02-114">Membros</span><span class="sxs-lookup"><span data-stu-id="19f02-114">Members</span></span>

<span data-ttu-id="19f02-115">A classe **MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="19f02-115">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="19f02-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="19f02-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19f02-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="19f02-117">Properties</span></span>

<span data-ttu-id="19f02-118">A classe **MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="19f02-118">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="19f02-119">CertThumbprint</span><span class="sxs-lookup"><span data-stu-id="19f02-119">CertThumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-certthumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19f02-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19f02-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19f02-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="19f02-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="19f02-122">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="19f02-122">ErrorCode</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-errorcode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19f02-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="19f02-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="19f02-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="19f02-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="19f02-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="19f02-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19f02-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19f02-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19f02-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="19f02-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19f02-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19f02-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19f02-129">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="19f02-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="19f02-130">Para essa classe, uma ID exclusiva para diferenciar solicitações de instalação de certificado diferentes.</span><span class="sxs-lookup"><span data-stu-id="19f02-130">For this class, a unique ID to differentiate different certificate install requests.</span></span>

</dd> <dt>

<span data-ttu-id="19f02-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="19f02-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19f02-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19f02-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19f02-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="19f02-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19f02-134">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19f02-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19f02-135">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="19f02-135">Describes the full path to the parent node.</span></span>

<span data-ttu-id="19f02-136">A cadeia de caracteres é "./Vendor/MSFT/ClientCertificateInstall/SCEP"</span><span class="sxs-lookup"><span data-stu-id="19f02-136">The string is "./Vendor/MSFT/ClientCertificateInstall/SCEP"</span></span>

</dd> <dt>

[<span data-ttu-id="19f02-137">RespondentServerUrl</span><span class="sxs-lookup"><span data-stu-id="19f02-137">RespondentServerUrl</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-respondentserverurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19f02-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19f02-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19f02-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="19f02-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="19f02-140">Status</span><span class="sxs-lookup"><span data-stu-id="19f02-140">Status</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19f02-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="19f02-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="19f02-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="19f02-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19f02-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19f02-143">Requirements</span></span>



| <span data-ttu-id="19f02-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="19f02-144">Requirement</span></span> | <span data-ttu-id="19f02-145">Valor</span><span class="sxs-lookup"><span data-stu-id="19f02-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19f02-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19f02-146">Minimum supported client</span></span><br/> | <span data-ttu-id="19f02-147">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="19f02-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19f02-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19f02-148">Minimum supported server</span></span><br/> | <span data-ttu-id="19f02-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="19f02-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="19f02-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="19f02-150">Namespace</span></span><br/>                | <span data-ttu-id="19f02-151">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="19f02-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="19f02-152">MOF</span><span class="sxs-lookup"><span data-stu-id="19f02-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19f02-153"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19f02-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="19f02-154">DLL</span><span class="sxs-lookup"><span data-stu-id="19f02-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19f02-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19f02-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19f02-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="19f02-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19f02-157">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="19f02-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

