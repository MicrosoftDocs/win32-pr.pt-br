---
title: Constantes de HTTP_AUTH_ENABLE_ (http. h)
description: Defina os esquemas de autenticação que podem ser habilitados em um grupo de URLs.
ms.assetid: db22645f-c9e4-427e-b3d5-91d568aec7c5
topic_type:
- apiref
api_name:
- HTTP_AUTH_ENABLE_BASIC
- HTTP_AUTH_ENABLE_DIGEST
- HTTP_AUTH_ENABLE_KERBEROS
- HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING
- HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL
- HTTP_AUTH_ENABLE_NTLM
- HTTP_AUTH_ENABLE_NEGOTIATE
- HTTP_AUTH_ENABLE_ALL
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6462a4f9d884244f460c4bf7714b45d3e17600c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455887"
---
# <a name="http_auth_enable_-constants"></a><span data-ttu-id="2a32f-103">\_Constantes http auth \_ Enable \_</span><span class="sxs-lookup"><span data-stu-id="2a32f-103">HTTP\_AUTH\_ENABLE\_ Constants</span></span>

<span data-ttu-id="2a32f-104">As constantes **http \_ auth \_ Enable** definem os esquemas de autenticação que podem ser habilitados em um grupo de URLs.</span><span class="sxs-lookup"><span data-stu-id="2a32f-104">The **HTTP\_AUTH\_ENABLE** constants define authentication schemes that can be enabled on a URL Group.</span></span>

<span data-ttu-id="2a32f-105">Essas constantes são usadas na estrutura [**de \_ \_ \_ informações de autenticação do servidor http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) .</span><span class="sxs-lookup"><span data-stu-id="2a32f-105">These constants are used in the [**HTTP\_SERVER\_AUTHENTICATION\_INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="2a32f-106"><span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**\_habilitação de http auth \_ \_ básico**</span><span class="sxs-lookup"><span data-stu-id="2a32f-106"><span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**HTTP\_AUTH\_ENABLE\_BASIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2a32f-107">O esquema de autenticação básica está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2a32f-107">The Basic authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2a32f-108"><span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**HTTP \_ auth \_ Enable \_ Digest**</span><span class="sxs-lookup"><span data-stu-id="2a32f-108"><span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**HTTP\_AUTH\_ENABLE\_DIGEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2a32f-109">O esquema de autenticação Digest está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2a32f-109">The Digest authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2a32f-110"><span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**HTTP \_ auth \_ habilitar \_ Kerberos**</span><span class="sxs-lookup"><span data-stu-id="2a32f-110"><span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**HTTP\_AUTH\_ENABLE\_KERBEROS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2a32f-111">O esquema de autenticação Kerberos está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2a32f-111">The Kerberos authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2a32f-112"><span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**\_sinalizador http auth \_ ex habilitar o cache de \_ \_ \_ \_ credenciais Kerberos \_**</span><span class="sxs-lookup"><span data-stu-id="2a32f-112"><span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**HTTP\_AUTH\_EX\_FLAG\_ENABLE\_KERBEROS\_CREDENTIAL\_CACHING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2a32f-113">O cache de credenciais Kerberos está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2a32f-113">Kerberos credential caching is enabled.</span></span>

<span data-ttu-id="2a32f-114">**Windows Server 2003 e anteriores:** Não disponível.</span><span class="sxs-lookup"><span data-stu-id="2a32f-114">**Windows Server 2003 and before:** Not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2a32f-115"><span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**\_ \_ \_ \_ credencial de captura de sinalizador http auth ex \_**</span><span class="sxs-lookup"><span data-stu-id="2a32f-115"><span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**HTTP\_AUTH\_EX\_FLAG\_CAPTURE\_CREDENTIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2a32f-116">A API do servidor HTTP captura a identidade do chamador e a usa para autenticação somente para esquemas Negotiate e Kerberos.</span><span class="sxs-lookup"><span data-stu-id="2a32f-116">The HTTP Server API captures the caller identity and uses it for authentication for Negotiate and Kerberos schemes only.</span></span>

<span data-ttu-id="2a32f-117">**Windows Server 2003 e anteriores:** Não disponível.</span><span class="sxs-lookup"><span data-stu-id="2a32f-117">**Windows Server 2003 and before:** Not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2a32f-118"><span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**HTTP \_ auth \_ habilitar \_ NTLM**</span><span class="sxs-lookup"><span data-stu-id="2a32f-118"><span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**HTTP\_AUTH\_ENABLE\_NTLM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2a32f-119">O esquema de autenticação NTLM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2a32f-119">The NTLM authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2a32f-120"><span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**\_ \_ habilitar \_ negociação de http auth**</span><span class="sxs-lookup"><span data-stu-id="2a32f-120"><span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**HTTP\_AUTH\_ENABLE\_NEGOTIATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2a32f-121">O esquema de autenticação Negotiate está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2a32f-121">The Negotiate authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2a32f-122"><span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**\_ \_ habilitar \_ todos os http auth**</span><span class="sxs-lookup"><span data-stu-id="2a32f-122"><span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**HTTP\_AUTH\_ENABLE\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2a32f-123">Todos os esquemas de autenticação estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="2a32f-123">All authentication schemes are enabled.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a32f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a32f-124">Requirements</span></span>



| <span data-ttu-id="2a32f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a32f-125">Requirement</span></span> | <span data-ttu-id="2a32f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2a32f-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2a32f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a32f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2a32f-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a32f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2a32f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a32f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2a32f-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2a32f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2a32f-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a32f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a32f-132"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a32f-132"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a32f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a32f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a32f-134">Constantes da API do servidor HTTP versão 2,0</span><span class="sxs-lookup"><span data-stu-id="2a32f-134">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="2a32f-135">**\_informações de \_ autenticação do servidor http \_**</span><span class="sxs-lookup"><span data-stu-id="2a32f-135">**HTTP\_SERVER\_AUTHENTICATION\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[<span data-ttu-id="2a32f-136">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="2a32f-136">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="2a32f-137">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="2a32f-137">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="2a32f-138">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="2a32f-138">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="2a32f-139">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="2a32f-139">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





