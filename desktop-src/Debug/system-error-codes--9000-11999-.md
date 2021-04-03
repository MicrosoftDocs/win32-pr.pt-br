---
description: Descreve os códigos de erro 9000-11999 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: Códigos de erro do sistema (9000-11999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 01eb071962d8d0f5beb801067ce1d72adc796bad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646369"
---
# <a name="system-error-codes-9000-11999"></a><span data-ttu-id="0dc4b-103">Códigos de erro do sistema (9000-11999)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-103">System Error Codes (9000-11999)</span></span>

> [!NOTE]
> <span data-ttu-id="0dc4b-104">Essas informações destinam-se a desenvolvedores Depurando erros do sistema.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="0dc4b-105">Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0dc4b-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="0dc4b-106">A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) (erros 9000 a 11999).</span><span class="sxs-lookup"><span data-stu-id="0dc4b-106">The following list describes [system error codes](system-error-codes.md) (errors 9000 to 11999).</span></span> <span data-ttu-id="0dc4b-107">Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="0dc4b-108">Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="0dc4b-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="0dc4b-109"><span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**erro \_ de \_ RCODE de \_ formato de \_ erro DNS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-109"><span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**DNS\_ERROR\_RCODE\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-110">9001 (0x2329)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-110">9001 (0x2329)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-111">O servidor DNS não pode interpretar o formato.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-111">DNS server unable to interpret format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-112"><span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**erro de DNS \_ \_ RCODE \_ falha do servidor \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-112"><span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**DNS\_ERROR\_RCODE\_SERVER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-113">9002 (0x232A)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-113">9002 (0x232A)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-114">Falha do servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-114">DNS server failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-115"><span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**erro \_ DNS \_ RCODE \_ nome \_ do erro**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-115"><span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**DNS\_ERROR\_RCODE\_NAME\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-116">9003 (0x232B)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-116">9003 (0x232B)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-117">O nome do DNS não existe.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-117">DNS name does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-118"><span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**\_RCODE de erro DNS \_ \_ não \_ implementado**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-118"><span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**DNS\_ERROR\_RCODE\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-119">9004 (0x232C)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-119">9004 (0x232C)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-120">O servidor de nomes não dá suporte à solicitação DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-120">DNS request not supported by name server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-121"><span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**erro de DNS \_ \_ RCODE \_ recusado**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-121"><span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**DNS\_ERROR\_RCODE\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-122">9005 (0x232D)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-122">9005 (0x232D)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-123">Operação DNS recusada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-123">DNS operation refused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-124"><span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**erro de DNS \_ \_ RCODE \_ YXDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-124"><span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**DNS\_ERROR\_RCODE\_YXDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-125">9006 (0x232E)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-125">9006 (0x232E)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-126">O nome DNS que não deveria existir, existe.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-126">DNS name that ought not exist, does exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-127"><span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**erro de DNS \_ \_ RCODE \_ YXRRSET**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-127"><span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**DNS\_ERROR\_RCODE\_YXRRSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-128">9007 (0x232F)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-128">9007 (0x232F)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-129">O conjunto de RR DNS que não deveria existir, existe.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-129">DNS RR set that ought not exist, does exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-130"><span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**erro de DNS \_ \_ RCODE \_ NXRRSET**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-130"><span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**DNS\_ERROR\_RCODE\_NXRRSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-131">9008 (0x2330)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-131">9008 (0x2330)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-132">O conjunto de RR do DNS que deveria existir não existe.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-132">DNS RR set that ought to exist, does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-133"><span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**erro de DNS \_ \_ RCODE não \_ auth**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-133"><span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**DNS\_ERROR\_RCODE\_NOTAUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-134">9009 (0x2331)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-134">9009 (0x2331)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-135">O servidor DNS não é autoritativo para a zona.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-135">DNS server not authoritative for zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-136"><span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**erro de DNS \_ \_ RCODE não \_ zona**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-136"><span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**DNS\_ERROR\_RCODE\_NOTZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-137">9010 (0x2332)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-137">9010 (0x2332)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-138">O nome DNS na atualização ou pré-requisito não está na zona.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-138">DNS name in update or prereq is not in zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-139"><span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**erro de DNS \_ \_ RCODE \_ BADSIG**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-139"><span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**DNS\_ERROR\_RCODE\_BADSIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-140">9016 (0x2338)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-140">9016 (0x2338)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-141">Falha na verificação da assinatura DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-141">DNS signature failed to verify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-142"><span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**erro de DNS \_ \_ RCODE \_ BADKEY**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-142"><span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**DNS\_ERROR\_RCODE\_BADKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-143">9017 (0x2339)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-143">9017 (0x2339)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-144">Chave inadequada do DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-144">DNS bad key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-145"><span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**erro de DNS \_ \_ RCODE \_ Badtime**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-145"><span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**DNS\_ERROR\_RCODE\_BADTIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-146">9018 (0x233A)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-146">9018 (0x233A)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-147">Validade da assinatura DNS expirada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-147">DNS signature validity expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-148"><span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**o mestre de erro de DNS é \_ \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-148"><span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**DNS\_ERROR\_KEYMASTER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-149">9101 (0x238D)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-149">9101 (0x238D)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-150">Somente o servidor DNS que atua como mestre de chave para a zona pode executar esta operação.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-150">Only the DNS server acting as the key master for the zone may perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-151"><span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**\_erro \_ de DNS não \_ permitido \_ em \_ zona assinada \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-151"><span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_SIGNED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-152">9102 (0x238E)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-152">9102 (0x238E)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-153">Esta operação não é permitida em uma zona assinada ou tem chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-153">This operation is not allowed on a zone that is signed or has signing keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-154"><span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**DNS \_ \_ de erro \_ de NSEC3 incompatível \_ com \_ RSA \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-154"><span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**DNS\_ERROR\_NSEC3\_INCOMPATIBLE\_WITH\_RSA\_SHA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-155">9103 (0x238F)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-155">9103 (0x238F)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-156">O NSEC3 não é compatível com o algoritmo RSA-SHA-1.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-156">NSEC3 is not compatible with the RSA-SHA-1 algorithm.</span></span> <span data-ttu-id="0dc4b-157">Escolha um algoritmo diferente ou use NSEC.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-157">Choose a different algorithm or use NSEC.</span></span>

