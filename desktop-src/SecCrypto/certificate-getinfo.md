---
description: Recupera informações do certificado.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: 'Método ICertificate2:: GetInfo'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.GetInfo
- ICertificate2.GetInfo
- ICertificate.GetInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41b3cb6cde796f64ee3a5953ed848d105a10bc5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770252"
---
# <a name="icertificate2getinfo-method"></a><span data-ttu-id="b7762-103">Método ICertificate2:: GetInfo</span><span class="sxs-lookup"><span data-stu-id="b7762-103">ICertificate2::GetInfo method</span></span>

<span data-ttu-id="b7762-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b7762-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b7762-105">Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b7762-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b7762-106">O método **GetInfo** recupera informações do [*certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b7762-106">The **GetInfo** method retrieves information from the [*certificate*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7762-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7762-107">Syntax</span></span>


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a><span data-ttu-id="b7762-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7762-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7762-109">*InfoType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7762-109">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7762-110">Um valor da enumeração [**de \_ \_ \_ tipo de informações do certificado capicor**](capicom-cert-info-type.md) que especifica que tipo de dados é recuperado do certificado.</span><span class="sxs-lookup"><span data-stu-id="b7762-110">A value of the [**CAPICOM\_CERT\_INFO\_TYPE**](capicom-cert-info-type.md) enumeration that specifies what type of data is retrieved from the certificate.</span></span> <span data-ttu-id="b7762-111">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="b7762-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="b7762-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b7762-112">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="b7762-113">Significado</span><span class="sxs-lookup"><span data-stu-id="b7762-113">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <span data-ttu-id="b7762-114"><dt>**informações de certificado capicor \_ \_ \_ \_ nome simples da entidade \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b7762-114"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_SIMPLE\_NAME**</dt></span></span> </dl> | <span data-ttu-id="b7762-115">Retorna o nome de exibição da entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="b7762-115">Returns the display name from the certificate subject.</span></span><br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <span data-ttu-id="b7762-116"><dt>**\_ \_ \_ nome simples do emissor de informações de \_ certificado CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b7762-116"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_SIMPLE\_NAME**</dt></span></span> </dl>    | <span data-ttu-id="b7762-117">Retorna o nome de exibição do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="b7762-117">Returns the display name of the issuer of the certificate.</span></span><br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <span data-ttu-id="b7762-118"><dt>**CAPICOM \_ informações de certificado \_ nome de \_ email da entidade \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b7762-118"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_EMAIL\_NAME**</dt></span></span> </dl>    | <span data-ttu-id="b7762-119">Retorna o endereço de email da entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="b7762-119">Returns the email address of the certificate subject.</span></span><br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <span data-ttu-id="b7762-120"><dt>**capicor \_ informações do certificado \_ nome do \_ email do emissor \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b7762-120"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_EMAIL\_NAME**</dt></span></span> </dl>       | <span data-ttu-id="b7762-121">Retorna o endereço de email do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="b7762-121">Returns the email address of the issuer of the certificate.</span></span><br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <span data-ttu-id="b7762-122"><dt>**informações de certificado capicor \_ \_ \_ UPN da entidade \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b7762-122"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_UPN**</dt></span></span> </dl>                          | <span data-ttu-id="b7762-123">Retorna o UPN da entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="b7762-123">Returns the UPN of the certificate subject.</span></span> <span data-ttu-id="b7762-124">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b7762-124">Introduced in CAPICOM 2.0.</span></span><br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <span data-ttu-id="b7762-125"><dt>**\_UPN do \_ emissor de informações de certificado CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b7762-125"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_UPN**</dt></span></span> </dl>                             | <span data-ttu-id="b7762-126">Retorna o UPN do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="b7762-126">Returns the UPN of the issuer of the certificate.</span></span> <span data-ttu-id="b7762-127">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b7762-127">Introduced in CAPICOM 2.0.</span></span><br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <span data-ttu-id="b7762-128"><dt>**CAPICOM \_ informações do certificado \_ \_ \_ nome DNS da entidade \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b7762-128"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_DNS\_NAME**</dt></span></span> </dl>          | <span data-ttu-id="b7762-129">Retorna o nome DNS da entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="b7762-129">Returns the DNS name of the certificate subject.</span></span> <span data-ttu-id="b7762-130">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b7762-130">Introduced in CAPICOM 2.0.</span></span><br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <span data-ttu-id="b7762-131"><dt>**CAPICOM \_ informações do certificado \_ \_ \_ nome DNS do emissor \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b7762-131"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_DNS\_NAME**</dt></span></span> </dl>             | <span data-ttu-id="b7762-132">Retorna o nome DNS do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="b7762-132">Returns the DNS name of the issuer of the certificate.</span></span> <span data-ttu-id="b7762-133">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b7762-133">Introduced in CAPICOM 2.0.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7762-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7762-134">Return value</span></span>

<span data-ttu-id="b7762-135">Uma cadeia de caracteres que contém as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="b7762-135">A string that contains the requested information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7762-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7762-136">Requirements</span></span>



| <span data-ttu-id="b7762-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7762-137">Requirement</span></span> | <span data-ttu-id="b7762-138">Valor</span><span class="sxs-lookup"><span data-stu-id="b7762-138">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7762-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b7762-139">End of client support</span></span><br/> | <span data-ttu-id="b7762-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7762-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b7762-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b7762-141">End of server support</span></span><br/> | <span data-ttu-id="b7762-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7762-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b7762-143">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b7762-143">Redistributable</span></span><br/>       | <span data-ttu-id="b7762-144">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="b7762-144">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b7762-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b7762-145">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b7762-146"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7762-146"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7762-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7762-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7762-148">Objetos de criptografia</span><span class="sxs-lookup"><span data-stu-id="b7762-148">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="b7762-149">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="b7762-149">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
