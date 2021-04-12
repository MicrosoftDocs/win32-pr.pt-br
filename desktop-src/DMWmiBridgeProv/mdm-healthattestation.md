---
title: Classe MDM_HealthAttestation
description: A \_ classe MDM HealthAttestation permite que os gerentes de ti corporativos avaliem a integridade dos dispositivos gerenciados e tomem ações de política corporativa.
ms.assetid: 64f40ccc-98f6-48d6-bcd4-793375e3dbfb
keywords:
- Classe MDM_HealthAttestation
- Classe MDM_HealthAttestation, descrita
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7f76af135e7eac09b3b104e924b26efbb359b256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454921"
---
# <a name="mdm_healthattestation-class"></a><span data-ttu-id="ce316-105">\_Classe HealthAttestation do MDM</span><span class="sxs-lookup"><span data-stu-id="ce316-105">MDM\_HealthAttestation class</span></span>

<span data-ttu-id="ce316-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="ce316-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ce316-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="ce316-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ce316-108">A classe **MDM \_ HealthAttestation** permite que os gerentes de ti corporativos avaliem a integridade dos dispositivos gerenciados e tomem ações de política corporativa.</span><span class="sxs-lookup"><span data-stu-id="ce316-108">The **MDM\_HealthAttestation** class enables enterprise IT managers to assess the health of managed devices and take enterprise policy actions.</span></span>

<span data-ttu-id="ce316-109">Veja a seguir uma lista de funções executadas pelo CSP HealthAttestation:</span><span class="sxs-lookup"><span data-stu-id="ce316-109">The following is a list of functions performed by the HealthAttestation CSP:</span></span>

-   <span data-ttu-id="ce316-110">Coleta dados que são usados na verificação de Estados de integridade de dispositivos</span><span class="sxs-lookup"><span data-stu-id="ce316-110">Collects data that is used in verifying a devices health states</span></span>
-   <span data-ttu-id="ce316-111">Encaminha os dados para o Serviço de Atestado de Integridade (HAS)</span><span class="sxs-lookup"><span data-stu-id="ce316-111">Forwards the data to the Health Attestation Service (HAS)</span></span>
-   <span data-ttu-id="ce316-112">Provisiona o certificado de atestado de integridade do qual ele recebe</span><span class="sxs-lookup"><span data-stu-id="ce316-112">Provisions the Health Attestation Certificate that it receives from HAS</span></span>
-   <span data-ttu-id="ce316-113">Mediante solicitação, o encaminha o certificado de atestado de integridade (recebido de) e as informações de tempo de execução relacionadas ao servidor MDM para verificação</span><span class="sxs-lookup"><span data-stu-id="ce316-113">Upon request, forwards the Health Attestation Certificate (received from HAS) and related runtime information to the MDM Server for verification</span></span>

