---
title: Credenciais de Segurança
description: As credenciais de segurança são uma parte da evidência que uma parte de comunicação possui que pode ser usada para criar ou obter um token de segurança.
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Serviços Web de credenciais de segurança para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0611e6e54fd83e09f811ffddcda4785cef162685
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "105791498"
---
# <a name="security-credentials"></a><span data-ttu-id="6d005-106">Credenciais de Segurança</span><span class="sxs-lookup"><span data-stu-id="6d005-106">Security Credentials</span></span>

<span data-ttu-id="6d005-107">As credenciais de segurança são uma parte da evidência que uma parte de comunicação possui que pode ser usada para criar ou obter um token de segurança.</span><span class="sxs-lookup"><span data-stu-id="6d005-107">Security credentials are a piece of evidence that a communicating party possesses that can be used to create or obtain a security token.</span></span> <span data-ttu-id="6d005-108">Assim, as credenciais normalmente são mais longas do que os tokens de segurança, e um token de segurança pode ser exibido como a manifestação de tempo de execução das credenciais de segurança.</span><span class="sxs-lookup"><span data-stu-id="6d005-108">Thus, credentials are typically longer-lived than security tokens, and a security token can be viewed as the runtime manifestation of the security credentials.</span></span> <span data-ttu-id="6d005-109">Exemplos de credenciais incluem um certificado de computador (que pode ser convertido em um token de segurança X. 509 em tempo de execução) ou um par de nome de usuário/senha para um domínio (que pode ser usado para obter um token de segurança Kerberos).</span><span class="sxs-lookup"><span data-stu-id="6d005-109">Example of credentials include a machine certificate (which can be converted into an X.509 security token at runtime) or a username/password pair for a domain (which can be used to obtain a Kerberos security token).</span></span>


<span data-ttu-id="6d005-110">As credenciais são especificadas como parte das [associações de segurança](security-bindings.md).</span><span class="sxs-lookup"><span data-stu-id="6d005-110">Credentials are specified as part of the [security bindings](security-bindings.md).</span></span>

<span data-ttu-id="6d005-111">Os seguintes elementos de API são usados com credenciais de segurança.</span><span class="sxs-lookup"><span data-stu-id="6d005-111">The following API elements are used with security credentials.</span></span>

