---
title: Classe MDM_ClientCertificateInstall_PFXCertInstall01_01
description: A \_ classe MDM ClientCertificateInstall \_ PFXCertInstall01 \_ 01 permite que a empresa use IDs exclusivas para diferenciar solicitações de instalação de certificado diferentes.
ms.assetid: 13b4d646-b49e-4a9d-b644-b52279249063
keywords:
- Classe MDM_ClientCertificateInstall_PFXCertInstall01_01
- Classe MDM_ClientCertificateInstall_PFXCertInstall01_01, descrita
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_PFXCertInstall01_01
- MDM_ClientCertificateInstall_PFXCertInstall01_01.InstanceID
- MDM_ClientCertificateInstall_PFXCertInstall01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed0bbbfad0e61a95fa8130921e639de1772233d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086001"
---
# <a name="mdm_clientcertificateinstall_pfxcertinstall01_01-class"></a><span data-ttu-id="3c5db-105">\_Classe MDM ClientCertificateInstall \_ PFXCertInstall01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="3c5db-105">MDM\_ClientCertificateInstall\_PFXCertInstall01\_01 class</span></span>

<span data-ttu-id="3c5db-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="3c5db-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3c5db-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="3c5db-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3c5db-108">A classe **MDM \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01** permite que a empresa use IDs exclusivas para diferenciar solicitações de instalação de certificado diferentes.</span><span class="sxs-lookup"><span data-stu-id="3c5db-108">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class enables the enterprise to use unique IDs to differentiate different certificate install requests.</span></span>

<span data-ttu-id="3c5db-109">Necessário para a instalação do certificado PFX.</span><span class="sxs-lookup"><span data-stu-id="3c5db-109">Required for PFX certificate installation.</span></span> <span data-ttu-id="3c5db-110">Chamar Delete nesse nó deve excluir os certificados e as chaves que foram instaladas pelo blob PFX correspondente.</span><span class="sxs-lookup"><span data-stu-id="3c5db-110">Calling Delete on the this node, should delete the certificates and the keys that were installed by the corresponding PFX blob.</span></span>

<span data-ttu-id="3c5db-111">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3c5db-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c5db-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c5db-112">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_PFXCertInstall01_01
{
  string  InstanceID;
  string  ParentID;
  sint32  KeyLocation;
  string  ContainerName;
  string  PFXCertBlob;
  string  PFXCertPassword;
  sint32  PFXCertPasswordEncryptionType;
  boolean PFXKeyExportable;
  string  Thumbprint;
  sint32  Status;
  string  PFXCertPasswordEncryptionStore;
};
```

## <a name="members"></a><span data-ttu-id="3c5db-113">Membros</span><span class="sxs-lookup"><span data-stu-id="3c5db-113">Members</span></span>

<span data-ttu-id="3c5db-114">A classe **MDM \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3c5db-114">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="3c5db-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3c5db-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c5db-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3c5db-116">Properties</span></span>

<span data-ttu-id="3c5db-117">A classe **MDM \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3c5db-117">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3c5db-118">ContainerName</span><span class="sxs-lookup"><span data-stu-id="3c5db-118">ContainerName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5db-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3c5db-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5db-120">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3c5db-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3c5db-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3c5db-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5db-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3c5db-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5db-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3c5db-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c5db-124">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3c5db-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3c5db-125">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="3c5db-125">Identifies the name of the parent node.</span></span> <span data-ttu-id="3c5db-126">Para essa classe, uma ID exclusiva para diferenciar solicitações de instalação de certificado diferentes.</span><span class="sxs-lookup"><span data-stu-id="3c5db-126">For this class, a unique ID to differentiate different certificate install requests.</span></span>

</dd> <dt>

[<span data-ttu-id="3c5db-127">KeyLocation</span><span class="sxs-lookup"><span data-stu-id="3c5db-127">KeyLocation</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-keylocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5db-128">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3c5db-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c5db-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3c5db-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3c5db-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3c5db-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5db-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3c5db-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5db-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3c5db-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c5db-133">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3c5db-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3c5db-134">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="3c5db-134">Describes the full path to the parent node.</span></span>

<span data-ttu-id="3c5db-135">A cadeia de caracteres é "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall"</span><span class="sxs-lookup"><span data-stu-id="3c5db-135">The string is "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall"</span></span>

</dd> <dt>

[<span data-ttu-id="3c5db-136">PFXCertBlob</span><span class="sxs-lookup"><span data-stu-id="3c5db-136">PFXCertBlob</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertblob)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5db-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3c5db-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5db-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3c5db-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c5db-139">Qualificadores: **octetstring**</span><span class="sxs-lookup"><span data-stu-id="3c5db-139">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c5db-140">PFXCertPassword</span><span class="sxs-lookup"><span data-stu-id="3c5db-140">PFXCertPassword</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5db-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3c5db-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5db-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3c5db-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c5db-143">PFXCertPasswordEncryptionStore</span><span class="sxs-lookup"><span data-stu-id="3c5db-143">PFXCertPasswordEncryptionStore</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptionstore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5db-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3c5db-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5db-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3c5db-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c5db-146">PFXCertPasswordEncryptionType</span><span class="sxs-lookup"><span data-stu-id="3c5db-146">PFXCertPasswordEncryptionType</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptiontype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5db-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3c5db-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c5db-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3c5db-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c5db-149">PFXKeyExportable</span><span class="sxs-lookup"><span data-stu-id="3c5db-149">PFXKeyExportable</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxkeyexportable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5db-150">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3c5db-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3c5db-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3c5db-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c5db-152">Status</span><span class="sxs-lookup"><span data-stu-id="3c5db-152">Status</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5db-153">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3c5db-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c5db-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3c5db-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c5db-155">Impressão Digital</span><span class="sxs-lookup"><span data-stu-id="3c5db-155">Thumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-thumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5db-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3c5db-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5db-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3c5db-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c5db-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c5db-158">Requirements</span></span>



| <span data-ttu-id="3c5db-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c5db-159">Requirement</span></span> | <span data-ttu-id="3c5db-160">Valor</span><span class="sxs-lookup"><span data-stu-id="3c5db-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c5db-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c5db-161">Minimum supported client</span></span><br/> | <span data-ttu-id="3c5db-162">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3c5db-162">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c5db-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c5db-163">Minimum supported server</span></span><br/> | <span data-ttu-id="3c5db-164">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3c5db-164">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3c5db-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c5db-165">Namespace</span></span><br/>                | <span data-ttu-id="3c5db-166">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="3c5db-166">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3c5db-167">MOF</span><span class="sxs-lookup"><span data-stu-id="3c5db-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c5db-168"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c5db-168"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c5db-169">DLL</span><span class="sxs-lookup"><span data-stu-id="3c5db-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c5db-170"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c5db-170"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c5db-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c5db-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c5db-172">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="3c5db-172">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

