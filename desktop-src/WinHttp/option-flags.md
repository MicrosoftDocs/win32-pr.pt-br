---
Description: Os seguintes sinalizadores de opção têm suporte de WinHttpQueryOption e WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Sinalizadores de opção (WinHTTP. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 25049ee11c59c6b320b794c07bd65e5ec9b930c9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395411"
---
# <a name="option-flags"></a><span data-ttu-id="a115f-103">Sinalizadores de opção</span><span class="sxs-lookup"><span data-stu-id="a115f-103">Option Flags</span></span>

<span data-ttu-id="a115f-104">Os seguintes sinalizadores de opção têm suporte de [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span><span class="sxs-lookup"><span data-stu-id="a115f-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="a115f-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**\_opção WinHTTP \_ garantindo \_ \_ \_ retornos de chamada sem bloqueio**</span><span class="sxs-lookup"><span data-stu-id="a115f-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-106">O padrão é FALSE.</span><span class="sxs-lookup"><span data-stu-id="a115f-106">The default is FALSE.</span></span> <span data-ttu-id="a115f-107">Se definido como TRUE, o WinHTTP não garantirá o progresso se os retornos de chamada de status forem bloqueados pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="a115f-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="a115f-108">O aplicativo cliente deve tomar cuidado especial para executar operações mínimas no retorno de chamada sem bloqueio, retornando o mais rápido possível e, em particular, não deve esperar por nenhuma chamada de WinHTTP subsequente.</span><span class="sxs-lookup"><span data-stu-id="a115f-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="a115f-109">Se não seguir essas diretrizes, provavelmente haverá um impacto negativo no desempenho ou um possível travamento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a115f-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="a115f-110">Se usado da maneira prescrita, essa opção pode melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="a115f-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**política de WINHTTP da \_ opção de \_ logon automático \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-112">Define um valor inteiro longo sem sinal que especifica a [política de logon automática](authentication-in-winhttp.md) com um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a115f-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="a115f-113">Termo</span><span class="sxs-lookup"><span data-stu-id="a115f-113">Term</span></span> | <span data-ttu-id="a115f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a115f-114">Description</span></span> |
|-|-|
| <span data-ttu-id="a115f-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>nível de segurança do WINHTTP \_ AUTOlogonn \_ \_ \_ alto</span><span class="sxs-lookup"><span data-stu-id="a115f-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="a115f-116">As credenciais padrão não são usadas.</span><span class="sxs-lookup"><span data-stu-id="a115f-116">Default credentials are not used.</span></span> <span data-ttu-id="a115f-117">Observe que esse sinalizador só terá efeito se você especificar o servidor pelo nome real do computador.</span><span class="sxs-lookup"><span data-stu-id="a115f-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="a115f-118">Ele não entrará em vigor, se você especificar o servidor por "localhost" ou endereço IP.</span><span class="sxs-lookup"><span data-stu-id="a115f-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="a115f-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>nível de segurança do WINHTTP com \_ \_ acesso automático \_ \_ reduzido</span><span class="sxs-lookup"><span data-stu-id="a115f-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="a115f-120">Um logon autenticado usando as credenciais padrão é executado para todas as solicitações.</span><span class="sxs-lookup"><span data-stu-id="a115f-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="a115f-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>nível de segurança do WINHTTP com \_ logon automático \_ \_ \_ médio</span><span class="sxs-lookup"><span data-stu-id="a115f-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="a115f-122">Um logon autenticado usando as credenciais padrão é executado somente para solicitações na intranet local.</span><span class="sxs-lookup"><span data-stu-id="a115f-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a115f-123"><span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**\_ \_ conexões em segundo plano da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-123"><span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**WINHTTP\_OPTION\_BACKGROUND\_CONNECTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a115f-124">Ao definir essa opção em um identificador de sessão, você deve passar o número de conexões que deseja abrir.</span><span class="sxs-lookup"><span data-stu-id="a115f-124">When you set this option on a session handle, you must pass the number of connections you wish to open.</span></span> <span data-ttu-id="a115f-125">Em seguida, após o envio de uma solicitação, em vez de abrir apenas uma única conexão, o WinHttp abre várias conexões em paralelo.</span><span class="sxs-lookup"><span data-stu-id="a115f-125">Then, upon first sending a request, rather than opening only a single connection, WinHttp opens a number of connections in parallel.</span></span> <span data-ttu-id="a115f-126">Isso pode melhorar o desempenho das solicitações subsequentes para o mesmo destino, o que não terá a sobrecarga do estabelecimento da conexão.</span><span class="sxs-lookup"><span data-stu-id="a115f-126">This can improve the performance of subsequent requests to the same destination, which won't have the overhead of connection establishment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-127"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**retorno de chamada de \_ opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-127"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-128">Recupera o ponteiro para a função de retorno de chamada definida com [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span><span class="sxs-lookup"><span data-stu-id="a115f-128">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-129"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**\_contexto de \_ certificado de cliente de opção WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-129"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-130">Define o contexto de certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="a115f-130">Sets the client certificate context.</span></span> <span data-ttu-id="a115f-131">Se um aplicativo receber [**o \_ certificado de autenticação de cliente WinHTTP de erro \_ \_ \_ \_ necessário**](error-messages.md), ele deverá chamar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para fornecer um certificado antes de repetir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a115f-131">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="a115f-132">Como parte do processamento dessa opção, o WinHttp chama [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) no contexto de certificado fornecido pelo chamador para que o contexto do certificado possa ser liberado independentemente pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="a115f-132">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="a115f-133">O aplicativo não deve tentar fechar o repositório de certificados com o \_ sinalizador de \_ sinalizador de força de armazenamento de fechamento de certificado \_ \_ na chamada para [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) no repositório de certificados do qual o contexto de certificado foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="a115f-133">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="a115f-134">Pode ocorrer uma violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="a115f-134">An access violation may occur.</span></span>

<span data-ttu-id="a115f-135">Quando o servidor solicita um certificado de cliente, o [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)ou o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retorna um erro WinHTTP erro de [**certificado de \_ \_ \_ autenticação de \_ \_ cliente**](error-messages.md) .</span><span class="sxs-lookup"><span data-stu-id="a115f-135">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="a115f-136">Se o servidor solicitar o certificado, mas não o exigir, o aplicativo poderá especificar essa opção para indicar que ele não tem um certificado.</span><span class="sxs-lookup"><span data-stu-id="a115f-136">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="a115f-137">O servidor pode escolher outro esquema de autenticação ou permitir acesso anônimo ao servidor.</span><span class="sxs-lookup"><span data-stu-id="a115f-137">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="a115f-138">O aplicativo fornece a macro de **contexto de \_ \_ \_ certificado \_ de cliente do WinHTTP** no parâmetro *lpBuffer* de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a115f-138">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="a115f-139">Se o servidor exigir um certificado de cliente, ele poderá enviar um código de status HTTP 403 em resposta.</span><span class="sxs-lookup"><span data-stu-id="a115f-139">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="a115f-140">Para obter mais informações, consulte **a \_ opção \_ WinHTTP \_ \_ \_ lista de emissor de certificado de cliente** .</span><span class="sxs-lookup"><span data-stu-id="a115f-140">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-141"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_opção WinHTTP \_ \_ lista de emissor de certificado de cliente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-141"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-142">Recupera uma [**estrutura SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) quando o erro de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) é um **erro \_ WinHTTP \_ Client \_ auth \_ CERT \_ necessário**.</span><span class="sxs-lookup"><span data-stu-id="a115f-142">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="a115f-143">A lista emissor na estrutura contém uma lista de autoridades de certificação aceitáveis (CA) do servidor.</span><span class="sxs-lookup"><span data-stu-id="a115f-143">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="a115f-144">O aplicativo cliente pode filtrar a lista de autoridades de certificação para recuperar o certificado do cliente para autenticação SSL.</span><span class="sxs-lookup"><span data-stu-id="a115f-144">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="a115f-145">Como alternativa, se o servidor solicitar o certificado do cliente, mas não precisar dele, o aplicativo poderá chamar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) com a opção **WinHTTP de contexto de \_ \_ \_ certificado \_ de cliente** .</span><span class="sxs-lookup"><span data-stu-id="a115f-145">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="a115f-146">Para obter mais informações, consulte opção **WinHTTP de contexto de certificado de \_ \_ cliente \_ \_ de opção** .</span><span class="sxs-lookup"><span data-stu-id="a115f-146">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-147"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**página de código da \_ opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-147"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-148">Define a [*página de código*](glossary.md) usada para processar a URL (ou seja, a cadeia de caracteres de consulta).</span><span class="sxs-lookup"><span data-stu-id="a115f-148">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="a115f-149">O padrão é UTF8.</span><span class="sxs-lookup"><span data-stu-id="a115f-149">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-150"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_opção WinHTTP \_ Configurar \_ autenticação do Passport \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-150"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-151">Define um valor inteiro longo sem sinal que especifica se a [autenticação do Passport na autenticação do WinHTTP](passport-authentication-in-winhttp.md) está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a115f-151">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="a115f-152">O valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="a115f-152">The value can be one of the following:</span></span>

| <span data-ttu-id="a115f-153">Termo</span><span class="sxs-lookup"><span data-stu-id="a115f-153">Term</span></span> | <span data-ttu-id="a115f-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="a115f-154">Description</span></span> |
|-|-|
| <span data-ttu-id="a115f-155"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ desabilitar \_ autenticação do Passport \_</span><span class="sxs-lookup"><span data-stu-id="a115f-155"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="a115f-156">A autenticação Microsoft Passport está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="a115f-156">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="a115f-157">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="a115f-157">This is the default.</span></span> |
| <span data-ttu-id="a115f-158"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ desabilitar \_ o \_ keyring do Passport</span><span class="sxs-lookup"><span data-stu-id="a115f-158"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="a115f-159">O token de telefone do Passport está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a115f-159">The Passport keyring is disabled.</span></span> <span data-ttu-id="a115f-160">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="a115f-160">This is the default.</span></span> |
| <span data-ttu-id="a115f-161"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ habilitar \_ autenticação do Passport \_</span><span class="sxs-lookup"><span data-stu-id="a115f-161"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="a115f-162">A autenticação do Passport está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a115f-162">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="a115f-163"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ habilitar \_ o \_ token de toque do Passport</span><span class="sxs-lookup"><span data-stu-id="a115f-163"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="a115f-164">O token de telefone do Passport está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a115f-164">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="a115f-165"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_ \_ novas tentativas de conexão de opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-165"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-166">Define ou recupera um valor inteiro longo sem sinal que contém o número de tentativas de timesWinHTTP para se conectar a um host.</span><span class="sxs-lookup"><span data-stu-id="a115f-166">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="a115f-167">O Microsoft Windows HTTP Services (WinHTTP) só tenta uma vez por endereço IP (Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="a115f-167">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="a115f-168">Por exemplo, se você tentar se conectar a um host de hospedagem múltipla que tem 10 endereços IP e **a \_ opção WinHTTP as \_ \_ repetições de conexão** estiver definida como 7, o WinHTTP tentará se conectar somente com o primeiro endereço IP sete.</span><span class="sxs-lookup"><span data-stu-id="a115f-168">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="a115f-169">Dado o mesmo conjunto de 10 endereços IP, se **a \_ opção WinHTTP \_ conectar \_ repetições** estiver definida como 20, o WinHTTP tentará cada uma das 10 somente uma vez.</span><span class="sxs-lookup"><span data-stu-id="a115f-169">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="a115f-170">Se uma tentativa de conexão ainda falhar após o número especificado de tentativas ou se o tempo limite de conexão expirar antes de então, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="a115f-170">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="a115f-171">O valor padrão para **as \_ \_ \_ repetições de conexão de opção de WinHTTP** é cinco tentativas.</span><span class="sxs-lookup"><span data-stu-id="a115f-171">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-172"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**\_ \_ tempo limite de conexão da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-172"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-173">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="a115f-173">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="a115f-174">Definir essa opção como infinito (0xFFFFFFFF) desabilitará esse temporizador.</span><span class="sxs-lookup"><span data-stu-id="a115f-174">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="a115f-175">Se uma solicitação de conexão TCP demorar mais do que esse valor de tempo limite, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="a115f-175">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="a115f-176">O tempo limite padrão é de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="a115f-176">The default timeout is 60 seconds.</span></span> <span data-ttu-id="a115f-177">Quando você está tentando se conectar a vários endereços IP para um único host (um host de hospedagem múltipla), o tempo limite é para cada conexão individual.</span><span class="sxs-lookup"><span data-stu-id="a115f-177">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-178"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**\_informações de \_ conexão da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-178"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-179">Recupera o endereço IP de origem e de destino e a porta da solicitação que gerou a resposta quando [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retorna.</span><span class="sxs-lookup"><span data-stu-id="a115f-179">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="a115f-180">O aplicativo chama [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) com a opção de **\_ informações de \_ conexão \_ da opção WinHTTP** e fornece a estrutura de [**informações de \_ conexão \_ WinHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) no parâmetro *lpBuffer* .</span><span class="sxs-lookup"><span data-stu-id="a115f-180">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="a115f-181">Para obter mais informações, **consulte \_ \_ informações de conexão do WinHTTP**.</span><span class="sxs-lookup"><span data-stu-id="a115f-181">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="a115f-182">**Windows Server 2003 com SP1 e Windows XP com SP2:** Este sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a115f-182">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**\_V0 de \_ Estatísticas de conexão da opção WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-184">Recupera o [**struct \_ \_ V0 de informações de TCP**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) para a conexão subjacente usada pela solicitação.</span><span class="sxs-lookup"><span data-stu-id="a115f-184">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="a115f-185">A estrutura retornada pode conter estatísticas de solicitações anteriores enviadas pela mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="a115f-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="a115f-186">Esta opção foi substituída por **WinHTTP \_ Option \_ Connection \_ stats \_ v1**.</span><span class="sxs-lookup"><span data-stu-id="a115f-186">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-187"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**\_Estatísticas de conexão da opção WinHTTP \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="a115f-187"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-188">Recupera a estrutura de [**informações do TCP \_ \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) para a conexão subjacente usada pela solicitação.</span><span class="sxs-lookup"><span data-stu-id="a115f-188">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="a115f-189">A estrutura retornada pode conter estatísticas de solicitações anteriores enviadas pela mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="a115f-189">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-190"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**\_valor de \_ contexto da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-190"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-191">Define ou recupera um **\_ PTR de DWORD** que contém um ponteiro para o valor de contexto associado a esse identificador [HINTERNET](hinternet-handles-in-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="a115f-191">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="a115f-192">O valor armazenado no buffer é usado e o sinalizador de opção de **\_ valor de \_ contexto \_ de opção WinHTTP** recebe um novo valor.</span><span class="sxs-lookup"><span data-stu-id="a115f-192">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-193"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**\_DEScompactação da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-193"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-194">Define um DWORD de sinalizadores que determinam se o WinHTTP irá descompactar automaticamente os corpos de resposta com codificações de conteúdo compactadas.</span><span class="sxs-lookup"><span data-stu-id="a115f-194">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="a115f-195">O WinHTTP também definirá um cabeçalho de Accept-Encoding apropriado, substituindo qualquer um fornecido pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="a115f-195">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="a115f-196">Os valores com suporte são:</span><span class="sxs-lookup"><span data-stu-id="a115f-196">Supported values are:</span></span>

| <span data-ttu-id="a115f-197">Termo</span><span class="sxs-lookup"><span data-stu-id="a115f-197">Term</span></span> | <span data-ttu-id="a115f-198">Descrição</span><span class="sxs-lookup"><span data-stu-id="a115f-198">Description</span></span> |
|-|-|
| <span data-ttu-id="a115f-199"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_sinalizador de DEScompactação de WinHTTP \_ \_ gzip</span><span class="sxs-lookup"><span data-stu-id="a115f-199"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="a115f-200">Descompactar conteúdo-codificação: respostas gzip.</span><span class="sxs-lookup"><span data-stu-id="a115f-200">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="a115f-201"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>SINALIZADOR DE \_ DESCOMPACTAÇÃO \_ \_ WINHTTP DEFLATE</span><span class="sxs-lookup"><span data-stu-id="a115f-201"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="a115f-202">Descompactar Codificação de Conteúdo: respostas defladas.</span><span class="sxs-lookup"><span data-stu-id="a115f-202">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="a115f-203"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>SINALIZADOR DE \_ DESCOMPACTAÇÃO WINHTTP \_ \_ ALL</span><span class="sxs-lookup"><span data-stu-id="a115f-203"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="a115f-204">Descompacte as respostas com qualquer codificação de conteúdo com suporte.</span><span class="sxs-lookup"><span data-stu-id="a115f-204">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="a115f-205">Por padrão, o WinHTTP fornecerá respostas compactadas ao chamador sem modificações.</span><span class="sxs-lookup"><span data-stu-id="a115f-205">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-206"><span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**OPÇÃO WINHTTP \_ \_ DESABILITAR \_ A CRIAÇÃO DE CADEIA \_ DE \_ CERTIFICADOS**</span><span class="sxs-lookup"><span data-stu-id="a115f-206"><span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**WINHTTP\_OPTION\_DISABLE\_CERT\_CHAIN\_BUILDING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="a115f-207">Definir essa opção em um alça de sessão winHttp permite habilitar/desabilitar se a cadeia de certificados do servidor é criada.</span><span class="sxs-lookup"><span data-stu-id="a115f-207">Setting this option on a WinHttp session handle allows you to enable/disable whether the server certificate chain is built.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-208"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**RECURSO DESABILITAR OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-208"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-209">Define um valor inteiro longo sem sinal que especifica quais recursos estão desabilitados com um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a115f-209">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="a115f-210">Esteja ciente de que esse recurso só deve ser passado para [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) em alças de solicitação depois que o handle de solicitação é criado com [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)e antes que a solicitação seja enviada com [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="a115f-210">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="a115f-211">Termo</span><span class="sxs-lookup"><span data-stu-id="a115f-211">Term</span></span> | <span data-ttu-id="a115f-212">Descrição</span><span class="sxs-lookup"><span data-stu-id="a115f-212">Description</span></span> |
|-|-|
| <span data-ttu-id="a115f-213"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>DESABILITAR AUTENTICAÇÃO DO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-213"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="a115f-214">A autenticação automática está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="a115f-214">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="a115f-215"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>DESABILITAR COOKIES WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-215"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="a115f-216">A adição automática de headers de cookie às solicitações está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="a115f-216">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="a115f-217">Além disso, os cookies retornados não são adicionados automaticamente ao banco de dados de cookie.</span><span class="sxs-lookup"><span data-stu-id="a115f-217">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="a115f-218">Desabilitar cookies pode resultar em baixo desempenho para autenticação do Passport.</span><span class="sxs-lookup"><span data-stu-id="a115f-218">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="a115f-219"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE</span><span class="sxs-lookup"><span data-stu-id="a115f-219"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="a115f-220">Desabilita a semântica keep alive para a conexão.</span><span class="sxs-lookup"><span data-stu-id="a115f-220">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="a115f-221">A semântica keep alive é necessária para MSN, NTLM e outros tipos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="a115f-221">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="a115f-222"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>DESABILITAR \_ REDIRECIONAMENTOS DO WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-222"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="a115f-223">O redirecionamento automático é desabilitado ao enviar solicitações [**com WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="a115f-223">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="a115f-224">Se o redirecionamento automático estiver desabilitado, um aplicativo deverá registrar uma função de retorno de chamada para que a autenticação do Passport seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a115f-224">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a115f-225"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**OPÇÃO WINHTTP \_ \_ DESABILITAR \_ \_ FALLBACK DE \_ PROTOCOLO SEGURO**</span><span class="sxs-lookup"><span data-stu-id="a115f-225"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-226">Impede que o WinHTTP repetir uma conexão com uma versão inferior do protocolo de segurança quando a negociação de protocolo inicial falhar.</span><span class="sxs-lookup"><span data-stu-id="a115f-226">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-227"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**OPÇÃO WINHTTP \_ \_ DESABILITAR \_ FILA DE \_ FLUXO**</span><span class="sxs-lookup"><span data-stu-id="a115f-227"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-228">Permite que novas solicitações abram uma conexão HTTP/2 adicional quando o limite máximo de fluxo simultâneo for atingido, em vez de aguardar o próximo fluxo disponível em uma conexão existente.</span><span class="sxs-lookup"><span data-stu-id="a115f-228">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-229"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**RECURSO \_ HABILITAR OPÇÃO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-229"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-230">Define um valor inteiro longo sem sinal que especifica os recursos atualmente habilitados.</span><span class="sxs-lookup"><span data-stu-id="a115f-230">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="a115f-231">Pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a115f-231">Can be one of the following values.</span></span>

| <span data-ttu-id="a115f-232">Termo</span><span class="sxs-lookup"><span data-stu-id="a115f-232">Term</span></span> | <span data-ttu-id="a115f-233">Descrição</span><span class="sxs-lookup"><span data-stu-id="a115f-233">Description</span></span> |
|-|-|
| <span data-ttu-id="a115f-234"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION</span><span class="sxs-lookup"><span data-stu-id="a115f-234"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="a115f-235">Se habilitada, o WinHTTP reverte temporariamente a representação do cliente durante as operações de autenticação de certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="a115f-235">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="a115f-236">Esse valor pode ser definido somente no alça de sessão.</span><span class="sxs-lookup"><span data-stu-id="a115f-236">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="a115f-237"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ \_ HABILITAR \_ REVOGAÇÃO DE SSL</span><span class="sxs-lookup"><span data-stu-id="a115f-237"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="a115f-238">Se habilitada, o WinHTTP permite a revogação de SSL.</span><span class="sxs-lookup"><span data-stu-id="a115f-238">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="a115f-239">Esse valor pode ser definido somente no alça de solicitação.</span><span class="sxs-lookup"><span data-stu-id="a115f-239">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-240"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**OPÇÃO WINHTTP \_ \_ HABILITAR \_ PROTOCOLO HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-240"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-241">Define uma máscara de bits DWORD de versões HTTP avançadas aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="a115f-241">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="a115f-242">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="a115f-242">Possible values are:</span></span>

| <span data-ttu-id="a115f-243">Termo</span><span class="sxs-lookup"><span data-stu-id="a115f-243">Term</span></span> | <span data-ttu-id="a115f-244">Descrição</span><span class="sxs-lookup"><span data-stu-id="a115f-244">Description</span></span> |
|-|-|
| <span data-ttu-id="a115f-245"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>SINALIZADOR DE PROTOCOLO WINHTTP \_ \_ \_ HTTP2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="a115f-245"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="a115f-246">Habilita HTTP/2 para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a115f-246">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="a115f-247">Nenhum (0x0)</span><span class="sxs-lookup"><span data-stu-id="a115f-247">None (0x0)</span></span> | <span data-ttu-id="a115f-248">Restringe a solicitação a HTTP/1.1 e anterior.</span><span class="sxs-lookup"><span data-stu-id="a115f-248">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="a115f-249">As versões herdadas do HTTP (1.1 e anteriores) não podem ser desabilitadas usando essa opção.</span><span class="sxs-lookup"><span data-stu-id="a115f-249">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="a115f-250">O padrão é 0x0.</span><span class="sxs-lookup"><span data-stu-id="a115f-250">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-251"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**OPÇÃO WINHTTP \_ ENABLE \_ \_ HTTP2 \_ PLUS CLIENT \_ \_ CERT**</span><span class="sxs-lookup"><span data-stu-id="a115f-251"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="a115f-252">Essa opção pode ser definida em um handle de sessão WinHttp para permitir que o WinHttp use o contexto de certificado do cliente fornecido pelo chamador quando HTTP/2 estiver sendo usado.</span><span class="sxs-lookup"><span data-stu-id="a115f-252">This option can be set on a WinHttp session handle to allow WinHttp to use the caller-provided client certificate context when HTTP/2 is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-253"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**OPÇÃO WINHTTP \_ \_ ENABLETRACING**</span><span class="sxs-lookup"><span data-stu-id="a115f-253"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-254">Define um **valor BOOL** que especifica se o rastreamento está habilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="a115f-254">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="a115f-255">Para obter mais informações sobre o recurso de rastreamento no WinHTTP, consulte [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="a115f-255">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="a115f-256">Essa opção só pode ser definida em um handle  **HINTERNET NULL.**</span><span class="sxs-lookup"><span data-stu-id="a115f-256">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="a115f-257"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**CODIFICAR EXTRA DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-257"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-258">Habilita a codificação de porcentagem de URL para caminho e cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="a115f-258">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="a115f-259">Como alternativa, você pode codificar por porcentagem antes de chamar WinHttp.</span><span class="sxs-lookup"><span data-stu-id="a115f-259">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="a115f-260"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP \_ OPTION \_ EXPIRE \_ CONNECTION**</span><span class="sxs-lookup"><span data-stu-id="a115f-260"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-261">Essa opção só pode ser definida em um handle de solicitação que ainda esteja ativo (envio ou recebimento).</span><span class="sxs-lookup"><span data-stu-id="a115f-261">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="a115f-262">Definir essa opção dirá ao WinHttp para parar de atender às solicitações na conexão associada ao handle de solicitação passado.</span><span class="sxs-lookup"><span data-stu-id="a115f-262">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="a115f-263">A conexão será fechada depois que o lidar com a solicitação com a qual essa opção é chamada for concluída.</span><span class="sxs-lookup"><span data-stu-id="a115f-263">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="a115f-264">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a115f-264">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-265"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**ERRO ESTENDIDO DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-265"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-266">Recupera um valor inteiro longo sem sinal que contém um código de erro do Microsoft Windows Sockets mapeado para as mensagens de erro ERROR WINHTTP retornadas pela última vez neste \_ \_ \* contexto de thread.</span><span class="sxs-lookup"><span data-stu-id="a115f-266">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="a115f-267">Você pode passar **NULL** como o valor do handle.</span><span class="sxs-lookup"><span data-stu-id="a115f-267">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-268"><span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**OPÇÃO WINHTTP \_ \_ PRIMEIRA CONEXÃO \_ \_ DISPONÍVEL**</span><span class="sxs-lookup"><span data-stu-id="a115f-268"><span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**WINHTTP\_OPTION\_FIRST\_AVAILABLE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="a115f-269">Por padrão, quando WinHttp envia uma solicitação, se não houver conexões disponíveis para atender à solicitação, o WinHttp tentará estabelecer uma nova conexão e a solicitação será vinculada a essa nova conexão.</span><span class="sxs-lookup"><span data-stu-id="a115f-269">By default, when WinHttp sends a request, if there are no available connections to serve the request, WinHttp will attempt to establish a new connection, and the request will be bound to this new connection.</span></span> <span data-ttu-id="a115f-270">Quando você definir essa opção, essa solicitação será atendida na primeira conexão que se tornar disponível e não necessariamente aquela que está sendo estabelecida.</span><span class="sxs-lookup"><span data-stu-id="a115f-270">When you set this option, such a request will instead be served on the first connection that becomes available, and not necessarily the one being established.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-271"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**CREDS DE \_ \_ PROXY GLOBAL DA \_ OPÇÃO WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-271"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-272">Leva um ponteiro para uma [**estrutura WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) com o *parâmetro de função hInternet* definido como **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a115f-272">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="a115f-273">Essa opção requer a chave do Registro **HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp.**</span><span class="sxs-lookup"><span data-stu-id="a115f-273">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="a115f-274">Se essa chave do Registro não estiver definida, WinHTTP retornará o **erro \_ ERRO WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="a115f-274">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="a115f-275">Essa chave do Registro não está presente por padrão.</span><span class="sxs-lookup"><span data-stu-id="a115f-275">This registry key is not present by default.</span></span> <span data-ttu-id="a115f-276">Quando estiver definido, o WinINet enviará credenciais para WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a115f-276">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="a115f-277">Sempre que o WinHttp receber um desafio de autenticação e se não houver credenciais definidas no alçamento atual, ele usará as credenciais fornecidas pelo WinINet.</span><span class="sxs-lookup"><span data-stu-id="a115f-277">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="a115f-278">Para compartilhar credenciais de servidor, além de credenciais de proxy, os usuários precisam definir **WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** .</span><span class="sxs-lookup"><span data-stu-id="a115f-278">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-279"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**CREDS DE SERVIDOR GLOBAL DA OPÇÃO WINHTTP \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-279"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-280">Leva um ponteiro para uma [**estrutura WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) com o *parâmetro de função hInternet* definido como **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a115f-280">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="a115f-281">Essa opção requer a chave do Registro **HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp.**</span><span class="sxs-lookup"><span data-stu-id="a115f-281">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="a115f-282">Se essa chave do Registro não estiver definida, WinHTTP retornará o **erro \_ ERRO WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="a115f-282">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="a115f-283">Essa chave do Registro não está presente por padrão.</span><span class="sxs-lookup"><span data-stu-id="a115f-283">This registry key is not present by default.</span></span> <span data-ttu-id="a115f-284">Quando estiver definido, o WinINet enviará credenciais para WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a115f-284">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="a115f-285">Sempre que o WinHttp receber um desafio de autenticação e se não houver credenciais definidas no alçamento atual, ele usará as credenciais fornecidas pelo WinINet.</span><span class="sxs-lookup"><span data-stu-id="a115f-285">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="a115f-286">Para compartilhar credenciais de servidor, além de credenciais de proxy, os usuários precisam definir **WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** .</span><span class="sxs-lookup"><span data-stu-id="a115f-286">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-287"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**TIPO DE \_ IDENTIFICADOR DE OPÇÃO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-287"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-288">Recupera um valor inteiro longo sem sinal que contém o tipo do identificador [HINTERNET](hinternet-handles-in-winhttp.md) passado.</span><span class="sxs-lookup"><span data-stu-id="a115f-288">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="a115f-289">O valor de retorno pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="a115f-289">The return value can be one of the following:</span></span>

| <span data-ttu-id="a115f-290">Termo</span><span class="sxs-lookup"><span data-stu-id="a115f-290">Term</span></span> | <span data-ttu-id="a115f-291">Descrição</span><span class="sxs-lookup"><span data-stu-id="a115f-291">Description</span></span> |
|-|-|
| <span data-ttu-id="a115f-292"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>TIPO DE IDENTIFICADOR WINHTTP \_ \_ \_ CONNECT</span><span class="sxs-lookup"><span data-stu-id="a115f-292"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="a115f-293">O handle é um alça de conexão.</span><span class="sxs-lookup"><span data-stu-id="a115f-293">The handle is a connection handle.</span></span> |
| <span data-ttu-id="a115f-294"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>SOLICITAÇÃO DE TIPO \_ DE \_ IDENTIFICADOR WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-294"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="a115f-295">O handle é um alça de solicitação.</span><span class="sxs-lookup"><span data-stu-id="a115f-295">The handle is a request handle.</span></span> |
| <span data-ttu-id="a115f-296"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>SESSÃO DE TIPO \_ DE \_ IDENTIFICADOR WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-296"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="a115f-297">O handle é um alça de sessão.</span><span class="sxs-lookup"><span data-stu-id="a115f-297">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a115f-298"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP \_ OPTION \_ HTTP \_ PROTOCOL \_ REQUIRED**</span><span class="sxs-lookup"><span data-stu-id="a115f-298"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-299">Impede que versões de protocolo diferentes daquelas habilitadas por **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL** seja usada para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a115f-299">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-300"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP \_ OPTION \_ HTTP \_ PROTOCOL \_ USED**</span><span class="sxs-lookup"><span data-stu-id="a115f-300"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-301">Obtém um DWORD que indica qual versão HTTP avançada foi usada em uma determinada solicitação.</span><span class="sxs-lookup"><span data-stu-id="a115f-301">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="a115f-302">Para obter uma lista de valores possíveis, consulte a **\_ opção WinHTTP \_ Enable \_ http \_ Protocol**.</span><span class="sxs-lookup"><span data-stu-id="a115f-302">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-303"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_versão de \_ http da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-303"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-304">Define ou recupera uma estrutura de [**\_ \_ informações de versão http**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) que contém a versão http com suporte.</span><span class="sxs-lookup"><span data-stu-id="a115f-304">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="a115f-305">Essa é uma opção de todo o processo; Use **NULL** para o identificador.</span><span class="sxs-lookup"><span data-stu-id="a115f-305">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-306"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**\_Opção WinHTTP \_ HTTP2 \_ KeepAlive**</span><span class="sxs-lookup"><span data-stu-id="a115f-306"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP\_OPTION\_HTTP2\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="a115f-307">Essa opção pode ser definida em um identificador de sessão para que o WinHttp use quadros de PING HTTP/2 como um mecanismo KeepAlive.</span><span class="sxs-lookup"><span data-stu-id="a115f-307">This option can be set on a session handle to have WinHttp use HTTP/2 PING frames as a keepalive mechanism.</span></span> <span data-ttu-id="a115f-308">Os chamadores especificam um tempo limite em milissegundos e, depois que não houver atividade em uma conexão para esse período de tempo limite, o WinHttp começará a enviar quadros de PING HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="a115f-308">Callers specify a timeout in milliseconds, and after there is no activity on a connection for that timeout period, WinHttp will begin to send HTTP/2 PING frames.</span></span> <span data-ttu-id="a115f-309">Os chamadores não podem definir um valor de tempo limite menor que 5000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="a115f-309">Callers cannot set a timeout value less than 5000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-310"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**\_Opção WinHTTP \_ HTTP2 \_ mais \_ codificação de transferência \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-310"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="a115f-311">Essa opção pode ser definida em um identificador de solicitação WinHttp para controlar como o WinHttp se comporta quando uma resposta HTTP/2 contém um cabeçalho "transferência-codificação".</span><span class="sxs-lookup"><span data-stu-id="a115f-311">This option can be set on a WinHttp request handle to control how WinHttp behaves when an HTTP/2 response contains a "Transfer-Encoding" header.</span></span> <span data-ttu-id="a115f-312">Nesse caso, o WinHttp retornará um erro se essa opção for definida como **false**.</span><span class="sxs-lookup"><span data-stu-id="a115f-312">In such a case, WinHttp will return an error if this option is set to **FALSE**.</span></span>


</dt> </dl> </dd> <dt>


<span data-ttu-id="a115f-313"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**\_opção WinHTTP \_ ignorar \_ \_ revogação de certificado \_ offline**</span><span class="sxs-lookup"><span data-stu-id="a115f-313"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-314">Permite conexões seguras para usar certificados de segurança para os quais a lista de certificados revogados não pôde ser baixada.</span><span class="sxs-lookup"><span data-stu-id="a115f-314">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-315"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**\_Opção WinHTTP \_ IPv6 \_ Fast \_ FALLBACK**</span><span class="sxs-lookup"><span data-stu-id="a115f-315"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-316">Habilita o fallback rápido IPv6 (mais feliz olhos) para a conexão.</span><span class="sxs-lookup"><span data-stu-id="a115f-316">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="a115f-317">Esse comportamento é semelhante ao comportamento feliz olhos descrito na [RFC 6555](https://tools.ietf.org/html/rfc6555) para melhorar os tempos de conexão em redes em que o IPv6 não é confiável.</span><span class="sxs-lookup"><span data-stu-id="a115f-317">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="a115f-318">Se os endereços IPv6 e IPv4 forem resolvidos para um determinado host, o WinHttp será iniciado conectando-se ao primeiro endereço IPv6 resolvido com um tempo limite curto (300 MS).</span><span class="sxs-lookup"><span data-stu-id="a115f-318">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="a115f-319">Se essa conexão falhar, o WinHttp tentará se conectar ao primeiro endereço IPv4 resolvido com o tempo limite padrão.</span><span class="sxs-lookup"><span data-stu-id="a115f-319">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="a115f-320">Se a segunda conexão falhar, o WinHttp tentará novamente o primeiro endereço IPv6 resolvido com o tempo limite padrão.</span><span class="sxs-lookup"><span data-stu-id="a115f-320">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="a115f-321">Se a terceira conexão falhar, o WinHttp reverterá para o comportamento padrão de todos os endereços restantes, tentando uma conexão com cada um com o tempo limite padrão até que uma conexão seja estabelecida ou nenhum endereço permaneça.</span><span class="sxs-lookup"><span data-stu-id="a115f-321">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-322"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**a \_ opção WinHTTP \_ é uma resposta de \_ conexão de proxy \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-322"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-323">Obtém se uma resposta de conexão de retorno de proxy pode ou não ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="a115f-323">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-324"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**Opção de WINHTTP \_ \_ Max \_ Conns \_ por \_ servidor de 1 \_ 0 \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-324"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-325">Define ou recupera um valor inteiro longo sem sinal que contém o número máximo de conexões permitidas por servidor HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="a115f-325">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="a115f-326">O valor padrão é **infinito**.</span><span class="sxs-lookup"><span data-stu-id="a115f-326">The default value is **INFINITE**.</span></span>

<span data-ttu-id="a115f-327">**Windows Vista com SP1 e Windows Server 2008:** Este sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a115f-327">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-328"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**opção de WINHTTP \_ \_ Max \_ Conns \_ por \_ servidor**</span><span class="sxs-lookup"><span data-stu-id="a115f-328"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-329">Define ou recupera um valor inteiro longo sem sinal que contém o número máximo de conexões permitidas por servidor.</span><span class="sxs-lookup"><span data-stu-id="a115f-329">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="a115f-330">O valor padrão é **infinito**.</span><span class="sxs-lookup"><span data-stu-id="a115f-330">The default value is **INFINITE**.</span></span>

<span data-ttu-id="a115f-331">Quando essa opção é definida como zero, o WinHTTP define o limite no número de conexões como 2.</span><span class="sxs-lookup"><span data-stu-id="a115f-331">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-332"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**opção WINHTTP máx. de \_ \_ \_ \_ redirecionamentos automáticos de http \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-332"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-333">Define o número máximo de redirecionamentos que o WinHTTP segue; o padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="a115f-333">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="a115f-334">Esse limite impede que sites não autorizados façam a pausa do cliente WinHTTP após um grande número de redirecionamentos.</span><span class="sxs-lookup"><span data-stu-id="a115f-334">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="a115f-335">**Windows XP com SP1 e windows 2000 com SP3:** Este sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a115f-335">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-336"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_máximo de \_ status HTTP da opção WinHTTP \_ \_ \_ continuar**</span><span class="sxs-lookup"><span data-stu-id="a115f-336"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-337">O número máximo de respostas de código de status 100-199 informativas ignoradas antes de retornar o código de status final para o cliente WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a115f-337">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="a115f-338">Os códigos de status informativos 100-199 podem ser enviados pelo servidor antes do código de status final e são descritos na especificação para HTTP/1.1 (para obter mais informações, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span><span class="sxs-lookup"><span data-stu-id="a115f-338">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="a115f-339">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="a115f-339">The default is 10.</span></span>

<span data-ttu-id="a115f-340">**Windows XP com SP1 e windows 2000 com SP3:** Este sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a115f-340">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-341"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**\_tamanho de \_ \_ dreno de resposta máx da opção \_ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-341"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-342">Um limite na quantidade de dados drenados de respostas para reutilizar uma conexão, especificada em bytes.</span><span class="sxs-lookup"><span data-stu-id="a115f-342">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="a115f-343">O padrão é 1MB.</span><span class="sxs-lookup"><span data-stu-id="a115f-343">The default is 1MB.</span></span>

<span data-ttu-id="a115f-344">**Windows XP com SP1 e windows 2000 com SP3:** Este sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a115f-344">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-345"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**\_ \_ tamanho máximo do \_ cabeçalho de resposta da \_ opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-345"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-346">Um conjunto associado no tamanho máximo da parte do cabeçalho da resposta do servidor, especificado em bytes.</span><span class="sxs-lookup"><span data-stu-id="a115f-346">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="a115f-347">Essa ligação protege o cliente de um servidor não autorizado tentando paralisar o cliente enviando uma resposta com uma quantidade infinita de dados de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="a115f-347">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="a115f-348">O valor padrão é 64 KB.</span><span class="sxs-lookup"><span data-stu-id="a115f-348">The default value is 64KB.</span></span>

<span data-ttu-id="a115f-349">**Windows XP com SP1 e windows 2000 com SP3:** Este sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a115f-349">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-350"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**\_ \_ identificador pai da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-350"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-351">Recupera o identificador pai para esse identificador.</span><span class="sxs-lookup"><span data-stu-id="a115f-351">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-352"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**opção WINHTTP de \_ \_ \_ texto de comarcação do Passport \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-352"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-353">Recupera uma cadeia de caracteres que contém o texto de [*comarcação*](glossary.md) fornecido pelo servidor de logon do Passport.</span><span class="sxs-lookup"><span data-stu-id="a115f-353">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="a115f-354">Essa opção deve ser recuperada imediatamente após o servidor de logon responder com um código de status 401.</span><span class="sxs-lookup"><span data-stu-id="a115f-354">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="a115f-355">Um aplicativo deve passar um tamanho de buffer, em bytes, que seja grande o suficiente para manter a cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="a115f-355">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-356"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_URL de \_ \_ comarcação do passaporte da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-356"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-357">Recupera uma cadeia de caracteres que contém uma URL para um gráfico de [*comarcação*](glossary.md) fornecido pelo servidor de logon do Passport.</span><span class="sxs-lookup"><span data-stu-id="a115f-357">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="a115f-358">Essa opção deve ser recuperada imediatamente após o servidor de logon responder com um código de status 401.</span><span class="sxs-lookup"><span data-stu-id="a115f-358">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="a115f-359">Um aplicativo deve passar um tamanho de buffer, em bytes, que seja grande o suficiente para manter a cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="a115f-359">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-360"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_opção WinHTTP \_ URL de retorno do Passport \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-360"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-361">Define uma opção somente leitura em um identificador de solicitação que recupera a URL de retorno do Passport.</span><span class="sxs-lookup"><span data-stu-id="a115f-361">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-362"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**opção WINHTTP sair do \_ \_ Passport \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-362"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-363">Define a opção em um identificador de sessão para sair de quaisquer logons do Passport.</span><span class="sxs-lookup"><span data-stu-id="a115f-363">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="a115f-364">Um aplicativo deve passar na URL de retorno do Passport que foi recuperada com a **\_ opção WinHTTP URL de \_ \_ retorno \_ do Passport**.</span><span class="sxs-lookup"><span data-stu-id="a115f-364">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="a115f-365">Todos os cookies relacionados à URL de retorno são apagados.</span><span class="sxs-lookup"><span data-stu-id="a115f-365">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-366"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_senha da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-366"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-367">Define ou recupera um valor de cadeia de caracteres que contém a senha associada a um identificador de solicitação.</span><span class="sxs-lookup"><span data-stu-id="a115f-367">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-368"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_proxy de opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-368"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-369">Define ou recupera uma estrutura de [**\_ \_ informações de proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contém os dados de proxy em um identificador de sessão existente ou identificador de solicitação.</span><span class="sxs-lookup"><span data-stu-id="a115f-369">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="a115f-370">Ao recuperar dados de proxy, um aplicativo deve liberar as cadeias de caracteres **lpszProxy** e **lpszProxyBypass** contidas nessa estrutura (se elas não forem **nulas**) usando a função [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="a115f-370">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="a115f-371">Um aplicativo pode consultar os dados do proxy global (o proxy padrão) passando um identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="a115f-371">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-372"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_senha do \_ proxy da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-372"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-373">Define ou recupera um valor de cadeia de caracteres que contém a senha usada para acessar o proxy.</span><span class="sxs-lookup"><span data-stu-id="a115f-373">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-374"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**SPN de proxy de opção de WINHTTP \_ \_ \_ \_ usado**</span><span class="sxs-lookup"><span data-stu-id="a115f-374"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-375">Obtém o nome da entidade de segurança do servidor proxy que o WinHTTP forneceu ao SSPI durante a autenticação.</span><span class="sxs-lookup"><span data-stu-id="a115f-375">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="a115f-376">Esse valor de cadeia de caracteres é usefor passando para [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) após uma falha de autenticação.</span><span class="sxs-lookup"><span data-stu-id="a115f-376">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-377"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_nome de \_ usuário do proxy de opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-377"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-378">Define ou recupera um valor de cadeia de caracteres que contém o nome de usuário usado para acessar o proxy.</span><span class="sxs-lookup"><span data-stu-id="a115f-378">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-379"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_tamanho do \_ buffer de leitura da opção WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-379"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-380">Esta opção foi preterida; Ele não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="a115f-380">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-381"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**a \_ opção \_ WinHTTP \_ recebe \_ resposta de conexão proxy \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-381"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-382">Define se a entidade de resposta de proxy pode ou não ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="a115f-382">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="a115f-383">Essa opção está desabilitada por padrão.</span><span class="sxs-lookup"><span data-stu-id="a115f-383">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-384"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**a \_ opção \_ WinHTTP \_ recebe \_ tempo limite de resposta**</span><span class="sxs-lookup"><span data-stu-id="a115f-384"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-385">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos, para aguardar a recepção de todos os cabeçalhos de resposta a uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="a115f-385">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="a115f-386">Se o WinHTTP não receber todos os cabeçalhos dentro desse período de tempo limite, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="a115f-386">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="a115f-387">O valor de tempo limite padrão é 90 segundos.</span><span class="sxs-lookup"><span data-stu-id="a115f-387">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="a115f-388">Esse tempo limite é verificado somente quando os dados são recebidos do soquete.</span><span class="sxs-lookup"><span data-stu-id="a115f-388">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="a115f-389">Como resultado, quando o tempo limite expira, o aplicativo cliente não é notificado até que mais dados cheguem do servidor.</span><span class="sxs-lookup"><span data-stu-id="a115f-389">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="a115f-390">Se nenhum dado chega do servidor, o atraso entre a expiração do tempo limite e a notificação do aplicativo cliente pode ser tão grande quanto o valor de tempo limite definido usando o parâmetro *dwReceiveTimeout* da função [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) .</span><span class="sxs-lookup"><span data-stu-id="a115f-390">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-391"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_ \_ tempo limite de recebimento da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-391"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-392">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos, para receber uma resposta parcial a uma solicitação ou ler alguns dados.</span><span class="sxs-lookup"><span data-stu-id="a115f-392">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="a115f-393">Se a resposta demorar mais do que esse valor de tempo limite, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="a115f-393">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="a115f-394">O valor do tempo limite padrão é de 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="a115f-394">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-395"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**\_política de \_ redirecionamento de opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-395"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-396">Define o comportamento do WinHTTP em relação ao tratamento de um código de status de redirecionamento HTTP 30 vezes.</span><span class="sxs-lookup"><span data-stu-id="a115f-396">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="a115f-397">Essa opção pode ser definida em uma sessão ou identificador de solicitação para um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="a115f-397">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="a115f-398">Termo</span><span class="sxs-lookup"><span data-stu-id="a115f-398">Term</span></span> | <span data-ttu-id="a115f-399">Descrição</span><span class="sxs-lookup"><span data-stu-id="a115f-399">Description</span></span> |
|-|-|
| <span data-ttu-id="a115f-400"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>\_política de \_ redirecionamento de opção de WinHTTP \_ \_ sempre</span><span class="sxs-lookup"><span data-stu-id="a115f-400"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="a115f-401">Todos os redirecionamentos são seguidos automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a115f-401">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="a115f-402"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>A POLÍTICA DE REDIRECIONAMENTO DE OPÇÃO WINHTTP \_ \_ NÃO PERMITE \_ \_ \_ HTTPS PARA \_ \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="a115f-402"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="a115f-403">Todos os redirecionamentos são seguidos, exceto aqueles originados de uma URL segura (https) para uma URL não segura (http).</span><span class="sxs-lookup"><span data-stu-id="a115f-403">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="a115f-404">Essa é a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="a115f-404">This is the default setting.</span></span> |
| <span data-ttu-id="a115f-405"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>POLÍTICA DE REDIRECIONAMENTO DE OPÇÃO WINHTTP \_ \_ \_ \_ NUNCA</span><span class="sxs-lookup"><span data-stu-id="a115f-405"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="a115f-406">Os redirecionamentos nunca são seguidos.</span><span class="sxs-lookup"><span data-stu-id="a115f-406">Redirects are never followed.</span></span> <span data-ttu-id="a115f-407">O status 30x é retornado ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a115f-407">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-408"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**OPÇÃO WINHTTP \_ REJEITAR \_ \_ USERPWD \_ NA \_ URL**</span><span class="sxs-lookup"><span data-stu-id="a115f-408"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-409">Rejeita URLs que contêm um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="a115f-409">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="a115f-410">Essa opção também rejeita URLs que contêm a semântica *username:password,* mesmo se nenhum nome de usuário ou senha for especificado.</span><span class="sxs-lookup"><span data-stu-id="a115f-410">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="a115f-411">Por exemplo, " u:p@hostname ", " ", " " e " " seriam :@hostname u:@hostname :p@hostname sinalizados como inválidos.</span><span class="sxs-lookup"><span data-stu-id="a115f-411">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="a115f-412">Se uma URL inválida for passada para a função, ela [retornará ERROR \_ WINHTTP \_ INVALID \_ URL](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a115f-412">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="a115f-413">Essa opção é desativada por padrão.</span><span class="sxs-lookup"><span data-stu-id="a115f-413">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-414"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**PRIORIDADE DE \_ SOLICITAÇÃO DE OPÇÃO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-414"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-415">Essa opção foi preterida; ele não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="a115f-415">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-416"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**ESTATÍSTICAS DE \_ SOLICITAÇÃO DE OPÇÃO \_ WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-416"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-417">Retreives estatísticas para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a115f-417">Retreives statistics for the request.</span></span>  <span data-ttu-id="a115f-418">Para ver uma lista das estatísticas disponíveis, consulte [**ESTATÍSTICAS DE SOLICITAÇÃO \_ \_ WINHTTP.**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)</span><span class="sxs-lookup"><span data-stu-id="a115f-418">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-419"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**TEMPOS DE \_ SOLICITAÇÃO DA OPÇÃO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-419"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-420">Retreive informações de tempo para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a115f-420">Retreives timing information for the request.</span></span> <span data-ttu-id="a115f-421">Para ver uma lista dos tempos disponíveis, consulte [**TEMPOS DE \_ SOLICITAÇÃO \_ WINHTTP.**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)</span><span class="sxs-lookup"><span data-stu-id="a115f-421">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-422"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**OPÇÃO WINHTTP \_ EXIGIR \_ FIM DO \_ \_ FLUXO**</span><span class="sxs-lookup"><span data-stu-id="a115f-422"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP\_OPTION\_REQUIRE\_STREAM\_END**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="a115f-423">Essa opção informa ao WinHttp para ignorar os headers de resposta "Content-Length" e continuar recebendo em um fluxo até que o sinalizador END_STREAM seja recebido.</span><span class="sxs-lookup"><span data-stu-id="a115f-423">This option tells WinHttp to ignore "Content-Length" response headers, and continue receiving on a stream until the END_STREAM flag is received.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-424"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP \_ OPTION \_ RESOLUTION \_ HOSTNAME**</span><span class="sxs-lookup"><span data-stu-id="a115f-424"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="a115f-425">Essa opção pode ser definida em um handle de solicitação WinHttp antes de ser enviada.</span><span class="sxs-lookup"><span data-stu-id="a115f-425">This option can be set on a WinHttp request handle before it has been sent.</span></span> <span data-ttu-id="a115f-426">Se definido, o WinHttp usará a cadeia de caracteres fornecida pelo chamador como o nome do host para a resolução dns.</span><span class="sxs-lookup"><span data-stu-id="a115f-426">If set, WinHttp will use the caller-provided string as the hostname for DNS resolution.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-427"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP \_ OPTION \_ RESOLVE \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="a115f-427"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-428">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo-máximo, em milissegundos, para resolver um nome de host.</span><span class="sxs-lookup"><span data-stu-id="a115f-428">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="a115f-429">O valor de tempo-máximo padrão é **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="a115f-429">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="a115f-430">Se um valor não padrão for especificado, haverá uma sobrecarga de uma criação de thread por resolução de nome.</span><span class="sxs-lookup"><span data-stu-id="a115f-430">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-431"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**PROTOCOLOS SEGUROS DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-431"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-432">Define um valor inteiro longo sem sinal que especifica quais protocolos seguros são aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="a115f-432">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="a115f-433">Por padrão, somente SSL3 e TLS1 estão habilitados no Windows 7 e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a115f-433">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="a115f-434">Por padrão, somente SSL3, TLS1.0, TLS1.1 e TLS1.2 são habilitados em Windows 8.1 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a115f-434">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="a115f-435">O valor pode ser uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a115f-435">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="a115f-436">Termo</span><span class="sxs-lookup"><span data-stu-id="a115f-436">Term</span></span> | <span data-ttu-id="a115f-437">Descrição</span><span class="sxs-lookup"><span data-stu-id="a115f-437">Description</span></span> |
|-|-|
| <span data-ttu-id="a115f-438"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>PROTOCOLO DE SEGURANÇA DO SINALIZADOR WINHTTP \_ \_ \_ \_ TODOS</span><span class="sxs-lookup"><span data-stu-id="a115f-438"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="a115f-439">Os protocolos protocolo SSL (SSL) 2.0, SSL 3.0 e TLS (Transport Layer Security) 1.0 podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="a115f-439">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="a115f-440"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>SINALIZADOR WINHTTP \_ \_ SECURE PROTOCOL \_ \_ SSL2</span><span class="sxs-lookup"><span data-stu-id="a115f-440"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="a115f-441">O protocolo SSL 2.0 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="a115f-441">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="a115f-442"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>PROTOCOLO \_ \_ \_ SSL3 DO SINALIZADOR \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a115f-442"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="a115f-443">O protocolo SSL 3.0 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="a115f-443">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="a115f-444"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>PROTOCOLO SEGURO DE SINALIZADOR \_ \_ WINHTTP \_ \_ TLS1</span><span class="sxs-lookup"><span data-stu-id="a115f-444"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="a115f-445">O protocolo TLS 1.0 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="a115f-445">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="a115f-446"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>PROTOCOLO SEGURO DE SINALIZADOR WINHTTP \_ \_ \_ \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a115f-446"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="a115f-447">O protocolo TLS 1.1 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="a115f-447">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="a115f-448"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>PROTOCOLO SEGURO DE SINALIZADOR WINHTTP \_ \_ \_ \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="a115f-448"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="a115f-449">O protocolo TLS 1.2 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="a115f-449">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a115f-450"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**STRUCT DO CERTIFICADO \_ \_ DE SEGURANÇA DA \_ OPÇÃO WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-450"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-451">Recupera o certificado de um servidor SSL/TLS na estrutura [**WINHTTP \_ CERTIFICATE \_ INFO.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)</span><span class="sxs-lookup"><span data-stu-id="a115f-451">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="a115f-452">O aplicativo deve liberar **os membros lpszSubjectInfo** e **lpszIssuerInfo** com [**LocalFree.**](/windows/desktop/api/winbase/nf-winbase-localfree)</span><span class="sxs-lookup"><span data-stu-id="a115f-452">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-453"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**SINALIZADORES DE SEGURANÇA DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-453"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-454">Define ou recupera um valor inteiro longo sem sinal que contém os sinalizadores de segurança para um handle.</span><span class="sxs-lookup"><span data-stu-id="a115f-454">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="a115f-455">Pode ser uma combinação desses valores:</span><span class="sxs-lookup"><span data-stu-id="a115f-455">It can be a combination of these values:</span></span>

| <span data-ttu-id="a115f-456">Termo</span><span class="sxs-lookup"><span data-stu-id="a115f-456">Term</span></span> | <span data-ttu-id="a115f-457">Descrição</span><span class="sxs-lookup"><span data-stu-id="a115f-457">Description</span></span> |
|-|-|
| <span data-ttu-id="a115f-458"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SINALIZADOR \_ DE SEGURANÇA IGNORAR CERTIFICADO CN \_ \_ \_ \_ INVÁLIDO</span><span class="sxs-lookup"><span data-stu-id="a115f-458"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="a115f-459">Permite um nome comum inválido em um certificado; ou seja, o nome do servidor especificado pelo aplicativo não corresponderá ao nome comum no certificado.</span><span class="sxs-lookup"><span data-stu-id="a115f-459">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="a115f-460">Se esse sinalizador for definido, o aplicativo não receberá um retorno de chamada **WINHTTP \_ CALLBACK \_ STATUS FLAG CERT CN \_ \_ \_ \_ INVALID.**</span><span class="sxs-lookup"><span data-stu-id="a115f-460">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="a115f-461"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SINALIZADOR DE \_ SEGURANÇA IGNORAR DATA DE CERTIFICADO \_ \_ \_ \_ INVÁLIDA</span><span class="sxs-lookup"><span data-stu-id="a115f-461"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="a115f-462">Permite uma data de certificado inválida, ou seja, um certificado expirado ou ainda não efetivo.</span><span class="sxs-lookup"><span data-stu-id="a115f-462">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="a115f-463">Se esse sinalizador for definido, o aplicativo não receberá um retorno de chamada **WINHTTP \_ CALLBACK STATUS FLAG \_ CERT \_ DATE \_ \_ \_ INVALID.**</span><span class="sxs-lookup"><span data-stu-id="a115f-463">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="a115f-464"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SINALIZADOR \_ DE SEGURANÇA IGNORAR AC \_ \_ \_ DESCONHECIDA</span><span class="sxs-lookup"><span data-stu-id="a115f-464"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="a115f-465">Permite uma autoridade de certificação inválida.</span><span class="sxs-lookup"><span data-stu-id="a115f-465">Allows an invalid certificate authority.</span></span> <span data-ttu-id="a115f-466">Se esse sinalizador for definido, o aplicativo não receberá um retorno de chamada DE CA INVÁLIDO DO SINALIZADOR DE STATUS DE RETORNO DE CHAMADA **WINHTTP. \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-466">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="a115f-467"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SINALIZADOR DE \_ SEGURANÇA IGNORAR O USO ERRADO DO \_ \_ \_ \_ CERTIFICADO</span><span class="sxs-lookup"><span data-stu-id="a115f-467"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="a115f-468">Permite que a identidade de um servidor seja estabelecida com um certificado não servidor (por exemplo, um certificado do cliente).</span><span class="sxs-lookup"><span data-stu-id="a115f-468">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="a115f-469"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SINALIZADOR DE \_ SEGURANÇA \_ IGNORAR ASSINATURA \_ \_ FRACA</span><span class="sxs-lookup"><span data-stu-id="a115f-469"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="a115f-470">Permite que uma assinatura fraca seja ignorada.</span><span class="sxs-lookup"><span data-stu-id="a115f-470">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="a115f-471">Esse sinalizador está disponível na atualização de rollup para cada sistema operacional, começando com o Windows 7 e o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a115f-471">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="a115f-472"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SINALIZADOR \_ DE \_ SEGURANÇA SEGURO</span><span class="sxs-lookup"><span data-stu-id="a115f-472"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="a115f-473">Usa transferências seguras.</span><span class="sxs-lookup"><span data-stu-id="a115f-473">Uses secure transfers.</span></span> <span data-ttu-id="a115f-474">Isso só é retornado em uma chamada para [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="a115f-474">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="a115f-475"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>MEIO DE \_ FORÇA DO SINALIZADOR DE \_ \_ SEGURANÇA</span><span class="sxs-lookup"><span data-stu-id="a115f-475"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="a115f-476">Usa criptografia média (56 bits).</span><span class="sxs-lookup"><span data-stu-id="a115f-476">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="a115f-477">Isso só é retornado em uma chamada para [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="a115f-477">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="a115f-478"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>FORÇA FORTE \_ DO \_ SINALIZADOR DE \_ SEGURANÇA</span><span class="sxs-lookup"><span data-stu-id="a115f-478"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="a115f-479">Usa criptografia forte (128 bits).</span><span class="sxs-lookup"><span data-stu-id="a115f-479">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="a115f-480">Isso só é retornado em uma chamada para [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="a115f-480">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="a115f-481"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>FORÇA DO \_ SINALIZADOR \_ DE SEGURANÇA \_ FRACA</span><span class="sxs-lookup"><span data-stu-id="a115f-481"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="a115f-482">Usa criptografia fraca (40 bits).</span><span class="sxs-lookup"><span data-stu-id="a115f-482">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="a115f-483">Isso só é retornado em uma chamada para [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="a115f-483">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a115f-484"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**INFORMAÇÕES DE SEGURANÇA DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-484"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-485">Retreive a conexão SChannel e informações de codificação para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="a115f-485">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-486"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**BITNESS \_ DA CHAVE \_ DE SEGURANÇA DA \_ \_ OPÇÃO WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a115f-486"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-487">Recupera um valor inteiro longo sem sinal que contém a força da criptografia da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="a115f-487">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="a115f-488">Um número maior indica criptografia de força de codificação mais forte.</span><span class="sxs-lookup"><span data-stu-id="a115f-488">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-489"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP \_ OPTION \_ SEND \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="a115f-489"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-490">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo-máximo, em milissegundos, para enviar uma solicitação ou gravar alguns dados.</span><span class="sxs-lookup"><span data-stu-id="a115f-490">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="a115f-491">Se o envio da solicitação demorar mais do que o tempo de vida, a operação de envio será cancelada.</span><span class="sxs-lookup"><span data-stu-id="a115f-491">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="a115f-492">O tempo de vida padrão é de 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="a115f-492">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-493"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**CBT DO \_ SERVIDOR DE OPÇÕES \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a115f-493"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-494">Obtém um ponteiro para a estrutura de Vinculações [**SecPkgContext \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) que especifica um CBT (Token de Associação de Canal).</span><span class="sxs-lookup"><span data-stu-id="a115f-494">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="a115f-495">Um Token de Associação de Canal é uma propriedade de um canal de transporte seguro e é usado para vincular um canal de autenticação ao canal de transporte seguro.</span><span class="sxs-lookup"><span data-stu-id="a115f-495">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="a115f-496">Esse token só pode ser obtido por essa opção depois que uma conexão SSL é estabelecida.</span><span class="sxs-lookup"><span data-stu-id="a115f-496">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="a115f-497">Passar essa opção  e um valor nulo para *lpBuffer* para [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) retornarão ERROR INSUFFICIENT BUFFER e o tamanho de byte necessário para o buffer no parâmetro \_ \_ *lpdwBufferLength.*</span><span class="sxs-lookup"><span data-stu-id="a115f-497">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="a115f-498">Esse valor de tamanho de buffer retornado pode ser passado em uma chamada subsequente para consulta para o Token de Associação de Canal.</span><span class="sxs-lookup"><span data-stu-id="a115f-498">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="a115f-499">Essas etapas são necessárias ao lidar com a SOLICITAÇÃO DE STATUS DE RETORNO DE CHAMADA WINHTTP se você quiser modificar os títulos de solicitação com \_ base no Token de Associação de \_ \_ Canal.</span><span class="sxs-lookup"><span data-stu-id="a115f-499">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="a115f-500">Observe que o Windows XP e o Vista não são suportados para modificar os headers de solicitação durante esse retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="a115f-500">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-501"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**CONTEXTO DA CADEIA DE \_ \_ CERTIFICADOS \_ DO SERVIDOR WINHTTP OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-501"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-502">Recupera o contexto da cadeia de certificação do servidor.</span><span class="sxs-lookup"><span data-stu-id="a115f-502">Retrieves the server certification chain context.</span></span> <span data-ttu-id="a115f-503">**WINHTTP \_ OPTION \_ SERVER CERT CHAIN \_ \_ \_ CONTEXT** pode ser passado para obter um ponteiro duplicado para o **CONTEXTO DE \_ CADEIA \_** DE CERTIFICADOs de uma cadeia de certificados de servidor recebida durante uma conexão SSL negociada.</span><span class="sxs-lookup"><span data-stu-id="a115f-503">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="a115f-504">O cliente deve chamar [**CertFreeCertificateContext no**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) ponteiro CONTEXT PCCERT retornado que \_ é preenchido no buffer.</span><span class="sxs-lookup"><span data-stu-id="a115f-504">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-505"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**CONTEXTO DE CERTIFICADO \_ DO \_ SERVIDOR WINHTTP OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-505"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-506">Recupera o contexto de certificação do servidor.</span><span class="sxs-lookup"><span data-stu-id="a115f-506">Retrieves the server certification context.</span></span> <span data-ttu-id="a115f-507">**WINHTTP \_ OPTION \_ SERVER CERT CONTEXT \_ \_ pode** ser passado para obter um ponteiro duplicado para o [**CONTEXTO DE CERTIFICADO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) para um certificado do servidor recebido durante uma conexão SSL negociada.</span><span class="sxs-lookup"><span data-stu-id="a115f-507">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="a115f-508">O cliente deve chamar [**CertFreeCertificateContext no**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) ponteiro CONTEXT PCCERT retornado que \_ é preenchido no buffer.</span><span class="sxs-lookup"><span data-stu-id="a115f-508">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-509"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**SPN DO \_ SERVIDOR DE OPÇÕES \_ \_ WINHTTP \_ USADO**</span><span class="sxs-lookup"><span data-stu-id="a115f-509"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-510">Obtém o nome principal do servidor que o WinHTTP forneceu ao SSPI durante a autenticação.</span><span class="sxs-lookup"><span data-stu-id="a115f-510">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="a115f-511">Esse valor de cadeia de caracteres pode ser passado [**para SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) após uma falha de autenticação.</span><span class="sxs-lookup"><span data-stu-id="a115f-511">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-512"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**SPN DA \_ OPÇÃO \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a115f-512"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-513">Inclui ou remove o número da porta do servidor quando o SPN (nome da entidade de serviço) é criado para autenticação Kerberos ou Negotiate Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a115f-513">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="a115f-514">Esse sinalizador é um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="a115f-514">This flag is one of the following values:</span></span>

| <span data-ttu-id="a115f-515">Termo</span><span class="sxs-lookup"><span data-stu-id="a115f-515">Term</span></span> | <span data-ttu-id="a115f-516">Descrição</span><span class="sxs-lookup"><span data-stu-id="a115f-516">Description</span></span> |
|-|-|
| <span data-ttu-id="a115f-517"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ DESABILITAR \_ A PORTA DO SERVIDOR SPN \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-517"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="a115f-518">Remove o número da porta do servidor.</span><span class="sxs-lookup"><span data-stu-id="a115f-518">Removes the server port number.</span></span> |
| <span data-ttu-id="a115f-519"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ ENABLE \_ SPN \_ SERVER \_ PORT</span><span class="sxs-lookup"><span data-stu-id="a115f-519"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="a115f-520">Inclui o número da porta do servidor.</span><span class="sxs-lookup"><span data-stu-id="a115f-520">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a115f-521"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**CÓDIGO DE ERRO DE FLUXO DE OPÇÃO WINHTTP \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-521"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP\_OPTION\_STREAM\_ERROR\_CODE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="a115f-522">Essa opção pode ser consultada em um handle de solicitação WinHttp e retornará o código de erro indicado por um RST_STREAM quadro recebido em um fluxo HTTP.</span><span class="sxs-lookup"><span data-stu-id="a115f-522">This option can be queried on a WinHttp request handle, and will return the error code indicated by a RST_STREAM frame received on an HTTP stream.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-523"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP \_ OPTION \_ TCP \_ FAST \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="a115f-523"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-524">Habilita o TCP Fast Open para a conexão.</span><span class="sxs-lookup"><span data-stu-id="a115f-524">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-525"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP \_ OPTION \_ TCP \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="a115f-525"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP\_OPTION\_TCP\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-526">Essa opção pode ser definida em um alça de sessão WinHttp para habilitar o comportamento keep alive do TCP no soquete subjacente.</span><span class="sxs-lookup"><span data-stu-id="a115f-526">This option can be set on a WinHttp session handle to enable TCP keep-alive behavior on the underlying socket.</span></span> <span data-ttu-id="a115f-527">Aceita um [**struct \_ tcp keepalive.**](/windows/win32/winsock/sio-keepalive-vals)</span><span class="sxs-lookup"><span data-stu-id="a115f-527">Takes a [**tcp\_keepalive**](/windows/win32/winsock/sio-keepalive-vals) struct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-528"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP \_ OPTION \_ TLS \_ FALSE \_ START**</span><span class="sxs-lookup"><span data-stu-id="a115f-528"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-529">Habilita o Início Falso do TLS para a conexão.</span><span class="sxs-lookup"><span data-stu-id="a115f-529">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-530"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**FALLBACK INSEGURO DO \_ \_ PROTOCOLO TLS \_ \_ DA OPÇÃO WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-530"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-531">Essa opção pode ser definida em um controle de sessão WinHttp para controlar se o fallback para o TLS 1.0 é permitido se houver uma falha de handshake TLS com uma versão de protocolo mais recente.</span><span class="sxs-lookup"><span data-stu-id="a115f-531">This option can be set on a WinHttp session handle to control whether fallback to TLS 1.0 is allowed if there is a TLS handshake failure with a newer protocol version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-532"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**EVENTO DE \_ NOTIFICAÇÃO \_ DE DESCARREGAMENTO DE OPÇÃO \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a115f-532"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-533">Recebe um evento que será definido quando o último retorno de chamada for concluído para uma sessão específica.</span><span class="sxs-lookup"><span data-stu-id="a115f-533">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="a115f-534">Esse sinalizador deve ser usado em um alça de sessão.</span><span class="sxs-lookup"><span data-stu-id="a115f-534">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="a115f-535">O evento não pode ser fechado até que ele tenha sido definido pelo WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a115f-535">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-536"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**ANÁLISE DE TÍTULO NÃO SEGURO DA OPÇÃO WINHTTP \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-536"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-537">Essa opção é reservada para uso interno e não deve ser chamada.</span><span class="sxs-lookup"><span data-stu-id="a115f-537">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-538"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**ATUALIZAÇÃO DA OPÇÃO WINHTTP \_ \_ PARA O \_ \_ SOQUETE DA \_ WEB**</span><span class="sxs-lookup"><span data-stu-id="a115f-538"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-539">Instrui a pilha a iniciar um processo de handshake do WebSocket com [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="a115f-539">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="a115f-540">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a115f-540">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-541"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**URL DA OPÇÃO \_ WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-541"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-542">Recupera um valor de cadeia de caracteres que contém a URL completa de um recurso baixado.</span><span class="sxs-lookup"><span data-stu-id="a115f-542">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="a115f-543">Se a URL original contiver dados extras, como cadeias de caracteres de pesquisa ou âncoras, ou se a chamada tiver sido redirecionada, a URL retornada será diferente da original.</span><span class="sxs-lookup"><span data-stu-id="a115f-543">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="a115f-544">O aplicativo deve passar um buffer, dimensionado em bytes, que é grande o suficiente para manter a URL retornada em caractere largo.</span><span class="sxs-lookup"><span data-stu-id="a115f-544">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-545"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**OPÇÃO WINHTTP \_ \_ USAR CREDENCIAIS DE \_ \_ SERVIDOR GLOBAL \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-545"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-546">Aceita um **BOOL** e pode ser definido apenas como um alça de sessão.</span><span class="sxs-lookup"><span data-stu-id="a115f-546">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="a115f-547">Ele só será propagado para os alças criados a partir do alça de sessão depois que a opção tiver sido definida.</span><span class="sxs-lookup"><span data-stu-id="a115f-547">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="a115f-548">Se **TRUE**, essa opção causará como último recurso o uso de credenciais de servidor global que foram pressionadas do WinInet.</span><span class="sxs-lookup"><span data-stu-id="a115f-548">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="a115f-549">O padrão para essa opção é **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="a115f-549">The default for this option is **FALSE**.</span></span> <span data-ttu-id="a115f-550">Essa opção requer a chave do Registro **HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp.**</span><span class="sxs-lookup"><span data-stu-id="a115f-550">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="a115f-551">Essa chave do Registro não está presente por padrão.</span><span class="sxs-lookup"><span data-stu-id="a115f-551">This registry key is not present by default.</span></span> <span data-ttu-id="a115f-552">Quando estiver definido, o WinINet enviará credenciais para WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a115f-552">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="a115f-553">Sempre que o WinHttp receber um desafio de autenticação e se não houver credenciais definidas no alçamento atual, ele usará as credenciais fornecidas pelo WinINet.</span><span class="sxs-lookup"><span data-stu-id="a115f-553">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-554"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**AGENTE DO USUÁRIO DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-554"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-555">Define ou recupera [](glossary.md) a cadeia de caracteres do agente do usuário em alças fornecidas por [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) e usadas em funções [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) subsequentes, desde que ela não seja substituído por um header adicionado por [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) ou **WinHttpSendRequest.**</span><span class="sxs-lookup"><span data-stu-id="a115f-555">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="a115f-556">Ao recuperar um agente de usuário, o aplicativo deve passar um buffer, dimensionado em bytes, que é grande o suficiente para manter a URL retornada em caractere largo.</span><span class="sxs-lookup"><span data-stu-id="a115f-556">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="a115f-557">Ao definir o agente do usuário, o tamanho do buffer é o comprimento da cadeia de caracteres, em caracteres, mais o **terminador NULL.**</span><span class="sxs-lookup"><span data-stu-id="a115f-557">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-558"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**NOME DE USUÁRIO DA OPÇÃO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-558"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-559">Define ou recupera uma cadeia de caracteres que contém o nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="a115f-559">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-560"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ CLOSE \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="a115f-560"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-561">Define o tempo, em milissegundos, que [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) deve aguardar para concluir o handshake de fechamento.</span><span class="sxs-lookup"><span data-stu-id="a115f-561">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="a115f-562">O padrão é 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="a115f-562">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-563"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ KEEPALIVE \_ INTERVAL**</span><span class="sxs-lookup"><span data-stu-id="a115f-563"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-564">Define o intervalo, em milissegundos, para enviar um pacote keep alive pela conexão.</span><span class="sxs-lookup"><span data-stu-id="a115f-564">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="a115f-565">O intervalo padrão é 30000 (30 segundos).</span><span class="sxs-lookup"><span data-stu-id="a115f-565">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="a115f-566">O intervalo mínimo é 15000 (15 segundos).</span><span class="sxs-lookup"><span data-stu-id="a115f-566">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="a115f-567">O [**uso de WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para definir um valor inferior a 15000 retornará com **ERROR INVALID \_ \_ PARAMETER**.</span><span class="sxs-lookup"><span data-stu-id="a115f-567">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="a115f-568">O valor padrão para **WINHTTP \_ OPTION WEB SOCKET \_ \_ \_ KEEPALIVE \_ INTERVAL** é lido de **HKLM: \\ SOFTWARE Microsoft \\ \\ WebSocket \\ KeepaliveInterval**.</span><span class="sxs-lookup"><span data-stu-id="a115f-568">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="a115f-569">Se um valor não for definido, o valor padrão de 30000 será usado.</span><span class="sxs-lookup"><span data-stu-id="a115f-569">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="a115f-570">Não é possível ter um intervalo keepalive inferior a 15000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="a115f-570">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-571"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ RECEIVE \_ BUFFER \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="a115f-571"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-572">Define ou recupera um DWORD que especifica o tamanho do buffer de recebimento a ser usado em conexões WebSocket.</span><span class="sxs-lookup"><span data-stu-id="a115f-572">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-573"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ SEND \_ BUFFER \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="a115f-573"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-574">Define ou recupera um DWORD que especifica o tamanho do buffer de envio a ser usado em conexões WebSocket.</span><span class="sxs-lookup"><span data-stu-id="a115f-574">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-575"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**CONTAGEM DE \_ \_ THREADS DE TRABALHO DA OPÇÃO \_ WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-575"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-576">Define um valor inteiro longo sem sinal que especifica o número de threads de trabalho que o pool de threads deve usar para preenchimentos assíncronos.</span><span class="sxs-lookup"><span data-stu-id="a115f-576">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="a115f-577">O valor padrão dessa opção é zero, que especifica que o número de threads de trabalho é igual ao número de CPUs no sistema.</span><span class="sxs-lookup"><span data-stu-id="a115f-577">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="a115f-578">Essa opção só pode ser definida em um manipular **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) antes que uma operação assíncrona tenha ocorrido.</span><span class="sxs-lookup"><span data-stu-id="a115f-578">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="a115f-579">Essa opção só pode ser definida uma vez.</span><span class="sxs-lookup"><span data-stu-id="a115f-579">This option can only be set once.</span></span>

<span data-ttu-id="a115f-580">**Windows Server 2008 R2 e Windows 7:** Esse sinalizador está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a115f-580">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a115f-581"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**TAMANHO DO \_ BUFFER DE GRAVAÇÃO DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-581"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a115f-582">Essa opção foi preterida; ele não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="a115f-582">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a115f-583">Comentários</span><span class="sxs-lookup"><span data-stu-id="a115f-583">Remarks</span></span>

<span data-ttu-id="a115f-584">A tabela a seguir lista os sinalizadores de opção especificando quais identificador eles podem agir, se eles podem ser consultados e definidos e o tipo de dados usado.</span><span class="sxs-lookup"><span data-stu-id="a115f-584">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="a115f-585">Um "X" indica que o sinalizador de opção é válido para uso com a função ou o handle, enquanto um "-" especifica que o sinalizador de opção é inválido.</span><span class="sxs-lookup"><span data-stu-id="a115f-585">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="a115f-586">Tentar definir ou consultar um sinalizador de opção em uma versão do Windows em que não há suporte resultará em **ERRO \_ WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="a115f-586">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="a115f-587">Sinalizador de opção e tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a115f-587">Option flag, and data type</span></span> | <span data-ttu-id="a115f-588">Alça de sessão</span><span class="sxs-lookup"><span data-stu-id="a115f-588">Session handle</span></span> | <span data-ttu-id="a115f-589">Alça de solicitação</span><span class="sxs-lookup"><span data-stu-id="a115f-589">Request handle</span></span> | <span data-ttu-id="a115f-590">Opção de consulta</span><span class="sxs-lookup"><span data-stu-id="a115f-590">Query option</span></span> | <span data-ttu-id="a115f-591">Opção Set</span><span class="sxs-lookup"><span data-stu-id="a115f-591">Set option</span></span> | <span data-ttu-id="a115f-592">Versão mínima do Windows</span><span class="sxs-lookup"><span data-stu-id="a115f-592">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="a115f-593">OPÇÃO WINHTTP \_ COM \_ CERTEZA \_ \_ \_ RETORNOS DE CHAMADA SEM BLOQUEIO</span><span class="sxs-lookup"><span data-stu-id="a115f-593">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="a115f-594">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a115f-594">**BOOL**</span></span> | <span data-ttu-id="a115f-595">X</span><span class="sxs-lookup"><span data-stu-id="a115f-595">X</span></span> | \- | \- | <span data-ttu-id="a115f-596">X</span><span class="sxs-lookup"><span data-stu-id="a115f-596">X</span></span> | \- |
| <span data-ttu-id="a115f-597">POLÍTICA DE LOGOM AUTOMÁTICO DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-597">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="a115f-598">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-598">**DWORD**</span></span> | \- | <span data-ttu-id="a115f-599">X</span><span class="sxs-lookup"><span data-stu-id="a115f-599">X</span></span> | \- | <span data-ttu-id="a115f-600">X</span><span class="sxs-lookup"><span data-stu-id="a115f-600">X</span></span> | \- |
| <span data-ttu-id="a115f-601">\_ \_ conexões em segundo plano da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-601">WINHTTP\_OPTION\_BACKGROUND\_CONNECTIONS</span></span><br/><span data-ttu-id="a115f-602">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-602">**DWORD**</span></span> | <span data-ttu-id="a115f-603">X</span><span class="sxs-lookup"><span data-stu-id="a115f-603">X</span></span> | \- | \- | <span data-ttu-id="a115f-604">X</span><span class="sxs-lookup"><span data-stu-id="a115f-604">X</span></span> | <span data-ttu-id="a115f-605">Windows 10 versão 21H1</span><span class="sxs-lookup"><span data-stu-id="a115f-605">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a115f-606">retorno de chamada de \_ opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-606">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="a115f-607">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="a115f-607">**LPVOID**</span></span> | <span data-ttu-id="a115f-608">X</span><span class="sxs-lookup"><span data-stu-id="a115f-608">X</span></span> | <span data-ttu-id="a115f-609">X</span><span class="sxs-lookup"><span data-stu-id="a115f-609">X</span></span> | <span data-ttu-id="a115f-610">X</span><span class="sxs-lookup"><span data-stu-id="a115f-610">X</span></span> | <span data-ttu-id="a115f-611">X</span><span class="sxs-lookup"><span data-stu-id="a115f-611">X</span></span> | \- |
| <span data-ttu-id="a115f-612">\_contexto de \_ certificado de cliente de opção WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-612">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="a115f-613">**contexto do certificado \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-613">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="a115f-614">X</span><span class="sxs-lookup"><span data-stu-id="a115f-614">X</span></span> | \- | <span data-ttu-id="a115f-615">X</span><span class="sxs-lookup"><span data-stu-id="a115f-615">X</span></span> | <span data-ttu-id="a115f-616">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a115f-616">Windows Vista</span></span> |
| <span data-ttu-id="a115f-617">\_opção WinHTTP \_ \_ lista de emissor de certificado de cliente \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-617">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="a115f-618">**SecPkgContext \_ IssuerListInfoEx**</span><span class="sxs-lookup"><span data-stu-id="a115f-618">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="a115f-619">X</span><span class="sxs-lookup"><span data-stu-id="a115f-619">X</span></span> | <span data-ttu-id="a115f-620">X</span><span class="sxs-lookup"><span data-stu-id="a115f-620">X</span></span> | \- | <span data-ttu-id="a115f-621">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a115f-621">Windows Vista</span></span> |
| <span data-ttu-id="a115f-622">página de código da \_ opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-622">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="a115f-623">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-623">**DWORD**</span></span> | <span data-ttu-id="a115f-624">X</span><span class="sxs-lookup"><span data-stu-id="a115f-624">X</span></span> | \- | \- | <span data-ttu-id="a115f-625">X</span><span class="sxs-lookup"><span data-stu-id="a115f-625">X</span></span> | \- |
| <span data-ttu-id="a115f-626">\_opção WinHTTP \_ Configurar \_ autenticação do Passport \_</span><span class="sxs-lookup"><span data-stu-id="a115f-626">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="a115f-627">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-627">**DWORD**</span></span> | <span data-ttu-id="a115f-628">X</span><span class="sxs-lookup"><span data-stu-id="a115f-628">X</span></span> | \- | \- | <span data-ttu-id="a115f-629">X</span><span class="sxs-lookup"><span data-stu-id="a115f-629">X</span></span> | \- |
| <span data-ttu-id="a115f-630">\_ \_ novas tentativas de conexão de opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-630">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="a115f-631">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-631">**DWORD**</span></span> | <span data-ttu-id="a115f-632">X</span><span class="sxs-lookup"><span data-stu-id="a115f-632">X</span></span> | <span data-ttu-id="a115f-633">X</span><span class="sxs-lookup"><span data-stu-id="a115f-633">X</span></span> | <span data-ttu-id="a115f-634">X</span><span class="sxs-lookup"><span data-stu-id="a115f-634">X</span></span> | <span data-ttu-id="a115f-635">X</span><span class="sxs-lookup"><span data-stu-id="a115f-635">X</span></span> | \- |
| <span data-ttu-id="a115f-636">\_ \_ tempo limite de conexão da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-636">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="a115f-637">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-637">**DWORD**</span></span> | <span data-ttu-id="a115f-638">X</span><span class="sxs-lookup"><span data-stu-id="a115f-638">X</span></span> | <span data-ttu-id="a115f-639">X</span><span class="sxs-lookup"><span data-stu-id="a115f-639">X</span></span> | <span data-ttu-id="a115f-640">X</span><span class="sxs-lookup"><span data-stu-id="a115f-640">X</span></span> | <span data-ttu-id="a115f-641">X</span><span class="sxs-lookup"><span data-stu-id="a115f-641">X</span></span> | \- |
| <span data-ttu-id="a115f-642">\_informações de \_ conexão da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-642">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="a115f-643">**\_informações de conexão WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-643">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="a115f-644">X</span><span class="sxs-lookup"><span data-stu-id="a115f-644">X</span></span> | <span data-ttu-id="a115f-645">X</span><span class="sxs-lookup"><span data-stu-id="a115f-645">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-646">\_V0 de \_ Estatísticas de conexão da opção WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-646">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="a115f-647">**\_V0 de informações TCP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-647">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="a115f-648">X</span><span class="sxs-lookup"><span data-stu-id="a115f-648">X</span></span> | <span data-ttu-id="a115f-649">X</span><span class="sxs-lookup"><span data-stu-id="a115f-649">X</span></span> | \- | <span data-ttu-id="a115f-650">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="a115f-650">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a115f-651">\_Estatísticas de conexão da opção WinHTTP \_ \_ \_ v1</span><span class="sxs-lookup"><span data-stu-id="a115f-651">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="a115f-652">**Informações de TCP \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="a115f-652">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="a115f-653">X</span><span class="sxs-lookup"><span data-stu-id="a115f-653">X</span></span> | <span data-ttu-id="a115f-654">X</span><span class="sxs-lookup"><span data-stu-id="a115f-654">X</span></span> | \- | <span data-ttu-id="a115f-655">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="a115f-655">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a115f-656">\_valor de \_ contexto da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-656">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="a115f-657">**PTR de DWORD \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-657">**DWORD\_PTR**</span></span> | <span data-ttu-id="a115f-658">X</span><span class="sxs-lookup"><span data-stu-id="a115f-658">X</span></span> | <span data-ttu-id="a115f-659">X</span><span class="sxs-lookup"><span data-stu-id="a115f-659">X</span></span> | <span data-ttu-id="a115f-660">X</span><span class="sxs-lookup"><span data-stu-id="a115f-660">X</span></span> | <span data-ttu-id="a115f-661">X</span><span class="sxs-lookup"><span data-stu-id="a115f-661">X</span></span> | \- |
| <span data-ttu-id="a115f-662">\_DEScompactação da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-662">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="a115f-663">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-663">**DWORD**</span></span> | <span data-ttu-id="a115f-664">X</span><span class="sxs-lookup"><span data-stu-id="a115f-664">X</span></span> | <span data-ttu-id="a115f-665">X</span><span class="sxs-lookup"><span data-stu-id="a115f-665">X</span></span> | \- | <span data-ttu-id="a115f-666">X</span><span class="sxs-lookup"><span data-stu-id="a115f-666">X</span></span> | <span data-ttu-id="a115f-667">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a115f-667">Windows 8.1</span></span> |
| <span data-ttu-id="a115f-668">\_opção WinHTTP \_ desabilitar \_ compilação da cadeia de certificados \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-668">WINHTTP\_OPTION\_DISABLE\_CERT\_CHAIN\_BUILDING</span></span><br/><span data-ttu-id="a115f-669">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="a115f-669">**BOOL**</span></span> | <span data-ttu-id="a115f-670">X</span><span class="sxs-lookup"><span data-stu-id="a115f-670">X</span></span> | \- | \- | <span data-ttu-id="a115f-671">X</span><span class="sxs-lookup"><span data-stu-id="a115f-671">X</span></span> | <span data-ttu-id="a115f-672">Windows 10 versão 21H1</span><span class="sxs-lookup"><span data-stu-id="a115f-672">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a115f-673">\_recurso de \_ desabilitação da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-673">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="a115f-674">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-674">**DWORD**</span></span> | \- | <span data-ttu-id="a115f-675">X</span><span class="sxs-lookup"><span data-stu-id="a115f-675">X</span></span> | \- | <span data-ttu-id="a115f-676">X</span><span class="sxs-lookup"><span data-stu-id="a115f-676">X</span></span> | \- |
| <span data-ttu-id="a115f-677">\_opção WinHTTP \_ desabilitar \_ \_ FALLBACK de protocolo seguro \_</span><span class="sxs-lookup"><span data-stu-id="a115f-677">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="a115f-678">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="a115f-678">**BOOL**</span></span> | <span data-ttu-id="a115f-679">X</span><span class="sxs-lookup"><span data-stu-id="a115f-679">X</span></span> | \- | \- | <span data-ttu-id="a115f-680">X</span><span class="sxs-lookup"><span data-stu-id="a115f-680">X</span></span> | <span data-ttu-id="a115f-681">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="a115f-681">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a115f-682">\_opção WinHTTP \_ desabilitar \_ fila de fluxos \_</span><span class="sxs-lookup"><span data-stu-id="a115f-682">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="a115f-683">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="a115f-683">**BOOL**</span></span> | <span data-ttu-id="a115f-684">X</span><span class="sxs-lookup"><span data-stu-id="a115f-684">X</span></span> | <span data-ttu-id="a115f-685">X</span><span class="sxs-lookup"><span data-stu-id="a115f-685">X</span></span> | \- | <span data-ttu-id="a115f-686">X</span><span class="sxs-lookup"><span data-stu-id="a115f-686">X</span></span> | <span data-ttu-id="a115f-687">Windows 10 versão 1809</span><span class="sxs-lookup"><span data-stu-id="a115f-687">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="a115f-688">\_opção WinHTTP \_ habilitar \_ recurso</span><span class="sxs-lookup"><span data-stu-id="a115f-688">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="a115f-689">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-689">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="a115f-690">X</span><span class="sxs-lookup"><span data-stu-id="a115f-690">X</span></span> | \- |
| <span data-ttu-id="a115f-691">\_opção WinHTTP \_ habilitar \_ \_ protocolo http</span><span class="sxs-lookup"><span data-stu-id="a115f-691">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="a115f-692">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-692">**DWORD**</span></span> | <span data-ttu-id="a115f-693">X</span><span class="sxs-lookup"><span data-stu-id="a115f-693">X</span></span> | <span data-ttu-id="a115f-694">X</span><span class="sxs-lookup"><span data-stu-id="a115f-694">X</span></span> | \- | <span data-ttu-id="a115f-695">X</span><span class="sxs-lookup"><span data-stu-id="a115f-695">X</span></span> | <span data-ttu-id="a115f-696">Windows 10, versão 1607</span><span class="sxs-lookup"><span data-stu-id="a115f-696">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="a115f-697">\_Opção WinHTTP \_ habilitar \_ HTTP2 \_ mais \_ contexto de certificado de cliente \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-697">WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT\_CONTEXT</span></span><br/><span data-ttu-id="a115f-698">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="a115f-698">**BOOL**</span></span> | <span data-ttu-id="a115f-699">X</span><span class="sxs-lookup"><span data-stu-id="a115f-699">X</span></span> | \- | \- | <span data-ttu-id="a115f-700">X</span><span class="sxs-lookup"><span data-stu-id="a115f-700">X</span></span> | <span data-ttu-id="a115f-701">Windows 10 versão 21H1</span><span class="sxs-lookup"><span data-stu-id="a115f-701">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a115f-702">OPÇÃO WINHTTP \_ \_ ENABLETRACING</span><span class="sxs-lookup"><span data-stu-id="a115f-702">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="a115f-703">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-703">**DWORD**</span></span> | \- | \- | <span data-ttu-id="a115f-704">X</span><span class="sxs-lookup"><span data-stu-id="a115f-704">X</span></span> | <span data-ttu-id="a115f-705">X</span><span class="sxs-lookup"><span data-stu-id="a115f-705">X</span></span> | \- |
| <span data-ttu-id="a115f-706">CODIFICAR EXTRA DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-706">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="a115f-707">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a115f-707">**BOOL**</span></span> | <span data-ttu-id="a115f-708">X</span><span class="sxs-lookup"><span data-stu-id="a115f-708">X</span></span> | <span data-ttu-id="a115f-709">X</span><span class="sxs-lookup"><span data-stu-id="a115f-709">X</span></span> | \- | <span data-ttu-id="a115f-710">X</span><span class="sxs-lookup"><span data-stu-id="a115f-710">X</span></span> | <span data-ttu-id="a115f-711">Windows 10 versão 1803</span><span class="sxs-lookup"><span data-stu-id="a115f-711">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="a115f-712">WINHTTP \_ OPTION \_ EXPIRE \_ CONNECTION</span><span class="sxs-lookup"><span data-stu-id="a115f-712">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="a115f-713">N/D</span><span class="sxs-lookup"><span data-stu-id="a115f-713">N/A</span></span> | \- | <span data-ttu-id="a115f-714">X</span><span class="sxs-lookup"><span data-stu-id="a115f-714">X</span></span> | \- | <span data-ttu-id="a115f-715">X</span><span class="sxs-lookup"><span data-stu-id="a115f-715">X</span></span> | <span data-ttu-id="a115f-716">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="a115f-716">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a115f-717">ERRO ESTENDIDO DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-717">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="a115f-718">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-718">**DWORD**</span></span> | <span data-ttu-id="a115f-719">X</span><span class="sxs-lookup"><span data-stu-id="a115f-719">X</span></span> | <span data-ttu-id="a115f-720">X</span><span class="sxs-lookup"><span data-stu-id="a115f-720">X</span></span> | <span data-ttu-id="a115f-721">X</span><span class="sxs-lookup"><span data-stu-id="a115f-721">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-722">OPÇÃO WINHTTP \_ \_ PRIMEIRA CONEXÃO \_ \_ DISPONÍVEL</span><span class="sxs-lookup"><span data-stu-id="a115f-722">WINHTTP\_OPTION\_FIRST\_AVAILABLE\_CONNECTION</span></span><br/><span data-ttu-id="a115f-723">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a115f-723">**BOOL**</span></span> | <span data-ttu-id="a115f-724">X</span><span class="sxs-lookup"><span data-stu-id="a115f-724">X</span></span> | \- | \- | <span data-ttu-id="a115f-725">X</span><span class="sxs-lookup"><span data-stu-id="a115f-725">X</span></span> | <span data-ttu-id="a115f-726">Windows 10 versão 21H1</span><span class="sxs-lookup"><span data-stu-id="a115f-726">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a115f-727">CREDS DE \_ \_ PROXY GLOBAL DA \_ OPÇÃO WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-727">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="a115f-728">**WINHTTP \_ CREDS**</span><span class="sxs-lookup"><span data-stu-id="a115f-728">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="a115f-729">X</span><span class="sxs-lookup"><span data-stu-id="a115f-729">X</span></span> | <span data-ttu-id="a115f-730">X</span><span class="sxs-lookup"><span data-stu-id="a115f-730">X</span></span> | \- | <span data-ttu-id="a115f-731">X</span><span class="sxs-lookup"><span data-stu-id="a115f-731">X</span></span> | \- |
| <span data-ttu-id="a115f-732">CREDS DE SERVIDOR GLOBAL DA OPÇÃO WINHTTP \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-732">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="a115f-733">**WINHTTP \_ CREDS \_ EX**</span><span class="sxs-lookup"><span data-stu-id="a115f-733">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="a115f-734">X</span><span class="sxs-lookup"><span data-stu-id="a115f-734">X</span></span> | <span data-ttu-id="a115f-735">X</span><span class="sxs-lookup"><span data-stu-id="a115f-735">X</span></span> | \- | <span data-ttu-id="a115f-736">X</span><span class="sxs-lookup"><span data-stu-id="a115f-736">X</span></span> | \- |
| <span data-ttu-id="a115f-737">TIPO DE \_ IDENTIFICADOR DE OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-737">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="a115f-738">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-738">**DWORD**</span></span> | <span data-ttu-id="a115f-739">X</span><span class="sxs-lookup"><span data-stu-id="a115f-739">X</span></span> | <span data-ttu-id="a115f-740">X</span><span class="sxs-lookup"><span data-stu-id="a115f-740">X</span></span> | <span data-ttu-id="a115f-741">X</span><span class="sxs-lookup"><span data-stu-id="a115f-741">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-742">WINHTTP \_ OPTION \_ HTTP \_ PROTOCOL \_ REQUIRED</span><span class="sxs-lookup"><span data-stu-id="a115f-742">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="a115f-743">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a115f-743">**BOOL**</span></span> | <span data-ttu-id="a115f-744">X</span><span class="sxs-lookup"><span data-stu-id="a115f-744">X</span></span> | <span data-ttu-id="a115f-745">X</span><span class="sxs-lookup"><span data-stu-id="a115f-745">X</span></span> | \- | <span data-ttu-id="a115f-746">X</span><span class="sxs-lookup"><span data-stu-id="a115f-746">X</span></span> | <span data-ttu-id="a115f-747">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="a115f-747">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a115f-748">WINHTTP \_ OPTION \_ HTTP \_ PROTOCOL \_ USED</span><span class="sxs-lookup"><span data-stu-id="a115f-748">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="a115f-749">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-749">**DWORD**</span></span> | \- | <span data-ttu-id="a115f-750">X</span><span class="sxs-lookup"><span data-stu-id="a115f-750">X</span></span> | <span data-ttu-id="a115f-751">X</span><span class="sxs-lookup"><span data-stu-id="a115f-751">X</span></span> | \- | <span data-ttu-id="a115f-752">Windows 10, versão 1607</span><span class="sxs-lookup"><span data-stu-id="a115f-752">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="a115f-753">WINHTTP \_ OPTION \_ HTTP \_ VERSION</span><span class="sxs-lookup"><span data-stu-id="a115f-753">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="a115f-754">**INFORMAÇÕES \_ DE VERSÃO \_ HTTP**</span><span class="sxs-lookup"><span data-stu-id="a115f-754">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="a115f-755">X</span><span class="sxs-lookup"><span data-stu-id="a115f-755">X</span></span> | <span data-ttu-id="a115f-756">X</span><span class="sxs-lookup"><span data-stu-id="a115f-756">X</span></span> | <span data-ttu-id="a115f-757">X</span><span class="sxs-lookup"><span data-stu-id="a115f-757">X</span></span> | <span data-ttu-id="a115f-758">X</span><span class="sxs-lookup"><span data-stu-id="a115f-758">X</span></span> | \- |
| <span data-ttu-id="a115f-759">WINHTTP \_ OPTION \_ HTTP2 \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="a115f-759">WINHTTP\_OPTION\_HTTP2\_KEEPALIVE</span></span><br/><span data-ttu-id="a115f-760">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-760">**DWORD**</span></span> | <span data-ttu-id="a115f-761">X</span><span class="sxs-lookup"><span data-stu-id="a115f-761">X</span></span> | \- | \- | <span data-ttu-id="a115f-762">X</span><span class="sxs-lookup"><span data-stu-id="a115f-762">X</span></span> | <span data-ttu-id="a115f-763">Windows 10 versão 21H1</span><span class="sxs-lookup"><span data-stu-id="a115f-763">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a115f-764">WINHTTP \_ OPTION \_ HTTP2 \_ PLUS \_ TRANSFER \_ ENCODING</span><span class="sxs-lookup"><span data-stu-id="a115f-764">WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING</span></span><br/><span data-ttu-id="a115f-765">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a115f-765">**BOOL**</span></span> | <span data-ttu-id="a115f-766">X</span><span class="sxs-lookup"><span data-stu-id="a115f-766">X</span></span> | <span data-ttu-id="a115f-767">X</span><span class="sxs-lookup"><span data-stu-id="a115f-767">X</span></span> | \- | <span data-ttu-id="a115f-768">X</span><span class="sxs-lookup"><span data-stu-id="a115f-768">X</span></span> | <span data-ttu-id="a115f-769">Windows 10 versão 21H1</span><span class="sxs-lookup"><span data-stu-id="a115f-769">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a115f-770">OPÇÃO WINHTTP \_ \_ IGNORAR \_ \_ REVOGAÇÃO DE CERTIFICADO \_ OFFLINE</span><span class="sxs-lookup"><span data-stu-id="a115f-770">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="a115f-771">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a115f-771">**BOOL**</span></span> | \- | <span data-ttu-id="a115f-772">X</span><span class="sxs-lookup"><span data-stu-id="a115f-772">X</span></span> | \- | <span data-ttu-id="a115f-773">X</span><span class="sxs-lookup"><span data-stu-id="a115f-773">X</span></span> | <span data-ttu-id="a115f-774">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="a115f-774">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a115f-775">FALLBACK RÁPIDO \_ \_ DE IPV6 \_ DA OPÇÃO WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-775">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="a115f-776">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a115f-776">**BOOL**</span></span> | <span data-ttu-id="a115f-777">X</span><span class="sxs-lookup"><span data-stu-id="a115f-777">X</span></span> | \- | \- | <span data-ttu-id="a115f-778">X</span><span class="sxs-lookup"><span data-stu-id="a115f-778">X</span></span> | <span data-ttu-id="a115f-779">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="a115f-779">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a115f-780">A OPÇÃO \_ WINHTTP É PROXY CONNECT \_ \_ \_ \_ RESPONSE</span><span class="sxs-lookup"><span data-stu-id="a115f-780">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="a115f-781">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a115f-781">**BOOL**</span></span> | <span data-ttu-id="a115f-782">X</span><span class="sxs-lookup"><span data-stu-id="a115f-782">X</span></span> | <span data-ttu-id="a115f-783">X</span><span class="sxs-lookup"><span data-stu-id="a115f-783">X</span></span> | <span data-ttu-id="a115f-784">X</span><span class="sxs-lookup"><span data-stu-id="a115f-784">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-785">WINHTTP \_ OPTION \_ MAX \_ CONNS \_ PER \_ 1 \_ 0 \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="a115f-785">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="a115f-786">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-786">**DWORD**</span></span> | <span data-ttu-id="a115f-787">X</span><span class="sxs-lookup"><span data-stu-id="a115f-787">X</span></span> | \- | <span data-ttu-id="a115f-788">X</span><span class="sxs-lookup"><span data-stu-id="a115f-788">X</span></span> | <span data-ttu-id="a115f-789">X</span><span class="sxs-lookup"><span data-stu-id="a115f-789">X</span></span> | \- |
| <span data-ttu-id="a115f-790">OPÇÃO WINHTTP \_ \_ MAX \_ CONNS POR \_ \_ SERVIDOR</span><span class="sxs-lookup"><span data-stu-id="a115f-790">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="a115f-791">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-791">**DWORD**</span></span> | <span data-ttu-id="a115f-792">X</span><span class="sxs-lookup"><span data-stu-id="a115f-792">X</span></span> | \- | <span data-ttu-id="a115f-793">X</span><span class="sxs-lookup"><span data-stu-id="a115f-793">X</span></span> | <span data-ttu-id="a115f-794">X</span><span class="sxs-lookup"><span data-stu-id="a115f-794">X</span></span> | \- |
| <span data-ttu-id="a115f-795">REDIRECIONAMENTOS \_ AUTOMÁTICOS \_ DE HTTP MÁXIMO DA \_ \_ \_ OPÇÃO WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a115f-795">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="a115f-796">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-796">**DWORD**</span></span> | <span data-ttu-id="a115f-797">X</span><span class="sxs-lookup"><span data-stu-id="a115f-797">X</span></span> | <span data-ttu-id="a115f-798">X</span><span class="sxs-lookup"><span data-stu-id="a115f-798">X</span></span> | <span data-ttu-id="a115f-799">X</span><span class="sxs-lookup"><span data-stu-id="a115f-799">X</span></span> | <span data-ttu-id="a115f-800">X</span><span class="sxs-lookup"><span data-stu-id="a115f-800">X</span></span> | \- |
| <span data-ttu-id="a115f-801">\_máximo de \_ status HTTP da opção WinHTTP \_ \_ \_ continuar</span><span class="sxs-lookup"><span data-stu-id="a115f-801">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="a115f-802">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-802">**DWORD**</span></span> | <span data-ttu-id="a115f-803">X</span><span class="sxs-lookup"><span data-stu-id="a115f-803">X</span></span> | <span data-ttu-id="a115f-804">X</span><span class="sxs-lookup"><span data-stu-id="a115f-804">X</span></span> | <span data-ttu-id="a115f-805">X</span><span class="sxs-lookup"><span data-stu-id="a115f-805">X</span></span> | <span data-ttu-id="a115f-806">X</span><span class="sxs-lookup"><span data-stu-id="a115f-806">X</span></span> | \- |
| <span data-ttu-id="a115f-807">\_tamanho de \_ \_ dreno de resposta máx da opção \_ WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-807">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="a115f-808">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-808">**DWORD**</span></span> | <span data-ttu-id="a115f-809">X</span><span class="sxs-lookup"><span data-stu-id="a115f-809">X</span></span> | <span data-ttu-id="a115f-810">X</span><span class="sxs-lookup"><span data-stu-id="a115f-810">X</span></span> | <span data-ttu-id="a115f-811">X</span><span class="sxs-lookup"><span data-stu-id="a115f-811">X</span></span> | <span data-ttu-id="a115f-812">X</span><span class="sxs-lookup"><span data-stu-id="a115f-812">X</span></span> | \- |
| <span data-ttu-id="a115f-813">\_ \_ tamanho máximo do \_ cabeçalho de resposta da \_ opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-813">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="a115f-814">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-814">**DWORD**</span></span> | <span data-ttu-id="a115f-815">X</span><span class="sxs-lookup"><span data-stu-id="a115f-815">X</span></span> | <span data-ttu-id="a115f-816">X</span><span class="sxs-lookup"><span data-stu-id="a115f-816">X</span></span> | <span data-ttu-id="a115f-817">X</span><span class="sxs-lookup"><span data-stu-id="a115f-817">X</span></span> | <span data-ttu-id="a115f-818">X</span><span class="sxs-lookup"><span data-stu-id="a115f-818">X</span></span> | \- |
| <span data-ttu-id="a115f-819">\_ \_ identificador pai da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-819">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="a115f-820">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="a115f-820">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="a115f-821">X</span><span class="sxs-lookup"><span data-stu-id="a115f-821">X</span></span> | <span data-ttu-id="a115f-822">X</span><span class="sxs-lookup"><span data-stu-id="a115f-822">X</span></span> | <span data-ttu-id="a115f-823">X</span><span class="sxs-lookup"><span data-stu-id="a115f-823">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-824">opção WINHTTP de \_ \_ \_ texto de comarcação do Passport \_</span><span class="sxs-lookup"><span data-stu-id="a115f-824">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="a115f-825">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a115f-825">**LPWSTR**</span></span> | \- | <span data-ttu-id="a115f-826">X</span><span class="sxs-lookup"><span data-stu-id="a115f-826">X</span></span> | <span data-ttu-id="a115f-827">X</span><span class="sxs-lookup"><span data-stu-id="a115f-827">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-828">\_URL de \_ \_ comarcação do passaporte da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-828">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="a115f-829">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a115f-829">**LPWSTR**</span></span> | \- | <span data-ttu-id="a115f-830">X</span><span class="sxs-lookup"><span data-stu-id="a115f-830">X</span></span> | <span data-ttu-id="a115f-831">X</span><span class="sxs-lookup"><span data-stu-id="a115f-831">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-832">\_opção WinHTTP \_ URL de retorno do Passport \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-832">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="a115f-833">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="a115f-833">**LPVOID**</span></span> | \- | <span data-ttu-id="a115f-834">X</span><span class="sxs-lookup"><span data-stu-id="a115f-834">X</span></span> | <span data-ttu-id="a115f-835">X</span><span class="sxs-lookup"><span data-stu-id="a115f-835">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-836">opção WINHTTP sair do \_ \_ Passport \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-836">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="a115f-837">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="a115f-837">**LPVOID**</span></span> | <span data-ttu-id="a115f-838">X</span><span class="sxs-lookup"><span data-stu-id="a115f-838">X</span></span> | \- | \- | <span data-ttu-id="a115f-839">X</span><span class="sxs-lookup"><span data-stu-id="a115f-839">X</span></span> | \- |
| <span data-ttu-id="a115f-840">\_senha da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-840">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="a115f-841">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a115f-841">**LPWSTR**</span></span> | \- | <span data-ttu-id="a115f-842">X</span><span class="sxs-lookup"><span data-stu-id="a115f-842">X</span></span> | <span data-ttu-id="a115f-843">X</span><span class="sxs-lookup"><span data-stu-id="a115f-843">X</span></span> | <span data-ttu-id="a115f-844">X</span><span class="sxs-lookup"><span data-stu-id="a115f-844">X</span></span> | \- |
| <span data-ttu-id="a115f-845">\_proxy de opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-845">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="a115f-846">**\_informações de proxy WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-846">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="a115f-847">X</span><span class="sxs-lookup"><span data-stu-id="a115f-847">X</span></span> | <span data-ttu-id="a115f-848">X</span><span class="sxs-lookup"><span data-stu-id="a115f-848">X</span></span> | <span data-ttu-id="a115f-849">X</span><span class="sxs-lookup"><span data-stu-id="a115f-849">X</span></span> | <span data-ttu-id="a115f-850">X</span><span class="sxs-lookup"><span data-stu-id="a115f-850">X</span></span> | \- |
| <span data-ttu-id="a115f-851">\_senha do \_ proxy da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-851">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="a115f-852">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a115f-852">**LPWSTR**</span></span> | \- | <span data-ttu-id="a115f-853">X</span><span class="sxs-lookup"><span data-stu-id="a115f-853">X</span></span> | <span data-ttu-id="a115f-854">X</span><span class="sxs-lookup"><span data-stu-id="a115f-854">X</span></span> | <span data-ttu-id="a115f-855">X</span><span class="sxs-lookup"><span data-stu-id="a115f-855">X</span></span> | \- |
| <span data-ttu-id="a115f-856">SPN de proxy de opção de WINHTTP \_ \_ \_ \_ usado</span><span class="sxs-lookup"><span data-stu-id="a115f-856">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="a115f-857">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a115f-857">**LPWSTR**</span></span> | \- | <span data-ttu-id="a115f-858">X</span><span class="sxs-lookup"><span data-stu-id="a115f-858">X</span></span> | <span data-ttu-id="a115f-859">X</span><span class="sxs-lookup"><span data-stu-id="a115f-859">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-860">\_nome de \_ usuário do proxy de opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-860">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="a115f-861">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a115f-861">**LPWSTR**</span></span> | \- | <span data-ttu-id="a115f-862">X</span><span class="sxs-lookup"><span data-stu-id="a115f-862">X</span></span> | <span data-ttu-id="a115f-863">X</span><span class="sxs-lookup"><span data-stu-id="a115f-863">X</span></span> | <span data-ttu-id="a115f-864">X</span><span class="sxs-lookup"><span data-stu-id="a115f-864">X</span></span> | \- |
| <span data-ttu-id="a115f-865">\_tamanho do \_ buffer de leitura da opção WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-865">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a115f-866">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-866">**DWORD**</span></span> | \- | <span data-ttu-id="a115f-867">X</span><span class="sxs-lookup"><span data-stu-id="a115f-867">X</span></span> | <span data-ttu-id="a115f-868">X</span><span class="sxs-lookup"><span data-stu-id="a115f-868">X</span></span> | <span data-ttu-id="a115f-869">X</span><span class="sxs-lookup"><span data-stu-id="a115f-869">X</span></span> | \- |
| <span data-ttu-id="a115f-870">a \_ opção \_ WinHTTP \_ recebe \_ resposta de conexão proxy \_</span><span class="sxs-lookup"><span data-stu-id="a115f-870">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="a115f-871">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="a115f-871">**BOOL**</span></span> | <span data-ttu-id="a115f-872">X</span><span class="sxs-lookup"><span data-stu-id="a115f-872">X</span></span> | <span data-ttu-id="a115f-873">X</span><span class="sxs-lookup"><span data-stu-id="a115f-873">X</span></span> | \- | <span data-ttu-id="a115f-874">X</span><span class="sxs-lookup"><span data-stu-id="a115f-874">X</span></span> | \- |
| <span data-ttu-id="a115f-875">a \_ opção \_ WinHTTP \_ recebe \_ tempo limite de resposta</span><span class="sxs-lookup"><span data-stu-id="a115f-875">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="a115f-876">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-876">**DWORD**</span></span> | <span data-ttu-id="a115f-877">X</span><span class="sxs-lookup"><span data-stu-id="a115f-877">X</span></span> | <span data-ttu-id="a115f-878">X</span><span class="sxs-lookup"><span data-stu-id="a115f-878">X</span></span> | <span data-ttu-id="a115f-879">X</span><span class="sxs-lookup"><span data-stu-id="a115f-879">X</span></span> | <span data-ttu-id="a115f-880">X</span><span class="sxs-lookup"><span data-stu-id="a115f-880">X</span></span> | \- |
| <span data-ttu-id="a115f-881">\_ \_ tempo limite de recebimento da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-881">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="a115f-882">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-882">**DWORD**</span></span> | <span data-ttu-id="a115f-883">X</span><span class="sxs-lookup"><span data-stu-id="a115f-883">X</span></span> | <span data-ttu-id="a115f-884">X</span><span class="sxs-lookup"><span data-stu-id="a115f-884">X</span></span> | <span data-ttu-id="a115f-885">X</span><span class="sxs-lookup"><span data-stu-id="a115f-885">X</span></span> | <span data-ttu-id="a115f-886">X</span><span class="sxs-lookup"><span data-stu-id="a115f-886">X</span></span> | \- |
| <span data-ttu-id="a115f-887">\_política de \_ redirecionamento de opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-887">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="a115f-888">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-888">**DWORD**</span></span> | <span data-ttu-id="a115f-889">X</span><span class="sxs-lookup"><span data-stu-id="a115f-889">X</span></span> | <span data-ttu-id="a115f-890">X</span><span class="sxs-lookup"><span data-stu-id="a115f-890">X</span></span> | <span data-ttu-id="a115f-891">X</span><span class="sxs-lookup"><span data-stu-id="a115f-891">X</span></span> | <span data-ttu-id="a115f-892">X</span><span class="sxs-lookup"><span data-stu-id="a115f-892">X</span></span> | \- |
| <span data-ttu-id="a115f-893">a \_ opção WinHTTP \_ rejeita \_ USERPWD \_ na \_ URL</span><span class="sxs-lookup"><span data-stu-id="a115f-893">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="a115f-894">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="a115f-894">**BOOL**</span></span> | \- | <span data-ttu-id="a115f-895">X</span><span class="sxs-lookup"><span data-stu-id="a115f-895">X</span></span> | \- | <span data-ttu-id="a115f-896">X</span><span class="sxs-lookup"><span data-stu-id="a115f-896">X</span></span> | \- |
| <span data-ttu-id="a115f-897">\_prioridade de \_ solicitação de opção de WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-897">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="a115f-898">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-898">**DWORD**</span></span> | \- | <span data-ttu-id="a115f-899">X</span><span class="sxs-lookup"><span data-stu-id="a115f-899">X</span></span> | <span data-ttu-id="a115f-900">X</span><span class="sxs-lookup"><span data-stu-id="a115f-900">X</span></span> | <span data-ttu-id="a115f-901">X</span><span class="sxs-lookup"><span data-stu-id="a115f-901">X</span></span> | \- |
| <span data-ttu-id="a115f-902">ESTATÍSTICAS DE \_ SOLICITAÇÃO DE OPÇÃO \_ WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-902">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="a115f-903">**ESTATÍSTICAS DE \_ SOLICITAÇÃO \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a115f-903">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="a115f-904">X</span><span class="sxs-lookup"><span data-stu-id="a115f-904">X</span></span> | <span data-ttu-id="a115f-905">X</span><span class="sxs-lookup"><span data-stu-id="a115f-905">X</span></span> | \- | <span data-ttu-id="a115f-906">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="a115f-906">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a115f-907">TEMPOS DE \_ SOLICITAÇÃO DA OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-907">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="a115f-908">**TEMPOS DE \_ SOLICITAÇÃO WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-908">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="a115f-909">X</span><span class="sxs-lookup"><span data-stu-id="a115f-909">X</span></span> | <span data-ttu-id="a115f-910">X</span><span class="sxs-lookup"><span data-stu-id="a115f-910">X</span></span> | \- | <span data-ttu-id="a115f-911">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="a115f-911">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a115f-912">OPÇÃO WINHTTP \_ EXIGIR \_ FIM DO \_ \_ FLUXO</span><span class="sxs-lookup"><span data-stu-id="a115f-912">WINHTTP\_OPTION\_REQUIRE\_STREAM\_END</span></span><br/><span data-ttu-id="a115f-913">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a115f-913">**BOOL**</span></span> | <span data-ttu-id="a115f-914">X</span><span class="sxs-lookup"><span data-stu-id="a115f-914">X</span></span> | <span data-ttu-id="a115f-915">X</span><span class="sxs-lookup"><span data-stu-id="a115f-915">X</span></span> | \- | <span data-ttu-id="a115f-916">X</span><span class="sxs-lookup"><span data-stu-id="a115f-916">X</span></span> | <span data-ttu-id="a115f-917">Windows 10 versão 21H1</span><span class="sxs-lookup"><span data-stu-id="a115f-917">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a115f-918">WINHTTP \_ OPTION \_ RESOLUTION \_ HOSTNAME</span><span class="sxs-lookup"><span data-stu-id="a115f-918">WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME</span></span><br/><span data-ttu-id="a115f-919">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="a115f-919">**LPWSTR**</span></span> | \- | <span data-ttu-id="a115f-920">X</span><span class="sxs-lookup"><span data-stu-id="a115f-920">X</span></span> | \- | <span data-ttu-id="a115f-921">X</span><span class="sxs-lookup"><span data-stu-id="a115f-921">X</span></span> | <span data-ttu-id="a115f-922">Windows 10 versão 21H1</span><span class="sxs-lookup"><span data-stu-id="a115f-922">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a115f-923">WINHTTP \_ OPTION \_ RESOLVE \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a115f-923">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="a115f-924">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-924">**DWORD**</span></span> | <span data-ttu-id="a115f-925">X</span><span class="sxs-lookup"><span data-stu-id="a115f-925">X</span></span> | <span data-ttu-id="a115f-926">X</span><span class="sxs-lookup"><span data-stu-id="a115f-926">X</span></span> | <span data-ttu-id="a115f-927">X</span><span class="sxs-lookup"><span data-stu-id="a115f-927">X</span></span> | <span data-ttu-id="a115f-928">X</span><span class="sxs-lookup"><span data-stu-id="a115f-928">X</span></span> | \- |
| <span data-ttu-id="a115f-929">PROTOCOLOS SEGUROS DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-929">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="a115f-930">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-930">**DWORD**</span></span> | <span data-ttu-id="a115f-931">X</span><span class="sxs-lookup"><span data-stu-id="a115f-931">X</span></span> | \- | \- | <span data-ttu-id="a115f-932">X</span><span class="sxs-lookup"><span data-stu-id="a115f-932">X</span></span> | \- |
| <span data-ttu-id="a115f-933">STRUCT DO CERTIFICADO \_ \_ DE SEGURANÇA DA \_ OPÇÃO WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-933">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="a115f-934">**INFORMAÇÕES DE CERTIFICADO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a115f-934">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="a115f-935">X</span><span class="sxs-lookup"><span data-stu-id="a115f-935">X</span></span> | <span data-ttu-id="a115f-936">X</span><span class="sxs-lookup"><span data-stu-id="a115f-936">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-937">SINALIZADORES DE SEGURANÇA DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-937">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="a115f-938">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-938">**DWORD**</span></span> | \- | <span data-ttu-id="a115f-939">X</span><span class="sxs-lookup"><span data-stu-id="a115f-939">X</span></span> | <span data-ttu-id="a115f-940">X</span><span class="sxs-lookup"><span data-stu-id="a115f-940">X</span></span> | <span data-ttu-id="a115f-941">X</span><span class="sxs-lookup"><span data-stu-id="a115f-941">X</span></span> | \- |
| <span data-ttu-id="a115f-942">INFORMAÇÕES DE SEGURANÇA DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-942">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="a115f-943">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="a115f-943">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="a115f-944">X</span><span class="sxs-lookup"><span data-stu-id="a115f-944">X</span></span> | <span data-ttu-id="a115f-945">X</span><span class="sxs-lookup"><span data-stu-id="a115f-945">X</span></span> | \- | <span data-ttu-id="a115f-946">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="a115f-946">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a115f-947">BITNESS \_ DA CHAVE \_ DE SEGURANÇA DA \_ \_ OPÇÃO WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a115f-947">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="a115f-948">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-948">**DWORD**</span></span> | \- | <span data-ttu-id="a115f-949">X</span><span class="sxs-lookup"><span data-stu-id="a115f-949">X</span></span> | <span data-ttu-id="a115f-950">X</span><span class="sxs-lookup"><span data-stu-id="a115f-950">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-951">WINHTTP \_ OPTION \_ SEND \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a115f-951">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="a115f-952">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-952">**DWORD**</span></span> | <span data-ttu-id="a115f-953">X</span><span class="sxs-lookup"><span data-stu-id="a115f-953">X</span></span> | <span data-ttu-id="a115f-954">X</span><span class="sxs-lookup"><span data-stu-id="a115f-954">X</span></span> | <span data-ttu-id="a115f-955">X</span><span class="sxs-lookup"><span data-stu-id="a115f-955">X</span></span> | <span data-ttu-id="a115f-956">X</span><span class="sxs-lookup"><span data-stu-id="a115f-956">X</span></span> | \- |
| <span data-ttu-id="a115f-957">CBT DO \_ SERVIDOR DE OPÇÕES \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a115f-957">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="a115f-958">[**Vinculações SecPkgContext \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="a115f-958">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="a115f-959">X</span><span class="sxs-lookup"><span data-stu-id="a115f-959">X</span></span> | <span data-ttu-id="a115f-960">X</span><span class="sxs-lookup"><span data-stu-id="a115f-960">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-961">CONTEXTO DA CADEIA DE \_ \_ CERTIFICADOS \_ DO SERVIDOR WINHTTP OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-961">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="a115f-962">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="a115f-962">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="a115f-963">X</span><span class="sxs-lookup"><span data-stu-id="a115f-963">X</span></span> | <span data-ttu-id="a115f-964">X</span><span class="sxs-lookup"><span data-stu-id="a115f-964">X</span></span> | \- | <span data-ttu-id="a115f-965">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="a115f-965">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a115f-966">CONTEXTO DE CERTIFICADO \_ DO \_ SERVIDOR WINHTTP OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-966">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="a115f-967">**CONTEXTO DO CERTIFICADO**</span><span class="sxs-lookup"><span data-stu-id="a115f-967">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="a115f-968">X</span><span class="sxs-lookup"><span data-stu-id="a115f-968">X</span></span> | <span data-ttu-id="a115f-969">X</span><span class="sxs-lookup"><span data-stu-id="a115f-969">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-970">SPN DO \_ SERVIDOR DE OPÇÕES \_ \_ WINHTTP \_ USADO</span><span class="sxs-lookup"><span data-stu-id="a115f-970">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="a115f-971">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="a115f-971">**LPWSTR**</span></span> | \- | <span data-ttu-id="a115f-972">X</span><span class="sxs-lookup"><span data-stu-id="a115f-972">X</span></span> | <span data-ttu-id="a115f-973">X</span><span class="sxs-lookup"><span data-stu-id="a115f-973">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-974">SPN DA \_ OPÇÃO \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a115f-974">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="a115f-975">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-975">**DWORD**</span></span> | \- | <span data-ttu-id="a115f-976">X</span><span class="sxs-lookup"><span data-stu-id="a115f-976">X</span></span> | \- | <span data-ttu-id="a115f-977">X</span><span class="sxs-lookup"><span data-stu-id="a115f-977">X</span></span> | \- |
| <span data-ttu-id="a115f-978">CÓDIGO DE ERRO DE FLUXO DE OPÇÃO WINHTTP \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-978">WINHTTP\_OPTION\_STREAM\_ERROR\_CODE</span></span><br/><span data-ttu-id="a115f-979">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-979">**DWORD**</span></span> | \- | <span data-ttu-id="a115f-980">X</span><span class="sxs-lookup"><span data-stu-id="a115f-980">X</span></span> | <span data-ttu-id="a115f-981">X</span><span class="sxs-lookup"><span data-stu-id="a115f-981">X</span></span> | \- | <span data-ttu-id="a115f-982">Windows 10 versão 21H1</span><span class="sxs-lookup"><span data-stu-id="a115f-982">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a115f-983">WINHTTP \_ OPTION \_ TCP \_ FAST \_ OPEN</span><span class="sxs-lookup"><span data-stu-id="a115f-983">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="a115f-984">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a115f-984">**BOOL**</span></span> | <span data-ttu-id="a115f-985">X</span><span class="sxs-lookup"><span data-stu-id="a115f-985">X</span></span> | \- | \- | <span data-ttu-id="a115f-986">X</span><span class="sxs-lookup"><span data-stu-id="a115f-986">X</span></span> | <span data-ttu-id="a115f-987">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="a115f-987">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a115f-988">WINHTTP \_ OPTION \_ TCP \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="a115f-988">WINHTTP\_OPTION\_TCP\_KEEPALIVE</span></span><br/>[<span data-ttu-id="a115f-989">**tcp \_ keepalive**</span><span class="sxs-lookup"><span data-stu-id="a115f-989">**tcp\_keepalive**</span></span>](/windows/win32/winsock/sio-keepalive-vals) | <span data-ttu-id="a115f-990">X</span><span class="sxs-lookup"><span data-stu-id="a115f-990">X</span></span> | \- | \- | <span data-ttu-id="a115f-991">X</span><span class="sxs-lookup"><span data-stu-id="a115f-991">X</span></span> | <span data-ttu-id="a115f-992">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="a115f-992">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a115f-993">WINHTTP \_ OPTION \_ TLS \_ FALSE \_ START</span><span class="sxs-lookup"><span data-stu-id="a115f-993">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="a115f-994">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a115f-994">**BOOL**</span></span> | <span data-ttu-id="a115f-995">X</span><span class="sxs-lookup"><span data-stu-id="a115f-995">X</span></span> | \- | \- | <span data-ttu-id="a115f-996">X</span><span class="sxs-lookup"><span data-stu-id="a115f-996">X</span></span> | <span data-ttu-id="a115f-997">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="a115f-997">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a115f-998">FALLBACK INSEGURO DO \_ \_ PROTOCOLO TLS \_ \_ DA OPÇÃO WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-998">WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK</span></span><br/><span data-ttu-id="a115f-999">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a115f-999">**BOOL**</span></span> | <span data-ttu-id="a115f-1000">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1000">X</span></span> | \- | \- | <span data-ttu-id="a115f-1001">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1001">X</span></span> | <span data-ttu-id="a115f-1002">Windows 10 versão 21H1</span><span class="sxs-lookup"><span data-stu-id="a115f-1002">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a115f-1003">\_evento de \_ notificação de descarregamento da opção WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-1003">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="a115f-1004">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="a115f-1004">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="a115f-1005">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1005">X</span></span> | \- | \- | <span data-ttu-id="a115f-1006">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1006">X</span></span> | \- |
| <span data-ttu-id="a115f-1007">\_opção WinHTTP \_ análise de \_ cabeçalho não seguro \_</span><span class="sxs-lookup"><span data-stu-id="a115f-1007">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="a115f-1008">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-1008">**DWORD**</span></span> | \- | <span data-ttu-id="a115f-1009">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1009">X</span></span> | \- | <span data-ttu-id="a115f-1010">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1010">X</span></span> | \- |
| <span data-ttu-id="a115f-1011">\_opção \_ de WinHTTP atualizar para o \_ \_ soquete da Web \_</span><span class="sxs-lookup"><span data-stu-id="a115f-1011">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="a115f-1012">N/D</span><span class="sxs-lookup"><span data-stu-id="a115f-1012">N/A</span></span> | \- | <span data-ttu-id="a115f-1013">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1013">X</span></span> | \- | <span data-ttu-id="a115f-1014">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1014">X</span></span> | \- |
| <span data-ttu-id="a115f-1015">\_URL da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-1015">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="a115f-1016">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a115f-1016">**LPWSTR**</span></span> | \- | <span data-ttu-id="a115f-1017">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1017">X</span></span> | <span data-ttu-id="a115f-1018">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1018">X</span></span> | \- | \- |
| <span data-ttu-id="a115f-1019">\_opção WinHTTP \_ usar \_ \_ credenciais do servidor global \_</span><span class="sxs-lookup"><span data-stu-id="a115f-1019">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="a115f-1020">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="a115f-1020">**BOOL**</span></span> | <span data-ttu-id="a115f-1021">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1021">X</span></span> | <span data-ttu-id="a115f-1022">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1022">X</span></span> | \- | <span data-ttu-id="a115f-1023">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1023">X</span></span> | \- |
| <span data-ttu-id="a115f-1024">\_agente do \_ usuário da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-1024">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="a115f-1025">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a115f-1025">**LPWSTR**</span></span> | <span data-ttu-id="a115f-1026">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1026">X</span></span> | \- | <span data-ttu-id="a115f-1027">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1027">X</span></span> | <span data-ttu-id="a115f-1028">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1028">X</span></span> | \- |
| <span data-ttu-id="a115f-1029">nome de usuário da \_ opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-1029">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="a115f-1030">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a115f-1030">**LPWSTR**</span></span> | \- | <span data-ttu-id="a115f-1031">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1031">X</span></span> | <span data-ttu-id="a115f-1032">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1032">X</span></span> | <span data-ttu-id="a115f-1033">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1033">X</span></span> | \- |
| <span data-ttu-id="a115f-1034">\_ \_ \_ \_ tempo limite de fechamento de soquete da Web de opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a115f-1034">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="a115f-1035">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-1035">**DWORD**</span></span> | \- | \- | <span data-ttu-id="a115f-1036">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1036">X</span></span> | <span data-ttu-id="a115f-1037">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1037">X</span></span> | \- |
| <span data-ttu-id="a115f-1038">\_intervalo de \_ KeepAlive de soquete da Web de opção WinHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-1038">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="a115f-1039">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-1039">**DWORD**</span></span> | \- | \- | <span data-ttu-id="a115f-1040">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1040">X</span></span> | <span data-ttu-id="a115f-1041">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1041">X</span></span> | \- |
| <span data-ttu-id="a115f-1042">\_opção WinHTTP \_ \_ tamanho do \_ buffer de recebimento de soquete da \_ Web \_</span><span class="sxs-lookup"><span data-stu-id="a115f-1042">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a115f-1043">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-1043">**DWORD**</span></span> | <span data-ttu-id="a115f-1044">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1044">X</span></span> | <span data-ttu-id="a115f-1045">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1045">X</span></span> | <span data-ttu-id="a115f-1046">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1046">X</span></span> | <span data-ttu-id="a115f-1047">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1047">X</span></span> | <span data-ttu-id="a115f-1048">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a115f-1048">Windows 8.1</span></span> |
| <span data-ttu-id="a115f-1049">\_opção WinHTTP \_ \_ tamanho do \_ buffer de envio de soquete da \_ Web \_</span><span class="sxs-lookup"><span data-stu-id="a115f-1049">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a115f-1050">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-1050">**DWORD**</span></span> | <span data-ttu-id="a115f-1051">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1051">X</span></span> | <span data-ttu-id="a115f-1052">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1052">X</span></span> | <span data-ttu-id="a115f-1053">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1053">X</span></span> | <span data-ttu-id="a115f-1054">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1054">X</span></span> | <span data-ttu-id="a115f-1055">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a115f-1055">Windows 8.1</span></span> |
| <span data-ttu-id="a115f-1056">\_opção WinHTTP \_ \_ contagem de threads de trabalho \_</span><span class="sxs-lookup"><span data-stu-id="a115f-1056">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="a115f-1057">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-1057">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="a115f-1058">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1058">X</span></span> | \- |
| <span data-ttu-id="a115f-1059">\_tamanho do \_ buffer de gravação da opção WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a115f-1059">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a115f-1060">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a115f-1060">**DWORD**</span></span> | \- | <span data-ttu-id="a115f-1061">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1061">X</span></span> | <span data-ttu-id="a115f-1062">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1062">X</span></span> | <span data-ttu-id="a115f-1063">X</span><span class="sxs-lookup"><span data-stu-id="a115f-1063">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="a115f-1064">Para o Windows XP e o Windows 2000, consulte [requisitos de tempo de execução](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="a115f-1064">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a115f-1065">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a115f-1065">Requirements</span></span>

| <span data-ttu-id="a115f-1066">Requisito</span><span class="sxs-lookup"><span data-stu-id="a115f-1066">Requirement</span></span> | <span data-ttu-id="a115f-1067">Valor</span><span class="sxs-lookup"><span data-stu-id="a115f-1067">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a115f-1068">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a115f-1068">Minimum supported client</span></span> | <span data-ttu-id="a115f-1069">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="a115f-1069">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="a115f-1070">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a115f-1070">Minimum supported server</span></span> | <span data-ttu-id="a115f-1071">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="a115f-1071">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="a115f-1072">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a115f-1072">Redistributable</span></span>          | <span data-ttu-id="a115f-1073">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a115f-1073">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="a115f-1074">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a115f-1074">Header</span></span>                   | <span data-ttu-id="a115f-1075">WinHTTP. h</span><span class="sxs-lookup"><span data-stu-id="a115f-1075">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="a115f-1076">Confira também</span><span class="sxs-lookup"><span data-stu-id="a115f-1076">See also</span></span>

[<span data-ttu-id="a115f-1077">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a115f-1077">WinHTTP Versions</span></span>](winhttp-versions.md)
