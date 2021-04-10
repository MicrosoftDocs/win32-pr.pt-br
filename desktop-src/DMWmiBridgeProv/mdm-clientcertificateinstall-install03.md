---
title: Classe MDM_ClientCertificateInstall_Install03
description: A \_ classe MDM ClientCertificateInstall \_ Install03 permite que a empresa defina a instalação de certificados de cliente.
ms.assetid: 0083e54c-e621-47da-a20d-17c8bbf7dd3a
keywords:
- Classe MDM_ClientCertificateInstall_Install03
- Classe MDM_ClientCertificateInstall_Install03, descrita
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03
- MDM_ClientCertificateInstall_Install03.InstanceID
- MDM_ClientCertificateInstall_Install03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ac690808551e05d6ceba4f3c84bcaa521d4d01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086002"
---
# <a name="mdm_clientcertificateinstall_install03-class"></a><span data-ttu-id="08094-105">\_ \_ Classe INSTALL03 do MDM ClientCertificateInstall</span><span class="sxs-lookup"><span data-stu-id="08094-105">MDM\_ClientCertificateInstall\_Install03 class</span></span>

<span data-ttu-id="08094-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="08094-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="08094-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="08094-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="08094-108">A classe **MDM \_ ClientCertificateInstall \_ Install03** permite que a empresa defina a instalação de certificados de cliente. Necessário para o registro de certificado SCEP.</span><span class="sxs-lookup"><span data-stu-id="08094-108">The **MDM\_ClientCertificateInstall\_Install03** class enables the enterprise to set the installation of client certificates.Required for SCEP certificate enrollment.</span></span> <span data-ttu-id="08094-109">Solicitação relacionada à instalação do certificado SCEP do nó pai a ser agrupado.</span><span class="sxs-lookup"><span data-stu-id="08094-109">Parent node to group SCEP cert install related request.</span></span>

> [!Note]  
> <span data-ttu-id="08094-110">Embora os nós filho em instalar suportem comandos Replace, depois que o comando exec for enviado para o dispositivo, o dispositivo usará os valores definidos quando o comando exec for aceito.</span><span class="sxs-lookup"><span data-stu-id="08094-110">Even though the child nodes under Install support Replace commands, after the Exec command is sent to the device, the device will take the values which are set when the Exec command is accepted.</span></span> <span data-ttu-id="08094-111">O servidor não deve esperar que o valor do nó seja alterado depois que o comando exec for aceito, afetará o registro atual em andamento.</span><span class="sxs-lookup"><span data-stu-id="08094-111">The server should not expect the node value change after Exec command is accepted will impact the current undergoing enrollment.</span></span> <span data-ttu-id="08094-112">O servidor deve verificar o valor do nó de status e verificar se o dispositivo não está em um estágio desconhecido antes de alterar os valores de nó filho.</span><span class="sxs-lookup"><span data-stu-id="08094-112">The server should check the Status node value and make sure the device is not at unknown stage before changing child node values.</span></span>

 

