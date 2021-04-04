---
title: Associações de segurança
description: Uma associação de segurança é a especificação de um token de segurança e informa ao tempo de execução como obter e usar um token de segurança para segurança de canal.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Serviços Web de associações de segurança para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a263c1a79212f3438e77c3dca519f6493cf40e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104085004"
---
# <a name="security-bindings"></a><span data-ttu-id="8fc95-106">Associações de segurança</span><span class="sxs-lookup"><span data-stu-id="8fc95-106">Security Bindings</span></span>

<span data-ttu-id="8fc95-107">Uma associação de segurança é a especificação de um token de segurança e informa ao tempo de execução como obter e usar um token de segurança para segurança de canal.</span><span class="sxs-lookup"><span data-stu-id="8fc95-107">A security binding is the specification of a security token, and tells the runtime how to obtain and use a security token for channel security.</span></span> <span data-ttu-id="8fc95-108">O token de segurança contém informações que comprovam o direito de acessar recursos.</span><span class="sxs-lookup"><span data-stu-id="8fc95-108">The security token contains information that vouches for the right to access resources.</span></span> <span data-ttu-id="8fc95-109">Ele também pode ter uma chave de criptografia associada para executar assinaturas e criptografia.</span><span class="sxs-lookup"><span data-stu-id="8fc95-109">It may also have an associated cryptographic key for performing signatures and encryption.</span></span>


<span data-ttu-id="8fc95-110">Cada associação de segurança contém sua própria coleção de [configurações de associação de segurança](security-binding-settings.md) opcionais que têm como escopo o token de segurança definido por ele.</span><span class="sxs-lookup"><span data-stu-id="8fc95-110">Each security binding contains its own collection of optional [security binding settings](security-binding-settings.md) that are scoped to the security token it defines.</span></span> <span data-ttu-id="8fc95-111">Ele também contém [credenciais de segurança](security-credentials.md), que representam as evidências de segurança (como nome de usuário e senhas ou certificados) necessários para criar tokens de segurança.</span><span class="sxs-lookup"><span data-stu-id="8fc95-111">It also contains [security credentials](security-credentials.md), representing the security evidence (such as username and passwords, or certificates) needed to create security tokens.</span></span>

<span data-ttu-id="8fc95-112">As seguintes chamadas de retorno fazem parte da Associação de segurança:</span><span class="sxs-lookup"><span data-stu-id="8fc95-112">The following callbacks are part of the security binding:</span></span>

-   [<span data-ttu-id="8fc95-113">**\_retorno de \_ \_ chamada SAML do WS Validate**</span><span class="sxs-lookup"><span data-stu-id="8fc95-113">**WS\_VALIDATE\_SAML\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

<span data-ttu-id="8fc95-114">As seguintes enumerações fazem parte da Associação de segurança:</span><span class="sxs-lookup"><span data-stu-id="8fc95-114">The following enumerations are part of the security binding:</span></span>

-   [<span data-ttu-id="8fc95-115">**uso de segurança do WS \_ Message \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-115">**WS\_MESSAGE\_SECURITY\_USAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [<span data-ttu-id="8fc95-116">**\_tipo de \_ autenticador SAML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-116">**WS\_SAML\_AUTHENTICATOR\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [<span data-ttu-id="8fc95-117">**\_tipo de \_ Associação de segurança do WS \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-117">**WS\_SECURITY\_BINDING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [<span data-ttu-id="8fc95-118">**\_tipo de \_ identificador de chave de segurança WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-118">**WS\_SECURITY\_KEY\_HANDLE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

<span data-ttu-id="8fc95-119">As funções a seguir fazem parte da Associação de segurança:</span><span class="sxs-lookup"><span data-stu-id="8fc95-119">The following functions are part of the security binding:</span></span>

-   [<span data-ttu-id="8fc95-120">**WsCreateXmlSecurityToken**</span><span class="sxs-lookup"><span data-stu-id="8fc95-120">**WsCreateXmlSecurityToken**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [<span data-ttu-id="8fc95-121">**WsFreeSecurityToken**</span><span class="sxs-lookup"><span data-stu-id="8fc95-121">**WsFreeSecurityToken**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

<span data-ttu-id="8fc95-122">As seguintes estruturas fazem parte da Associação de segurança:</span><span class="sxs-lookup"><span data-stu-id="8fc95-122">The following structures are part of the security binding:</span></span>

-   [<span data-ttu-id="8fc95-123">**\_identificador de \_ \_ chave de segurança assimétrica do WS \_ CAPI \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-123">**WS\_CAPI\_ASYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [<span data-ttu-id="8fc95-124">**\_ \_ \_ autenticador SAML assinado por certificado WS \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-124">**WS\_CERT\_SIGNED\_SAML\_AUTHENTICATOR**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [<span data-ttu-id="8fc95-125">**\_Associação de \_ \_ segurança de autenticação de cabeçalho http \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-125">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [<span data-ttu-id="8fc95-126">**\_Associação de \_ \_ segurança de mensagem APREQ \_ \_ do WS Kerberos**</span><span class="sxs-lookup"><span data-stu-id="8fc95-126">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [<span data-ttu-id="8fc95-127">**\_Associação de \_ \_ segurança de transporte SSPI \_ \_ do WS NAMEDPIPE**</span><span class="sxs-lookup"><span data-stu-id="8fc95-127">**WS\_NAMEDPIPE\_SSPI\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [<span data-ttu-id="8fc95-128">**\_identificador de \_ chave de segurança assimétrica WS NCRYPT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-128">**WS\_NCRYPT\_ASYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [<span data-ttu-id="8fc95-129">**\_identificador de \_ \_ chave de segurança simétrica \_ \_ WS-RAW**</span><span class="sxs-lookup"><span data-stu-id="8fc95-129">**WS\_RAW\_SYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [<span data-ttu-id="8fc95-130">**\_autenticador SAML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-130">**WS\_SAML\_AUTHENTICATOR**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [<span data-ttu-id="8fc95-131">**\_Associação de \_ segurança de mensagem SAML \_ do WS \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-131">**WS\_SAML\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [<span data-ttu-id="8fc95-132">**\_Associação de segurança WS \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-132">**WS\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [<span data-ttu-id="8fc95-133">**\_Associação de \_ segurança de mensagem de contexto de segurança WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-133">**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [<span data-ttu-id="8fc95-134">**\_identificador de \_ chave de segurança do WS \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-134">**WS\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [<span data-ttu-id="8fc95-135">**\_Associação de \_ segurança de transporte WS SSL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-135">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [<span data-ttu-id="8fc95-136">**Associação de segurança de transporte do WS \_ TCP \_ SSPI \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-136">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [<span data-ttu-id="8fc95-137">**\_Associação de \_ segurança de mensagem WS username \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-137">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [<span data-ttu-id="8fc95-138">**\_Associação de \_ \_ segurança de mensagem de token XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="8fc95-138">**WS\_XML\_TOKEN\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




