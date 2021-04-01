---
description: Localiza um certificado do emissor dos repositórios de certificados especificados que correspondem ao certificado de entidade especificado.
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: Função WTHelperCertFindIssuerCertificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperCertFindIssuerCertificate
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 99135ac22509b288726732ca4a16248b304f294b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169685"
---
# <a name="wthelpercertfindissuercertificate-function"></a><span data-ttu-id="d75f5-103">Função WTHelperCertFindIssuerCertificate</span><span class="sxs-lookup"><span data-stu-id="d75f5-103">WTHelperCertFindIssuerCertificate function</span></span>

<span data-ttu-id="d75f5-104">\[A função **WTHelperCertFindIssuerCertificate** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="d75f5-104">\[The **WTHelperCertFindIssuerCertificate** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d75f5-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="d75f5-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="d75f5-106">A função **WTHelperCertFindIssuerCertificate** localiza um certificado de emissor dos repositórios de certificados especificados que correspondem ao certificado de entidade especificado.</span><span class="sxs-lookup"><span data-stu-id="d75f5-106">The **WTHelperCertFindIssuerCertificate** function finds an issuer certificate from the specified certificate stores that matches the specified subject certificate.</span></span>

> [!Note]  
> <span data-ttu-id="d75f5-107">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="d75f5-107">This function has no associated import library.</span></span> <span data-ttu-id="d75f5-108">Você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Wintrust.dll.</span><span class="sxs-lookup"><span data-stu-id="d75f5-108">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Wintrust.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d75f5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d75f5-109">Syntax</span></span>


```C++
PCCERT_CONTEXT WINAPI WTHelperCertFindIssuerCertificate(
  _In_      PCCERT_CONTEXT pChildContext,
  _In_      DWORD          chStores,
  _In_      HCERTSTORE     *pahStores,
  _In_      FILETIME       *psftVerifyAsOf,
  _In_      DWORD          dwEncoding,
  _Out_opt_ DWORD          *pdwConfidence,
  _Out_     DWORD          *dwError
);
```



## <a name="parameters"></a><span data-ttu-id="d75f5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d75f5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d75f5-111">*pChildContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d75f5-111">*pChildContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d75f5-112">O certificado do requerente para o qual encontrar um certificado de emissor correspondente.</span><span class="sxs-lookup"><span data-stu-id="d75f5-112">The subject certificate for which to find a matching issuer certificate.</span></span>

</dd> <dt>

<span data-ttu-id="d75f5-113">*chStores* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d75f5-113">*chStores* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d75f5-114">O número de elementos na matriz *pahStores* .</span><span class="sxs-lookup"><span data-stu-id="d75f5-114">The number of elements in the *pahStores* array.</span></span>

</dd> <dt>

<span data-ttu-id="d75f5-115">*pahStores* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d75f5-115">*pahStores* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d75f5-116">Uma matriz de repositórios de certificados no qual Pesquisar.</span><span class="sxs-lookup"><span data-stu-id="d75f5-116">An array of certificate stores in which to search.</span></span>

</dd> <dt>

<span data-ttu-id="d75f5-117">*psftVerifyAsOf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d75f5-117">*psftVerifyAsOf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d75f5-118">A hora da verificação.</span><span class="sxs-lookup"><span data-stu-id="d75f5-118">The time of verification.</span></span>

</dd> <dt>

<span data-ttu-id="d75f5-119">*dwEncoding* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d75f5-119">*dwEncoding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d75f5-120">Um valor **DWORD** que especifica os tipos de codificação do certificado a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="d75f5-120">A **DWORD** value that specifies the encoding types of the certificate to check.</span></span> <span data-ttu-id="d75f5-121">Para obter informações sobre os tipos de codificação possíveis, consulte [certificados e tipos de codificação de mensagem](certificate-and-message-encoding-types.md).</span><span class="sxs-lookup"><span data-stu-id="d75f5-121">For information about possible encoding types, see [Certificate and Message Encoding Types](certificate-and-message-encoding-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="d75f5-122">*pdwConfidence* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d75f5-122">*pdwConfidence* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d75f5-123">Esse parâmetro pode ser uma combinação de bits zero ou mais dos valores de confiança a seguir.</span><span class="sxs-lookup"><span data-stu-id="d75f5-123">This parameter can be a bitwise combination of zero or more of the following confidence values.</span></span>



| <span data-ttu-id="d75f5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d75f5-124">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="d75f5-125">Significado</span><span class="sxs-lookup"><span data-stu-id="d75f5-125">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <span data-ttu-id="d75f5-126"><dt>**Certificado \_ SEGURANÇA \_ SIG**</dt> <dt> 0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="d75f5-126"><dt>**CERT\_CONFIDENCE\_SIG**</dt> <dt> 0x10000000</dt></span></span> </dl>                     | <span data-ttu-id="d75f5-127">A assinatura do certificado é válida.</span><span class="sxs-lookup"><span data-stu-id="d75f5-127">The signature of the certificate is valid.</span></span><br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <span data-ttu-id="d75f5-128"><dt>**Certificado \_ 0x01000000 de \_ tempo de confiança**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d75f5-128"><dt>**CERT\_CONFIDENCE\_TIME**</dt> <dt> 0x01000000</dt></span></span> </dl>                  | <span data-ttu-id="d75f5-129">A hora do emissor do certificado é válida.</span><span class="sxs-lookup"><span data-stu-id="d75f5-129">The time of the certificate issuer is valid.</span></span><br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <span data-ttu-id="d75f5-130"><dt>0x00100000</dt> de <dt> **\_ \_ aninhamento de confiança de certificado**</dt></span><span class="sxs-lookup"><span data-stu-id="d75f5-130"><dt> **CERT\_CONFIDENCE\_TIMENEST**</dt> <dt>0x00100000</dt></span></span> </dl>    | <span data-ttu-id="d75f5-131">A hora do certificado é válida.</span><span class="sxs-lookup"><span data-stu-id="d75f5-131">The time of the certificate is valid.</span></span><br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <span data-ttu-id="d75f5-132"><dt> **\_ \_ AUTHIDEXT de confiança de certificado**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="d75f5-132"><dt> **CERT\_CONFIDENCE\_AUTHIDEXT**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="d75f5-133">A extensão de ID de autoridade é válida.</span><span class="sxs-lookup"><span data-stu-id="d75f5-133">The authority ID extension is valid.</span></span><br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <span data-ttu-id="d75f5-134"><dt>0x00001000</dt> de <dt> **\_ \_ higiene de confiança de certificado**</dt></span><span class="sxs-lookup"><span data-stu-id="d75f5-134"><dt> **CERT\_CONFIDENCE\_HYGIENE**</dt> <dt>0x00001000</dt></span></span> </dl>       | <span data-ttu-id="d75f5-135">No mínimo, a assinatura do certificado e a extensão da ID de autoridade são válidas.</span><span class="sxs-lookup"><span data-stu-id="d75f5-135">At a minimum, the signature of the certificate and authority ID extension are valid.</span></span><br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <span data-ttu-id="d75f5-136"><dt>0x11111000</dt> de <dt> **\_ confiança \_ máxima de certificado**</dt></span><span class="sxs-lookup"><span data-stu-id="d75f5-136"><dt> **CERT\_CONFIDENCE\_HIGHEST**</dt> <dt>0x11111000</dt></span></span> </dl>       | <span data-ttu-id="d75f5-137">Uma combinação de todos os outros valores de confiança.</span><span class="sxs-lookup"><span data-stu-id="d75f5-137">A combination of all of the other confidence values.</span></span><br/>                                 |



 

</dd> <dt>

<span data-ttu-id="d75f5-138">*dwError* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d75f5-138">*dwError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d75f5-139">Um ponteiro para uma variável **DWORD** que contém o valor de erro para esse certificado, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="d75f5-139">A pointer to a **DWORD** variable that contains the error value for this certificate, if applicable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d75f5-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d75f5-140">Return value</span></span>

<span data-ttu-id="d75f5-141">Um certificado de emissor que corresponde ao certificado de entidade especificado pelo parâmetro *pChildContext* .</span><span class="sxs-lookup"><span data-stu-id="d75f5-141">An issuer certificate that matches the subject certificate specified by the *pChildContext* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="d75f5-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="d75f5-142">Remarks</span></span>

<span data-ttu-id="d75f5-143">Para localizar com êxito um certificado de emissor correspondente, os requisitos a seguir devem ser atendidos:</span><span class="sxs-lookup"><span data-stu-id="d75f5-143">To successfully find a matching issuer certificate, the following requirements must be met:</span></span>

-   <span data-ttu-id="d75f5-144">A assinatura do certificado da entidade especificada pelo parâmetro *pChildContext* deve ser válida.</span><span class="sxs-lookup"><span data-stu-id="d75f5-144">The signature of the subject certificate specified by the *pChildContext* parameter must be valid.</span></span>
-   <span data-ttu-id="d75f5-145">O membro **rgExtension** do membro **PCertInfo** do parâmetro *pChildContext* deve conter uma estrutura de [**informações de \_ ID de chave de autoridade \_ \_ \_ de certificação**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) .</span><span class="sxs-lookup"><span data-stu-id="d75f5-145">The **rgExtension** member of the **pCertInfo** member of the *pChildContext* parameter must contain a [**CERT\_AUTHORITY\_KEY\_ID\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) structure.</span></span> <span data-ttu-id="d75f5-146">Os membros **CertIssuer** e **CertSerialMember** dessa estrutura correspondem muito aos membros correspondentes para o certificado do emissor.</span><span class="sxs-lookup"><span data-stu-id="d75f5-146">The **CertIssuer** and **CertSerialMember** members of this structure much match the corresponding members for the issuer certificate.</span></span>
-   <span data-ttu-id="d75f5-147">O valor do parâmetro *psftVerifyAsOf* deve estar dentro do período de validade do certificado da entidade.</span><span class="sxs-lookup"><span data-stu-id="d75f5-147">The value of the *psftVerifyAsOf* parameter must be within the period of validity of the subject certificate.</span></span>
-   <span data-ttu-id="d75f5-148">O período de validade do certificado da entidade deve estar dentro do período de validade do certificado do emissor.</span><span class="sxs-lookup"><span data-stu-id="d75f5-148">The period of validity of the subject certificate must be within the period of validity of the issuer certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="d75f5-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d75f5-149">Requirements</span></span>



| <span data-ttu-id="d75f5-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="d75f5-150">Requirement</span></span> | <span data-ttu-id="d75f5-151">Valor</span><span class="sxs-lookup"><span data-stu-id="d75f5-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d75f5-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d75f5-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d75f5-153">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d75f5-153">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d75f5-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d75f5-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d75f5-155">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d75f5-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d75f5-156">DLL</span><span class="sxs-lookup"><span data-stu-id="d75f5-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d75f5-157"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d75f5-157"><dt>Wintrust.dll</dt></span></span> </dl> |



 

 