<span data-ttu-id="08094-113">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="08094-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="08094-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08094-114">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_Install03
{
  string InstanceID;
  string ParentID;
  string ServerURL;
  string Challenge;
  string EKUMapping;
  sint32 KeyUsage;
  string SubjectName;
  sint32 KeyProtection;
  sint32 RetryDelay;
  sint32 RetryCount;
  string TemplateName;
  sint32 KeyLength;
  string HashAlgorithm;
  string CAThumbprint;
  string SubjectAlternativeNames;
  string ValidPeriod;
  sint32 ValidPeriodUnits;
  string ContainerName;
  string CustomTextToShowInPrompt;
  string AADKeyIdentifierList;
};
```

## <a name="members"></a><span data-ttu-id="08094-115">Membros</span><span class="sxs-lookup"><span data-stu-id="08094-115">Members</span></span>

<span data-ttu-id="08094-116">A **classe \_ \_ Install03 de MDM ClientCertificateInstall** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="08094-116">The **MDM\_ClientCertificateInstall\_Install03** class has these types of members:</span></span>

-   [<span data-ttu-id="08094-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="08094-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="08094-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08094-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="08094-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="08094-119">Methods</span></span>

<span data-ttu-id="08094-120">A **classe \_ \_ Install03 do MDM ClientCertificateInstall** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="08094-120">The **MDM\_ClientCertificateInstall\_Install03** class has these methods.</span></span>



| <span data-ttu-id="08094-121">Método</span><span class="sxs-lookup"><span data-stu-id="08094-121">Method</span></span>                                                                      | <span data-ttu-id="08094-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="08094-122">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="08094-123">**EnrollMethod**</span><span class="sxs-lookup"><span data-stu-id="08094-123">**EnrollMethod**</span></span>](mdm-clientcertificateinstall-install03-enrollmethod.md) | <span data-ttu-id="08094-124">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="08094-124">Required.</span></span> <span data-ttu-id="08094-125">Dispara o dispositivo para iniciar o registro de certificado.</span><span class="sxs-lookup"><span data-stu-id="08094-125">Triggers the device to start the certificate enrollment.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="08094-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08094-126">Properties</span></span>

<span data-ttu-id="08094-127">A **classe \_ \_ Install03 do MDM ClientCertificateInstall** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="08094-127">The **MDM\_ClientCertificateInstall\_Install03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="08094-128">AADKeyIdentifierList</span><span class="sxs-lookup"><span data-stu-id="08094-128">AADKeyIdentifierList</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-aadkeyidentifierlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08094-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08094-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-131">CAThumbprint</span><span class="sxs-lookup"><span data-stu-id="08094-131">CAThumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-cathumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08094-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08094-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-134">Desafio</span><span class="sxs-lookup"><span data-stu-id="08094-134">Challenge</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-challenge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08094-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08094-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-137">ContainerName</span><span class="sxs-lookup"><span data-stu-id="08094-137">ContainerName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08094-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08094-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-140">CustomTextToShowInPrompt</span><span class="sxs-lookup"><span data-stu-id="08094-140">CustomTextToShowInPrompt</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-customtexttoshowinprompt)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08094-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08094-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-143">EKUMapping</span><span class="sxs-lookup"><span data-stu-id="08094-143">EKUMapping</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-ekumapping)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08094-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08094-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-146">HashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="08094-146">HashAlgorithm</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-hashalgorithm)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08094-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08094-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08094-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="08094-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08094-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08094-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08094-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08094-152">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="08094-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="08094-153">Necessário para o registro de certificado SCEP.</span><span class="sxs-lookup"><span data-stu-id="08094-153">Required for SCEP certificate enrollment.</span></span> <span data-ttu-id="08094-154">Solicitação relacionada à instalação do certificado SCEP do nó pai a ser agrupado.</span><span class="sxs-lookup"><span data-stu-id="08094-154">Parent node to group SCEP cert install related request.</span></span>

<span data-ttu-id="08094-155">O formato é node.</span><span class="sxs-lookup"><span data-stu-id="08094-155">The Format is node.</span></span>

</dd> <dt>

[<span data-ttu-id="08094-156">KeyLength da</span><span class="sxs-lookup"><span data-stu-id="08094-156">KeyLength</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keylength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-157">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08094-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08094-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-159">Proteção contra keyprotection</span><span class="sxs-lookup"><span data-stu-id="08094-159">KeyProtection</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keyprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-160">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08094-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08094-161">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-162">Uso de</span><span class="sxs-lookup"><span data-stu-id="08094-162">KeyUsage</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-163">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08094-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08094-164">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08094-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="08094-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08094-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08094-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08094-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08094-168">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="08094-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="08094-169">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="08094-169">Describes the full path to the parent node.</span></span>

<span data-ttu-id="08094-170">A cadeia de caracteres é "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueId*"</span><span class="sxs-lookup"><span data-stu-id="08094-170">The string is "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueID*"</span></span>

</dd> <dt>

[<span data-ttu-id="08094-171">RetryCount</span><span class="sxs-lookup"><span data-stu-id="08094-171">RetryCount</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrycount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-172">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08094-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08094-173">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-174">RetryDelay</span><span class="sxs-lookup"><span data-stu-id="08094-174">RetryDelay</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrydelay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-175">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08094-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08094-176">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-177">ServerURL</span><span class="sxs-lookup"><span data-stu-id="08094-177">ServerURL</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-serverurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08094-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08094-179">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-180">SubjectAlternativeNames</span><span class="sxs-lookup"><span data-stu-id="08094-180">SubjectAlternativeNames</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectalternativenames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08094-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08094-182">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-183">SubjectName</span><span class="sxs-lookup"><span data-stu-id="08094-183">SubjectName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08094-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08094-185">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-185">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-186">TemplateName</span><span class="sxs-lookup"><span data-stu-id="08094-186">TemplateName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-templatename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08094-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08094-188">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-188">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-189">ValidPeriod</span><span class="sxs-lookup"><span data-stu-id="08094-189">ValidPeriod</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08094-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08094-191">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-191">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08094-192">ValidPeriodUnits</span><span class="sxs-lookup"><span data-stu-id="08094-192">ValidPeriodUnits</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiodunits)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08094-193">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08094-193">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08094-194">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08094-194">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08094-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08094-195">Requirements</span></span>



| <span data-ttu-id="08094-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="08094-196">Requirement</span></span> | <span data-ttu-id="08094-197">Valor</span><span class="sxs-lookup"><span data-stu-id="08094-197">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08094-198">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08094-198">Minimum supported client</span></span><br/> | <span data-ttu-id="08094-199">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="08094-199">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="08094-200">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08094-200">Minimum supported server</span></span><br/> | <span data-ttu-id="08094-201">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="08094-201">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="08094-202">Namespace</span><span class="sxs-lookup"><span data-stu-id="08094-202">Namespace</span></span><br/>                | <span data-ttu-id="08094-203">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="08094-203">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="08094-204">MOF</span><span class="sxs-lookup"><span data-stu-id="08094-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08094-205"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08094-205"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="08094-206">DLL</span><span class="sxs-lookup"><span data-stu-id="08094-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08094-207"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08094-207"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08094-208">Confira também</span><span class="sxs-lookup"><span data-stu-id="08094-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08094-209">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="08094-209">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