<span data-ttu-id="0dc4b-158">Esse valor também foi nomeado **DNS \_ erro \_ \_ \_ parâmetros de NSEC3 inválido**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-158">This value was also named **DNS\_ERROR\_INVALID\_NSEC3\_PARAMETERS**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-159"><span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**erro de DNS \_ \_ não \_ há \_ \_ descritores de chave de assinatura suficientes \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-159"><span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**DNS\_ERROR\_NOT\_ENOUGH\_SIGNING\_KEY\_DESCRIPTORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-160">9104 (0x2390)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-160">9104 (0x2390)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-161">A zona não tem chaves de assinatura suficientes.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-161">The zone does not have enough signing keys.</span></span> <span data-ttu-id="0dc4b-162">Deve haver pelo menos uma KSK (chave de assinatura de chave) e pelo menos uma ZSK (chave de assinatura de zona).</span><span class="sxs-lookup"><span data-stu-id="0dc4b-162">There must be at least one key signing key (KSK) and at least one zone signing key (ZSK).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-163"><span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**algoritmo de erro de DNS \_ \_ sem suporte \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-163"><span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**DNS\_ERROR\_UNSUPPORTED\_ALGORITHM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-164">9105 (0x2391)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-164">9105 (0x2391)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-165">Não há suporte para o algoritmo especificado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-165">The specified algorithm is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-166"><span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**\_tamanho de \_ \_ chave inválido do erro \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-166"><span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**DNS\_ERROR\_INVALID\_KEY\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-167">9106 (0x2392)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-167">9106 (0x2392)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-168">Não há suporte para o tamanho de chave especificado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-168">The specified key size is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-169"><span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**\_chave de assinatura de erro DNS \_ \_ \_ não \_ acessível**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-169"><span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**DNS\_ERROR\_SIGNING\_KEY\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-170">9107 (0x2393)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-170">9107 (0x2393)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-171">Uma ou mais das chaves de assinatura de uma zona não podem ser acessadas pelo servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-171">One or more of the signing keys for a zone are not accessible to the DNS server.</span></span> <span data-ttu-id="0dc4b-172">A assinatura de zona não estará operacional até que esse erro seja resolvido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-172">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-173"><span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**\_o KSP de erro DNS não \_ \_ \_ \_ oferece suporte à \_ proteção**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-173"><span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**DNS\_ERROR\_KSP\_DOES\_NOT\_SUPPORT\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-174">9108 (0x2394)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-174">9108 (0x2394)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-175">O provedor de armazenamento de chaves especificado não dá suporte à proteção de dados DPAPI + +.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-175">The specified key storage provider does not support DPAPI++ data protection.</span></span> <span data-ttu-id="0dc4b-176">A assinatura de zona não estará operacional até que esse erro seja resolvido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-176">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-177"><span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**erro \_ de \_ \_ proteção de dados inesperada \_ \_ do DNS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-177"><span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**DNS\_ERROR\_UNEXPECTED\_DATA\_PROTECTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-178">9109 (0x2395)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-178">9109 (0x2395)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-179">Foi encontrado um erro não esperado DPAPI + +.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-179">An unexpected DPAPI++ error was encountered.</span></span> <span data-ttu-id="0dc4b-180">A assinatura de zona não estará operacional até que esse erro seja resolvido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-180">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-181"><span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**erro \_ de \_ CNG inesperado de erro DNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-181"><span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**DNS\_ERROR\_UNEXPECTED\_CNG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-182">9110 (0x2396)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-182">9110 (0x2396)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-183">Foi encontrado um erro de criptografia inesperado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-183">An unexpected crypto error was encountered.</span></span> <span data-ttu-id="0dc4b-184">A assinatura de zona pode não estar operacional até que esse erro seja resolvido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-184">Zone signing may not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-185"><span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**\_erro DNS \_ versão desconhecida do \_ parâmetro de assinatura \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-185"><span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**DNS\_ERROR\_UNKNOWN\_SIGNING\_PARAMETER\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-186">9111 (0x2397)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-186">9111 (0x2397)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-187">O servidor DNS encontrou uma chave de assinatura com uma versão desconhecida.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-187">The DNS server encountered a signing key with an unknown version.</span></span> <span data-ttu-id="0dc4b-188">A assinatura de zona não estará operacional até que esse erro seja resolvido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-188">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-189"><span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**\_KSP de erro DNS \_ \_ não \_ acessível**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-189"><span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**DNS\_ERROR\_KSP\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-190">9112 (0x2398)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-190">9112 (0x2398)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-191">O provedor de serviços de chave especificado não pode ser aberto pelo servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-191">The specified key service provider cannot be opened by the DNS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-192"><span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**erro de DNS em excesso de \_ \_ \_ \_ SKDS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-192"><span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**DNS\_ERROR\_TOO\_MANY\_SKDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-193">9113 (0x2399)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-193">9113 (0x2399)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-194">O servidor DNS não pode aceitar mais chaves de assinatura com o algoritmo especificado e o valor do sinalizador KSK para essa zona.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-194">The DNS server cannot accept any more signing keys with the specified algorithm and KSK flag value for this zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-195"><span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**erro de DNS \_ \_ \_ período de substituição inválido \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-195"><span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**DNS\_ERROR\_INVALID\_ROLLOVER\_PERIOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-196">9114 (0x239A)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-196">9114 (0x239A)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-197">O período de substituição especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-197">The specified rollover period is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-198"><span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**erro de DNS \_ \_ \_ deslocamento de substituição inicial inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-198"><span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**DNS\_ERROR\_INVALID\_INITIAL\_ROLLOVER\_OFFSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-199">9115 (0x239B)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-199">9115 (0x239B)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-200">O deslocamento de substituição inicial especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-200">The specified initial rollover offset is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-201"><span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**\_ \_ substituição de erro \_ de DNS em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-201"><span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**DNS\_ERROR\_ROLLOVER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-202">9116 (0x239C)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-202">9116 (0x239C)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-203">A chave de assinatura especificada já está em processo de substituição de chaves.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-203">The specified signing key is already in process of rolling over keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-204"><span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**a \_ chave de espera de erro DNS \_ \_ \_ não \_ está presente**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-204"><span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**DNS\_ERROR\_STANDBY\_KEY\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-205">9117 (0x239D)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-205">9117 (0x239D)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-206">A chave de assinatura especificada não tem uma chave em espera para revogar.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-206">The specified signing key does not have a standby key to revoke.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-207"><span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**\_erro \_ de DNS não \_ permitido \_ em \_ ZSK**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-207"><span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ZSK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-208">9118 (0x239E)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-208">9118 (0x239E)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-209">Esta operação não é permitida em uma ZSK (chave de assinatura de zona).</span><span class="sxs-lookup"><span data-stu-id="0dc4b-209">This operation is not allowed on a zone signing key (ZSK).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-210"><span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**\_erro \_ de DNS não \_ permitido \_ no \_ \_ SKD ativo**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-210"><span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ACTIVE\_SKD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-211">9119 (0x239F)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-211">9119 (0x239F)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-212">Esta operação não é permitida em uma chave de assinatura ativa.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-212">This operation is not allowed on an active signing key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-213"><span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**\_substituição de erro DNS \_ \_ já \_ colocada na fila**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-213"><span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**DNS\_ERROR\_ROLLOVER\_ALREADY\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-214">9120 (0x23A0)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-214">9120 (0x23A0)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-215">A chave de assinatura especificada já está na fila para substituição.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-215">The specified signing key is already queued for rollover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-216"><span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**\_erro \_ de DNS não \_ permitido \_ em \_ zona não assinada \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-216"><span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_UNSIGNED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-217">9121 (0x23A1)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-217">9121 (0x23A1)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-218">Esta operação não é permitida em uma zona não assinada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-218">This operation is not allowed on an unsigned zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-219"><span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**erro de DNS- \_ \_ mestre inadequado \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-219"><span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**DNS\_ERROR\_BAD\_KEYMASTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-220">9122 (0x23A2)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-220">9122 (0x23A2)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-221">Esta operação não pôde ser concluída porque o servidor DNS listado como o mestre de chave atual para esta zona está inoperante ou configurado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-221">This operation could not be completed because the DNS server listed as the current key master for this zone is down or misconfigured.</span></span> <span data-ttu-id="0dc4b-222">Resolva o problema no mestre de chave atual dessa zona ou use outro servidor DNS para executar a função mestre de chave.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-222">Resolve the problem on the current key master for this zone or use another DNS server to seize the key master role.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-223"><span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**erro de DNS \_ \_ período de \_ validade de assinatura inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-223"><span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**DNS\_ERROR\_INVALID\_SIGNATURE\_VALIDITY\_PERIOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-224">9123 (0x23A3)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-224">9123 (0x23A3)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-225">O período de validade da assinatura especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-225">The specified signature validity period is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-226"><span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**\_Erro DNS \_ \_ contagem de \_ iteração NSEC3 inválida \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-226"><span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**DNS\_ERROR\_INVALID\_NSEC3\_ITERATION\_COUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-227">9124 (0x23A4)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-227">9124 (0x23A4)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-228">A contagem de iteração NSEC3 especificada é maior do que a permitida pelo comprimento mínimo de chave usado na zona.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-228">The specified NSEC3 iteration count is higher than allowed by the minimum key length used in the zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-229"><span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**erro DNS o \_ \_ DNSSEC \_ está \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-229"><span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**DNS\_ERROR\_DNSSEC\_IS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-230">9125 (0x23A5)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-230">9125 (0x23A5)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-231">Esta operação não pôde ser concluída porque o servidor DNS foi configurado com recursos de DNSSEC desabilitados.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-231">This operation could not be completed because the DNS server has been configured with DNSSEC features disabled.</span></span> <span data-ttu-id="0dc4b-232">Habilite o DNSSEC no servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-232">Enable DNSSEC on the DNS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-233"><span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**\_ \_ XML inválido de erro DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-233"><span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**DNS\_ERROR\_INVALID\_XML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-234">9126 (0x23A6)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-234">9126 (0x23A6)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-235">Esta operação não pôde ser concluída porque o fluxo XML recebido está vazio ou é sintaticamente inválido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-235">This operation could not be completed because the XML stream received is empty or syntactically invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-236"><span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**erro de DNS \_ \_ sem \_ \_ âncoras de confiança válidas \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-236"><span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**DNS\_ERROR\_NO\_VALID\_TRUST\_ANCHORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-237">9127 (0x23A7)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-237">9127 (0x23A7)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-238">Esta operação foi concluída, mas nenhuma âncora de confiança foi adicionada porque todas as âncoras de confiança recebidas eram inválidas, sem suporte, expiraram ou não se tornarão válidas em menos de 30 dias.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-238">This operation completed, but no trust anchors were added because all of the trust anchors received were either invalid, unsupported, expired, or would not become valid in less than 30 days.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-239"><span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**substituição de erro de DNS \_ \_ \_ não \_ puder ser acessada**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-239"><span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**DNS\_ERROR\_ROLLOVER\_NOT\_POKEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-240">9128 (0x23A8)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-240">9128 (0x23A8)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-241">A chave de assinatura especificada não está aguardando a atualização do DS pai.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-241">The specified signing key is not waiting for parental DS update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-242"><span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**Erro de DNS \_ \_ colisão de nome de NSEC3 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-242"><span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**DNS\_ERROR\_NSEC3\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-243">9129 (0x23A9)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-243">9129 (0x23A9)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-244">Colisão de hash detectada durante assinatura de NSEC3.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-244">Hash collision detected during NSEC3 signing.</span></span> <span data-ttu-id="0dc4b-245">Especifique um Salt fornecido pelo usuário diferente ou use um Salt gerado aleatoriamente e tente assinar a zona novamente.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-245">Specify a different user-provided salt, or use a randomly generated salt, and attempt to sign the zone again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-246"><span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**\_Erro DNS \_ \_ de NSEC incompatível \_ com \_ NSEC3 \_ RSA \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-246"><span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**DNS\_ERROR\_NSEC\_INCOMPATIBLE\_WITH\_NSEC3\_RSA\_SHA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-247">9130 (0x23AA)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-247">9130 (0x23AA)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-248">NSEC não é compatível com o algoritmo NSEC3-RSA-SHA-1.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-248">NSEC is not compatible with the NSEC3-RSA-SHA-1 algorithm.</span></span> <span data-ttu-id="0dc4b-249">Escolha um algoritmo diferente ou use NSEC3.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-249">Choose a different algorithm or use NSEC3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-250"><span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**informações de DNS \_ \_ sem \_ registros**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-250"><span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**DNS\_INFO\_NO\_RECORDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-251">9501 (0x251D)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-251">9501 (0x251D)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-252">Não foram encontrados registros para uma determinada consulta ao DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-252">No records found for given DNS query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-253"><span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**erro DNS de \_ \_ pacote insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-253"><span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**DNS\_ERROR\_BAD\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-254">9502 (0x251E)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-254">9502 (0x251E)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-255">Pacote DNS inadequado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-255">Bad DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-256"><span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**erro de DNS \_ \_ sem \_ pacote**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-256"><span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**DNS\_ERROR\_NO\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-257">9503 (0x251F)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-257">9503 (0x251F)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-258">Nenhum pacote DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-258">No DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-259"><span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**erro de DNS \_ \_ RCODE**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-259"><span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**DNS\_ERROR\_RCODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-260">9504 (0x2520)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-260">9504 (0x2520)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-261">Erro de DNS, verifique RCODE.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-261">DNS error, check rcode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-262"><span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**pacote de erro de DNS \_ \_ não seguro \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-262"><span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**DNS\_ERROR\_UNSECURE\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-263">9505 (0x2521)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-263">9505 (0x2521)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-264">Pacote DNS não seguro.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-264">Unsecured DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-265"><span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**solicitação de DNS \_ \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-265"><span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**DNS\_REQUEST\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-266">9506 (0x2522)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-266">9506 (0x2522)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-267">A solicitação de consulta DNS está pendente.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-267">DNS query request is pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-268"><span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**\_ \_ tipo inválido de erro DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-268"><span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**DNS\_ERROR\_INVALID\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-269">9551 (0x254F)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-269">9551 (0x254F)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-270">Tipo DNS inválido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-270">Invalid DNS type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-271"><span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**\_ \_ \_ endereço IP inválido do erro DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-271"><span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**DNS\_ERROR\_INVALID\_IP\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-272">9552 (0x2550)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-272">9552 (0x2550)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-273">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-273">Invalid IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-274"><span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**\_ \_ Propriedade inválida de erro DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-274"><span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**DNS\_ERROR\_INVALID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-275">9553 (0x2551)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-275">9553 (0x2551)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-276">Propriedade inválida.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-276">Invalid property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-277"><span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**erro de DNS \_ \_ tente \_ novamente \_ mais tarde**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-277"><span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**DNS\_ERROR\_TRY\_AGAIN\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-278">9554 (0x2552)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-278">9554 (0x2552)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-279">Tente a operação DNS novamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-279">Try DNS operation again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-280"><span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**erro de DNS \_ \_ não \_ exclusivo**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-280"><span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**DNS\_ERROR\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-281">9555 (0x2553)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-281">9555 (0x2553)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-282">O registro para o nome e tipo fornecidos não é exclusivo.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-282">Record for given name and type is not unique.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-283"><span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**\_erro DNS \_ não \_ RFC \_ nome**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-283"><span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**DNS\_ERROR\_NON\_RFC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-284">9556 (0x2554)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-284">9556 (0x2554)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-285">O nome DNS não está em conformidade com as especificações RFC.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-285">DNS name does not comply with RFC specifications.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-286"><span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**\_FQDN de status DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-286"><span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**DNS\_STATUS\_FQDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-287">9557 (0x2555)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-287">9557 (0x2555)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-288">O nome DNS é um nome DNS totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-288">DNS name is a fully-qualified DNS name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-289"><span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**nome do DNS de \_ status \_ pontilhado \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-289"><span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**DNS\_STATUS\_DOTTED\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-290">9558 (0x2556)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-290">9558 (0x2556)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-291">O nome DNS é pontilhado (vários rótulos).</span><span class="sxs-lookup"><span data-stu-id="0dc4b-291">DNS name is dotted (multi-label).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-292"><span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**\_nome de \_ \_ parte única do status \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-292"><span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**DNS\_STATUS\_SINGLE\_PART\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-293">9559 (0x2557)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-293">9559 (0x2557)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-294">O nome DNS é um nome de parte única.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-294">DNS name is a single-part name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-295"><span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**erro de DNS \_ \_ \_ nome inválido \_ Char**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-295"><span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**DNS\_ERROR\_INVALID\_NAME\_CHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-296">9560 (0x2558)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-296">9560 (0x2558)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-297">O nome DNS contém um caractere inválido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-297">DNS name contains an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-298"><span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**\_ \_ nome numérico do erro DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-298"><span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**DNS\_ERROR\_NUMERIC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-299">9561 (0x2559)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-299">9561 (0x2559)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-300">O nome DNS é totalmente numérico.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-300">DNS name is entirely numeric.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-301"><span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**\_erro \_ de DNS não \_ permitido \_ no \_ \_ servidor raiz**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-301"><span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ROOT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-302">9562 (0x255A)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-302">9562 (0x255A)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-303">A operação solicitada não é permitida em um servidor raiz DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-303">The operation requested is not permitted on a DNS root server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-304"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**erro de DNS \_ \_ não \_ permitido \_ em \_ delegação**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-304"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**DNS\_ERROR\_NOT\_ALLOWED\_UNDER\_DELEGATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-305">9563 (0x255B)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-305">9563 (0x255B)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-306">Não foi possível criar o registro porque esta parte do namespace DNS foi delegada a outro servidor.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-306">The record could not be created because this part of the DNS namespace has been delegated to another server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-307"><span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**erro de DNS \_ \_ não pode \_ localizar \_ dicas de raiz \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-307"><span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**DNS\_ERROR\_CANNOT\_FIND\_ROOT\_HINTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-308">9564 (0x255C)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-308">9564 (0x255C)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-309">O servidor DNS não pôde encontrar um conjunto de dicas de raiz.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-309">The DNS server could not find a set of root hints.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-310"><span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**\_dicas de \_ raiz inconsistentes de erro DNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-310"><span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**DNS\_ERROR\_INCONSISTENT\_ROOT\_HINTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-311">9565 (0x255D)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-311">9565 (0x255D)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-312">O servidor DNS encontrou dicas de raiz, mas elas não eram consistentes em todos os adaptadores.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-312">The DNS server found root hints but they were not consistent across all adapters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-313"><span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**valor de DWORD de erro de DNS \_ \_ \_ \_ muito \_ pequeno**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-313"><span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**DNS\_ERROR\_DWORD\_VALUE\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-314">9566 (0x255E)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-314">9566 (0x255E)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-315">O valor especificado é muito pequeno para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-315">The specified value is too small for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-316"><span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**valor de DWORD de erro de DNS \_ \_ \_ \_ muito \_ grande**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-316"><span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**DNS\_ERROR\_DWORD\_VALUE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-317">9567 (0x255F)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-317">9567 (0x255F)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-318">O valor especificado é muito grande para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-318">The specified value is too large for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-319"><span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**\_ \_ carregamento em segundo plano de erro DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-319"><span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**DNS\_ERROR\_BACKGROUND\_LOADING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-320">9568 (0x2560)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-320">9568 (0x2560)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-321">Esta operação não é permitida enquanto o servidor DNS está carregando zonas em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-321">This operation is not allowed while the DNS server is loading zones in the background.</span></span> <span data-ttu-id="0dc4b-322">Tente novamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-322">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-323"><span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**\_erro \_ de DNS não \_ permitido \_ no \_ RODC**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-323"><span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_RODC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-324">9569 (0x2561)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-324">9569 (0x2561)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-325">A operação solicitada não é permitida em um servidor DNS em execução em um controlador de domínio somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-325">The operation requested is not permitted on against a DNS server running on a read-only DC.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-326"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**erro de DNS \_ \_ não \_ permitido \_ sob \_ dname**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-326"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**DNS\_ERROR\_NOT\_ALLOWED\_UNDER\_DNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-327">9570 (0x2562)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-327">9570 (0x2562)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-328">Nenhum dado pode existir sob um registro DNAME.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-328">No data is allowed to exist underneath a DNAME record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-329"><span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**Delegação de erro de DNS \_ \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-329"><span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**DNS\_ERROR\_DELEGATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-330">9571 (0x2563)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-330">9571 (0x2563)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-331">Esta operação requer delegação de credenciais.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-331">This operation requires credentials delegation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-332"><span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**\_tabela de política de erro DNS \_ inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-332"><span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**DNS\_ERROR\_INVALID\_POLICY\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-333">9572 (0x2564)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-333">9572 (0x2564)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-334">A tabela de políticas de resolução de nomes foi corrompida.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-334">Name resolution policy table has been corrupted.</span></span> <span data-ttu-id="0dc4b-335">A resolução de DNS falhará até que seja corrigida.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-335">DNS resolution will fail until it is fixed.</span></span> <span data-ttu-id="0dc4b-336">Entre em contato com o administrador de rede.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-336">Contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-337"><span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**a \_ zona de erro DNS não \_ \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-337"><span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**DNS\_ERROR\_ZONE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-338">9601 (0x2581)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-338">9601 (0x2581)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-339">A zona DNS não existe.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-339">DNS zone does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-340"><span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**erro de DNS \_ \_ sem \_ informações de zona \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-340"><span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**DNS\_ERROR\_NO\_ZONE\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-341">9602 (0x2582)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-341">9602 (0x2582)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-342">Informações de zona DNS não disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-342">DNS zone information not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-343"><span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**\_operação de \_ zona inválida de erro \_ DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-343"><span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**DNS\_ERROR\_INVALID\_ZONE\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-344">9603 (0x2583)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-344">9603 (0x2583)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-345">Operação inválida para a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-345">Invalid operation for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-346"><span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**\_erro de \_ configuração de zona de erro DNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-346"><span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**DNS\_ERROR\_ZONE\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-347">9604 (0x2584)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-347">9604 (0x2584)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-348">Configuração de zona DNS inválida.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-348">Invalid DNS zone configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-349"><span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**a \_ zona de erro DNS \_ \_ \_ não tem \_ \_ registro soa**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-349"><span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**DNS\_ERROR\_ZONE\_HAS\_NO\_SOA\_RECORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-350">9605 (0x2585)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-350">9605 (0x2585)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-351">A zona DNS não tem registro de início de autoridade (SOA).</span><span class="sxs-lookup"><span data-stu-id="0dc4b-351">DNS zone has no start of authority (SOA) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-352"><span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**a \_ zona de erro DNS \_ \_ \_ não tem \_ \_ registros NS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-352"><span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**DNS\_ERROR\_ZONE\_HAS\_NO\_NS\_RECORDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-353">9606 (0x2586)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-353">9606 (0x2586)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-354">A zona DNS não tem registro de servidor de nomes (NS).</span><span class="sxs-lookup"><span data-stu-id="0dc4b-354">DNS zone has no Name Server (NS) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-355"><span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**\_zona de erro DNS \_ \_ bloqueada**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-355"><span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**DNS\_ERROR\_ZONE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-356">9607 (0x2587)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-356">9607 (0x2587)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-357">A zona DNS está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-357">DNS zone is locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-358"><span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**\_ \_ \_ falha na criação de zona de erro DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-358"><span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**DNS\_ERROR\_ZONE\_CREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-359">9608 (0x2588)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-359">9608 (0x2588)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-360">Falha na criação da zona DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-360">DNS zone creation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-361"><span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**a \_ zona de erro DNS \_ \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-361"><span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**DNS\_ERROR\_ZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-362">9609 (0x2589)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-362">9609 (0x2589)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-363">A zona DNS já existe.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-363">DNS zone already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-364"><span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**a \_ AUTOzona de erro DNS \_ \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-364"><span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**DNS\_ERROR\_AUTOZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-365">9610 (0x258A)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-365">9610 (0x258A)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-366">A zona automática de DNS já existe.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-366">DNS automatic zone already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-367"><span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**\_erro DNS \_ \_ tipo de zona inválido \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-367"><span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**DNS\_ERROR\_INVALID\_ZONE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-368">9611 (0x258B)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-368">9611 (0x258B)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-369">Tipo de zona DNS inválido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-369">Invalid DNS zone type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-370"><span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**o \_ erro de DNS \_ secundário \_ requer \_ \_ IP mestre**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-370"><span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**DNS\_ERROR\_SECONDARY\_REQUIRES\_MASTER\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-371">9612 (0x258C)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-371">9612 (0x258C)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-372">A zona DNS secundária requer um endereço IP mestre.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-372">Secondary DNS zone requires master IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-373"><span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**\_zona de erro DNS \_ \_ não \_ secundária**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-373"><span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**DNS\_ERROR\_ZONE\_NOT\_SECONDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-374">9613 (0x258D)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-374">9613 (0x258D)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-375">Zona DNS não secundária.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-375">DNS zone not secondary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-376"><span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**erro de DNS \_ \_ precisa de \_ endereços secundários \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-376"><span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**DNS\_ERROR\_NEED\_SECONDARY\_ADDRESSES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-377">9614 (0x258E)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-377">9614 (0x258E)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-378">É necessário um endereço IP secundário.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-378">Need secondary IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-379"><span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**\_erro DNS \_ \_ \_ falha na inicialização do WINS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-379"><span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**DNS\_ERROR\_WINS\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-380">9615 (0x258F)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-380">9615 (0x258F)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-381">Falha na inicialização do WINS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-381">WINS initialization failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-382"><span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**o \_ erro DNS \_ precisa de \_ \_ servidores WINS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-382"><span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**DNS\_ERROR\_NEED\_WINS\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-383">9616 (0x2590)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-383">9616 (0x2590)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-384">Servidores WINS necessários.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-384">Need WINS servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-385"><span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**\_erro de \_ DNS \_ \_ falha na inicialização de NBSTAT**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-385"><span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**DNS\_ERROR\_NBSTAT\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-386">9617 (0x2591)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-386">9617 (0x2591)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-387">Falha na chamada de inicialização de NBTSTAT.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-387">NBTSTAT initialization call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-388"><span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**\_exclusão de soa de erro DNS \_ \_ \_ inválida**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-388"><span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**DNS\_ERROR\_SOA\_DELETE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-389">9618 (0x2592)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-389">9618 (0x2592)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-390">Exclusão de início de autoridade (SOA) inválida.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-390">Invalid delete of start of authority (SOA).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-391"><span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**o \_ encaminhador de erro DNS \_ \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-391"><span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**DNS\_ERROR\_FORWARDER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-392">9619 (0x2593)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-392">9619 (0x2593)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-393">Já existe uma zona de encaminhamento condicional para esse nome.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-393">A conditional forwarding zone already exists for that name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-394"><span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**a \_ zona de erro DNS \_ requer o \_ \_ \_ IP mestre**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-394"><span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**DNS\_ERROR\_ZONE\_REQUIRES\_MASTER\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-395">9620 (0x2594)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-395">9620 (0x2594)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-396">Essa zona deve ser configurada com um ou mais endereços IP do servidor DNS mestre.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-396">This zone must be configured with one or more master DNS server IP addresses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-397"><span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**a \_ zona de erro DNS \_ \_ está \_ desligada**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-397"><span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**DNS\_ERROR\_ZONE\_IS\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-398">9621 (0x2595)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-398">9621 (0x2595)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-399">A operação não pode ser executada porque esta zona está desligada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-399">The operation cannot be performed because this zone is shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-400"><span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**\_ \_ zona de erro DNS \_ bloqueada \_ para \_ assinatura**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-400"><span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**DNS\_ERROR\_ZONE\_LOCKED\_FOR\_SIGNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-401">9622 (0x2596)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-401">9622 (0x2596)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-402">Esta operação não pode ser executada porque a zona está sendo assinada no momento.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-402">This operation cannot be performed because the zone is currently being signed.</span></span> <span data-ttu-id="0dc4b-403">Tente novamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-403">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-404"><span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**o \_ erro de DNS \_ primário \_ requer o \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-404"><span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**DNS\_ERROR\_PRIMARY\_REQUIRES\_DATAFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-405">9651 (0x25B3)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-405">9651 (0x25B3)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-406">A zona DNS primária requer o DataFile.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-406">Primary DNS zone requires datafile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-407"><span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**\_nome de \_ \_ DataFile inválido do erro \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-407"><span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**DNS\_ERROR\_INVALID\_DATAFILE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-408">9652 (0x25B4)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-408">9652 (0x25B4)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-409">Nome de DataFile inválido para a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-409">Invalid datafile name for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-410"><span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**\_falha de \_ abertura de DataFile de erro DNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-410"><span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**DNS\_ERROR\_DATAFILE\_OPEN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-411">9653 (0x25B5)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-411">9653 (0x25B5)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-412">Falha ao abrir o DataFile para a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-412">Failed to open datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-413"><span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**\_ \_ \_ falha no write-back do arquivo de erro DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-413"><span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**DNS\_ERROR\_FILE\_WRITEBACK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-414">9654 (0x25B6)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-414">9654 (0x25B6)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-415">Falha ao gravar o arquivo de configuração para a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-415">Failed to write datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-416"><span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**erro de DNS \_ \_ análise de DataFile \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-416"><span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**DNS\_ERROR\_DATAFILE\_PARSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-417">9655 (0x25B7)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-417">9655 (0x25B7)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-418">Falha ao ler o arquivo de leitura para a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-418">Failure while reading datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-419"><span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**\_o registro de erro DNS não \_ \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-419"><span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**DNS\_ERROR\_RECORD\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-420">9701 (0x25E5)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-420">9701 (0x25E5)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-421">O registro DNS não existe.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-421">DNS record does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-422"><span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**\_formato de \_ registro de erro DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-422"><span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**DNS\_ERROR\_RECORD\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-423">9702 (0x25E6)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-423">9702 (0x25E6)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-424">Erro de formato de registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-424">DNS record format error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-425"><span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**\_ \_ \_ falha na criação do nó de erro DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-425"><span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**DNS\_ERROR\_NODE\_CREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-426">9703 (0x25E7)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-426">9703 (0x25E7)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-427">Falha na criação de nó no DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-427">Node creation failure in DNS.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-428"><span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**\_tipo de registro de erro DNS \_ desconhecido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-428"><span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**DNS\_ERROR\_UNKNOWN\_RECORD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-429">9704 (0x25E8)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-429">9704 (0x25E8)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-430">Tipo de registro DNS desconhecido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-430">Unknown DNS record type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-431"><span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**o \_ registro de erro DNS \_ atingiu o \_ tempo \_ limite**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-431"><span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**DNS\_ERROR\_RECORD\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-432">9705 (0x25E9)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-432">9705 (0x25E9)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-433">O registro DNS atingiu o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-433">DNS record timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-434"><span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**\_ \_ nome de erro DNS não está \_ \_ na \_ zona**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-434"><span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**DNS\_ERROR\_NAME\_NOT\_IN\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-435">9706 (0x25EA)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-435">9706 (0x25EA)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-436">Nome não está na zona DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-436">Name not in DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-437"><span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**\_ \_ loop CNAME de erro DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-437"><span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**DNS\_ERROR\_CNAME\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-438">9707 (0x25EB)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-438">9707 (0x25EB)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-439">Loop CNAME detectado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-439">CNAME loop detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-440"><span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**o \_ nó de erro DNS \_ \_ é \_ CNAME**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-440"><span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**DNS\_ERROR\_NODE\_IS\_CNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-441">9708 (0x25EC)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-441">9708 (0x25EC)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-442">O nó é um registro DNS CNAME.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-442">Node is a CNAME DNS record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-443"><span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**\_colisão de \_ CNAME de erro DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-443"><span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**DNS\_ERROR\_CNAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-444">9709 (0x25ED)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-444">9709 (0x25ED)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-445">Já existe um registro CNAME para o nome fornecido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-445">A CNAME record already exists for given name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-446"><span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**\_ \_ registro de erro \_ DNS \_ somente \_ na \_ raiz da zona**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-446"><span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**DNS\_ERROR\_RECORD\_ONLY\_AT\_ZONE\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-447">9710 (0x25EE)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-447">9710 (0x25EE)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-448">Registrar somente na raiz da zona DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-448">Record only at DNS zone root.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-449"><span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**o \_ registro de erro DNS \_ \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-449"><span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**DNS\_ERROR\_RECORD\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-450">9711 (0x25EF)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-450">9711 (0x25EF)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-451">O registro DNS já existe.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-451">DNS record already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-452"><span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**\_ \_ dados secundários de erro DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-452"><span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**DNS\_ERROR\_SECONDARY\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-453">9712 (0x25F0)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-453">9712 (0x25F0)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-454">Erro de dados de zona DNS secundário.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-454">Secondary DNS zone data error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-455"><span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**erro de DNS \_ \_ sem \_ criar \_ dados de cache \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-455"><span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**DNS\_ERROR\_NO\_CREATE\_CACHE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-456">9713 (0x25F1)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-456">9713 (0x25F1)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-457">Não foi possível criar dados de cache DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-457">Could not create DNS cache data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-458"><span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**\_o nome do erro DNS não \_ \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-458"><span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**DNS\_ERROR\_NAME\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-459">9714 (0x25F2)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-459">9714 (0x25F2)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-460">O nome do DNS não existe.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-460">DNS name does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-461"><span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**\_ \_ \_ falha ao criar PTR de aviso DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-461"><span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**DNS\_WARNING\_PTR\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-462">9715 (0x25F3)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-462">9715 (0x25F3)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-463">Não foi possível criar o registro de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="0dc4b-463">Could not create pointer (PTR) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-464"><span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**o domínio de aviso DNS não foi \_ \_ \_ excluído**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-464"><span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**DNS\_WARNING\_DOMAIN\_UNDELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-465">9716 (0x25F4)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-465">9716 (0x25F4)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-466">O domínio DNS não foi excluído.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-466">DNS domain was undeleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-467"><span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**\_erro DNS \_ DS \_ não disponível**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-467"><span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**DNS\_ERROR\_DS\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-468">9717 (0x25F5)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-468">9717 (0x25F5)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-469">O serviço de diretório não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-469">The directory service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-470"><span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**a \_ zona DS de erro DNS \_ \_ \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-470"><span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**DNS\_ERROR\_DS\_ZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-471">9718 (0x25F6)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-471">9718 (0x25F6)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-472">A zona DNS já existe no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-472">DNS zone already exists in the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-473"><span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**erro de DNS \_ \_ sem \_ Bootfile \_ se a \_ \_ zona DS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-473"><span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**DNS\_ERROR\_NO\_BOOTFILE\_IF\_DS\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-474">9719 (0x25F7)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-474">9719 (0x25F7)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-475">O servidor DNS não está criando ou lendo o arquivo de inicialização para a zona DNS integrada ao serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-475">DNS server not creating or reading the boot file for the directory service integrated DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-476"><span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**o \_ nó de erro DNS \_ \_ é \_ dname**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-476"><span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**DNS\_ERROR\_NODE\_IS\_DNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-477">9720 (0x25F8)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-477">9720 (0x25F8)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-478">O nó é um registro DNS DNAME.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-478">Node is a DNAME DNS record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-479"><span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**colisão de erro de DNS \_ \_ dname \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-479"><span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**DNS\_ERROR\_DNAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-480">9721 (0x25F9)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-480">9721 (0x25F9)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-481">Um registro DNAME já existe para o nome fornecido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-481">A DNAME record already exists for given name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-482"><span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**\_loop de \_ alias de erro DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-482"><span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**DNS\_ERROR\_ALIAS\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-483">9722 (0x25FA)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-483">9722 (0x25FA)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-484">Um loop de alias foi detectado com registros CNAME ou DNAME.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-484">An alias loop has been detected with either CNAME or DNAME records.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-485"><span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**\_ \_ AXFR completo de informações de DNS \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-485"><span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**DNS\_INFO\_AXFR\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-486">9751 (0x2617)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-486">9751 (0x2617)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-487">DNS AXFR (transferência de zona) concluído.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-487">DNS AXFR (zone transfer) complete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-488"><span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**erro de DNS \_ \_ AXFR**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-488"><span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**DNS\_ERROR\_AXFR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-489">9752 (0x2618)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-489">9752 (0x2618)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-490">Falha na transferência de zona DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-490">DNS zone transfer failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-491"><span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**informações de DNS \_ \_ adicionadas \_ \_ WINS local**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-491"><span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**DNS\_INFO\_ADDED\_LOCAL\_WINS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-492">9753 (0x2619)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-492">9753 (0x2619)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-493">Servidor WINS local adicionado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-493">Added local WINS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-494"><span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**o \_ status do DNS \_ continua \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-494"><span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**DNS\_STATUS\_CONTINUE\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-495">9801 (0x2649)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-495">9801 (0x2649)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-496">A chamada de atualização segura precisa continuar a solicitação de atualização.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-496">Secure update call needs to continue update request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-497"><span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**erro de DNS \_ \_ sem \_ tcpip**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-497"><span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**DNS\_ERROR\_NO\_TCPIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-498">9851 (0x267B)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-498">9851 (0x267B)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-499">Protocolo de rede TCP/IP não instalado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-499">TCP/IP network protocol not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-500"><span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**erro de DNS \_ \_ sem \_ \_ servidores DNS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-500"><span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**DNS\_ERROR\_NO\_DNS\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-501">9852 (0x267C)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-501">9852 (0x267C)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-502">Nenhum servidor DNS configurado para o sistema local.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-502">No DNS servers configured for local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-503"><span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**\_o erro DNS \_ DP não \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-503"><span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**DNS\_ERROR\_DP\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-504">9901 (0x26AD)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-504">9901 (0x26AD)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-505">A partição de diretório especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-505">The specified directory partition does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-506"><span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**o \_ erro DNS \_ DP \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-506"><span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**DNS\_ERROR\_DP\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-507">9902 (0x26AE)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-507">9902 (0x26AE)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-508">A partição de diretório especificada já existe.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-508">The specified directory partition already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-509"><span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**\_erro DNS \_ DP \_ não \_ inscrito**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-509"><span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**DNS\_ERROR\_DP\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-510">9903 (0x26AF)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-510">9903 (0x26AF)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-511">Este servidor DNS não está inscrito na partição de diretório especificada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-511">This DNS server is not enlisted in the specified directory partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-512"><span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**\_erro DNS \_ DP \_ já \_ inscrito**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-512"><span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**DNS\_ERROR\_DP\_ALREADY\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-513">9904 (0x26B0)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-513">9904 (0x26B0)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-514">Este servidor DNS já está inscrito na partição de diretório especificada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-514">This DNS server is already enlisted in the specified directory partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-515"><span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**\_erro DNS \_ DP \_ não \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-515"><span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**DNS\_ERROR\_DP\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-516">9905 (0x26B1)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-516">9905 (0x26B1)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-517">A partição de diretório não está disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-517">The directory partition is not available at this time.</span></span> <span data-ttu-id="0dc4b-518">Aguarde alguns minutos e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-518">Please wait a few minutes and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-519"><span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**erro de DNS \_ \_ DP \_ FSMO \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-519"><span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**DNS\_ERROR\_DP\_FSMO\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-520">9906 (0x26B2)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-520">9906 (0x26B2)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-521">A operação falhou porque a função FSMO do mestre de nomeação de domínio não pôde ser acessada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-521">The operation failed because the domain naming master FSMO role could not be reached.</span></span> <span data-ttu-id="0dc4b-522">O controlador de domínio que contém a função FSMO do mestre de nomeação de domínio está inoperante ou não pode atender à solicitação ou não está executando o Windows Server 2003 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-522">The domain controller holding the domain naming master FSMO role is down or unable to service the request or is not running Windows Server 2003 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-523"><span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-523"><span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-524">10004 (0x2714)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-524">10004 (0x2714)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-525">Uma operação de bloqueio foi interrompida por uma chamada para WSACancelBlockingCall.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-525">A blocking operation was interrupted by a call to WSACancelBlockingCall.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-526"><span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-526"><span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-527">10009 (0x2719)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-527">10009 (0x2719)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-528">O identificador de arquivo fornecido não é válido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-528">The file handle supplied is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-529"><span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-529"><span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-530">10013 (0x271D)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-530">10013 (0x271D)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-531">Foi feita uma tentativa de acessar um soquete de uma maneira proibida por suas permissões de acesso.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-531">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-532"><span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-532"><span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-533">10014 (0x271E)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-533">10014 (0x271E)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-534">O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-534">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-535"><span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-535"><span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-536">10022 (0x2726)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-536">10022 (0x2726)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-537">Foi fornecido um argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-537">An invalid argument was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-538"><span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-538"><span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-539">10024 (0x2728)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-539">10024 (0x2728)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-540">Muitos soquetes abertos.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-540">Too many open sockets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-541"><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-541"><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-542">10035 (0x2733)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-542">10035 (0x2733)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-543">Uma operação de soquete sem bloqueio não pôde ser concluída imediatamente.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-543">A non-blocking socket operation could not be completed immediately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-544"><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-544"><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-545">10036 (0x2734)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-545">10036 (0x2734)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-546">Uma operação de bloqueio está atualmente em execução.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-546">A blocking operation is currently executing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-547"><span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-547"><span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-548">10037 (0x2735)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-548">10037 (0x2735)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-549">Foi tentada uma operação em um soquete sem bloqueio que já tinha uma operação em andamento.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-549">An operation was attempted on a non-blocking socket that already had an operation in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-550"><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-550"><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-551">10038 (0x2736)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-551">10038 (0x2736)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-552">Uma operação foi tentada em algo que não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-552">An operation was attempted on something that is not a socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-553"><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-553"><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-554">10039 (0x2737)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-554">10039 (0x2737)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-555">Um endereço necessário foi omitido de uma operação em um soquete.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-555">A required address was omitted from an operation on a socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-556"><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-556"><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-557">10040 (0x2738)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-557">10040 (0x2738)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-558">Uma mensagem enviada em um soquete de datagrama era maior do que o buffer de mensagem interno ou que algum outro limite de rede, ou o buffer usado para receber um datagrama era menor que o próprio datagrama.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-558">A message sent on a datagram socket was larger than the internal message buffer or some other network limit, or the buffer used to receive a datagram into was smaller than the datagram itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-559"><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-559"><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-560">10041 (0x2739)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-560">10041 (0x2739)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-561">Um protocolo foi especificado na chamada de função de soquete que não oferece suporte à semântica do tipo de soquete solicitado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-561">A protocol was specified in the socket function call that does not support the semantics of the socket type requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-562"><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-562"><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-563">10042 (0x273A)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-563">10042 (0x273A)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-564">Uma opção ou um nível desconhecido, inválido ou sem suporte foi especificado em uma chamada de getsockopt ou setsockopt.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-564">An unknown, invalid, or unsupported option or level was specified in a getsockopt or setsockopt call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-565"><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-565"><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-566">10043 (0x273B)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-566">10043 (0x273B)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-567">O protocolo solicitado não foi configurado no sistema ou não existe nenhuma implementação para ele.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-567">The requested protocol has not been configured into the system, or no implementation for it exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-568"><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-568"><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-569">10044 (0x273C)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-569">10044 (0x273C)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-570">O suporte para o tipo de soquete especificado não existe nessa família de endereços.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-570">The support for the specified socket type does not exist in this address family.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-571"><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-571"><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-572">10045 (0x273D)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-572">10045 (0x273D)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-573">Não há suporte para a operação tentada para o tipo de objeto referenciado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-573">The attempted operation is not supported for the type of object referenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-574"><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-574"><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-575">10046 (0x273E)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-575">10046 (0x273E)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-576">A família de protocolos não foi configurada no sistema ou não existe nenhuma implementação para ela.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-576">The protocol family has not been configured into the system or no implementation for it exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-577"><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-577"><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-578">10047 (0x273F)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-578">10047 (0x273F)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-579">Foi usado um endereço incompatível com o protocolo solicitado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-579">An address incompatible with the requested protocol was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-580"><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-580"><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-581">10048 (0x2740)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-581">10048 (0x2740)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-582">Normalmente, apenas um tipo de uso de cada endereço de soquete (endereço de rede/protocolo/porta) é permitido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-582">Only one usage of each socket address (protocol/network address/port) is normally permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-583"><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-583"><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-584">10049 (0x2741)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-584">10049 (0x2741)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-585">O endereço solicitado não é válido em seu contexto.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-585">The requested address is not valid in its context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-586"><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-586"><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-587">10050 (0x2742)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-587">10050 (0x2742)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-588">Uma operação de soquete encontrou uma rede inoperante.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-588">A socket operation encountered a dead network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-589"><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-589"><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-590">10051 (0x2743)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-590">10051 (0x2743)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-591">Uma operação de soquete foi tentada em uma rede inacessível.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-591">A socket operation was attempted to an unreachable network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-592"><span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-592"><span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-593">10052 (0x2744)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-593">10052 (0x2744)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-594">A conexão foi interrompida devido à atividade Keep Alive que detecta uma falha enquanto a operação estava em andamento.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-594">The connection has been broken due to keep-alive activity detecting a failure while the operation was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-595"><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-595"><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-596">10053 (0x2745)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-596">10053 (0x2745)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-597">Uma conexão estabelecida foi interrompida pelo software na sua máquina host.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-597">An established connection was aborted by the software in your host machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-598"><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-598"><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-599">10054 (0x2746)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-599">10054 (0x2746)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-600">uma conexão existente foi fechada forçadamente pelo host remoto.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-600">An existing connection was forcibly closed by the remote host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-601"><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-601"><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-602">10055 (0x2747)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-602">10055 (0x2747)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-603">Uma operação em um soquete não pôde ser executada porque o sistema não tem espaço suficiente no buffer ou porque uma fila estava cheia.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-603">An operation on a socket could not be performed because the system lacked sufficient buffer space or because a queue was full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-604"><span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-604"><span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-605">10056 (0x2748)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-605">10056 (0x2748)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-606">Uma solicitação de conexão foi feita em um soquete já conectado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-606">A connect request was made on an already connected socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-607"><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-607"><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-608">10057 (0x2749)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-608">10057 (0x2749)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-609">Uma solicitação de envio ou recebimento de dados foi impedida porque o soquete não está conectado e (durante o envio em um soquete de datagrama usando uma chamada sendto) nenhum endereço foi informado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-609">A request to send or receive data was disallowed because the socket is not connected and (when sending on a datagram socket using a sendto call) no address was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-610"><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-610"><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-611">10058 (0x274A)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-611">10058 (0x274A)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-612">Uma solicitação para enviar ou receber dados não foi permitida, pois o soquete já havia sido desligado nessa direção com uma chamada de desligamento anterior.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-612">A request to send or receive data was disallowed because the socket had already been shut down in that direction with a previous shutdown call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-613"><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-613"><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-614">10059 (0x274B)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-614">10059 (0x274B)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-615">Muitas referências a algum objeto de kernel.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-615">Too many references to some kernel object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-616"><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-616"><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-617">10060 (0x274C)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-617">10060 (0x274C)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-618">Uma tentativa de conexão falhou porque a parte conectada não respondeu corretamente após um período de tempo ou a conexão estabelecida falhou porque o host conectado falhou ao responder.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-618">A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-619"><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-619"><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-620">10061 (0x274D)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-620">10061 (0x274D)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-621">Não foi possível estabelecer uma conexão porque a máquina de destino a recusou ativamente.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-621">No connection could be made because the target machine actively refused it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-622"><span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-622"><span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-623">10062 (0x274E)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-623">10062 (0x274E)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-624">Não é possível converter o nome.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-624">Cannot translate name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-625"><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-625"><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-626">10063 (0x274F)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-626">10063 (0x274F)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-627">O nome ou componente de nome era muito longo.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-627">Name component or name was too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-628"><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-628"><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-629">10064 (0x2750)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-629">10064 (0x2750)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-630">Uma operação de soquete falhou porque o host de destino estava inoperante.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-630">A socket operation failed because the destination host was down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-631"><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-631"><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-632">10065 (0x2751)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-632">10065 (0x2751)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-633">Uma operação de soquete foi tentada em um host inacessível.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-633">A socket operation was attempted to an unreachable host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-634"><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-634"><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-635">10066 (0x2752)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-635">10066 (0x2752)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-636">Não é possível remover um diretório que não esteja vazio.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-636">Cannot remove a directory that is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-637"><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-637"><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-638">10067 (0x2753)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-638">10067 (0x2753)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-639">Uma implementação do Windows Sockets pode ter um limite no número de aplicativos que podem usá-lo simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-639">A Windows Sockets implementation may have a limit on the number of applications that may use it simultaneously.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-640"><span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-640"><span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-641">10068 (0x2754)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-641">10068 (0x2754)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-642">Ficou sem cota.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-642">Ran out of quota.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-643"><span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-643"><span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-644">10069 (0x2755)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-644">10069 (0x2755)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-645">Cota de disco esgotada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-645">Ran out of disk quota.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-646"><span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-646"><span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-647">10070 (0x2756)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-647">10070 (0x2756)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-648">A referência de identificador de arquivo não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-648">File handle reference is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-649"><span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-649"><span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-650">10071 (0x2757)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-650">10071 (0x2757)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-651">O item não está disponível localmente.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-651">Item is not available locally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-652"><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-652"><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-653">10091 (0x276B)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-653">10091 (0x276B)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-654">O WSAStartup não pode funcionar neste momento porque o sistema subjacente usado para fornecer serviços de rede não está disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-654">WSAStartup cannot function at this time because the underlying system it uses to provide network services is currently unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-655"><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-655"><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-656">10092 (0x276C)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-656">10092 (0x276C)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-657">Não há suporte para a versão solicitada do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-657">The Windows Sockets version requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-658"><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-658"><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-659">10093 (0x276D)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-659">10093 (0x276D)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-660">O aplicativo não chamou WSAStartup ou WSAStartup falhou.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-660">Either the application has not called WSAStartup, or WSAStartup failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-661"><span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-661"><span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-662">10101 (0x2775)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-662">10101 (0x2775)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-663">Retornado por WSARecv ou WSARecvFrom para indicar que a parte remota iniciou uma sequência de desligamento normal.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-663">Returned by WSARecv or WSARecvFrom to indicate the remote party has initiated a graceful shutdown sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-664"><span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-664"><span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-665">10102 (0x2776)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-665">10102 (0x2776)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-666">Não é possível retornar mais resultados por WSALookupServiceNext.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-666">No more results can be returned by WSALookupServiceNext.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-667"><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-667"><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-668">10103 (0x2777)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-668">10103 (0x2777)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-669">Uma chamada para WSALookupServiceEnd foi feita enquanto essa chamada ainda estava sendo processada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-669">A call to WSALookupServiceEnd was made while this call was still processing.</span></span> <span data-ttu-id="0dc4b-670">A chamada foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-670">The call has been canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-671"><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-671"><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-672">10104 (0x2778)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-672">10104 (0x2778)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-673">A tabela de chamada de procedimento é inválida.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-673">The procedure call table is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-674"><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-674"><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-675">10105 (0x2779)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-675">10105 (0x2779)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-676">O provedor de serviços solicitado é inválido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-676">The requested service provider is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-677"><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-677"><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-678">10106 (0x277A)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-678">10106 (0x277A)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-679">O provedor de serviços solicitado não pôde ser carregado ou inicializado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-679">The requested service provider could not be loaded or initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-680"><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-680"><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-681">10107 (0x277B)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-681">10107 (0x277B)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-682">Falha em uma chamada do sistema.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-682">A system call has failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-683"><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**WSASERVICE \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-683"><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**WSASERVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-684">10108 (0x277C)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-684">10108 (0x277C)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-685">Esse serviço não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-685">No such service is known.</span></span> <span data-ttu-id="0dc4b-686">O serviço não pode ser encontrado no espaço de nome especificado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-686">The service cannot be found in the specified name space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-687"><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**WSATYPE \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-687"><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**WSATYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-688">10109 (0x277D)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-688">10109 (0x277D)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-689">A classe especificada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-689">The specified class was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-690"><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**CABEÇALHO \_ E \_ não \_ mais**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-690"><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA\_E\_NO\_MORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-691">10110 (0x277E)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-691">10110 (0x277E)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-692">Não é possível retornar mais resultados por WSALookupServiceNext.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-692">No more results can be returned by WSALookupServiceNext.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-693"><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-693"><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA\_E\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-694">10111 (0x277F)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-694">10111 (0x277F)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-695">Uma chamada para WSALookupServiceEnd foi feita enquanto essa chamada ainda estava sendo processada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-695">A call to WSALookupServiceEnd was made while this call was still processing.</span></span> <span data-ttu-id="0dc4b-696">A chamada foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-696">The call has been canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-697"><span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-697"><span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-698">10112 (0x2780)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-698">10112 (0x2780)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-699">Uma consulta de banco de dados falhou porque foi ativamente recusada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-699">A database query failed because it was actively refused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-700"><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**WSAHOST \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-700"><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**WSAHOST\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-701">11001 (0x2AF9)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-701">11001 (0x2AF9)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-702">Esse host não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-702">No such host is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-703"><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY \_ novamente**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-703"><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY\_AGAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-704">11002 (0x2AFA)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-704">11002 (0x2AFA)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-705">Esse é geralmente um erro temporário durante a resolução do nome do host e significa que o servidor local não recebeu uma resposta de um servidor autorizado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-705">This is usually a temporary error during hostname resolution and means that the local server did not receive a response from an authoritative server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-706"><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**recuperação do WSANO \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-706"><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**WSANO\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-707">11003 (0x2AFB)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-707">11003 (0x2AFB)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-708">Ocorreu um erro não recuperável durante uma pesquisa de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-708">A non-recoverable error occurred during a database lookup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-709"><span id="WSANO_DATA"></span><span id="wsano_data"></span>**dados do WSANO \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-709"><span id="WSANO_DATA"></span><span id="wsano_data"></span>**WSANO\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-710">11004 (0x2AFC)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-710">11004 (0x2AFC)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-711">O nome solicitado é válido, mas nenhum dado do tipo solicitado foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-711">The requested name is valid, but no data of the requested type was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-712"><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**\_receptores de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-712"><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**WSA\_QOS\_RECEIVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-713">11005 (0x2AFD)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-713">11005 (0x2AFD)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-714">Pelo menos uma reserva chegou.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-714">At least one reserve has arrived.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-715"><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**\_remetentes de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-715"><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**WSA\_QOS\_SENDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-716">11006 (0x2AFE)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-716">11006 (0x2AFE)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-717">Pelo menos um caminho chegou.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-717">At least one path has arrived.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-718"><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**QoS de WSA \_ \_ sem \_ remetentes**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-718"><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**WSA\_QOS\_NO\_SENDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-719">11007 (0x2AFF)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-719">11007 (0x2AFF)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-720">Não há remetentes.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-720">There are no senders.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-721"><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**QoS de WSA \_ \_ sem \_ receptores**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-721"><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**WSA\_QOS\_NO\_RECEIVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-722">11008 (0x2B00)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-722">11008 (0x2B00)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-723">Não há destinatários.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-723">There are no receivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-724"><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**solicitação de QoS de WSA \_ \_ \_ confirmada**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-724"><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**WSA\_QOS\_REQUEST\_CONFIRMED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-725">11009 (0x2B01)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-725">11009 (0x2B01)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-726">A reserva foi confirmada.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-726">Reserve has been confirmed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-727"><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**\_falha de \_ admissão de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-727"><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**WSA\_QOS\_ADMISSION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-728">11010 (0x2B02)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-728">11010 (0x2B02)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-729">Erro devido à falta de recursos.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-729">Error due to lack of resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-730"><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**\_ \_ falha na política de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-730"><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**WSA\_QOS\_POLICY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-731">11011 (0x2B03)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-731">11011 (0x2B03)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-732">Rejeitado por motivos administrativos-credenciais inadequadas.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-732">Rejected for administrative reasons - bad credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-733"><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**\_ \_ estilo insatisfatório de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-733"><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**WSA\_QOS\_BAD\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-734">11012 (0x2B04)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-734">11012 (0x2B04)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-735">Estilo desconhecido ou conflitante.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-735">Unknown or conflicting style.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-736"><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**\_ \_ objeto insatisfatório de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-736"><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**WSA\_QOS\_BAD\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-737">11013 (0x2B05)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-737">11013 (0x2B05)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-738">Problema com alguma parte do buffer filterspec ou ProviderSpecific em geral.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-738">Problem with some part of the filterspec or providerspecific buffer in general.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-739"><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**\_erro de \_ Ctrl de tráfego de QoS de WSA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-739"><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**WSA\_QOS\_TRAFFIC\_CTRL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-740">11014 (0x2B06)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-740">11014 (0x2B06)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-741">Problema com alguma parte do FLOWSPEC.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-741">Problem with some part of the flowspec.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-742"><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**\_ \_ erro genérico de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-742"><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**WSA\_QOS\_GENERIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-743">11015 (0x2B07)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-743">11015 (0x2B07)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-744">Erro de QOS geral.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-744">General QOS error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-745"><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**\_ESERVICETYPE de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-745"><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**WSA\_QOS\_ESERVICETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-746">11016 (0x2B08)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-746">11016 (0x2B08)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-747">Um tipo de serviço inválido ou não reconhecido foi encontrado no FLOWSPEC.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-747">An invalid or unrecognized service type was found in the flowspec.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-748"><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**\_EFLOWSPEC de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-748"><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**WSA\_QOS\_EFLOWSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-749">11017 (0x2B09)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-749">11017 (0x2B09)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-750">Um FLOWSPEC inválido ou inconsistente foi encontrado na estrutura de QOS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-750">An invalid or inconsistent flowspec was found in the QOS structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-751"><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**\_EPROVSPECBUF de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-751"><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**WSA\_QOS\_EPROVSPECBUF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-752">11018 (0x2B0A)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-752">11018 (0x2B0A)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-753">Buffer específico do provedor de QOS inválido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-753">Invalid QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-754"><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**\_EFILTERSTYLE de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-754"><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**WSA\_QOS\_EFILTERSTYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-755">11019 (0x2B0B)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-755">11019 (0x2B0B)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-756">Um estilo de filtro QOS inválido foi usado.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-756">An invalid QOS filter style was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-757"><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**\_EFILTERTYPE de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-757"><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**WSA\_QOS\_EFILTERTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-758">11020 (0x2B0C)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-758">11020 (0x2B0C)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-759">Foi usado um tipo de filtro QOS inválido.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-759">An invalid QOS filter type was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-760"><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**\_EFILTERCOUNT de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-760"><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**WSA\_QOS\_EFILTERCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-761">11021 (0x2B0D)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-761">11021 (0x2B0D)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-762">Um número incorreto de FILTERSPECs de QOS foi especificado no FLOWDESCRIPTOR.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-762">An incorrect number of QOS FILTERSPECs were specified in the FLOWDESCRIPTOR.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-763"><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**\_EOBJLENGTH de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-763"><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**WSA\_QOS\_EOBJLENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-764">11022 (0x2B0E)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-764">11022 (0x2B0E)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-765">Um objeto com um campo ObjectLength inválido foi especificado no buffer específico do provedor de QOS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-765">An object with an invalid ObjectLength field was specified in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-766"><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**\_EFLOWCOUNT de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-766"><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**WSA\_QOS\_EFLOWCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-767">11023 (0x2B0F)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-767">11023 (0x2B0F)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-768">Um número incorreto de descritores de fluxo foi especificado na estrutura de QOS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-768">An incorrect number of flow descriptors was specified in the QOS structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-769"><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**\_EUNKOWNPSOBJ de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-769"><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**WSA\_QOS\_EUNKOWNPSOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-770">11024 (0x2B10)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-770">11024 (0x2B10)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-771">Um objeto não reconhecido foi encontrado no buffer específico do provedor de QOS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-771">An unrecognized object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-772"><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**\_EPOLICYOBJ de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-772"><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**WSA\_QOS\_EPOLICYOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-773">11025 (0x2B11)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-773">11025 (0x2B11)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-774">Um objeto de política inválido foi encontrado no buffer específico do provedor de QOS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-774">An invalid policy object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-775"><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**\_EFLOWDESC de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-775"><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**WSA\_QOS\_EFLOWDESC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-776">11026 (0x2B12)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-776">11026 (0x2B12)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-777">Foi encontrado um descritor de fluxo QOS inválido na lista de descritores de fluxo.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-777">An invalid QOS flow descriptor was found in the flow descriptor list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-778"><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**\_EPSFLOWSPEC de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-778"><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**WSA\_QOS\_EPSFLOWSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-779">11027 (0x2B13)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-779">11027 (0x2B13)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-780">Um FLOWSPEC inválido ou inconsistente foi encontrado no buffer específico do provedor de QOS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-780">An invalid or inconsistent flowspec was found in the QOS provider specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-781"><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**\_EPSFILTERSPEC de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-781"><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**WSA\_QOS\_EPSFILTERSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-782">11028 (0x2B14)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-782">11028 (0x2B14)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-783">Um FILTERSPEC inválido foi encontrado no buffer específico do provedor de QOS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-783">An invalid FILTERSPEC was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-784"><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**\_ESDMODEOBJ de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-784"><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**WSA\_QOS\_ESDMODEOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-785">11029 (0x2B15)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-785">11029 (0x2B15)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-786">Um objeto de modo de descarte de forma inválido foi encontrado no buffer específico do provedor de QOS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-786">An invalid shape discard mode object was found in the QOS provider specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-787"><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**\_ESHAPERATEOBJ de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-787"><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**WSA\_QOS\_ESHAPERATEOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-788">11030 (0x2B16)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-788">11030 (0x2B16)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-789">Um objeto de taxa de formatação inválido foi encontrado no buffer específico do provedor de QOS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-789">An invalid shaping rate object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-790"><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**\_ \_ PETYPE reservado de QoS de WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-790"><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**WSA\_QOS\_RESERVED\_PETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-791">11031 (0x2B17)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-791">11031 (0x2B17)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-792">Um elemento de política reservado foi encontrado no buffer específico do provedor de QOS.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-792">A reserved policy element was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-793"><span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**\_host seguro do WSA \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-793"><span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**WSA\_SECURE\_HOST\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-794">11032 (0x2B18)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-794">11032 (0x2B18)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-795">Esse host não é conhecido com segurança.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-795">No such host is known securely.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0dc4b-796"><span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**\_erro de \_ política de nome de IPsec do WSA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0dc4b-796"><span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**WSA\_IPSEC\_NAME\_POLICY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc4b-797">11033 (0x2B19)</span><span class="sxs-lookup"><span data-stu-id="0dc4b-797">11033 (0x2B19)</span></span>
</dt> <dt>



<span data-ttu-id="0dc4b-798">Não foi possível adicionar a política IPSEC baseada em nome.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-798">Name based IPSEC policy could not be added.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="0dc4b-799">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dc4b-799">Requirements</span></span>



| <span data-ttu-id="0dc4b-800">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dc4b-800">Requirement</span></span> | <span data-ttu-id="0dc4b-801">Valor</span><span class="sxs-lookup"><span data-stu-id="0dc4b-801">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc4b-802">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0dc4b-802">Minimum supported client</span></span><br/> | <span data-ttu-id="0dc4b-803">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0dc4b-803">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0dc4b-804">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0dc4b-804">Minimum supported server</span></span><br/> | <span data-ttu-id="0dc4b-805">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0dc4b-805">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0dc4b-806">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0dc4b-806">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dc4b-807"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dc4b-807"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dc4b-808">Confira também</span><span class="sxs-lookup"><span data-stu-id="0dc4b-808">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dc4b-809">Códigos de erro do sistema</span><span class="sxs-lookup"><span data-stu-id="0dc4b-809">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




