---
description: Recupera o status de validade da cadeia ou um certificado específico na cadeia.
title: 'Propriedade IChain2:: status'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Status
- IChain.Status
- Chain.Status
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23673289e2ff39d4180a4be8dc0be61f4a5cffc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758165"
---
# <a name="ichain2status-property"></a><span data-ttu-id="d2968-103">Propriedade IChain2:: status</span><span class="sxs-lookup"><span data-stu-id="d2968-103">IChain2::Status property</span></span>

<span data-ttu-id="d2968-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d2968-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d2968-105">Em vez disso, use a [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d2968-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d2968-106">A propriedade **status** recupera o status de validade da cadeia ou um certificado específico na cadeia.</span><span class="sxs-lookup"><span data-stu-id="d2968-106">The **Status** property retrieves the validity status of the chain or a specific certificate in the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2968-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2968-107">Syntax</span></span>


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a><span data-ttu-id="d2968-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d2968-108">Property value</span></span>

<span data-ttu-id="d2968-109">Um valor **longo** que representa o indicador de status de validade da cadeia ou o certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="d2968-109">A **LONG** value that represents the validity status indicator of the chain or the specified certificate.</span></span> <span data-ttu-id="d2968-110">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="d2968-110">The following table shows the possible values.</span></span> <span data-ttu-id="d2968-111">Essa propriedade conterá zero se a cadeia ou o certificado especificado for válido.</span><span class="sxs-lookup"><span data-stu-id="d2968-111">This property will contain zero if the chain or specified certificate is valid.</span></span> <span data-ttu-id="d2968-112">Caso contrário, essa propriedade conterá uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2968-112">Otherwise, this property will contain a combination of one or more of the following values.</span></span>

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span data-ttu-id="d2968-113"><span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ A relação de confiança \_ não é um \_ \_ tempo \_ válido** (&H00000001)</span><span class="sxs-lookup"><span data-stu-id="d2968-113"><span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM\_TRUST\_IS\_NOT\_TIME\_VALID** (&H00000001)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-114">Este certificado ou um dos certificados na cadeia de certificados não é válido.</span><span class="sxs-lookup"><span data-stu-id="d2968-114">This certificate or one of the certificates in the certificate chain is not time valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span data-ttu-id="d2968-115"><span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ A relação de confiança \_ não é um \_ \_ tempo \_ aninhado** (&H00000002)</span><span class="sxs-lookup"><span data-stu-id="d2968-115"><span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM\_TRUST\_IS\_NOT\_TIME\_NESTED** (&H00000002)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-116">Os certificados na cadeia não têm o tempo corretamente aninhado.</span><span class="sxs-lookup"><span data-stu-id="d2968-116">Certificates in the chain are not properly time nested.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span data-ttu-id="d2968-117"><span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ A confiança \_ é \_ revogada** (&H00000004)</span><span class="sxs-lookup"><span data-stu-id="d2968-117"><span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM\_TRUST\_IS\_REVOKED** (&H00000004)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-118">A confiança para este certificado ou um dos certificados na cadeia de certificados foi revogada.</span><span class="sxs-lookup"><span data-stu-id="d2968-118">Trust for this certificate or one of the certificates in the certificate chain has been revoked.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span data-ttu-id="d2968-119"><span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ A \_ confiança \_ não é uma \_ assinatura \_ válida** (&H00000008)</span><span class="sxs-lookup"><span data-stu-id="d2968-119"><span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM\_TRUST\_IS\_NOT\_SIGNATURE\_VALID** (&H00000008)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-120">O certificado ou um dos certificados na cadeia de certificados não tem uma assinatura válida.</span><span class="sxs-lookup"><span data-stu-id="d2968-120">The certificate or one of the certificates in the certificate chain does not have a valid signature.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span data-ttu-id="d2968-121"><span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ \_A relação \_ de confiança não é \_ válida \_ para \_ uso** (&H00000010)</span><span class="sxs-lookup"><span data-stu-id="d2968-121"><span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM\_TRUST\_IS\_NOT\_VALID\_FOR\_USAGE** (&H00000010)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-122">O certificado ou a cadeia de certificados não é válido para seu uso proposto.</span><span class="sxs-lookup"><span data-stu-id="d2968-122">The certificate or certificate chain is not valid for its proposed usage.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span data-ttu-id="d2968-123"><span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ CONFIAR \_ é \_ \_ raiz não confiável** (&H00000020)</span><span class="sxs-lookup"><span data-stu-id="d2968-123"><span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM\_TRUST\_IS\_UNTRUSTED\_ROOT** (&H00000020)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-124">O certificado ou a cadeia de certificados baseia-se em uma raiz não confiável.</span><span class="sxs-lookup"><span data-stu-id="d2968-124">The certificate or certificate chain is based on an untrusted root.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span data-ttu-id="d2968-125"><span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ \_Status de revogação de confiança \_ \_ desconhecido** (&H00000040)</span><span class="sxs-lookup"><span data-stu-id="d2968-125"><span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM\_TRUST\_REVOCATION\_STATUS\_UNKNOWN** (&H00000040)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-126">O status de revogação do certificado ou um dos certificados na cadeia de certificados é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="d2968-126">The revocation status of the certificate or one of the certificates in the certificate chain is unknown.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span data-ttu-id="d2968-127"><span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ A relação de confiança \_ é \_ cíclica** (&H00000080)</span><span class="sxs-lookup"><span data-stu-id="d2968-127"><span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM\_TRUST\_IS\_CYCLIC** (&H00000080)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-128">Um dos certificados na cadeia foi emitido por uma autoridade de [*certificação*](../secgloss/c-gly.md) que o certificado original certificou.</span><span class="sxs-lookup"><span data-stu-id="d2968-128">One of the certificates in the chain was issued by a [*certification authority*](../secgloss/c-gly.md) that the original certificate had certified.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span data-ttu-id="d2968-129"><span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ \_ \_ Extensão de confiança inválida** (&H00000100)</span><span class="sxs-lookup"><span data-stu-id="d2968-129"><span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM\_TRUST\_INVALID\_EXTENSION** (&H00000100)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-130">Um dos certificados tem uma extensão que não é válida.</span><span class="sxs-lookup"><span data-stu-id="d2968-130">One of the certificates has an extension that is not valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span data-ttu-id="d2968-131"><span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ CONFIAR \_ em \_ \_ restrições de política inválidas** (&H00000200)</span><span class="sxs-lookup"><span data-stu-id="d2968-131"><span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM\_TRUST\_INVALID\_POLICY\_CONSTRAINTS** (&H00000200)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-132">O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de política e um dos certificados emitidos tem uma extensão de mapeamento de política não permitida ou não tem uma extensão de políticas de emissão necessária.</span><span class="sxs-lookup"><span data-stu-id="d2968-132">The certificate or one of the certificates in the certificate chain has a policy constraints extension, and one of the issued certificates has a disallowed policy mapping extension or does not have a required issuance policies extension.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span data-ttu-id="d2968-133"><span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ CONFIAR \_ em \_ \_ restrições básicas inválidas** (&H00000400)</span><span class="sxs-lookup"><span data-stu-id="d2968-133"><span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM\_TRUST\_INVALID\_BASIC\_CONSTRAINTS** (&H00000400)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-134">O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições básicas e o certificado não pode ser usado para emitir outros certificados ou o comprimento do caminho da cadeia foi excedido.</span><span class="sxs-lookup"><span data-stu-id="d2968-134">The certificate or one of the certificates in the certificate chain has a basic constraints extension, and either the certificate cannot be used to issue other certificates, or the chain path length has been exceeded.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span data-ttu-id="d2968-135"><span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ CONFIAR \_ em \_ \_ restrições de nome inválido** (&H00000800)</span><span class="sxs-lookup"><span data-stu-id="d2968-135"><span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM\_TRUST\_INVALID\_NAME\_CONSTRAINTS** (&H00000800)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-136">O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome que não é válida.</span><span class="sxs-lookup"><span data-stu-id="d2968-136">The certificate or one of the certificates in the certificate chain has a name constraints extension that is not valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span data-ttu-id="d2968-137"><span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ TRUST \_ \_ não tem \_ suporte para a \_ \_ restrição de nome** (&H00001000)</span><span class="sxs-lookup"><span data-stu-id="d2968-137"><span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_SUPPORTED\_NAME\_CONSTRAINT** (&H00001000)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-138">O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome que contém campos sem suporte.</span><span class="sxs-lookup"><span data-stu-id="d2968-138">The certificate or one of the certificates in the certificate chain has a name constraints extension that contains unsupported fields.</span></span> <span data-ttu-id="d2968-139">Não há suporte para os campos mínimo e máximo.</span><span class="sxs-lookup"><span data-stu-id="d2968-139">The minimum and maximum fields are not supported.</span></span> <span data-ttu-id="d2968-140">Portanto, o mínimo sempre deve ser zero e o máximo deve estar sempre ausente.</span><span class="sxs-lookup"><span data-stu-id="d2968-140">Thus minimum must always be zero and maximum must always be absent.</span></span> <span data-ttu-id="d2968-141">Somente o UPN tem suporte para um outro nome.</span><span class="sxs-lookup"><span data-stu-id="d2968-141">Only UPN is supported for an Other Name.</span></span> <span data-ttu-id="d2968-142">Não há suporte para as seguintes opções de nome alternativo:</span><span class="sxs-lookup"><span data-stu-id="d2968-142">The following alternative name choices are not supported:</span></span>

-   <span data-ttu-id="d2968-143">Endereço X400</span><span class="sxs-lookup"><span data-stu-id="d2968-143">X400 Address</span></span>
-   <span data-ttu-id="d2968-144">Nome da parte EDI</span><span class="sxs-lookup"><span data-stu-id="d2968-144">EDI Party Name</span></span>
-   <span data-ttu-id="d2968-145">ID registrada</span><span class="sxs-lookup"><span data-stu-id="d2968-145">Registered Id</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span data-ttu-id="d2968-146"><span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ A relação de confiança \_ \_ não \_ definiu a \_ \_ restrição de nome** (&H00002000)</span><span class="sxs-lookup"><span data-stu-id="d2968-146"><span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_DEFINED\_NAME\_CONSTRAINT** (&H00002000)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-147">O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome e uma restrição de nome está ausente para uma das opções de nome no certificado final.</span><span class="sxs-lookup"><span data-stu-id="d2968-147">The certificate or one of the certificates in the certificate chain has a name constraints extension, and a name constraint is missing for one of the name choices in the end certificate.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span data-ttu-id="d2968-148"><span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ TRUST \_ \_ não \_ permitiu a \_ \_ restrição de nome** (&H00004000)</span><span class="sxs-lookup"><span data-stu-id="d2968-148"><span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_PERMITTED\_NAME\_CONSTRAINT** (&H00004000)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-149">O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome e não há uma restrição de nome permitida para uma das opções de nome no certificado final.</span><span class="sxs-lookup"><span data-stu-id="d2968-149">The certificate or one of the certificates in the certificate chain has a name constraints extension, and there is not a permitted name constraint for one of the name choices in the end certificate.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span data-ttu-id="d2968-150"><span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ A confiança \_ tem uma \_ \_ \_ restrição de nome excluída** (&H00008000)</span><span class="sxs-lookup"><span data-stu-id="d2968-150"><span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_EXCLUDED\_NAME\_CONSTRAINT** (&H00008000)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-151">O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome e uma das opções de nome no certificado final é explicitamente excluída.</span><span class="sxs-lookup"><span data-stu-id="d2968-151">The certificate or one of the certificates in the certificate chain has a name constraints extension, and one of the name choices in the end certificate is explicitly excluded.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span data-ttu-id="d2968-152"><span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ A relação de confiança \_ é de \_ \_ revogação offline** (&H01000000)</span><span class="sxs-lookup"><span data-stu-id="d2968-152"><span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM\_TRUST\_IS\_OFFLINE\_REVOCATION** (&H01000000)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-153">O status de revogação do certificado ou um dos certificados na cadeia de certificados está offline ou obsoleto.</span><span class="sxs-lookup"><span data-stu-id="d2968-153">The revocation status of the certificate or one of the certificates in the certificate chain is either offline or stale.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span data-ttu-id="d2968-154"><span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ CONFIAR \_ em \_ nenhuma \_ \_ política de cadeia de emissão** (&H02000000)</span><span class="sxs-lookup"><span data-stu-id="d2968-154"><span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM\_TRUST\_NO\_ISSUANCE\_CHAIN\_POLICY** (&H02000000)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-155">O certificado final não tem nenhuma política de emissão resultante e um dos certificados de AC emissora tem uma extensão de restrições de política que o exige.</span><span class="sxs-lookup"><span data-stu-id="d2968-155">The end certificate does not have any resultant issuance policies, and one of the issuing CA certificates has a policy constraints extension requiring it.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span data-ttu-id="d2968-156"><span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ CONFIAR \_ é \_ uma \_ cadeia parcial** (&H00010000)</span><span class="sxs-lookup"><span data-stu-id="d2968-156"><span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM\_TRUST\_IS\_PARTIAL\_CHAIN** (&H00010000)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-157">A cadeia de certificados não é concorrente.</span><span class="sxs-lookup"><span data-stu-id="d2968-157">The certificate chain is not compete.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span data-ttu-id="d2968-158"><span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ A \_ CTL de confiança \_ não é um \_ \_ tempo \_ válido** (&H00020000)</span><span class="sxs-lookup"><span data-stu-id="d2968-158"><span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_TIME\_VALID** (&H00020000)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-159">Uma CTL usada para criar essa cadeia não estava em tempo válido.</span><span class="sxs-lookup"><span data-stu-id="d2968-159">A CTL used to create this chain was not time valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span data-ttu-id="d2968-160"><span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ A \_ CTL \_ confiável \_ não é uma \_ assinatura \_ válida** (&H00040000)</span><span class="sxs-lookup"><span data-stu-id="d2968-160"><span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_SIGNATURE\_VALID** (&H00040000)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-161">Uma CTL usada para criar essa cadeia não tinha uma assinatura válida.</span><span class="sxs-lookup"><span data-stu-id="d2968-161">A CTL used to create this chain did not have a valid signature.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span data-ttu-id="d2968-162"><span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ \_A CTL \_ \_ de confiança não é \_ válida \_ para \_ uso** (&H00080000)</span><span class="sxs-lookup"><span data-stu-id="d2968-162"><span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_VALID\_FOR\_USAGE** (&H00080000)</span></span>


</dt> <dd>

<span data-ttu-id="d2968-163">Uma CTL usada para criar esta cadeia não é válida para esse uso.</span><span class="sxs-lookup"><span data-stu-id="d2968-163">A CTL used to create this chain is not valid for this usage.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2968-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2968-164">Requirements</span></span>



| <span data-ttu-id="d2968-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2968-165">Requirement</span></span> | <span data-ttu-id="d2968-166">Valor</span><span class="sxs-lookup"><span data-stu-id="d2968-166">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2968-167">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d2968-167">End of client support</span></span><br/> | <span data-ttu-id="d2968-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2968-168">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d2968-169">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="d2968-169">End of server support</span></span><br/> | <span data-ttu-id="d2968-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2968-170">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d2968-171">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d2968-171">Redistributable</span></span><br/>       | <span data-ttu-id="d2968-172">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2968-172">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d2968-173">DLL</span><span class="sxs-lookup"><span data-stu-id="d2968-173">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d2968-174"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2968-174"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