| <span data-ttu-id="6d005-112">Callback</span><span class="sxs-lookup"><span data-stu-id="6d005-112">Callback</span></span>                                                                  | <span data-ttu-id="6d005-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d005-113">Description</span></span>                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="6d005-114">**\_retorno de chamada WS get \_ CERT \_**</span><span class="sxs-lookup"><span data-stu-id="6d005-114">**WS\_GET\_CERT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | <span data-ttu-id="6d005-115">Fornece um certificado para o tempo de execução de segurança.</span><span class="sxs-lookup"><span data-stu-id="6d005-115">Provides a certificate to the security runtime.</span></span>          |
| [<span data-ttu-id="6d005-116">**\_retorno de \_ chamada de senha do WS Validate \_**</span><span class="sxs-lookup"><span data-stu-id="6d005-116">**WS\_VALIDATE\_PASSWORD\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | <span data-ttu-id="6d005-117">Valida um par de nome de usuário/senha no lado do destinatário.</span><span class="sxs-lookup"><span data-stu-id="6d005-117">Validates a username/password pair on the receiver side.</span></span> |



 



| <span data-ttu-id="6d005-118">Enumeração</span><span class="sxs-lookup"><span data-stu-id="6d005-118">Enumeration</span></span>                                                                                           | <span data-ttu-id="6d005-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d005-119">Description</span></span>                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="6d005-120">**\_tipo de \_ credencial WS CERT \_**</span><span class="sxs-lookup"><span data-stu-id="6d005-120">**WS\_CERT\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | <span data-ttu-id="6d005-121">O tipo da credencial do certificado.</span><span class="sxs-lookup"><span data-stu-id="6d005-121">The type of the certificate credential.</span></span>                       |
| [<span data-ttu-id="6d005-122">**\_tipo de \_ credencial WS username \_**</span><span class="sxs-lookup"><span data-stu-id="6d005-122">**WS\_USERNAME\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | <span data-ttu-id="6d005-123">O tipo de credencial de nome de usuário/senha.</span><span class="sxs-lookup"><span data-stu-id="6d005-123">The type of the username/password credential.</span></span>                 |
| [<span data-ttu-id="6d005-124">**\_tipo de \_ \_ \_ credencial de \_ autenticação integrada do Windows WS**</span><span class="sxs-lookup"><span data-stu-id="6d005-124">**WS\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | <span data-ttu-id="6d005-125">O tipo da credencial de autenticação integrada do Windows.</span><span class="sxs-lookup"><span data-stu-id="6d005-125">The type of the Windows Integrated Authentication credential.</span></span> |



 



| <span data-ttu-id="6d005-126">Estrutura</span><span class="sxs-lookup"><span data-stu-id="6d005-126">Structure</span></span>                                                                                                   | <span data-ttu-id="6d005-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d005-127">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d005-128">**\_ \_ credencial WS CERT**</span><span class="sxs-lookup"><span data-stu-id="6d005-128">**WS\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | <span data-ttu-id="6d005-129">O tipo base abstrato para todos os tipos de credencial de certificado.</span><span class="sxs-lookup"><span data-stu-id="6d005-129">The abstract base type for all certificate credential types.</span></span>                                                          |
| [<span data-ttu-id="6d005-130">**\_ \_ credencial de certificado personalizado WS \_**</span><span class="sxs-lookup"><span data-stu-id="6d005-130">**WS\_CUSTOM\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | <span data-ttu-id="6d005-131">O tipo para especificar uma credencial de certificado que deve ser fornecida por um retorno de chamada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6d005-131">The type for specifying a certificate credential that is to be supplied by a callback to the application.</span></span>             |
| [<span data-ttu-id="6d005-132">**\_ \_ \_ \_ credencial de autenticação integrada do Windows WS padrão \_**</span><span class="sxs-lookup"><span data-stu-id="6d005-132">**WS\_DEFAULT\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | <span data-ttu-id="6d005-133">Tipo para fornecer uma credencial de autenticação integrada do Windows com base no token de thread atual.</span><span class="sxs-lookup"><span data-stu-id="6d005-133">Type for supplying a Windows Integrated Authentication credential based on the current thread token.</span></span>                  |
| [<span data-ttu-id="6d005-134">**\_ \_ \_ \_ credencial de autenticação integrada do Windows WS opaca \_**</span><span class="sxs-lookup"><span data-stu-id="6d005-134">**WS\_OPAQUE\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | <span data-ttu-id="6d005-135">Digite para fornecer uma credencial de autenticação integrada do Windows.</span><span class="sxs-lookup"><span data-stu-id="6d005-135">Type for supplying a Windows Integrated Authentication credential.</span></span>                                                    |
| [<span data-ttu-id="6d005-136">**\_ \_ credencial de nome de usuário WS String \_**</span><span class="sxs-lookup"><span data-stu-id="6d005-136">**WS\_STRING\_USERNAME\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | <span data-ttu-id="6d005-137">O tipo para fornecer um par de nome de usuário/senha como cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6d005-137">The type for supplying a username/password pair as strings.</span></span>                                                           |
| [<span data-ttu-id="6d005-138">**\_ \_ \_ \_ credencial de autenticação integrada do Windows WS String \_**</span><span class="sxs-lookup"><span data-stu-id="6d005-138">**WS\_STRING\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | <span data-ttu-id="6d005-139">Digite para fornecer uma credencial do Windows como nome de usuário, senha e cadeias de caracteres de domínio.</span><span class="sxs-lookup"><span data-stu-id="6d005-139">Type for supplying a Windows credential as username, password, domain strings.</span></span>                                        |
| [<span data-ttu-id="6d005-140">**\_ \_ \_ credencial de certificado do nome da entidade WS \_**</span><span class="sxs-lookup"><span data-stu-id="6d005-140">**WS\_SUBJECT\_NAME\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | <span data-ttu-id="6d005-141">O tipo para especificar uma credencial de certificado usando o nome da entidade do certificado, o local do repositório e o nome do repositório.</span><span class="sxs-lookup"><span data-stu-id="6d005-141">The type for specifying a certificate credential using the certificate's subject name, store location and store name.</span></span> |
| [<span data-ttu-id="6d005-142">**\_ \_ credencial de certificado de impressão digital WS \_**</span><span class="sxs-lookup"><span data-stu-id="6d005-142">**WS\_THUMBPRINT\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | <span data-ttu-id="6d005-143">O tipo para especificar uma credencial de certificado usando a impressão digital do certificado, o local do repositório e o nome do repositório.</span><span class="sxs-lookup"><span data-stu-id="6d005-143">The type for specifying a certificate credential using the certificate's thumbprint, store location and store name.</span></span>   |
| [<span data-ttu-id="6d005-144">**\_ \_ credencial WS username**</span><span class="sxs-lookup"><span data-stu-id="6d005-144">**WS\_USERNAME\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | <span data-ttu-id="6d005-145">O tipo base abstrato para todas as credenciais de nome de usuário/senha.</span><span class="sxs-lookup"><span data-stu-id="6d005-145">The abstract base type for all username/password credentials.</span></span>                                                         |
| [<span data-ttu-id="6d005-146">**\_ \_ \_ credencial de autenticação \_ integrada do Windows WS**</span><span class="sxs-lookup"><span data-stu-id="6d005-146">**WS\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | <span data-ttu-id="6d005-147">O tipo base abstrato para todos os tipos de credenciais usados com a autenticação integrada do Windows.</span><span class="sxs-lookup"><span data-stu-id="6d005-147">The abstract base type for all credential types used with Windows Integrated Authentication.</span></span>                          |



 

 

 