<span data-ttu-id="ce316-114">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ce316-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce316-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce316-115">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_HealthAttestation
{
  string  InstanceID;
  string  ParentID;
  sint32  Status;
  boolean ForceRetrieve;
  string  Certificate;
  string  Nonce;
  string  CorrelationID;
  sint32  TpmReadyStatus;
  sint32  MaxSupportedProtocolVersion;
  sint32  PreferredMaxProtocolVersion;
  sint32  CurrentProtocolVersion;
  string  HASEndpoint;
};
```

## <a name="members"></a><span data-ttu-id="ce316-116">Membros</span><span class="sxs-lookup"><span data-stu-id="ce316-116">Members</span></span>

<span data-ttu-id="ce316-117">A classe **MDM \_ HealthAttestation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ce316-117">The **MDM\_HealthAttestation** class has these types of members:</span></span>

-   [<span data-ttu-id="ce316-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce316-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="ce316-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ce316-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ce316-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce316-120">Methods</span></span>

<span data-ttu-id="ce316-121">A classe **MDM \_ HealthAttestation** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ce316-121">The **MDM\_HealthAttestation** class has these methods.</span></span>



| <span data-ttu-id="ce316-122">Método</span><span class="sxs-lookup"><span data-stu-id="ce316-122">Method</span></span>                                                                 | <span data-ttu-id="ce316-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce316-123">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce316-124">**VerifyHealthMethod**</span><span class="sxs-lookup"><span data-stu-id="ce316-124">**VerifyHealthMethod**</span></span>](mdm-healthattestation-verifyhealthmethod.md) | <span data-ttu-id="ce316-125">Método para notificar o dispositivo para preparar uma solicitação de verificação de certificado de integridade.</span><span class="sxs-lookup"><span data-stu-id="ce316-125">Method to notify the device to prepare a health certificate verification request.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ce316-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ce316-126">Properties</span></span>

<span data-ttu-id="ce316-127">A classe **MDM \_ HealthAttestation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ce316-127">The **MDM\_HealthAttestation** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ce316-128">Certificado</span><span class="sxs-lookup"><span data-stu-id="ce316-128">Certificate</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce316-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ce316-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce316-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ce316-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ce316-131">Qualificadores: **octetstring**</span><span class="sxs-lookup"><span data-stu-id="ce316-131">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ce316-132">CorrelationID</span><span class="sxs-lookup"><span data-stu-id="ce316-132">CorrelationID</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce316-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ce316-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce316-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ce316-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ce316-135">**CurrentProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="ce316-135">**CurrentProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce316-136">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ce316-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce316-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ce316-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ce316-138">TBD</span><span class="sxs-lookup"><span data-stu-id="ce316-138">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="ce316-139">ForceRetrieve</span><span class="sxs-lookup"><span data-stu-id="ce316-139">ForceRetrieve</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce316-140">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ce316-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ce316-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ce316-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ce316-142">HASEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce316-142">HASEndpoint</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce316-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ce316-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce316-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ce316-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ce316-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ce316-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce316-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ce316-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce316-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce316-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce316-148">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ce316-148">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ce316-149">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="ce316-149">Identifies the name of the parent node.</span></span> <span data-ttu-id="ce316-150">Para essa classe, a cadeia de caracteres é "HealthAttestation".</span><span class="sxs-lookup"><span data-stu-id="ce316-150">For this class, the string is "HealthAttestation".</span></span>

</dd> <dt>

<span data-ttu-id="ce316-151">**MaxSupportedProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="ce316-151">**MaxSupportedProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce316-152">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ce316-152">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce316-153">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ce316-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ce316-154">TBD</span><span class="sxs-lookup"><span data-stu-id="ce316-154">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="ce316-155">Momentos</span><span class="sxs-lookup"><span data-stu-id="ce316-155">Nonce</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce316-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ce316-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce316-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ce316-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ce316-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ce316-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce316-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ce316-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce316-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce316-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce316-161">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ce316-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ce316-162">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="ce316-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="ce316-163">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="ce316-163">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

<span data-ttu-id="ce316-164">**PreferredMaxProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="ce316-164">**PreferredMaxProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce316-165">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ce316-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce316-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ce316-166">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ce316-167">TBD</span><span class="sxs-lookup"><span data-stu-id="ce316-167">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="ce316-168">Status</span><span class="sxs-lookup"><span data-stu-id="ce316-168">Status</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce316-169">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ce316-169">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce316-170">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ce316-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ce316-171">TpmReadyStatus</span><span class="sxs-lookup"><span data-stu-id="ce316-171">TpmReadyStatus</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce316-172">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ce316-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce316-173">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ce316-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce316-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce316-174">Requirements</span></span>



| <span data-ttu-id="ce316-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce316-175">Requirement</span></span> | <span data-ttu-id="ce316-176">Valor</span><span class="sxs-lookup"><span data-stu-id="ce316-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce316-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce316-177">Minimum supported client</span></span><br/> | <span data-ttu-id="ce316-178">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ce316-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ce316-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce316-179">Minimum supported server</span></span><br/> | <span data-ttu-id="ce316-180">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ce316-180">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ce316-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce316-181">Namespace</span></span><br/>                | <span data-ttu-id="ce316-182">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="ce316-182">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ce316-183">MOF</span><span class="sxs-lookup"><span data-stu-id="ce316-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce316-184"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce316-184"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce316-185">DLL</span><span class="sxs-lookup"><span data-stu-id="ce316-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce316-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce316-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce316-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce316-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce316-188">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="ce316-188">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

