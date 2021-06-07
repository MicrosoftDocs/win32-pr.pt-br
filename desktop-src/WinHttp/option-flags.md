---
Description: Os seguintes sinalizadores de opção têm suporte de WinHttpQueryOption e WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Sinalizadores de opção (WinHTTP. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: f9ca6b7c74d484a6bcac235b2396b2005c8c3260
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386675"
---
# <a name="option-flags"></a><span data-ttu-id="e233c-103">Sinalizadores de opção</span><span class="sxs-lookup"><span data-stu-id="e233c-103">Option Flags</span></span>

<span data-ttu-id="e233c-104">Os seguintes sinalizadores de opção têm suporte de [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span><span class="sxs-lookup"><span data-stu-id="e233c-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="e233c-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**\_opção WinHTTP \_ garantindo \_ \_ \_ retornos de chamada sem bloqueio**</span><span class="sxs-lookup"><span data-stu-id="e233c-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-106">O padrão é FALSE.</span><span class="sxs-lookup"><span data-stu-id="e233c-106">The default is FALSE.</span></span> <span data-ttu-id="e233c-107">Se definido como TRUE, o WinHTTP não garantirá o progresso se os retornos de chamada de status forem bloqueados pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="e233c-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="e233c-108">O aplicativo cliente deve tomar cuidado especial para executar operações mínimas no retorno de chamada sem bloqueio, retornando o mais rápido possível e, em particular, não deve esperar por nenhuma chamada de WinHTTP subsequente.</span><span class="sxs-lookup"><span data-stu-id="e233c-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="e233c-109">Se não seguir essas diretrizes, provavelmente haverá um impacto negativo no desempenho ou um possível travamento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e233c-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="e233c-110">Se usado da maneira prescrita, essa opção pode melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="e233c-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**política de WINHTTP da \_ opção de \_ logon automático \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-112">Define um valor inteiro longo sem sinal que especifica a [política de logon automática](authentication-in-winhttp.md) com um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e233c-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="e233c-113">Termo</span><span class="sxs-lookup"><span data-stu-id="e233c-113">Term</span></span> | <span data-ttu-id="e233c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e233c-114">Description</span></span> |
|-|-|
| <span data-ttu-id="e233c-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>nível de segurança do WINHTTP \_ AUTOlogonn \_ \_ \_ alto</span><span class="sxs-lookup"><span data-stu-id="e233c-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="e233c-116">As credenciais padrão não são usadas.</span><span class="sxs-lookup"><span data-stu-id="e233c-116">Default credentials are not used.</span></span> <span data-ttu-id="e233c-117">Observe que esse sinalizador só terá efeito se você especificar o servidor pelo nome real do computador.</span><span class="sxs-lookup"><span data-stu-id="e233c-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="e233c-118">Ele não entrará em vigor, se você especificar o servidor por "localhost" ou endereço IP.</span><span class="sxs-lookup"><span data-stu-id="e233c-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="e233c-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>nível de segurança do WINHTTP com \_ \_ acesso automático \_ \_ reduzido</span><span class="sxs-lookup"><span data-stu-id="e233c-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="e233c-120">Um logon autenticado usando as credenciais padrão é executado para todas as solicitações.</span><span class="sxs-lookup"><span data-stu-id="e233c-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="e233c-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>nível de segurança do WINHTTP com \_ logon automático \_ \_ \_ médio</span><span class="sxs-lookup"><span data-stu-id="e233c-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="e233c-122">Um logon autenticado usando as credenciais padrão é executado somente para solicitações na intranet local.</span><span class="sxs-lookup"><span data-stu-id="e233c-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="e233c-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**retorno de chamada de \_ opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-124">Recupera o ponteiro para a função de retorno de chamada definida com [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span><span class="sxs-lookup"><span data-stu-id="e233c-124">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**\_contexto de \_ certificado de cliente de opção WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-126">Define o contexto de certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="e233c-126">Sets the client certificate context.</span></span> <span data-ttu-id="e233c-127">Se um aplicativo receber [**o \_ certificado de autenticação de cliente WinHTTP de erro \_ \_ \_ \_ necessário**](error-messages.md), ele deverá chamar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para fornecer um certificado antes de repetir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e233c-127">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="e233c-128">Como parte do processamento dessa opção, o WinHttp chama [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) no contexto de certificado fornecido pelo chamador para que o contexto do certificado possa ser liberado independentemente pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e233c-128">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="e233c-129">O aplicativo não deve tentar fechar o repositório de certificados com o \_ sinalizador de \_ sinalizador de força de armazenamento de fechamento de certificado \_ \_ na chamada para [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) no repositório de certificados do qual o contexto de certificado foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="e233c-129">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="e233c-130">Pode ocorrer uma violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="e233c-130">An access violation may occur.</span></span>

<span data-ttu-id="e233c-131">Quando o servidor solicita um certificado de cliente, o [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)ou o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retorna um erro WinHTTP erro de [**certificado de \_ \_ \_ autenticação de \_ \_ cliente**](error-messages.md) .</span><span class="sxs-lookup"><span data-stu-id="e233c-131">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="e233c-132">Se o servidor solicitar o certificado, mas não o exigir, o aplicativo poderá especificar essa opção para indicar que ele não tem um certificado.</span><span class="sxs-lookup"><span data-stu-id="e233c-132">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="e233c-133">O servidor pode escolher outro esquema de autenticação ou permitir acesso anônimo ao servidor.</span><span class="sxs-lookup"><span data-stu-id="e233c-133">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="e233c-134">O aplicativo fornece a macro de **contexto de \_ \_ \_ certificado \_ de cliente do WinHTTP** no parâmetro *lpBuffer* de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="e233c-134">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="e233c-135">Se o servidor exigir um certificado de cliente, ele poderá enviar um código de status HTTP 403 em resposta.</span><span class="sxs-lookup"><span data-stu-id="e233c-135">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="e233c-136">Para obter mais informações, consulte **a \_ opção \_ WinHTTP \_ \_ \_ lista de emissor de certificado de cliente** .</span><span class="sxs-lookup"><span data-stu-id="e233c-136">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_opção WinHTTP \_ \_ lista de emissor de certificado de cliente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-138">Recupera uma [**estrutura SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) quando o erro de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) é um **erro \_ WinHTTP \_ Client \_ auth \_ CERT \_ necessário**.</span><span class="sxs-lookup"><span data-stu-id="e233c-138">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="e233c-139">A lista emissor na estrutura contém uma lista de autoridades de certificação aceitáveis (CA) do servidor.</span><span class="sxs-lookup"><span data-stu-id="e233c-139">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="e233c-140">O aplicativo cliente pode filtrar a lista de autoridades de certificação para recuperar o certificado do cliente para autenticação SSL.</span><span class="sxs-lookup"><span data-stu-id="e233c-140">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="e233c-141">Como alternativa, se o servidor solicitar o certificado do cliente, mas não precisar dele, o aplicativo poderá chamar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) com a opção **WinHTTP de contexto de \_ \_ \_ certificado \_ de cliente** .</span><span class="sxs-lookup"><span data-stu-id="e233c-141">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="e233c-142">Para obter mais informações, consulte opção **WinHTTP de contexto de certificado de \_ \_ cliente \_ \_ de opção** .</span><span class="sxs-lookup"><span data-stu-id="e233c-142">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**página de código da \_ opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-144">Define a [*página de código*](glossary.md) usada para processar a URL (ou seja, a cadeia de caracteres de consulta).</span><span class="sxs-lookup"><span data-stu-id="e233c-144">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="e233c-145">O padrão é UTF8.</span><span class="sxs-lookup"><span data-stu-id="e233c-145">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_opção WinHTTP \_ Configurar \_ autenticação do Passport \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-147">Define um valor inteiro longo sem sinal que especifica se a [autenticação do Passport na autenticação do WinHTTP](passport-authentication-in-winhttp.md) está habilitada.</span><span class="sxs-lookup"><span data-stu-id="e233c-147">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="e233c-148">O valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="e233c-148">The value can be one of the following:</span></span>

| <span data-ttu-id="e233c-149">Termo</span><span class="sxs-lookup"><span data-stu-id="e233c-149">Term</span></span> | <span data-ttu-id="e233c-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="e233c-150">Description</span></span> |
|-|-|
| <span data-ttu-id="e233c-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ desabilitar \_ autenticação do Passport \_</span><span class="sxs-lookup"><span data-stu-id="e233c-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="e233c-152">A autenticação Microsoft Passport está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="e233c-152">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="e233c-153">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="e233c-153">This is the default.</span></span> |
| <span data-ttu-id="e233c-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ desabilitar \_ o \_ keyring do Passport</span><span class="sxs-lookup"><span data-stu-id="e233c-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="e233c-155">O token de telefone do Passport está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e233c-155">The Passport keyring is disabled.</span></span> <span data-ttu-id="e233c-156">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="e233c-156">This is the default.</span></span> |
| <span data-ttu-id="e233c-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ habilitar \_ autenticação do Passport \_</span><span class="sxs-lookup"><span data-stu-id="e233c-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="e233c-158">A autenticação do Passport está habilitada.</span><span class="sxs-lookup"><span data-stu-id="e233c-158">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="e233c-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ habilitar \_ o \_ token de toque do Passport</span><span class="sxs-lookup"><span data-stu-id="e233c-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="e233c-160">O token de telefone do Passport está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e233c-160">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="e233c-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_ \_ novas tentativas de conexão de opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-162">Define ou recupera um valor inteiro longo sem sinal que contém o número de tentativas de timesWinHTTP para se conectar a um host.</span><span class="sxs-lookup"><span data-stu-id="e233c-162">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="e233c-163">O Microsoft Windows HTTP Services (WinHTTP) só tenta uma vez por endereço IP (Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="e233c-163">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="e233c-164">Por exemplo, se você tentar se conectar a um host de hospedagem múltipla que tem 10 endereços IP e **a \_ opção WinHTTP as \_ \_ repetições de conexão** estiver definida como 7, o WinHTTP tentará se conectar somente com o primeiro endereço IP sete.</span><span class="sxs-lookup"><span data-stu-id="e233c-164">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="e233c-165">Dado o mesmo conjunto de 10 endereços IP, se **a \_ opção WinHTTP \_ conectar \_ repetições** estiver definida como 20, o WinHTTP tentará cada uma das 10 somente uma vez.</span><span class="sxs-lookup"><span data-stu-id="e233c-165">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="e233c-166">Se uma tentativa de conexão ainda falhar após o número especificado de tentativas ou se o tempo limite de conexão expirar antes de então, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="e233c-166">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="e233c-167">O valor padrão para **as \_ \_ \_ repetições de conexão de opção de WinHTTP** é cinco tentativas.</span><span class="sxs-lookup"><span data-stu-id="e233c-167">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**\_ \_ tempo limite de conexão da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-169">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="e233c-169">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="e233c-170">Definir essa opção como infinito (0xFFFFFFFF) desabilitará esse temporizador.</span><span class="sxs-lookup"><span data-stu-id="e233c-170">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="e233c-171">Se uma solicitação de conexão TCP demorar mais do que esse valor de tempo limite, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="e233c-171">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="e233c-172">O tempo limite padrão é de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="e233c-172">The default timeout is 60 seconds.</span></span> <span data-ttu-id="e233c-173">Quando você está tentando se conectar a vários endereços IP para um único host (um host de hospedagem múltipla), o tempo limite é para cada conexão individual.</span><span class="sxs-lookup"><span data-stu-id="e233c-173">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**\_informações de \_ conexão da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-175">Recupera o endereço IP de origem e de destino e a porta da solicitação que gerou a resposta quando [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retorna.</span><span class="sxs-lookup"><span data-stu-id="e233c-175">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="e233c-176">O aplicativo chama [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) com a opção de **\_ informações de \_ conexão \_ da opção WinHTTP** e fornece a estrutura de [**informações de \_ conexão \_ WinHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) no parâmetro *lpBuffer* .</span><span class="sxs-lookup"><span data-stu-id="e233c-176">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="e233c-177">Para obter mais informações, **consulte \_ \_ informações de conexão do WinHTTP**.</span><span class="sxs-lookup"><span data-stu-id="e233c-177">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="e233c-178">**Windows Server 2003 com SP1 e Windows XP com SP2:** Este sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="e233c-178">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**\_V0 de \_ Estatísticas de conexão da opção WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-180">Recupera o [**struct \_ \_ V0 de informações de TCP**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) para a conexão subjacente usada pela solicitação.</span><span class="sxs-lookup"><span data-stu-id="e233c-180">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="e233c-181">A estrutura retornada pode conter estatísticas de solicitações anteriores enviadas pela mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="e233c-181">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="e233c-182">Esta opção foi substituída por **WinHTTP \_ Option \_ Connection \_ stats \_ v1**.</span><span class="sxs-lookup"><span data-stu-id="e233c-182">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**\_Estatísticas de conexão da opção WinHTTP \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="e233c-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-184">Recupera a estrutura de [**informações do TCP \_ \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) para a conexão subjacente usada pela solicitação.</span><span class="sxs-lookup"><span data-stu-id="e233c-184">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="e233c-185">A estrutura retornada pode conter estatísticas de solicitações anteriores enviadas pela mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="e233c-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**\_valor de \_ contexto da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-187">Define ou recupera um **\_ PTR de DWORD** que contém um ponteiro para o valor de contexto associado a esse identificador [HINTERNET](hinternet-handles-in-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="e233c-187">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="e233c-188">O valor armazenado no buffer é usado e o sinalizador de opção de **\_ valor de \_ contexto \_ de opção WinHTTP** recebe um novo valor.</span><span class="sxs-lookup"><span data-stu-id="e233c-188">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**\_DEScompactação da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-190">Define um DWORD de sinalizadores que determinam se o WinHTTP irá descompactar automaticamente os corpos de resposta com codificações de conteúdo compactadas.</span><span class="sxs-lookup"><span data-stu-id="e233c-190">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="e233c-191">O WinHTTP também definirá um cabeçalho de Accept-Encoding apropriado, substituindo qualquer um fornecido pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e233c-191">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="e233c-192">Os valores com suporte são:</span><span class="sxs-lookup"><span data-stu-id="e233c-192">Supported values are:</span></span>

| <span data-ttu-id="e233c-193">Termo</span><span class="sxs-lookup"><span data-stu-id="e233c-193">Term</span></span> | <span data-ttu-id="e233c-194">Descrição</span><span class="sxs-lookup"><span data-stu-id="e233c-194">Description</span></span> |
|-|-|
| <span data-ttu-id="e233c-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_sinalizador de DEScompactação de WinHTTP \_ \_ gzip</span><span class="sxs-lookup"><span data-stu-id="e233c-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="e233c-196">Descompactar conteúdo-codificação: respostas gzip.</span><span class="sxs-lookup"><span data-stu-id="e233c-196">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="e233c-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>\_sinalizador de DEScompactação WinHTTP \_ \_ deflate</span><span class="sxs-lookup"><span data-stu-id="e233c-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="e233c-198">Descompactar conteúdo-codificação: reinflar respostas.</span><span class="sxs-lookup"><span data-stu-id="e233c-198">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="e233c-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_sinalizador de DEScompactação de WinHTTP \_ \_ All</span><span class="sxs-lookup"><span data-stu-id="e233c-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="e233c-200">Descompacte as respostas com qualquer codificação de conteúdo com suporte.</span><span class="sxs-lookup"><span data-stu-id="e233c-200">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="e233c-201">Por padrão, o WinHTTP fornecerá respostas compactadas ao chamador sem modificações.</span><span class="sxs-lookup"><span data-stu-id="e233c-201">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**RECURSO DESABILITAR OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-203">Define um valor inteiro longo sem sinal que especifica quais recursos estão desabilitados com um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e233c-203">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="e233c-204">Esteja ciente de que esse recurso só deve ser passado para [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) em alças de solicitação depois que o handle de solicitação é criado com [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)e antes que a solicitação seja enviada com [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="e233c-204">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="e233c-205">Termo</span><span class="sxs-lookup"><span data-stu-id="e233c-205">Term</span></span> | <span data-ttu-id="e233c-206">Descrição</span><span class="sxs-lookup"><span data-stu-id="e233c-206">Description</span></span> |
|-|-|
| <span data-ttu-id="e233c-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>DESABILITAR AUTENTICAÇÃO DO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="e233c-208">A autenticação automática está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="e233c-208">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="e233c-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>DESABILITAR COOKIES WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="e233c-210">A adição automática de headers de cookie às solicitações está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="e233c-210">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="e233c-211">Além disso, os cookies retornados não são adicionados automaticamente ao banco de dados de cookie.</span><span class="sxs-lookup"><span data-stu-id="e233c-211">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="e233c-212">Desabilitar cookies pode resultar em baixo desempenho para autenticação do Passport.</span><span class="sxs-lookup"><span data-stu-id="e233c-212">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="e233c-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE</span><span class="sxs-lookup"><span data-stu-id="e233c-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="e233c-214">Desabilita a semântica keep alive para a conexão.</span><span class="sxs-lookup"><span data-stu-id="e233c-214">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="e233c-215">A semântica keep alive é necessária para MSN, NTLM e outros tipos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="e233c-215">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="e233c-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>DESABILITAR \_ REDIRECIONAMENTOS DO WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="e233c-217">O redirecionamento automático é desabilitado ao enviar solicitações [**com WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="e233c-217">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="e233c-218">Se o redirecionamento automático estiver desabilitado, um aplicativo deverá registrar uma função de retorno de chamada para que a autenticação do Passport seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e233c-218">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="e233c-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**OPÇÃO WINHTTP \_ \_ DESABILITAR \_ \_ FALLBACK DE \_ PROTOCOLO SEGURO**</span><span class="sxs-lookup"><span data-stu-id="e233c-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-220">Impede que o WinHTTP repetir uma conexão com uma versão inferior do protocolo de segurança quando a negociação de protocolo inicial falhar.</span><span class="sxs-lookup"><span data-stu-id="e233c-220">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**OPÇÃO WINHTTP \_ \_ DESABILITAR \_ FILA DE \_ FLUXO**</span><span class="sxs-lookup"><span data-stu-id="e233c-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-222">Permite que novas solicitações abram uma conexão HTTP/2 adicional quando o limite máximo de fluxo simultâneo for atingido, em vez de aguardar o próximo fluxo disponível em uma conexão existente.</span><span class="sxs-lookup"><span data-stu-id="e233c-222">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**RECURSO \_ HABILITAR OPÇÃO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-224">Define um valor inteiro longo sem sinal que especifica os recursos atualmente habilitados.</span><span class="sxs-lookup"><span data-stu-id="e233c-224">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="e233c-225">Pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e233c-225">Can be one of the following values.</span></span>

| <span data-ttu-id="e233c-226">Termo</span><span class="sxs-lookup"><span data-stu-id="e233c-226">Term</span></span> | <span data-ttu-id="e233c-227">Descrição</span><span class="sxs-lookup"><span data-stu-id="e233c-227">Description</span></span> |
|-|-|
| <span data-ttu-id="e233c-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION</span><span class="sxs-lookup"><span data-stu-id="e233c-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="e233c-229">Se habilitada, o WinHTTP reverte temporariamente a representação do cliente durante as operações de autenticação de certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="e233c-229">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="e233c-230">Esse valor pode ser definido somente no alça de sessão.</span><span class="sxs-lookup"><span data-stu-id="e233c-230">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="e233c-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ \_ HABILITAR \_ REVOGAÇÃO DE SSL</span><span class="sxs-lookup"><span data-stu-id="e233c-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="e233c-232">Se habilitada, o WinHTTP permite a revogação de SSL.</span><span class="sxs-lookup"><span data-stu-id="e233c-232">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="e233c-233">Esse valor pode ser definido somente no alça de solicitação.</span><span class="sxs-lookup"><span data-stu-id="e233c-233">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**OPÇÃO WINHTTP \_ \_ HABILITAR \_ PROTOCOLO HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-235">Define uma máscara de bits DWORD de versões HTTP avançadas aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="e233c-235">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="e233c-236">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="e233c-236">Possible values are:</span></span>

| <span data-ttu-id="e233c-237">Termo</span><span class="sxs-lookup"><span data-stu-id="e233c-237">Term</span></span> | <span data-ttu-id="e233c-238">Descrição</span><span class="sxs-lookup"><span data-stu-id="e233c-238">Description</span></span> |
|-|-|
| <span data-ttu-id="e233c-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>SINALIZADOR DE PROTOCOLO WINHTTP \_ \_ \_ HTTP2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="e233c-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="e233c-240">Habilita HTTP/2 para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e233c-240">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="e233c-241">Nenhum (0x0)</span><span class="sxs-lookup"><span data-stu-id="e233c-241">None (0x0)</span></span> | <span data-ttu-id="e233c-242">Restringe a solicitação a HTTP/1.1 e anterior.</span><span class="sxs-lookup"><span data-stu-id="e233c-242">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="e233c-243">As versões herdadas do HTTP (1.1 e anteriores) não podem ser desabilitadas usando essa opção.</span><span class="sxs-lookup"><span data-stu-id="e233c-243">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="e233c-244">O padrão é 0x0.</span><span class="sxs-lookup"><span data-stu-id="e233c-244">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-245"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**OPÇÃO WINHTTP \_ \_ ENABLETRACING**</span><span class="sxs-lookup"><span data-stu-id="e233c-245"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-246">Define um **valor BOOL** que especifica se o rastreamento está habilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="e233c-246">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="e233c-247">Para obter mais informações sobre o recurso de rastreamento no WinHTTP, consulte [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="e233c-247">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="e233c-248">Essa opção só pode ser definida em um handle  **HINTERNET NULL.**</span><span class="sxs-lookup"><span data-stu-id="e233c-248">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="e233c-249"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**CODIFICAR EXTRA DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-249"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-250">Habilita a codificação de porcentagem de URL para caminho e cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="e233c-250">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="e233c-251">Como alternativa, você pode codificar por porcentagem antes de chamar WinHttp.</span><span class="sxs-lookup"><span data-stu-id="e233c-251">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="e233c-252"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP \_ OPTION \_ EXPIRE \_ CONNECTION**</span><span class="sxs-lookup"><span data-stu-id="e233c-252"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-253">Essa opção só pode ser definida em um handle de solicitação que ainda esteja ativo (envio ou recebimento).</span><span class="sxs-lookup"><span data-stu-id="e233c-253">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="e233c-254">Definir essa opção dirá ao WinHttp para parar de atender às solicitações na conexão associada ao handle de solicitação passado.</span><span class="sxs-lookup"><span data-stu-id="e233c-254">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="e233c-255">A conexão será fechada depois que o lidar com a solicitação com a qual essa opção é chamada for concluída.</span><span class="sxs-lookup"><span data-stu-id="e233c-255">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="e233c-256">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e233c-256">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-257"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**ERRO ESTENDIDO DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-257"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-258">Recupera um valor inteiro longo sem sinal que contém um código de erro do Microsoft Windows Sockets mapeado para as mensagens de erro ERROR WINHTTP retornadas pela última vez neste \_ \_ \* contexto de thread.</span><span class="sxs-lookup"><span data-stu-id="e233c-258">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="e233c-259">Você pode passar **NULL** como o valor do handle.</span><span class="sxs-lookup"><span data-stu-id="e233c-259">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-260"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**CREDS DE \_ \_ PROXY GLOBAL DA \_ OPÇÃO WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-260"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-261">Leva um ponteiro para uma [**estrutura WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) com o *parâmetro de função hInternet* definido como **NULL.**</span><span class="sxs-lookup"><span data-stu-id="e233c-261">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="e233c-262">Essa opção requer a chave do Registro **HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp.**</span><span class="sxs-lookup"><span data-stu-id="e233c-262">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="e233c-263">Se essa chave do Registro não estiver definida, WinHTTP retornará o **erro \_ ERRO WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="e233c-263">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="e233c-264">Essa chave do Registro não está presente por padrão.</span><span class="sxs-lookup"><span data-stu-id="e233c-264">This registry key is not present by default.</span></span> <span data-ttu-id="e233c-265">Quando estiver definido, o WinINet enviará credenciais para WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="e233c-265">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="e233c-266">Sempre que o WinHttp receber um desafio de autenticação e se não houver credenciais definidas no alçamento atual, ele usará as credenciais fornecidas pelo WinINet.</span><span class="sxs-lookup"><span data-stu-id="e233c-266">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="e233c-267">Para compartilhar credenciais de servidor, além de credenciais de proxy, os usuários precisam definir **WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** .</span><span class="sxs-lookup"><span data-stu-id="e233c-267">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-268"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**CREDS DE SERVIDOR GLOBAL DA OPÇÃO WINHTTP \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-268"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-269">Leva um ponteiro para uma [**estrutura WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) com o *parâmetro de função hInternet* definido como **NULL.**</span><span class="sxs-lookup"><span data-stu-id="e233c-269">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="e233c-270">Essa opção requer a chave do Registro **HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp.**</span><span class="sxs-lookup"><span data-stu-id="e233c-270">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="e233c-271">Se essa chave do Registro não estiver definida, WinHTTP retornará o **erro \_ ERRO WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="e233c-271">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="e233c-272">Essa chave do Registro não está presente por padrão.</span><span class="sxs-lookup"><span data-stu-id="e233c-272">This registry key is not present by default.</span></span> <span data-ttu-id="e233c-273">Quando estiver definido, o WinINet enviará credenciais para WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="e233c-273">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="e233c-274">Sempre que o WinHttp receber um desafio de autenticação e se não houver credenciais definidas no alçamento atual, ele usará as credenciais fornecidas pelo WinINet.</span><span class="sxs-lookup"><span data-stu-id="e233c-274">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="e233c-275">Para compartilhar credenciais de servidor, além de credenciais de proxy, os usuários precisam definir **WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** .</span><span class="sxs-lookup"><span data-stu-id="e233c-275">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-276"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**TIPO DE \_ IDENTIFICADOR DE OPÇÃO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-276"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-277">Recupera um valor inteiro longo sem sinal que contém o tipo do identificador [HINTERNET](hinternet-handles-in-winhttp.md) passado.</span><span class="sxs-lookup"><span data-stu-id="e233c-277">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="e233c-278">O valor de retorno pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="e233c-278">The return value can be one of the following:</span></span>

| <span data-ttu-id="e233c-279">Termo</span><span class="sxs-lookup"><span data-stu-id="e233c-279">Term</span></span> | <span data-ttu-id="e233c-280">Descrição</span><span class="sxs-lookup"><span data-stu-id="e233c-280">Description</span></span> |
|-|-|
| <span data-ttu-id="e233c-281"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>TIPO DE IDENTIFICADOR WINHTTP \_ \_ \_ CONNECT</span><span class="sxs-lookup"><span data-stu-id="e233c-281"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="e233c-282">O handle é um alça de conexão.</span><span class="sxs-lookup"><span data-stu-id="e233c-282">The handle is a connection handle.</span></span> |
| <span data-ttu-id="e233c-283"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>SOLICITAÇÃO DE TIPO \_ DE \_ IDENTIFICADOR WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-283"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="e233c-284">O handle é um alça de solicitação.</span><span class="sxs-lookup"><span data-stu-id="e233c-284">The handle is a request handle.</span></span> |
| <span data-ttu-id="e233c-285"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>SESSÃO DE TIPO \_ DE \_ IDENTIFICADOR WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-285"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="e233c-286">O handle é um alça de sessão.</span><span class="sxs-lookup"><span data-stu-id="e233c-286">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="e233c-287"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP \_ OPTION \_ HTTP \_ PROTOCOL \_ REQUIRED**</span><span class="sxs-lookup"><span data-stu-id="e233c-287"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-288">Impede que versões de protocolo diferentes daquelas habilitadas por **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL** seja usada para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e233c-288">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP \_ OPTION \_ HTTP \_ PROTOCOL \_ USED**</span><span class="sxs-lookup"><span data-stu-id="e233c-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-290">Obtém um DWORD que indica qual versão HTTP avançada foi usada em uma determinada solicitação.</span><span class="sxs-lookup"><span data-stu-id="e233c-290">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="e233c-291">Para ver uma lista de valores possíveis, consulte **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL**.</span><span class="sxs-lookup"><span data-stu-id="e233c-291">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-292"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP \_ OPTION \_ HTTP \_ VERSION**</span><span class="sxs-lookup"><span data-stu-id="e233c-292"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-293">Define ou recupera uma estrutura [**HTTP \_ VERSION \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) que contém a versão HTTP com suporte.</span><span class="sxs-lookup"><span data-stu-id="e233c-293">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="e233c-294">Essa é uma opção em todo o processo; use **NULL** para o handle.</span><span class="sxs-lookup"><span data-stu-id="e233c-294">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-295"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**OPÇÃO WINHTTP \_ \_ IGNORAR \_ \_ REVOGAÇÃO DE CERTIFICADO \_ OFFLINE**</span><span class="sxs-lookup"><span data-stu-id="e233c-295"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-296">Permite que as conexões seguras usem certificados de segurança para os quais a lista de certificados revogados não pôde ser baixada.</span><span class="sxs-lookup"><span data-stu-id="e233c-296">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-297"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**FALLBACK RÁPIDO \_ \_ DE IPV6 \_ DA OPÇÃO WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-297"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-298">Habilita o fallback rápido de IPv6 (Desamarros Desamarros) para a conexão.</span><span class="sxs-lookup"><span data-stu-id="e233c-298">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="e233c-299">Esse comportamento é semelhante ao comportamento de Feliz Buscas descrito em [RFC 6555](https://tools.ietf.org/html/rfc6555) para melhorar os tempos de conexão em redes em que iPv6 não é confiável.</span><span class="sxs-lookup"><span data-stu-id="e233c-299">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="e233c-300">Se os endereços IPv6 e IPv4 são resolvidos para um determinado host, o WinHttp começará conectando-se ao primeiro endereço IPv6 resolvido com um tempo de tempo de curto (300 ms).</span><span class="sxs-lookup"><span data-stu-id="e233c-300">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="e233c-301">Se essa conexão falhar, o WinHttp tentará se conectar ao primeiro endereço IPv4 resolvido com o tempo de vida padrão.</span><span class="sxs-lookup"><span data-stu-id="e233c-301">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="e233c-302">Se a segunda conexão falhar, o WinHttp repetirá o primeiro endereço IPv6 resolvido com o tempo de vida padrão.</span><span class="sxs-lookup"><span data-stu-id="e233c-302">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="e233c-303">Se a terceira conexão falhar, o WinHttp será revertido para o comportamento padrão para quaisquer endereços restantes, tentando uma conexão com cada um deles com o tempo de vida padrão até que uma conexão seja feita ou nenhum endereço permaneça.</span><span class="sxs-lookup"><span data-stu-id="e233c-303">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-304"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**A OPÇÃO \_ WINHTTP É PROXY CONNECT \_ \_ \_ \_ RESPONSE**</span><span class="sxs-lookup"><span data-stu-id="e233c-304"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-305">Obtém se uma Resposta de Conexão de Retorno de Proxy pode ou não ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="e233c-305">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-306"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP \_ OPTION \_ MAX \_ CONNS \_ PER \_ 1 \_ 0 \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="e233c-306"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-307">Define ou recupera um valor inteiro longo sem sinal que contém o número máximo de conexões permitidas por servidor HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="e233c-307">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="e233c-308">O valor padrão é **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="e233c-308">The default value is **INFINITE**.</span></span>

<span data-ttu-id="e233c-309">**Windows Vista com SP1 e Windows Server 2008:** Esse sinalizador está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="e233c-309">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-310"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**OPÇÃO WINHTTP \_ \_ MAX \_ CONNS POR \_ \_ SERVIDOR**</span><span class="sxs-lookup"><span data-stu-id="e233c-310"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-311">Define ou recupera um valor inteiro longo sem sinal que contém o número máximo de conexões permitidas por servidor.</span><span class="sxs-lookup"><span data-stu-id="e233c-311">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="e233c-312">O valor padrão é **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="e233c-312">The default value is **INFINITE**.</span></span>

<span data-ttu-id="e233c-313">Quando essa opção é definida como zero, o WinHTTP define o limite no número de conexões como 2.</span><span class="sxs-lookup"><span data-stu-id="e233c-313">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-314"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**REDIRECIONAMENTOS \_ AUTOMÁTICOS \_ DE HTTP MÁXIMO DA \_ \_ \_ OPÇÃO WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="e233c-314"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-315">Define o número máximo de redirecionamentos que o WinHTTP segue; o padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="e233c-315">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="e233c-316">Esse limite impede que sites não autorizados pausem o cliente WinHTTP após um grande número de redirecionamentos.</span><span class="sxs-lookup"><span data-stu-id="e233c-316">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="e233c-317">**Windows XP com SP1 e Windows 2000 com SP3:** Esse sinalizador está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="e233c-317">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-318"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP \_ OPTION \_ MAX \_ HTTP \_ STATUS \_ CONTINUE**</span><span class="sxs-lookup"><span data-stu-id="e233c-318"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-319">O número máximo de respostas de código de status informativas 100-199 ignoradas antes de retornar o código de status final para o cliente WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="e233c-319">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="e233c-320">Códigos de status informacionais 100-199 podem ser enviados pelo servidor antes do código de status final e são descritos na especificação para HTTP/1.1 (para obter mais informações, [consulte RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span><span class="sxs-lookup"><span data-stu-id="e233c-320">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="e233c-321">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="e233c-321">The default is 10.</span></span>

<span data-ttu-id="e233c-322">**Windows XP com SP1 e Windows 2000 com SP3:** Esse sinalizador está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="e233c-322">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-323"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="e233c-323"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-324">Um limite na quantidade de dados esvaziados de respostas para reutilizar uma conexão, especificada em bytes.</span><span class="sxs-lookup"><span data-stu-id="e233c-324">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="e233c-325">O padrão é 1 MB.</span><span class="sxs-lookup"><span data-stu-id="e233c-325">The default is 1MB.</span></span>

<span data-ttu-id="e233c-326">**Windows XP com SP1 e Windows 2000 com SP3:** Esse sinalizador está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="e233c-326">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-327"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**TAMANHO MÁXIMO \_ DO \_ \_ \_ HEADER DE RESPOSTA DA \_ OPÇÃO WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="e233c-327"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-328">Um conjunto de limites no tamanho máximo da parte do header da resposta do servidor, especificado em bytes.</span><span class="sxs-lookup"><span data-stu-id="e233c-328">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="e233c-329">Esse limite protege o cliente de um servidor não autorizado que tenta parar o cliente enviando uma resposta com uma quantidade infinita de dados de header.</span><span class="sxs-lookup"><span data-stu-id="e233c-329">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="e233c-330">O valor padrão é 64KB.</span><span class="sxs-lookup"><span data-stu-id="e233c-330">The default value is 64KB.</span></span>

<span data-ttu-id="e233c-331">**Windows XP com SP1 e Windows 2000 com SP3:** Esse sinalizador está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="e233c-331">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-332"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP \_ OPTION \_ PARENT \_ HANDLE**</span><span class="sxs-lookup"><span data-stu-id="e233c-332"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-333">Recupera o alça pai para esse alça.</span><span class="sxs-lookup"><span data-stu-id="e233c-333">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-334"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP \_ OPTION \_ PASSPORT \_ COBRANDING \_ TEXT**</span><span class="sxs-lookup"><span data-stu-id="e233c-334"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-335">Recupera uma cadeia de caracteres que contém o [*texto de*](glossary.md) cobrança fornecido pelo servidor de logon do Passport.</span><span class="sxs-lookup"><span data-stu-id="e233c-335">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="e233c-336">Essa opção deve ser recuperada imediatamente após o servidor de logon responder com um código de status 401.</span><span class="sxs-lookup"><span data-stu-id="e233c-336">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="e233c-337">Um aplicativo deve passar um tamanho de buffer, em bytes, que é grande o suficiente para manter a cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="e233c-337">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-338"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP \_ OPTION \_ PASSPORT \_ COBRANDING \_ URL**</span><span class="sxs-lookup"><span data-stu-id="e233c-338"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-339">Recupera uma cadeia de caracteres que contém uma URL para um gráfico [*de*](glossary.md) cobra fornecido pelo servidor de logon do Passport.</span><span class="sxs-lookup"><span data-stu-id="e233c-339">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="e233c-340">Essa opção deve ser recuperada imediatamente após o servidor de logon responder com um código de status 401.</span><span class="sxs-lookup"><span data-stu-id="e233c-340">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="e233c-341">Um aplicativo deve passar um tamanho de buffer, em bytes, que é grande o suficiente para manter a cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="e233c-341">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-342"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**URL DE RETORNO \_ DO \_ PASSPORT DA OPÇÃO \_ WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-342"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-343">Define uma opção somente leitura em um alça de solicitação que recupera a URL de retorno do Passport.</span><span class="sxs-lookup"><span data-stu-id="e233c-343">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-344"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP \_ OPTION \_ PASSPORT \_ SIGN \_ OUT**</span><span class="sxs-lookup"><span data-stu-id="e233c-344"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-345">Define a opção em um alça de sessão para sair de qualquer logon do Passport.</span><span class="sxs-lookup"><span data-stu-id="e233c-345">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="e233c-346">Um aplicativo deve passar a URL de retorno do Passport que foi recuperada com a URL DE RETORNO DO **PASSPORT DA OPÇÃO \_ \_ \_ \_ WINHTTP.**</span><span class="sxs-lookup"><span data-stu-id="e233c-346">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="e233c-347">Todos os cookies relacionados à URL de retorno são limpos.</span><span class="sxs-lookup"><span data-stu-id="e233c-347">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-348"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**SENHA DA OPÇÃO \_ WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-348"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-349">Define ou recupera um valor de cadeia de caracteres que contém a senha associada a um handle de solicitação.</span><span class="sxs-lookup"><span data-stu-id="e233c-349">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-350"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**PROXY DE OPÇÃO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-350"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-351">Define ou recupera uma estrutura [**WINHTTP \_ PROXY \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contém os dados de proxy em um handle de sessão existente ou no alça de solicitação.</span><span class="sxs-lookup"><span data-stu-id="e233c-351">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="e233c-352">Ao recuperar dados de proxy, um aplicativo deve liberar as cadeias de caracteres **lpszProxy** e **lpszProxyBypass** contidas nessa estrutura (se elas não são **NULL**) usando a [**função GlobalFree.**](/windows/desktop/api/winbase/nf-winbase-globalfree)</span><span class="sxs-lookup"><span data-stu-id="e233c-352">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="e233c-353">Um aplicativo pode consultar os dados de proxy global (o proxy padrão) passando um **alça NULL.**</span><span class="sxs-lookup"><span data-stu-id="e233c-353">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-354"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**SENHA DE PROXY DE OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-354"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-355">Define ou recupera um valor de cadeia de caracteres que contém a senha usada para acessar o proxy.</span><span class="sxs-lookup"><span data-stu-id="e233c-355">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-356"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**SPN DE \_ PROXY DE OPÇÃO \_ \_ WINHTTP \_ USADO**</span><span class="sxs-lookup"><span data-stu-id="e233c-356"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-357">Obtém o nome principal do servidor proxy fornecido pelo WinHTTP ao SSPI durante a autenticação.</span><span class="sxs-lookup"><span data-stu-id="e233c-357">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="e233c-358">Esse valor de cadeia de caracteres é usadopara passar [**para SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) após uma falha de autenticação.</span><span class="sxs-lookup"><span data-stu-id="e233c-358">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-359"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**NOME DE USUÁRIO DO PROXY DE OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-359"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-360">Define ou recupera um valor de cadeia de caracteres que contém o nome de usuário usado para acessar o proxy.</span><span class="sxs-lookup"><span data-stu-id="e233c-360">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-361"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**TAMANHO DO \_ BUFFER DE LEITURA DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-361"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-362">Essa opção foi preterida; ele não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="e233c-362">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-363"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**RESPOSTA DE CONEXÃO DE \_ \_ PROXY DE RECEBIMENTO DA \_ \_ \_ OPÇÃO WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="e233c-363"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-364">Define se a entidade de resposta proxy pode ou não ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="e233c-364">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="e233c-365">Essa opção está desabilitada por padrão.</span><span class="sxs-lookup"><span data-stu-id="e233c-365">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-366"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP \_ OPTION \_ RECEIVE \_ RESPONSE \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="e233c-366"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-367">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempoout, em milissegundos, para aguardar para receber todos os headers de resposta para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="e233c-367">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="e233c-368">Se o WinHTTP não receber todos os títulos dentro desse período, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="e233c-368">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="e233c-369">O valor de tempo-máximo padrão é de 90 segundos.</span><span class="sxs-lookup"><span data-stu-id="e233c-369">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="e233c-370">Esse tempoout é verificado somente quando os dados são recebidos do soquete.</span><span class="sxs-lookup"><span data-stu-id="e233c-370">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="e233c-371">Como resultado, quando o tempo expirar, o aplicativo cliente não será notificado até que mais dados cheguem do servidor.</span><span class="sxs-lookup"><span data-stu-id="e233c-371">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="e233c-372">Se nenhum dado chegar do servidor, o atraso entre a expiração de tempo e a notificação do aplicativo cliente poderá ser tão grande quanto o valor de tempoout definido usando o parâmetro *dwReceiveTimeout* da função [**WinHttpSetTimeouts.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)</span><span class="sxs-lookup"><span data-stu-id="e233c-372">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-373"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP \_ OPTION \_ RECEIVE \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="e233c-373"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-374">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo-máximo, em milissegundos, para receber uma resposta parcial a uma solicitação ou ler alguns dados.</span><span class="sxs-lookup"><span data-stu-id="e233c-374">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="e233c-375">Se a resposta demorar mais do que esse valor de tempo-máximo, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="e233c-375">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="e233c-376">O valor do tempo limite padrão é de 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="e233c-376">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-377"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**POLÍTICA DE \_ REDIRECIONAMENTO DE OPÇÃO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-377"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-378">Define o comportamento do WinHTTP em relação à manipulação de um código de status de redirecionamento HTTP 30x.</span><span class="sxs-lookup"><span data-stu-id="e233c-378">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="e233c-379">Essa opção pode ser definida em uma sessão ou no handle de solicitação para um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="e233c-379">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="e233c-380">Termo</span><span class="sxs-lookup"><span data-stu-id="e233c-380">Term</span></span> | <span data-ttu-id="e233c-381">Descrição</span><span class="sxs-lookup"><span data-stu-id="e233c-381">Description</span></span> |
|-|-|
| <span data-ttu-id="e233c-382"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>POLÍTICA DE REDIRECIONAMENTO DE OPÇÃO WINHTTP \_ \_ \_ \_ SEMPRE</span><span class="sxs-lookup"><span data-stu-id="e233c-382"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="e233c-383">Todos os redirecionamentos são seguidos automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e233c-383">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="e233c-384"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>A POLÍTICA DE REDIRECIONAMENTO DE OPÇÃO WINHTTP \_ \_ NÃO PERMITE \_ \_ \_ HTTPS PARA \_ \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="e233c-384"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="e233c-385">Todos os redirecionamentos são seguidos, exceto aqueles originados de uma URL segura (https) para uma URL não segura (http).</span><span class="sxs-lookup"><span data-stu-id="e233c-385">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="e233c-386">Essa é a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="e233c-386">This is the default setting.</span></span> |
| <span data-ttu-id="e233c-387"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>POLÍTICA DE REDIRECIONAMENTO DE OPÇÃO WINHTTP \_ \_ \_ \_ NUNCA</span><span class="sxs-lookup"><span data-stu-id="e233c-387"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="e233c-388">Os redirecionamentos nunca são seguidos.</span><span class="sxs-lookup"><span data-stu-id="e233c-388">Redirects are never followed.</span></span> <span data-ttu-id="e233c-389">O status 30x é retornado ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e233c-389">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-390"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**OPÇÃO WINHTTP \_ REJEITAR \_ \_ USERPWD \_ NA \_ URL**</span><span class="sxs-lookup"><span data-stu-id="e233c-390"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-391">Rejeita URLs que contêm um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="e233c-391">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="e233c-392">Essa opção também rejeita URLs que contêm a semântica *username:password,* mesmo se nenhum nome de usuário ou senha for especificado.</span><span class="sxs-lookup"><span data-stu-id="e233c-392">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="e233c-393">Por exemplo, " u:p@hostname ", " ", " " e " " seriam :@hostname u:@hostname :p@hostname sinalizados como inválidos.</span><span class="sxs-lookup"><span data-stu-id="e233c-393">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="e233c-394">Se uma URL inválida for passada para a função, ela [retornará ERROR \_ WINHTTP \_ INVALID \_ URL](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="e233c-394">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="e233c-395">Essa opção é desativada por padrão.</span><span class="sxs-lookup"><span data-stu-id="e233c-395">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-396"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**PRIORIDADE DE \_ SOLICITAÇÃO DE OPÇÃO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-396"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-397">Essa opção foi preterida; ele não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="e233c-397">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-398"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**ESTATÍSTICAS DE \_ SOLICITAÇÃO DE OPÇÃO \_ WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-398"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-399">Retreives estatísticas para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e233c-399">Retreives statistics for the request.</span></span>  <span data-ttu-id="e233c-400">Para ver uma lista das estatísticas disponíveis, consulte [**ESTATÍSTICAS DE SOLICITAÇÃO \_ \_ WINHTTP.**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)</span><span class="sxs-lookup"><span data-stu-id="e233c-400">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-401"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**\_tempos de \_ solicitação de opção de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-401"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-402">Recupera informações de tempo para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e233c-402">Retreives timing information for the request.</span></span> <span data-ttu-id="e233c-403">Para obter uma lista dos intervalos disponíveis, confira [**\_ \_ tempos de solicitação do WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span><span class="sxs-lookup"><span data-stu-id="e233c-403">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-404"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**\_opção WinHTTP \_ resolver \_ tempo limite**</span><span class="sxs-lookup"><span data-stu-id="e233c-404"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-405">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos, para resolver um nome de host.</span><span class="sxs-lookup"><span data-stu-id="e233c-405">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="e233c-406">O valor de tempo limite padrão é **infinito**.</span><span class="sxs-lookup"><span data-stu-id="e233c-406">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="e233c-407">Se um valor não padrão for especificado, haverá uma sobrecarga de uma criação de thread por resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="e233c-407">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-408"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**\_protocolos de \_ segurança de opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-408"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-409">Define um valor inteiro longo sem sinal que especifica quais protocolos seguros são aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="e233c-409">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="e233c-410">Por padrão, somente SSL3 e TLS1 são habilitados no Windows 7 e no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e233c-410">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="e233c-411">Por padrão, somente SSL3, TLS 1.0, TLS 1.1 e TLS 1.2 estão habilitados no Windows 8.1 e no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e233c-411">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="e233c-412">O valor pode ser uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e233c-412">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="e233c-413">Termo</span><span class="sxs-lookup"><span data-stu-id="e233c-413">Term</span></span> | <span data-ttu-id="e233c-414">Descrição</span><span class="sxs-lookup"><span data-stu-id="e233c-414">Description</span></span> |
|-|-|
| <span data-ttu-id="e233c-415"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>\_sinalizador WinHTTP \_ - \_ \_ todos os protocolos seguros</span><span class="sxs-lookup"><span data-stu-id="e233c-415"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="e233c-416">Os protocolos protocolo SSL (SSL) 2,0, SSL 3,0 e protocolo TLS 1,0 podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="e233c-416">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="e233c-417"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>\_Sinalizador WinHTTP \_ \_ SSL2 protocolo \_ seguro</span><span class="sxs-lookup"><span data-stu-id="e233c-417"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="e233c-418">O protocolo SSL 2,0 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="e233c-418">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="e233c-419"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>\_Sinalizador WinHTTP \_ \_ SSL3 protocolo \_ seguro</span><span class="sxs-lookup"><span data-stu-id="e233c-419"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="e233c-420">O protocolo SSL 3,0 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="e233c-420">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="e233c-421"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>\_Sinalizador WinHTTP \_ \_ TLS1 protocolo \_ seguro</span><span class="sxs-lookup"><span data-stu-id="e233c-421"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="e233c-422">O protocolo TLS 1,0 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="e233c-422">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="e233c-423"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>Sinalizador WINHTTP de \_ \_ protocolo de segurança \_ \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e233c-423"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="e233c-424">O protocolo TLS 1,1 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="e233c-424">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="e233c-425"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>Sinalizador WINHTTP de \_ \_ protocolo de segurança \_ \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="e233c-425"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="e233c-426">O protocolo TLS 1,2 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="e233c-426">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="e233c-427"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_estrutura do \_ certificado de segurança da opção WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-427"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-428">Recupera o certificado para um servidor SSL/TLS na estrutura [**de \_ \_ informações do certificado WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) .</span><span class="sxs-lookup"><span data-stu-id="e233c-428">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="e233c-429">O aplicativo deve liberar os membros **lpszSubjectInfo** e **lpszIssuerInfo** com [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span><span class="sxs-lookup"><span data-stu-id="e233c-429">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-430"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**\_sinalizadores de \_ segurança da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-430"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-431">Define ou recupera um valor inteiro longo sem sinal que contém os sinalizadores de segurança para um identificador.</span><span class="sxs-lookup"><span data-stu-id="e233c-431">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="e233c-432">Pode ser uma combinação desses valores:</span><span class="sxs-lookup"><span data-stu-id="e233c-432">It can be a combination of these values:</span></span>

| <span data-ttu-id="e233c-433">Termo</span><span class="sxs-lookup"><span data-stu-id="e233c-433">Term</span></span> | <span data-ttu-id="e233c-434">Descrição</span><span class="sxs-lookup"><span data-stu-id="e233c-434">Description</span></span> |
|-|-|
| <span data-ttu-id="e233c-435"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>sinalizador de segurança \_ \_ ignorar \_ certificado \_ CN \_ inválido</span><span class="sxs-lookup"><span data-stu-id="e233c-435"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="e233c-436">Permite um nome comum inválido em um certificado; ou seja, o nome do servidor especificado pelo aplicativo não corresponde ao nome comum no certificado.</span><span class="sxs-lookup"><span data-stu-id="e233c-436">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="e233c-437">Se esse sinalizador for definido, o aplicativo não receberá um retorno de chamada do **sinalizador de status de retorno de chamada do WinHTTP \_ \_ \_ \_ \_ CN \_ inválido** .</span><span class="sxs-lookup"><span data-stu-id="e233c-437">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="e233c-438"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>sinalizador de segurança \_ \_ ignorar \_ data de certificado \_ \_ inválida</span><span class="sxs-lookup"><span data-stu-id="e233c-438"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="e233c-439">Permite uma data de certificado inválida, ou seja, um certificado expirado ou ainda não efetivo.</span><span class="sxs-lookup"><span data-stu-id="e233c-439">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="e233c-440">Se esse sinalizador for definido, o aplicativo não receberá um retorno de chamada de **certificado de sinalizador de status de retorno de chamada de \_ \_ \_ \_ \_ dados \_ inválido** .</span><span class="sxs-lookup"><span data-stu-id="e233c-440">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="e233c-441"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>sinalizador de segurança \_ \_ ignorar \_ \_ AC desconhecida</span><span class="sxs-lookup"><span data-stu-id="e233c-441"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="e233c-442">Permite uma autoridade de certificação inválida.</span><span class="sxs-lookup"><span data-stu-id="e233c-442">Allows an invalid certificate authority.</span></span> <span data-ttu-id="e233c-443">Se esse sinalizador for definido, o aplicativo não receberá um sinalizador de status de retorno de chamada do WinHTTP com retorno de chamada de **\_ \_ \_ \_ \_ AC inválido** .</span><span class="sxs-lookup"><span data-stu-id="e233c-443">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="e233c-444"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>sinalizador de segurança \_ \_ ignorar \_ \_ uso incorreto do certificado \_</span><span class="sxs-lookup"><span data-stu-id="e233c-444"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="e233c-445">Permite que a identidade de um servidor seja estabelecida com um certificado que não seja de servidor (por exemplo, um certificado de cliente).</span><span class="sxs-lookup"><span data-stu-id="e233c-445">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="e233c-446"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>sinalizador de segurança \_ \_ ignorar \_ \_ assinatura fraca</span><span class="sxs-lookup"><span data-stu-id="e233c-446"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="e233c-447">Permite que uma assinatura fraca seja ignorada.</span><span class="sxs-lookup"><span data-stu-id="e233c-447">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="e233c-448">Esse sinalizador está disponível na atualização cumulativa para cada sistema operacional, começando com o Windows 7 e o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="e233c-448">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="e233c-449"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>sinalizador de segurança \_ \_ seguro</span><span class="sxs-lookup"><span data-stu-id="e233c-449"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="e233c-450">Usa transferências seguras.</span><span class="sxs-lookup"><span data-stu-id="e233c-450">Uses secure transfers.</span></span> <span data-ttu-id="e233c-451">Isso só é retornado em uma chamada para [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="e233c-451">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="e233c-452"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>\_ \_ nível médio do sinalizador de segurança \_</span><span class="sxs-lookup"><span data-stu-id="e233c-452"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="e233c-453">Usa a criptografia média (56 bits).</span><span class="sxs-lookup"><span data-stu-id="e233c-453">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="e233c-454">Isso só é retornado em uma chamada para [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="e233c-454">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="e233c-455"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>\_ \_ forte força do sinalizador de segurança \_</span><span class="sxs-lookup"><span data-stu-id="e233c-455"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="e233c-456">Usa criptografia forte (128 bits).</span><span class="sxs-lookup"><span data-stu-id="e233c-456">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="e233c-457">Isso só é retornado em uma chamada para [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="e233c-457">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="e233c-458"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>intensidade de sinalizador de segurança \_ \_ \_ fraca</span><span class="sxs-lookup"><span data-stu-id="e233c-458"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="e233c-459">Usa criptografia fraca (40 bits).</span><span class="sxs-lookup"><span data-stu-id="e233c-459">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="e233c-460">Isso só é retornado em uma chamada para [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="e233c-460">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="e233c-461"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**\_informações de \_ segurança da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-461"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-462">Recupera a conexão SChannel e as informações de codificação para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="e233c-462">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-463"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**chave de segurança de bit de bits de opção de WINHTTP \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-463"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-464">Recupera um valor inteiro longo sem sinal que contém a intensidade de codificação da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="e233c-464">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="e233c-465">Um número maior indica criptografia de intensidade de codificação mais forte.</span><span class="sxs-lookup"><span data-stu-id="e233c-465">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-466"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**\_ \_ tempo limite de envio da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-466"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-467">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos, para enviar uma solicitação ou gravar alguns dados.</span><span class="sxs-lookup"><span data-stu-id="e233c-467">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="e233c-468">Se o envio da solicitação demorar mais do que o tempo limite, a operação enviar será cancelada.</span><span class="sxs-lookup"><span data-stu-id="e233c-468">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="e233c-469">O tempo limite padrão é de 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="e233c-469">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-470"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**\_CBT de \_ servidor de opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-470"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-471">Obtém um ponteiro para a estrutura de [**\_ associações SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) que especifica um token de associação de canal (CBT).</span><span class="sxs-lookup"><span data-stu-id="e233c-471">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="e233c-472">Um token de associação de canal é uma propriedade de um canal de transporte seguro e é usado para associar um canal de autenticação ao canal de transporte seguro.</span><span class="sxs-lookup"><span data-stu-id="e233c-472">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="e233c-473">Esse token só pode ser obtido por essa opção depois que uma conexão SSL é estabelecida.</span><span class="sxs-lookup"><span data-stu-id="e233c-473">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="e233c-474">Passar essa opção e um valor **nulo** para *lpBuffer* para [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) retornará \_ o buffer insuficiente de erro \_ e o tamanho de byte necessário para o buffer no parâmetro *lpdwBufferLength* .</span><span class="sxs-lookup"><span data-stu-id="e233c-474">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="e233c-475">Esse valor de tamanho de buffer retornado pode ser passado em uma chamada subsequente para consulta para o token de associação de canal.</span><span class="sxs-lookup"><span data-stu-id="e233c-475">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="e233c-476">Essas etapas são necessárias ao manipular \_ \_ a solicitação de status de retorno de chamada WinHTTP \_ se você quiser modificar cabeçalhos de solicitação com base no token de associação de canal.</span><span class="sxs-lookup"><span data-stu-id="e233c-476">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="e233c-477">Observe que o Windows XP e o vista não dão suporte à modificação de cabeçalhos de solicitação durante esse retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e233c-477">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-478"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**\_contexto da \_ cadeia de certificados do servidor de opção WinHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-478"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-479">Recupera o contexto da cadeia de certificação do servidor.</span><span class="sxs-lookup"><span data-stu-id="e233c-479">Retrieves the server certification chain context.</span></span> <span data-ttu-id="e233c-480">**WinHTTP \_ O \_ \_ contexto de \_ cadeia \_ de certificados de servidor de opção** pode ser passado para obter um ponteiro duplicado para o **\_ \_ contexto da cadeia** de certificados para uma cadeia de certificados de servidor recebida durante uma conexão SSL negociada.</span><span class="sxs-lookup"><span data-stu-id="e233c-480">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="e233c-481">O cliente deve chamar [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) no ponteiro de contexto PCCERT retornado \_ que é preenchido no buffer.</span><span class="sxs-lookup"><span data-stu-id="e233c-481">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-482"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**\_contexto de \_ certificado de servidor de opção WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-482"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-483">Recupera o contexto de certificação do servidor.</span><span class="sxs-lookup"><span data-stu-id="e233c-483">Retrieves the server certification context.</span></span> <span data-ttu-id="e233c-484">**WinHTTP \_ O \_ \_ \_ contexto de certificado de servidor de opção** pode ser passado para obter um ponteiro DUPLICAdo para o [**contexto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de certificado para um certificado de servidor recebido durante uma conexão SSL negociada.</span><span class="sxs-lookup"><span data-stu-id="e233c-484">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="e233c-485">O cliente deve chamar [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) no ponteiro de contexto PCCERT retornado \_ que é preenchido no buffer.</span><span class="sxs-lookup"><span data-stu-id="e233c-485">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-486"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**\_SPN de servidor de opção WinHTTP \_ \_ \_ usado**</span><span class="sxs-lookup"><span data-stu-id="e233c-486"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-487">Obtém o nome principal do servidor do servidor que o WinHTTP forneceu ao SSPI durante a autenticação.</span><span class="sxs-lookup"><span data-stu-id="e233c-487">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="e233c-488">Esse valor de cadeia de caracteres pode ser passado para [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) após uma falha de autenticação.</span><span class="sxs-lookup"><span data-stu-id="e233c-488">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-489"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**\_SPN da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-489"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-490">Inclui ou remove o número da porta do servidor quando o SPN (nome da entidade de serviço) é criado para Kerberos ou negociar autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="e233c-490">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="e233c-491">Esse sinalizador é um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="e233c-491">This flag is one of the following values:</span></span>

| <span data-ttu-id="e233c-492">Termo</span><span class="sxs-lookup"><span data-stu-id="e233c-492">Term</span></span> | <span data-ttu-id="e233c-493">Descrição</span><span class="sxs-lookup"><span data-stu-id="e233c-493">Description</span></span> |
|-|-|
| <span data-ttu-id="e233c-494"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ desabilitar \_ \_ porta do servidor SPN \_</span><span class="sxs-lookup"><span data-stu-id="e233c-494"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="e233c-495">Remove o número da porta do servidor.</span><span class="sxs-lookup"><span data-stu-id="e233c-495">Removes the server port number.</span></span> |
| <span data-ttu-id="e233c-496"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>\_ \_ \_ porta do servidor SPN habilitar WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-496"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="e233c-497">Inclui o número da porta do servidor.</span><span class="sxs-lookup"><span data-stu-id="e233c-497">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="e233c-498"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**\_opção WinHTTP \_ TCP \_ Fast \_ aberta**</span><span class="sxs-lookup"><span data-stu-id="e233c-498"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-499">Habilita o TCP Fast Open para a conexão.</span><span class="sxs-lookup"><span data-stu-id="e233c-499">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-500"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**\_opção WinHTTP \_ TCP \_ KeepAlive**</span><span class="sxs-lookup"><span data-stu-id="e233c-500"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP\_OPTION\_TCP\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-501">Essa opção pode ser definida em um identificador de sessão do WinHttp para habilitar o comportamento Keep-Alive TCP no soquete subjacente.</span><span class="sxs-lookup"><span data-stu-id="e233c-501">This option can be set on a WinHttp session handle to enable TCP keep-alive behavior on the underlying socket.</span></span> <span data-ttu-id="e233c-502">Usa um struct [**TCP \_ KeepAlive**](/windows/win32/winsock/sio-keepalive-vals) .</span><span class="sxs-lookup"><span data-stu-id="e233c-502">Takes a [**tcp\_keepalive**](/windows/win32/winsock/sio-keepalive-vals) struct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-503"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**\_ \_ Início falso de TLS da opção WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-503"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-504">Habilita o início falso do TLS para a conexão.</span><span class="sxs-lookup"><span data-stu-id="e233c-504">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-505"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**\_evento de \_ notificação de descarregamento da opção WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-505"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-506">Assume um evento que será definido quando o último retorno de chamada for concluído para uma sessão específica.</span><span class="sxs-lookup"><span data-stu-id="e233c-506">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="e233c-507">Esse sinalizador deve ser usado em um identificador de sessão.</span><span class="sxs-lookup"><span data-stu-id="e233c-507">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="e233c-508">O evento não pode ser fechado até que tenha sido definido pelo WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="e233c-508">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-509"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**\_opção WinHTTP \_ análise de \_ cabeçalho não seguro \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-509"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-510">Essa opção é reservada para uso interno e não deve ser chamada.</span><span class="sxs-lookup"><span data-stu-id="e233c-510">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-511"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**\_opção \_ de WinHTTP atualizar para o \_ \_ soquete da Web \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-511"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-512">Instrui a pilha para iniciar um processo de handshake do WebSocket com [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="e233c-512">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="e233c-513">Essa opção não usa parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e233c-513">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-514"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**\_URL da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-514"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-515">Recupera um valor de cadeia de caracteres que contém a URL completa de um recurso baixado.</span><span class="sxs-lookup"><span data-stu-id="e233c-515">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="e233c-516">Se a URL original contiver dados adicionais, como cadeias de caracteres de pesquisa ou âncoras, ou se a chamada tiver sido redirecionada, a URL retornada será diferente da original.</span><span class="sxs-lookup"><span data-stu-id="e233c-516">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="e233c-517">O aplicativo deve passar um buffer, dimensionado em bytes, que é grande o suficiente para manter a URL retornada em caracteres largos.</span><span class="sxs-lookup"><span data-stu-id="e233c-517">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-518"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_opção WinHTTP \_ usar \_ \_ credenciais do servidor global \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-518"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-519">Usa um **bool** e pode ser definido apenas como um identificador de sessão.</span><span class="sxs-lookup"><span data-stu-id="e233c-519">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="e233c-520">Ele só se propagará para os identificadores criados a partir do identificador de sessão depois que a opção tiver sido definida.</span><span class="sxs-lookup"><span data-stu-id="e233c-520">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="e233c-521">Se **for true**, essa opção fará com que o último recurso use as credenciais do servidor global que foram enviadas do Wininet.</span><span class="sxs-lookup"><span data-stu-id="e233c-521">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="e233c-522">O padrão para essa opção é **false**.</span><span class="sxs-lookup"><span data-stu-id="e233c-522">The default for this option is **FALSE**.</span></span> <span data-ttu-id="e233c-523">Essa opção requer a chave do registro **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="e233c-523">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="e233c-524">Essa chave do registro não está presente por padrão.</span><span class="sxs-lookup"><span data-stu-id="e233c-524">This registry key is not present by default.</span></span> <span data-ttu-id="e233c-525">Quando definido, o WinINet enviará as credenciais para o WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="e233c-525">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="e233c-526">Sempre que o WinHttp obtiver um desafio de autenticação e se não houver nenhuma credencial definida no identificador atual, ele usará as credenciais fornecidas pelo WinINet.</span><span class="sxs-lookup"><span data-stu-id="e233c-526">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-527"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**\_agente do \_ usuário da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-527"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-528">Define ou recupera a cadeia de caracteres do [*agente do usuário*](glossary.md) nos identificadores fornecidos pelo [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) e usado em funções [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) subsequentes, desde que ele não seja substituído por um cabeçalho adicionado por [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) ou **WinHttpSendRequest**.</span><span class="sxs-lookup"><span data-stu-id="e233c-528">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="e233c-529">Ao recuperar um agente do usuário, o aplicativo deve passar um buffer, dimensionado em bytes, que é grande o suficiente para manter a URL retornada em caracteres largos.</span><span class="sxs-lookup"><span data-stu-id="e233c-529">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="e233c-530">Ao definir o agente do usuário, o tamanho do buffer é o comprimento da cadeia de caracteres, em valores, mais o terminador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="e233c-530">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-531"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**nome de usuário da \_ opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-531"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-532">Define ou recupera uma cadeia de caracteres que contém o nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="e233c-532">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-533"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**\_ \_ \_ \_ tempo limite de fechamento de soquete da Web de opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-533"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-534">Define o tempo, em milissegundos, que [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) deve aguardar para concluir o handshake de fechamento.</span><span class="sxs-lookup"><span data-stu-id="e233c-534">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="e233c-535">O padrão é 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="e233c-535">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-536"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**\_intervalo de \_ KeepAlive de soquete da Web de opção WinHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-536"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-537">Define o intervalo, em milissegundos, para enviar um pacote Keep-Alive pela conexão.</span><span class="sxs-lookup"><span data-stu-id="e233c-537">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="e233c-538">O intervalo padrão é 30000 (30 segundos).</span><span class="sxs-lookup"><span data-stu-id="e233c-538">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="e233c-539">O intervalo mínimo é 15000 (15 segundos).</span><span class="sxs-lookup"><span data-stu-id="e233c-539">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="e233c-540">Usar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para definir um valor inferior a 15000 retornará com um **\_ \_ parâmetro de erro inválido**.</span><span class="sxs-lookup"><span data-stu-id="e233c-540">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="e233c-541">O valor padrão para **a \_ opção \_ WinHTTP \_ \_ \_ intervalo de KeepAlive do soquete da Web** é lido em **HKLM: \\ software \\ Microsoft \\ WebSocket \\ KeepaliveInterval**.</span><span class="sxs-lookup"><span data-stu-id="e233c-541">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="e233c-542">Se um valor não for definido, o valor padrão de 30000 será usado.</span><span class="sxs-lookup"><span data-stu-id="e233c-542">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="e233c-543">Não é possível ter um intervalo de KeepAlive inferior a 15000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="e233c-543">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-544"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**\_opção WinHTTP \_ \_ tamanho do \_ buffer de recebimento de soquete da \_ Web \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-544"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-545">Define ou recupera um DWORD que especifica o tamanho do buffer de recebimento a ser usado em conexões WebSocket.</span><span class="sxs-lookup"><span data-stu-id="e233c-545">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-546"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**\_opção WinHTTP \_ \_ tamanho do \_ buffer de envio de soquete da \_ Web \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-546"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-547">Define ou recupera um DWORD que especifica o tamanho do buffer de envio a ser usado em conexões WebSocket.</span><span class="sxs-lookup"><span data-stu-id="e233c-547">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-548"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**\_opção WinHTTP \_ \_ contagem de threads de trabalho \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-548"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-549">Define um valor inteiro longo sem sinal que especifica o número de threads de trabalho que o pool de threads deve usar para conclusões assíncronas.</span><span class="sxs-lookup"><span data-stu-id="e233c-549">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="e233c-550">O valor padrão dessa opção é zero, que especifica que o número de threads de trabalho é igual ao número de CPUs no sistema.</span><span class="sxs-lookup"><span data-stu-id="e233c-550">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="e233c-551">Essa opção só pode ser definida em um identificador [HINTERNET](hinternet-handles-in-winhttp.md) **nulo** antes que uma operação assíncrona tenha ocorrido.  </span><span class="sxs-lookup"><span data-stu-id="e233c-551">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="e233c-552">Essa opção só pode ser definida uma vez.</span><span class="sxs-lookup"><span data-stu-id="e233c-552">This option can only be set once.</span></span>

<span data-ttu-id="e233c-553">**Windows Server 2008 R2 e Windows 7:** Este sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="e233c-553">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e233c-554"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**\_tamanho do \_ buffer de gravação da opção WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-554"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e233c-555">Esta opção foi preterida; Ele não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="e233c-555">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e233c-556">Comentários</span><span class="sxs-lookup"><span data-stu-id="e233c-556">Remarks</span></span>

<span data-ttu-id="e233c-557">A tabela a seguir lista os sinalizadores de opção especificando em quais identificadores eles podem atuar, se eles podem ser consultados e definidos e o tipo de dados usado.</span><span class="sxs-lookup"><span data-stu-id="e233c-557">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="e233c-558">Um "X" indica que o sinalizador de opção é válido para uso com a função ou o identificador, enquanto um "-" especifica que o sinalizador de opção é inválido.</span><span class="sxs-lookup"><span data-stu-id="e233c-558">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="e233c-559">A tentativa de definir ou consultar um sinalizador de opção em uma versão do Windows em que não tem suporte resultará na **\_ \_ \_ opção erro WinHTTP inválido**.</span><span class="sxs-lookup"><span data-stu-id="e233c-559">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="e233c-560">Sinalizador de opção e tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e233c-560">Option flag, and data type</span></span> | <span data-ttu-id="e233c-561">Identificador de sessão</span><span class="sxs-lookup"><span data-stu-id="e233c-561">Session handle</span></span> | <span data-ttu-id="e233c-562">Identificador de solicitação</span><span class="sxs-lookup"><span data-stu-id="e233c-562">Request handle</span></span> | <span data-ttu-id="e233c-563">Opção de consulta</span><span class="sxs-lookup"><span data-stu-id="e233c-563">Query option</span></span> | <span data-ttu-id="e233c-564">Opção Set</span><span class="sxs-lookup"><span data-stu-id="e233c-564">Set option</span></span> | <span data-ttu-id="e233c-565">Versão mínima do Windows</span><span class="sxs-lookup"><span data-stu-id="e233c-565">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="e233c-566">\_opção WinHTTP \_ garantindo \_ \_ \_ retornos de chamada sem bloqueio</span><span class="sxs-lookup"><span data-stu-id="e233c-566">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="e233c-567">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="e233c-567">**BOOL**</span></span> | <span data-ttu-id="e233c-568">X</span><span class="sxs-lookup"><span data-stu-id="e233c-568">X</span></span> | \- | \- | <span data-ttu-id="e233c-569">X</span><span class="sxs-lookup"><span data-stu-id="e233c-569">X</span></span> | \- |
| <span data-ttu-id="e233c-570">política de WINHTTP da \_ opção de \_ logon automático \_</span><span class="sxs-lookup"><span data-stu-id="e233c-570">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="e233c-571">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-571">**DWORD**</span></span> | \- | <span data-ttu-id="e233c-572">X</span><span class="sxs-lookup"><span data-stu-id="e233c-572">X</span></span> | \- | <span data-ttu-id="e233c-573">X</span><span class="sxs-lookup"><span data-stu-id="e233c-573">X</span></span> | \- |
| <span data-ttu-id="e233c-574">retorno de chamada de \_ opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-574">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="e233c-575">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="e233c-575">**LPVOID**</span></span> | <span data-ttu-id="e233c-576">X</span><span class="sxs-lookup"><span data-stu-id="e233c-576">X</span></span> | <span data-ttu-id="e233c-577">X</span><span class="sxs-lookup"><span data-stu-id="e233c-577">X</span></span> | <span data-ttu-id="e233c-578">X</span><span class="sxs-lookup"><span data-stu-id="e233c-578">X</span></span> | <span data-ttu-id="e233c-579">X</span><span class="sxs-lookup"><span data-stu-id="e233c-579">X</span></span> | \- |
| <span data-ttu-id="e233c-580">\_contexto de \_ certificado de cliente de opção WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-580">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="e233c-581">**contexto do certificado \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-581">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="e233c-582">X</span><span class="sxs-lookup"><span data-stu-id="e233c-582">X</span></span> | \- | <span data-ttu-id="e233c-583">X</span><span class="sxs-lookup"><span data-stu-id="e233c-583">X</span></span> | <span data-ttu-id="e233c-584">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e233c-584">Windows Vista</span></span> |
| <span data-ttu-id="e233c-585">\_opção WinHTTP \_ \_ lista de emissor de certificado de cliente \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-585">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="e233c-586">**SecPkgContext \_ IssuerListInfoEx**</span><span class="sxs-lookup"><span data-stu-id="e233c-586">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="e233c-587">X</span><span class="sxs-lookup"><span data-stu-id="e233c-587">X</span></span> | <span data-ttu-id="e233c-588">X</span><span class="sxs-lookup"><span data-stu-id="e233c-588">X</span></span> | \- | <span data-ttu-id="e233c-589">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e233c-589">Windows Vista</span></span> |
| <span data-ttu-id="e233c-590">página de código da \_ opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-590">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="e233c-591">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-591">**DWORD**</span></span> | <span data-ttu-id="e233c-592">X</span><span class="sxs-lookup"><span data-stu-id="e233c-592">X</span></span> | \- | \- | <span data-ttu-id="e233c-593">X</span><span class="sxs-lookup"><span data-stu-id="e233c-593">X</span></span> | \- |
| <span data-ttu-id="e233c-594">\_opção WinHTTP \_ Configurar \_ autenticação do Passport \_</span><span class="sxs-lookup"><span data-stu-id="e233c-594">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="e233c-595">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-595">**DWORD**</span></span> | <span data-ttu-id="e233c-596">X</span><span class="sxs-lookup"><span data-stu-id="e233c-596">X</span></span> | \- | \- | <span data-ttu-id="e233c-597">X</span><span class="sxs-lookup"><span data-stu-id="e233c-597">X</span></span> | \- |
| <span data-ttu-id="e233c-598">\_ \_ novas tentativas de conexão de opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-598">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="e233c-599">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-599">**DWORD**</span></span> | <span data-ttu-id="e233c-600">X</span><span class="sxs-lookup"><span data-stu-id="e233c-600">X</span></span> | <span data-ttu-id="e233c-601">X</span><span class="sxs-lookup"><span data-stu-id="e233c-601">X</span></span> | <span data-ttu-id="e233c-602">X</span><span class="sxs-lookup"><span data-stu-id="e233c-602">X</span></span> | <span data-ttu-id="e233c-603">X</span><span class="sxs-lookup"><span data-stu-id="e233c-603">X</span></span> | \- |
| <span data-ttu-id="e233c-604">WINHTTP \_ OPTION \_ CONNECT \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e233c-604">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="e233c-605">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-605">**DWORD**</span></span> | <span data-ttu-id="e233c-606">X</span><span class="sxs-lookup"><span data-stu-id="e233c-606">X</span></span> | <span data-ttu-id="e233c-607">X</span><span class="sxs-lookup"><span data-stu-id="e233c-607">X</span></span> | <span data-ttu-id="e233c-608">X</span><span class="sxs-lookup"><span data-stu-id="e233c-608">X</span></span> | <span data-ttu-id="e233c-609">X</span><span class="sxs-lookup"><span data-stu-id="e233c-609">X</span></span> | \- |
| <span data-ttu-id="e233c-610">INFORMAÇÕES DE CONEXÃO DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-610">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="e233c-611">**INFORMAÇÕES DE CONEXÃO \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="e233c-611">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="e233c-612">X</span><span class="sxs-lookup"><span data-stu-id="e233c-612">X</span></span> | <span data-ttu-id="e233c-613">X</span><span class="sxs-lookup"><span data-stu-id="e233c-613">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-614">ESTATÍSTICAS DE CONEXÃO DA OPÇÃO WINHTTP \_ \_ \_ \_ V0</span><span class="sxs-lookup"><span data-stu-id="e233c-614">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="e233c-615">**TCP \_ INFO \_ v0**</span><span class="sxs-lookup"><span data-stu-id="e233c-615">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="e233c-616">X</span><span class="sxs-lookup"><span data-stu-id="e233c-616">X</span></span> | <span data-ttu-id="e233c-617">X</span><span class="sxs-lookup"><span data-stu-id="e233c-617">X</span></span> | \- | <span data-ttu-id="e233c-618">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="e233c-618">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="e233c-619">ESTATÍSTICAS DE CONEXÃO DA OPÇÃO WINHTTP \_ \_ \_ \_ V1</span><span class="sxs-lookup"><span data-stu-id="e233c-619">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="e233c-620">**TCP \_ INFO \_ v1**</span><span class="sxs-lookup"><span data-stu-id="e233c-620">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="e233c-621">X</span><span class="sxs-lookup"><span data-stu-id="e233c-621">X</span></span> | <span data-ttu-id="e233c-622">X</span><span class="sxs-lookup"><span data-stu-id="e233c-622">X</span></span> | \- | <span data-ttu-id="e233c-623">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="e233c-623">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="e233c-624">VALOR DE CONTEXTO DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-624">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="e233c-625">**DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="e233c-625">**DWORD\_PTR**</span></span> | <span data-ttu-id="e233c-626">X</span><span class="sxs-lookup"><span data-stu-id="e233c-626">X</span></span> | <span data-ttu-id="e233c-627">X</span><span class="sxs-lookup"><span data-stu-id="e233c-627">X</span></span> | <span data-ttu-id="e233c-628">X</span><span class="sxs-lookup"><span data-stu-id="e233c-628">X</span></span> | <span data-ttu-id="e233c-629">X</span><span class="sxs-lookup"><span data-stu-id="e233c-629">X</span></span> | \- |
| <span data-ttu-id="e233c-630">DESCOMPACTAÇÃO DA OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-630">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="e233c-631">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-631">**DWORD**</span></span> | <span data-ttu-id="e233c-632">X</span><span class="sxs-lookup"><span data-stu-id="e233c-632">X</span></span> | <span data-ttu-id="e233c-633">X</span><span class="sxs-lookup"><span data-stu-id="e233c-633">X</span></span> | \- | <span data-ttu-id="e233c-634">X</span><span class="sxs-lookup"><span data-stu-id="e233c-634">X</span></span> | <span data-ttu-id="e233c-635">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e233c-635">Windows 8.1</span></span> |
| <span data-ttu-id="e233c-636">RECURSO DESABILITAR OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-636">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="e233c-637">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-637">**DWORD**</span></span> | \- | <span data-ttu-id="e233c-638">X</span><span class="sxs-lookup"><span data-stu-id="e233c-638">X</span></span> | \- | <span data-ttu-id="e233c-639">X</span><span class="sxs-lookup"><span data-stu-id="e233c-639">X</span></span> | \- |
| <span data-ttu-id="e233c-640">OPÇÃO WINHTTP \_ \_ DESABILITAR \_ \_ FALLBACK DE \_ PROTOCOLO SEGURO</span><span class="sxs-lookup"><span data-stu-id="e233c-640">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="e233c-641">**Bool**</span><span class="sxs-lookup"><span data-stu-id="e233c-641">**BOOL**</span></span> | <span data-ttu-id="e233c-642">X</span><span class="sxs-lookup"><span data-stu-id="e233c-642">X</span></span> | \- | \- | <span data-ttu-id="e233c-643">X</span><span class="sxs-lookup"><span data-stu-id="e233c-643">X</span></span> | <span data-ttu-id="e233c-644">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="e233c-644">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="e233c-645">OPÇÃO WINHTTP \_ \_ DESABILITAR \_ FILA DE \_ FLUXO</span><span class="sxs-lookup"><span data-stu-id="e233c-645">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="e233c-646">**Bool**</span><span class="sxs-lookup"><span data-stu-id="e233c-646">**BOOL**</span></span> | <span data-ttu-id="e233c-647">X</span><span class="sxs-lookup"><span data-stu-id="e233c-647">X</span></span> | <span data-ttu-id="e233c-648">X</span><span class="sxs-lookup"><span data-stu-id="e233c-648">X</span></span> | \- | <span data-ttu-id="e233c-649">X</span><span class="sxs-lookup"><span data-stu-id="e233c-649">X</span></span> | <span data-ttu-id="e233c-650">Windows 10 versão 1809</span><span class="sxs-lookup"><span data-stu-id="e233c-650">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="e233c-651">RECURSO \_ HABILITAR OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-651">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="e233c-652">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-652">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="e233c-653">X</span><span class="sxs-lookup"><span data-stu-id="e233c-653">X</span></span> | \- |
| <span data-ttu-id="e233c-654">OPÇÃO WINHTTP \_ \_ HABILITAR \_ PROTOCOLO HTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-654">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="e233c-655">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-655">**DWORD**</span></span> | <span data-ttu-id="e233c-656">X</span><span class="sxs-lookup"><span data-stu-id="e233c-656">X</span></span> | <span data-ttu-id="e233c-657">X</span><span class="sxs-lookup"><span data-stu-id="e233c-657">X</span></span> | \- | <span data-ttu-id="e233c-658">X</span><span class="sxs-lookup"><span data-stu-id="e233c-658">X</span></span> | <span data-ttu-id="e233c-659">Windows 10, versão 1607</span><span class="sxs-lookup"><span data-stu-id="e233c-659">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="e233c-660">OPÇÃO WINHTTP \_ \_ ENABLETRACING</span><span class="sxs-lookup"><span data-stu-id="e233c-660">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="e233c-661">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-661">**DWORD**</span></span> | \- | \- | <span data-ttu-id="e233c-662">X</span><span class="sxs-lookup"><span data-stu-id="e233c-662">X</span></span> | <span data-ttu-id="e233c-663">X</span><span class="sxs-lookup"><span data-stu-id="e233c-663">X</span></span> | \- |
| <span data-ttu-id="e233c-664">CODIFICAR EXTRA DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-664">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="e233c-665">**Bool**</span><span class="sxs-lookup"><span data-stu-id="e233c-665">**BOOL**</span></span> | <span data-ttu-id="e233c-666">X</span><span class="sxs-lookup"><span data-stu-id="e233c-666">X</span></span> | <span data-ttu-id="e233c-667">X</span><span class="sxs-lookup"><span data-stu-id="e233c-667">X</span></span> | \- | <span data-ttu-id="e233c-668">X</span><span class="sxs-lookup"><span data-stu-id="e233c-668">X</span></span> | <span data-ttu-id="e233c-669">Windows 10 versão 1803</span><span class="sxs-lookup"><span data-stu-id="e233c-669">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="e233c-670">WINHTTP \_ OPTION \_ EXPIRE \_ CONNECTION</span><span class="sxs-lookup"><span data-stu-id="e233c-670">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="e233c-671">N/D</span><span class="sxs-lookup"><span data-stu-id="e233c-671">N/A</span></span> | \- | <span data-ttu-id="e233c-672">X</span><span class="sxs-lookup"><span data-stu-id="e233c-672">X</span></span> | \- | <span data-ttu-id="e233c-673">X</span><span class="sxs-lookup"><span data-stu-id="e233c-673">X</span></span> | <span data-ttu-id="e233c-674">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="e233c-674">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="e233c-675">ERRO ESTENDIDO DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-675">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="e233c-676">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-676">**DWORD**</span></span> | <span data-ttu-id="e233c-677">X</span><span class="sxs-lookup"><span data-stu-id="e233c-677">X</span></span> | <span data-ttu-id="e233c-678">X</span><span class="sxs-lookup"><span data-stu-id="e233c-678">X</span></span> | <span data-ttu-id="e233c-679">X</span><span class="sxs-lookup"><span data-stu-id="e233c-679">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-680">CREDS DE \_ \_ PROXY GLOBAL DA \_ OPÇÃO WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-680">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="e233c-681">**WINHTTP \_ CREDS**</span><span class="sxs-lookup"><span data-stu-id="e233c-681">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="e233c-682">X</span><span class="sxs-lookup"><span data-stu-id="e233c-682">X</span></span> | <span data-ttu-id="e233c-683">X</span><span class="sxs-lookup"><span data-stu-id="e233c-683">X</span></span> | \- | <span data-ttu-id="e233c-684">X</span><span class="sxs-lookup"><span data-stu-id="e233c-684">X</span></span> | \- |
| <span data-ttu-id="e233c-685">CREDS DE SERVIDOR GLOBAL DA OPÇÃO WINHTTP \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-685">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="e233c-686">**WINHTTP \_ CREDS \_ EX**</span><span class="sxs-lookup"><span data-stu-id="e233c-686">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="e233c-687">X</span><span class="sxs-lookup"><span data-stu-id="e233c-687">X</span></span> | <span data-ttu-id="e233c-688">X</span><span class="sxs-lookup"><span data-stu-id="e233c-688">X</span></span> | \- | <span data-ttu-id="e233c-689">X</span><span class="sxs-lookup"><span data-stu-id="e233c-689">X</span></span> | \- |
| <span data-ttu-id="e233c-690">TIPO DE \_ IDENTIFICADOR DE OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-690">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="e233c-691">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-691">**DWORD**</span></span> | <span data-ttu-id="e233c-692">X</span><span class="sxs-lookup"><span data-stu-id="e233c-692">X</span></span> | <span data-ttu-id="e233c-693">X</span><span class="sxs-lookup"><span data-stu-id="e233c-693">X</span></span> | <span data-ttu-id="e233c-694">X</span><span class="sxs-lookup"><span data-stu-id="e233c-694">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-695">WINHTTP \_ OPTION \_ HTTP \_ PROTOCOL \_ REQUIRED</span><span class="sxs-lookup"><span data-stu-id="e233c-695">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="e233c-696">**Bool**</span><span class="sxs-lookup"><span data-stu-id="e233c-696">**BOOL**</span></span> | <span data-ttu-id="e233c-697">X</span><span class="sxs-lookup"><span data-stu-id="e233c-697">X</span></span> | <span data-ttu-id="e233c-698">X</span><span class="sxs-lookup"><span data-stu-id="e233c-698">X</span></span> | \- | <span data-ttu-id="e233c-699">X</span><span class="sxs-lookup"><span data-stu-id="e233c-699">X</span></span> | <span data-ttu-id="e233c-700">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="e233c-700">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="e233c-701">WINHTTP \_ OPTION \_ HTTP \_ PROTOCOL \_ USED</span><span class="sxs-lookup"><span data-stu-id="e233c-701">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="e233c-702">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-702">**DWORD**</span></span> | \- | <span data-ttu-id="e233c-703">X</span><span class="sxs-lookup"><span data-stu-id="e233c-703">X</span></span> | <span data-ttu-id="e233c-704">X</span><span class="sxs-lookup"><span data-stu-id="e233c-704">X</span></span> | \- | <span data-ttu-id="e233c-705">Windows 10, versão 1607</span><span class="sxs-lookup"><span data-stu-id="e233c-705">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="e233c-706">WINHTTP \_ OPTION \_ HTTP \_ VERSION</span><span class="sxs-lookup"><span data-stu-id="e233c-706">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="e233c-707">**INFORMAÇÕES \_ DE VERSÃO \_ HTTP**</span><span class="sxs-lookup"><span data-stu-id="e233c-707">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="e233c-708">X</span><span class="sxs-lookup"><span data-stu-id="e233c-708">X</span></span> | <span data-ttu-id="e233c-709">X</span><span class="sxs-lookup"><span data-stu-id="e233c-709">X</span></span> | <span data-ttu-id="e233c-710">X</span><span class="sxs-lookup"><span data-stu-id="e233c-710">X</span></span> | <span data-ttu-id="e233c-711">X</span><span class="sxs-lookup"><span data-stu-id="e233c-711">X</span></span> | \- |
| <span data-ttu-id="e233c-712">OPÇÃO WINHTTP \_ \_ IGNORAR \_ \_ REVOGAÇÃO DE CERTIFICADO \_ OFFLINE</span><span class="sxs-lookup"><span data-stu-id="e233c-712">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="e233c-713">**Bool**</span><span class="sxs-lookup"><span data-stu-id="e233c-713">**BOOL**</span></span> | \- | <span data-ttu-id="e233c-714">X</span><span class="sxs-lookup"><span data-stu-id="e233c-714">X</span></span> | \- | <span data-ttu-id="e233c-715">X</span><span class="sxs-lookup"><span data-stu-id="e233c-715">X</span></span> | <span data-ttu-id="e233c-716">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="e233c-716">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="e233c-717">FALLBACK RÁPIDO \_ \_ DE IPV6 \_ DA OPÇÃO WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-717">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="e233c-718">**Bool**</span><span class="sxs-lookup"><span data-stu-id="e233c-718">**BOOL**</span></span> | <span data-ttu-id="e233c-719">X</span><span class="sxs-lookup"><span data-stu-id="e233c-719">X</span></span> | \- | \- | <span data-ttu-id="e233c-720">X</span><span class="sxs-lookup"><span data-stu-id="e233c-720">X</span></span> | <span data-ttu-id="e233c-721">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="e233c-721">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="e233c-722">A OPÇÃO \_ WINHTTP É PROXY CONNECT \_ \_ \_ \_ RESPONSE</span><span class="sxs-lookup"><span data-stu-id="e233c-722">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="e233c-723">**Bool**</span><span class="sxs-lookup"><span data-stu-id="e233c-723">**BOOL**</span></span> | <span data-ttu-id="e233c-724">X</span><span class="sxs-lookup"><span data-stu-id="e233c-724">X</span></span> | <span data-ttu-id="e233c-725">X</span><span class="sxs-lookup"><span data-stu-id="e233c-725">X</span></span> | <span data-ttu-id="e233c-726">X</span><span class="sxs-lookup"><span data-stu-id="e233c-726">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-727">WINHTTP \_ OPTION \_ MAX \_ CONNS \_ PER \_ 1 \_ 0 \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="e233c-727">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="e233c-728">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-728">**DWORD**</span></span> | <span data-ttu-id="e233c-729">X</span><span class="sxs-lookup"><span data-stu-id="e233c-729">X</span></span> | \- | <span data-ttu-id="e233c-730">X</span><span class="sxs-lookup"><span data-stu-id="e233c-730">X</span></span> | <span data-ttu-id="e233c-731">X</span><span class="sxs-lookup"><span data-stu-id="e233c-731">X</span></span> | \- |
| <span data-ttu-id="e233c-732">OPÇÃO WINHTTP \_ \_ MAX \_ CONNS POR \_ \_ SERVIDOR</span><span class="sxs-lookup"><span data-stu-id="e233c-732">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="e233c-733">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-733">**DWORD**</span></span> | <span data-ttu-id="e233c-734">X</span><span class="sxs-lookup"><span data-stu-id="e233c-734">X</span></span> | \- | <span data-ttu-id="e233c-735">X</span><span class="sxs-lookup"><span data-stu-id="e233c-735">X</span></span> | <span data-ttu-id="e233c-736">X</span><span class="sxs-lookup"><span data-stu-id="e233c-736">X</span></span> | \- |
| <span data-ttu-id="e233c-737">REDIRECIONAMENTOS \_ AUTOMÁTICOS \_ DE HTTP MÁXIMO DA \_ \_ \_ OPÇÃO WINHTTP</span><span class="sxs-lookup"><span data-stu-id="e233c-737">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="e233c-738">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-738">**DWORD**</span></span> | <span data-ttu-id="e233c-739">X</span><span class="sxs-lookup"><span data-stu-id="e233c-739">X</span></span> | <span data-ttu-id="e233c-740">X</span><span class="sxs-lookup"><span data-stu-id="e233c-740">X</span></span> | <span data-ttu-id="e233c-741">X</span><span class="sxs-lookup"><span data-stu-id="e233c-741">X</span></span> | <span data-ttu-id="e233c-742">X</span><span class="sxs-lookup"><span data-stu-id="e233c-742">X</span></span> | \- |
| <span data-ttu-id="e233c-743">WINHTTP \_ OPTION \_ MAX \_ HTTP \_ STATUS \_ CONTINUE</span><span class="sxs-lookup"><span data-stu-id="e233c-743">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="e233c-744">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-744">**DWORD**</span></span> | <span data-ttu-id="e233c-745">X</span><span class="sxs-lookup"><span data-stu-id="e233c-745">X</span></span> | <span data-ttu-id="e233c-746">X</span><span class="sxs-lookup"><span data-stu-id="e233c-746">X</span></span> | <span data-ttu-id="e233c-747">X</span><span class="sxs-lookup"><span data-stu-id="e233c-747">X</span></span> | <span data-ttu-id="e233c-748">X</span><span class="sxs-lookup"><span data-stu-id="e233c-748">X</span></span> | \- |
| <span data-ttu-id="e233c-749">WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="e233c-749">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="e233c-750">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-750">**DWORD**</span></span> | <span data-ttu-id="e233c-751">X</span><span class="sxs-lookup"><span data-stu-id="e233c-751">X</span></span> | <span data-ttu-id="e233c-752">X</span><span class="sxs-lookup"><span data-stu-id="e233c-752">X</span></span> | <span data-ttu-id="e233c-753">X</span><span class="sxs-lookup"><span data-stu-id="e233c-753">X</span></span> | <span data-ttu-id="e233c-754">X</span><span class="sxs-lookup"><span data-stu-id="e233c-754">X</span></span> | \- |
| <span data-ttu-id="e233c-755">TAMANHO MÁXIMO \_ DO \_ \_ \_ HEADER DE RESPOSTA DA \_ OPÇÃO WINHTTP</span><span class="sxs-lookup"><span data-stu-id="e233c-755">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="e233c-756">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-756">**DWORD**</span></span> | <span data-ttu-id="e233c-757">X</span><span class="sxs-lookup"><span data-stu-id="e233c-757">X</span></span> | <span data-ttu-id="e233c-758">X</span><span class="sxs-lookup"><span data-stu-id="e233c-758">X</span></span> | <span data-ttu-id="e233c-759">X</span><span class="sxs-lookup"><span data-stu-id="e233c-759">X</span></span> | <span data-ttu-id="e233c-760">X</span><span class="sxs-lookup"><span data-stu-id="e233c-760">X</span></span> | \- |
| <span data-ttu-id="e233c-761">WINHTTP \_ OPTION \_ PARENT \_ HANDLE</span><span class="sxs-lookup"><span data-stu-id="e233c-761">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="e233c-762">Hinternet</span><span class="sxs-lookup"><span data-stu-id="e233c-762">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="e233c-763">X</span><span class="sxs-lookup"><span data-stu-id="e233c-763">X</span></span> | <span data-ttu-id="e233c-764">X</span><span class="sxs-lookup"><span data-stu-id="e233c-764">X</span></span> | <span data-ttu-id="e233c-765">X</span><span class="sxs-lookup"><span data-stu-id="e233c-765">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-766">WINHTTP \_ OPTION \_ PASSPORT \_ COBRANDING \_ TEXT</span><span class="sxs-lookup"><span data-stu-id="e233c-766">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="e233c-767">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="e233c-767">**LPWSTR**</span></span> | \- | <span data-ttu-id="e233c-768">X</span><span class="sxs-lookup"><span data-stu-id="e233c-768">X</span></span> | <span data-ttu-id="e233c-769">X</span><span class="sxs-lookup"><span data-stu-id="e233c-769">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-770">WINHTTP \_ OPTION \_ PASSPORT \_ COBRANDING \_ URL</span><span class="sxs-lookup"><span data-stu-id="e233c-770">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="e233c-771">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="e233c-771">**LPWSTR**</span></span> | \- | <span data-ttu-id="e233c-772">X</span><span class="sxs-lookup"><span data-stu-id="e233c-772">X</span></span> | <span data-ttu-id="e233c-773">X</span><span class="sxs-lookup"><span data-stu-id="e233c-773">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-774">URL DE RETORNO \_ DO \_ PASSPORT DA OPÇÃO \_ WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-774">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="e233c-775">**Lpvoid**</span><span class="sxs-lookup"><span data-stu-id="e233c-775">**LPVOID**</span></span> | \- | <span data-ttu-id="e233c-776">X</span><span class="sxs-lookup"><span data-stu-id="e233c-776">X</span></span> | <span data-ttu-id="e233c-777">X</span><span class="sxs-lookup"><span data-stu-id="e233c-777">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-778">WINHTTP \_ OPTION \_ PASSPORT \_ SIGN \_ OUT</span><span class="sxs-lookup"><span data-stu-id="e233c-778">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="e233c-779">**Lpvoid**</span><span class="sxs-lookup"><span data-stu-id="e233c-779">**LPVOID**</span></span> | <span data-ttu-id="e233c-780">X</span><span class="sxs-lookup"><span data-stu-id="e233c-780">X</span></span> | \- | \- | <span data-ttu-id="e233c-781">X</span><span class="sxs-lookup"><span data-stu-id="e233c-781">X</span></span> | \- |
| <span data-ttu-id="e233c-782">SENHA DA OPÇÃO \_ WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-782">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="e233c-783">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="e233c-783">**LPWSTR**</span></span> | \- | <span data-ttu-id="e233c-784">X</span><span class="sxs-lookup"><span data-stu-id="e233c-784">X</span></span> | <span data-ttu-id="e233c-785">X</span><span class="sxs-lookup"><span data-stu-id="e233c-785">X</span></span> | <span data-ttu-id="e233c-786">X</span><span class="sxs-lookup"><span data-stu-id="e233c-786">X</span></span> | \- |
| <span data-ttu-id="e233c-787">PROXY DE OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-787">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="e233c-788">**INFORMAÇÕES DE \_ PROXY WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-788">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="e233c-789">X</span><span class="sxs-lookup"><span data-stu-id="e233c-789">X</span></span> | <span data-ttu-id="e233c-790">X</span><span class="sxs-lookup"><span data-stu-id="e233c-790">X</span></span> | <span data-ttu-id="e233c-791">X</span><span class="sxs-lookup"><span data-stu-id="e233c-791">X</span></span> | <span data-ttu-id="e233c-792">X</span><span class="sxs-lookup"><span data-stu-id="e233c-792">X</span></span> | \- |
| <span data-ttu-id="e233c-793">SENHA DE PROXY DE OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-793">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="e233c-794">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="e233c-794">**LPWSTR**</span></span> | \- | <span data-ttu-id="e233c-795">X</span><span class="sxs-lookup"><span data-stu-id="e233c-795">X</span></span> | <span data-ttu-id="e233c-796">X</span><span class="sxs-lookup"><span data-stu-id="e233c-796">X</span></span> | <span data-ttu-id="e233c-797">X</span><span class="sxs-lookup"><span data-stu-id="e233c-797">X</span></span> | \- |
| <span data-ttu-id="e233c-798">SPN DE \_ PROXY DE OPÇÃO \_ \_ WINHTTP \_ USADO</span><span class="sxs-lookup"><span data-stu-id="e233c-798">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="e233c-799">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="e233c-799">**LPWSTR**</span></span> | \- | <span data-ttu-id="e233c-800">X</span><span class="sxs-lookup"><span data-stu-id="e233c-800">X</span></span> | <span data-ttu-id="e233c-801">X</span><span class="sxs-lookup"><span data-stu-id="e233c-801">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-802">NOME DE USUÁRIO DO PROXY DE OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-802">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="e233c-803">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="e233c-803">**LPWSTR**</span></span> | \- | <span data-ttu-id="e233c-804">X</span><span class="sxs-lookup"><span data-stu-id="e233c-804">X</span></span> | <span data-ttu-id="e233c-805">X</span><span class="sxs-lookup"><span data-stu-id="e233c-805">X</span></span> | <span data-ttu-id="e233c-806">X</span><span class="sxs-lookup"><span data-stu-id="e233c-806">X</span></span> | \- |
| <span data-ttu-id="e233c-807">TAMANHO DO \_ BUFFER DE LEITURA DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-807">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="e233c-808">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-808">**DWORD**</span></span> | \- | <span data-ttu-id="e233c-809">X</span><span class="sxs-lookup"><span data-stu-id="e233c-809">X</span></span> | <span data-ttu-id="e233c-810">X</span><span class="sxs-lookup"><span data-stu-id="e233c-810">X</span></span> | <span data-ttu-id="e233c-811">X</span><span class="sxs-lookup"><span data-stu-id="e233c-811">X</span></span> | \- |
| <span data-ttu-id="e233c-812">RESPOSTA DE CONEXÃO DE \_ \_ PROXY DE RECEBIMENTO DA \_ \_ \_ OPÇÃO WINHTTP</span><span class="sxs-lookup"><span data-stu-id="e233c-812">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="e233c-813">**Bool**</span><span class="sxs-lookup"><span data-stu-id="e233c-813">**BOOL**</span></span> | <span data-ttu-id="e233c-814">X</span><span class="sxs-lookup"><span data-stu-id="e233c-814">X</span></span> | <span data-ttu-id="e233c-815">X</span><span class="sxs-lookup"><span data-stu-id="e233c-815">X</span></span> | \- | <span data-ttu-id="e233c-816">X</span><span class="sxs-lookup"><span data-stu-id="e233c-816">X</span></span> | \- |
| <span data-ttu-id="e233c-817">WINHTTP \_ OPTION \_ RECEIVE \_ RESPONSE \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e233c-817">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="e233c-818">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-818">**DWORD**</span></span> | <span data-ttu-id="e233c-819">X</span><span class="sxs-lookup"><span data-stu-id="e233c-819">X</span></span> | <span data-ttu-id="e233c-820">X</span><span class="sxs-lookup"><span data-stu-id="e233c-820">X</span></span> | <span data-ttu-id="e233c-821">X</span><span class="sxs-lookup"><span data-stu-id="e233c-821">X</span></span> | <span data-ttu-id="e233c-822">X</span><span class="sxs-lookup"><span data-stu-id="e233c-822">X</span></span> | \- |
| <span data-ttu-id="e233c-823">WINHTTP \_ OPTION \_ RECEIVE \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e233c-823">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="e233c-824">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-824">**DWORD**</span></span> | <span data-ttu-id="e233c-825">X</span><span class="sxs-lookup"><span data-stu-id="e233c-825">X</span></span> | <span data-ttu-id="e233c-826">X</span><span class="sxs-lookup"><span data-stu-id="e233c-826">X</span></span> | <span data-ttu-id="e233c-827">X</span><span class="sxs-lookup"><span data-stu-id="e233c-827">X</span></span> | <span data-ttu-id="e233c-828">X</span><span class="sxs-lookup"><span data-stu-id="e233c-828">X</span></span> | \- |
| <span data-ttu-id="e233c-829">POLÍTICA DE \_ REDIRECIONAMENTO DE OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-829">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="e233c-830">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-830">**DWORD**</span></span> | <span data-ttu-id="e233c-831">X</span><span class="sxs-lookup"><span data-stu-id="e233c-831">X</span></span> | <span data-ttu-id="e233c-832">X</span><span class="sxs-lookup"><span data-stu-id="e233c-832">X</span></span> | <span data-ttu-id="e233c-833">X</span><span class="sxs-lookup"><span data-stu-id="e233c-833">X</span></span> | <span data-ttu-id="e233c-834">X</span><span class="sxs-lookup"><span data-stu-id="e233c-834">X</span></span> | \- |
| <span data-ttu-id="e233c-835">OPÇÃO WINHTTP \_ REJEITAR \_ \_ USERPWD \_ NA \_ URL</span><span class="sxs-lookup"><span data-stu-id="e233c-835">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="e233c-836">**Bool**</span><span class="sxs-lookup"><span data-stu-id="e233c-836">**BOOL**</span></span> | \- | <span data-ttu-id="e233c-837">X</span><span class="sxs-lookup"><span data-stu-id="e233c-837">X</span></span> | \- | <span data-ttu-id="e233c-838">X</span><span class="sxs-lookup"><span data-stu-id="e233c-838">X</span></span> | \- |
| <span data-ttu-id="e233c-839">PRIORIDADE DE \_ SOLICITAÇÃO DE OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-839">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="e233c-840">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-840">**DWORD**</span></span> | \- | <span data-ttu-id="e233c-841">X</span><span class="sxs-lookup"><span data-stu-id="e233c-841">X</span></span> | <span data-ttu-id="e233c-842">X</span><span class="sxs-lookup"><span data-stu-id="e233c-842">X</span></span> | <span data-ttu-id="e233c-843">X</span><span class="sxs-lookup"><span data-stu-id="e233c-843">X</span></span> | \- |
| <span data-ttu-id="e233c-844">ESTATÍSTICAS DE \_ SOLICITAÇÃO DE OPÇÃO \_ WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-844">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="e233c-845">**ESTATÍSTICAS DE \_ SOLICITAÇÃO \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="e233c-845">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="e233c-846">X</span><span class="sxs-lookup"><span data-stu-id="e233c-846">X</span></span> | <span data-ttu-id="e233c-847">X</span><span class="sxs-lookup"><span data-stu-id="e233c-847">X</span></span> | \- | <span data-ttu-id="e233c-848">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="e233c-848">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="e233c-849">TEMPOS DE \_ SOLICITAÇÃO DA OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-849">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="e233c-850">**TEMPOS DE \_ SOLICITAÇÃO WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-850">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="e233c-851">X</span><span class="sxs-lookup"><span data-stu-id="e233c-851">X</span></span> | <span data-ttu-id="e233c-852">X</span><span class="sxs-lookup"><span data-stu-id="e233c-852">X</span></span> | \- | <span data-ttu-id="e233c-853">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="e233c-853">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="e233c-854">WINHTTP \_ OPTION \_ RESOLVE \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e233c-854">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="e233c-855">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-855">**DWORD**</span></span> | <span data-ttu-id="e233c-856">X</span><span class="sxs-lookup"><span data-stu-id="e233c-856">X</span></span> | <span data-ttu-id="e233c-857">X</span><span class="sxs-lookup"><span data-stu-id="e233c-857">X</span></span> | <span data-ttu-id="e233c-858">X</span><span class="sxs-lookup"><span data-stu-id="e233c-858">X</span></span> | <span data-ttu-id="e233c-859">X</span><span class="sxs-lookup"><span data-stu-id="e233c-859">X</span></span> | \- |
| <span data-ttu-id="e233c-860">PROTOCOLOS SEGUROS DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-860">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="e233c-861">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-861">**DWORD**</span></span> | <span data-ttu-id="e233c-862">X</span><span class="sxs-lookup"><span data-stu-id="e233c-862">X</span></span> | \- | \- | <span data-ttu-id="e233c-863">X</span><span class="sxs-lookup"><span data-stu-id="e233c-863">X</span></span> | \- |
| <span data-ttu-id="e233c-864">STRUCT DO CERTIFICADO \_ \_ DE SEGURANÇA DA \_ OPÇÃO WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-864">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="e233c-865">**INFORMAÇÕES DE CERTIFICADO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e233c-865">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="e233c-866">X</span><span class="sxs-lookup"><span data-stu-id="e233c-866">X</span></span> | <span data-ttu-id="e233c-867">X</span><span class="sxs-lookup"><span data-stu-id="e233c-867">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-868">SINALIZADORES DE SEGURANÇA DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-868">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="e233c-869">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-869">**DWORD**</span></span> | \- | <span data-ttu-id="e233c-870">X</span><span class="sxs-lookup"><span data-stu-id="e233c-870">X</span></span> | <span data-ttu-id="e233c-871">X</span><span class="sxs-lookup"><span data-stu-id="e233c-871">X</span></span> | <span data-ttu-id="e233c-872">X</span><span class="sxs-lookup"><span data-stu-id="e233c-872">X</span></span> | \- |
| <span data-ttu-id="e233c-873">INFORMAÇÕES DE SEGURANÇA DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-873">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="e233c-874">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="e233c-874">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="e233c-875">X</span><span class="sxs-lookup"><span data-stu-id="e233c-875">X</span></span> | <span data-ttu-id="e233c-876">X</span><span class="sxs-lookup"><span data-stu-id="e233c-876">X</span></span> | \- | <span data-ttu-id="e233c-877">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="e233c-877">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="e233c-878">BITNESS \_ DA CHAVE \_ DE SEGURANÇA DA \_ \_ OPÇÃO WINHTTP</span><span class="sxs-lookup"><span data-stu-id="e233c-878">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="e233c-879">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-879">**DWORD**</span></span> | \- | <span data-ttu-id="e233c-880">X</span><span class="sxs-lookup"><span data-stu-id="e233c-880">X</span></span> | <span data-ttu-id="e233c-881">X</span><span class="sxs-lookup"><span data-stu-id="e233c-881">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-882">WINHTTP \_ OPTION \_ SEND \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e233c-882">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="e233c-883">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-883">**DWORD**</span></span> | <span data-ttu-id="e233c-884">X</span><span class="sxs-lookup"><span data-stu-id="e233c-884">X</span></span> | <span data-ttu-id="e233c-885">X</span><span class="sxs-lookup"><span data-stu-id="e233c-885">X</span></span> | <span data-ttu-id="e233c-886">X</span><span class="sxs-lookup"><span data-stu-id="e233c-886">X</span></span> | <span data-ttu-id="e233c-887">X</span><span class="sxs-lookup"><span data-stu-id="e233c-887">X</span></span> | \- |
| <span data-ttu-id="e233c-888">CBT DO \_ SERVIDOR DE OPÇÕES \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="e233c-888">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="e233c-889">[**Vinculações SecPkgContext \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="e233c-889">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="e233c-890">X</span><span class="sxs-lookup"><span data-stu-id="e233c-890">X</span></span> | <span data-ttu-id="e233c-891">X</span><span class="sxs-lookup"><span data-stu-id="e233c-891">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-892">CONTEXTO DA CADEIA DE \_ \_ CERTIFICADOS \_ DO SERVIDOR WINHTTP OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-892">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="e233c-893">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="e233c-893">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="e233c-894">X</span><span class="sxs-lookup"><span data-stu-id="e233c-894">X</span></span> | <span data-ttu-id="e233c-895">X</span><span class="sxs-lookup"><span data-stu-id="e233c-895">X</span></span> | \- | <span data-ttu-id="e233c-896">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="e233c-896">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="e233c-897">CONTEXTO DE CERTIFICADO \_ DO \_ SERVIDOR WINHTTP OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-897">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="e233c-898">**CONTEXTO DO CERTIFICADO**</span><span class="sxs-lookup"><span data-stu-id="e233c-898">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="e233c-899">X</span><span class="sxs-lookup"><span data-stu-id="e233c-899">X</span></span> | <span data-ttu-id="e233c-900">X</span><span class="sxs-lookup"><span data-stu-id="e233c-900">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-901">\_SPN de servidor de opção WinHTTP \_ \_ \_ usado</span><span class="sxs-lookup"><span data-stu-id="e233c-901">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="e233c-902">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="e233c-902">**LPWSTR**</span></span> | \- | <span data-ttu-id="e233c-903">X</span><span class="sxs-lookup"><span data-stu-id="e233c-903">X</span></span> | <span data-ttu-id="e233c-904">X</span><span class="sxs-lookup"><span data-stu-id="e233c-904">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-905">\_SPN da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-905">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="e233c-906">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-906">**DWORD**</span></span> | \- | <span data-ttu-id="e233c-907">X</span><span class="sxs-lookup"><span data-stu-id="e233c-907">X</span></span> | \- | <span data-ttu-id="e233c-908">X</span><span class="sxs-lookup"><span data-stu-id="e233c-908">X</span></span> | \- |
| <span data-ttu-id="e233c-909">\_opção WinHTTP \_ TCP \_ Fast \_ aberta</span><span class="sxs-lookup"><span data-stu-id="e233c-909">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="e233c-910">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="e233c-910">**BOOL**</span></span> | <span data-ttu-id="e233c-911">X</span><span class="sxs-lookup"><span data-stu-id="e233c-911">X</span></span> | \- | \- | <span data-ttu-id="e233c-912">X</span><span class="sxs-lookup"><span data-stu-id="e233c-912">X</span></span> | <span data-ttu-id="e233c-913">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="e233c-913">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="e233c-914">\_opção WinHTTP \_ TCP \_ KeepAlive</span><span class="sxs-lookup"><span data-stu-id="e233c-914">WINHTTP\_OPTION\_TCP\_KEEPALIVE</span></span><br/>[<span data-ttu-id="e233c-915">**TCP \_ KeepAlive**</span><span class="sxs-lookup"><span data-stu-id="e233c-915">**tcp\_keepalive**</span></span>](/windows/win32/winsock/sio-keepalive-vals) | <span data-ttu-id="e233c-916">X</span><span class="sxs-lookup"><span data-stu-id="e233c-916">X</span></span> | \- | \- | <span data-ttu-id="e233c-917">X</span><span class="sxs-lookup"><span data-stu-id="e233c-917">X</span></span> | <span data-ttu-id="e233c-918">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="e233c-918">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="e233c-919">\_ \_ Início falso de TLS da opção WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-919">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="e233c-920">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="e233c-920">**BOOL**</span></span> | <span data-ttu-id="e233c-921">X</span><span class="sxs-lookup"><span data-stu-id="e233c-921">X</span></span> | \- | \- | <span data-ttu-id="e233c-922">X</span><span class="sxs-lookup"><span data-stu-id="e233c-922">X</span></span> | <span data-ttu-id="e233c-923">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="e233c-923">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="e233c-924">\_evento de \_ notificação de descarregamento da opção WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-924">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="e233c-925">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="e233c-925">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="e233c-926">X</span><span class="sxs-lookup"><span data-stu-id="e233c-926">X</span></span> | \- | \- | <span data-ttu-id="e233c-927">X</span><span class="sxs-lookup"><span data-stu-id="e233c-927">X</span></span> | \- |
| <span data-ttu-id="e233c-928">\_opção WinHTTP \_ análise de \_ cabeçalho não seguro \_</span><span class="sxs-lookup"><span data-stu-id="e233c-928">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="e233c-929">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-929">**DWORD**</span></span> | \- | <span data-ttu-id="e233c-930">X</span><span class="sxs-lookup"><span data-stu-id="e233c-930">X</span></span> | \- | <span data-ttu-id="e233c-931">X</span><span class="sxs-lookup"><span data-stu-id="e233c-931">X</span></span> | \- |
| <span data-ttu-id="e233c-932">\_opção \_ de WinHTTP atualizar para o \_ \_ soquete da Web \_</span><span class="sxs-lookup"><span data-stu-id="e233c-932">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="e233c-933">N/D</span><span class="sxs-lookup"><span data-stu-id="e233c-933">N/A</span></span> | \- | <span data-ttu-id="e233c-934">X</span><span class="sxs-lookup"><span data-stu-id="e233c-934">X</span></span> | \- | <span data-ttu-id="e233c-935">X</span><span class="sxs-lookup"><span data-stu-id="e233c-935">X</span></span> | \- |
| <span data-ttu-id="e233c-936">\_URL da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-936">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="e233c-937">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="e233c-937">**LPWSTR**</span></span> | \- | <span data-ttu-id="e233c-938">X</span><span class="sxs-lookup"><span data-stu-id="e233c-938">X</span></span> | <span data-ttu-id="e233c-939">X</span><span class="sxs-lookup"><span data-stu-id="e233c-939">X</span></span> | \- | \- |
| <span data-ttu-id="e233c-940">\_opção WinHTTP \_ usar \_ \_ credenciais do servidor global \_</span><span class="sxs-lookup"><span data-stu-id="e233c-940">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="e233c-941">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="e233c-941">**BOOL**</span></span> | <span data-ttu-id="e233c-942">X</span><span class="sxs-lookup"><span data-stu-id="e233c-942">X</span></span> | <span data-ttu-id="e233c-943">X</span><span class="sxs-lookup"><span data-stu-id="e233c-943">X</span></span> | \- | <span data-ttu-id="e233c-944">X</span><span class="sxs-lookup"><span data-stu-id="e233c-944">X</span></span> | \- |
| <span data-ttu-id="e233c-945">\_agente do \_ usuário da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-945">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="e233c-946">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="e233c-946">**LPWSTR**</span></span> | <span data-ttu-id="e233c-947">X</span><span class="sxs-lookup"><span data-stu-id="e233c-947">X</span></span> | \- | <span data-ttu-id="e233c-948">X</span><span class="sxs-lookup"><span data-stu-id="e233c-948">X</span></span> | <span data-ttu-id="e233c-949">X</span><span class="sxs-lookup"><span data-stu-id="e233c-949">X</span></span> | \- |
| <span data-ttu-id="e233c-950">nome de usuário da \_ opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-950">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="e233c-951">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="e233c-951">**LPWSTR**</span></span> | \- | <span data-ttu-id="e233c-952">X</span><span class="sxs-lookup"><span data-stu-id="e233c-952">X</span></span> | <span data-ttu-id="e233c-953">X</span><span class="sxs-lookup"><span data-stu-id="e233c-953">X</span></span> | <span data-ttu-id="e233c-954">X</span><span class="sxs-lookup"><span data-stu-id="e233c-954">X</span></span> | \- |
| <span data-ttu-id="e233c-955">\_ \_ \_ \_ tempo limite de fechamento de soquete da Web de opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="e233c-955">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="e233c-956">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-956">**DWORD**</span></span> | \- | \- | <span data-ttu-id="e233c-957">X</span><span class="sxs-lookup"><span data-stu-id="e233c-957">X</span></span> | <span data-ttu-id="e233c-958">X</span><span class="sxs-lookup"><span data-stu-id="e233c-958">X</span></span> | \- |
| <span data-ttu-id="e233c-959">\_intervalo de \_ KeepAlive de soquete da Web de opção WinHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-959">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="e233c-960">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-960">**DWORD**</span></span> | \- | \- | <span data-ttu-id="e233c-961">X</span><span class="sxs-lookup"><span data-stu-id="e233c-961">X</span></span> | <span data-ttu-id="e233c-962">X</span><span class="sxs-lookup"><span data-stu-id="e233c-962">X</span></span> | \- |
| <span data-ttu-id="e233c-963">\_opção WinHTTP \_ \_ tamanho do \_ buffer de recebimento de soquete da \_ Web \_</span><span class="sxs-lookup"><span data-stu-id="e233c-963">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="e233c-964">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-964">**DWORD**</span></span> | <span data-ttu-id="e233c-965">X</span><span class="sxs-lookup"><span data-stu-id="e233c-965">X</span></span> | <span data-ttu-id="e233c-966">X</span><span class="sxs-lookup"><span data-stu-id="e233c-966">X</span></span> | <span data-ttu-id="e233c-967">X</span><span class="sxs-lookup"><span data-stu-id="e233c-967">X</span></span> | <span data-ttu-id="e233c-968">X</span><span class="sxs-lookup"><span data-stu-id="e233c-968">X</span></span> | <span data-ttu-id="e233c-969">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e233c-969">Windows 8.1</span></span> |
| <span data-ttu-id="e233c-970">\_opção WinHTTP \_ \_ tamanho do \_ buffer de envio de soquete da \_ Web \_</span><span class="sxs-lookup"><span data-stu-id="e233c-970">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="e233c-971">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-971">**DWORD**</span></span> | <span data-ttu-id="e233c-972">X</span><span class="sxs-lookup"><span data-stu-id="e233c-972">X</span></span> | <span data-ttu-id="e233c-973">X</span><span class="sxs-lookup"><span data-stu-id="e233c-973">X</span></span> | <span data-ttu-id="e233c-974">X</span><span class="sxs-lookup"><span data-stu-id="e233c-974">X</span></span> | <span data-ttu-id="e233c-975">X</span><span class="sxs-lookup"><span data-stu-id="e233c-975">X</span></span> | <span data-ttu-id="e233c-976">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e233c-976">Windows 8.1</span></span> |
| <span data-ttu-id="e233c-977">\_opção WinHTTP \_ \_ contagem de threads de trabalho \_</span><span class="sxs-lookup"><span data-stu-id="e233c-977">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="e233c-978">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-978">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="e233c-979">X</span><span class="sxs-lookup"><span data-stu-id="e233c-979">X</span></span> | \- |
| <span data-ttu-id="e233c-980">\_tamanho do \_ buffer de gravação da opção WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="e233c-980">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="e233c-981">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e233c-981">**DWORD**</span></span> | \- | <span data-ttu-id="e233c-982">X</span><span class="sxs-lookup"><span data-stu-id="e233c-982">X</span></span> | <span data-ttu-id="e233c-983">X</span><span class="sxs-lookup"><span data-stu-id="e233c-983">X</span></span> | <span data-ttu-id="e233c-984">X</span><span class="sxs-lookup"><span data-stu-id="e233c-984">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="e233c-985">Para o Windows XP e o Windows 2000, consulte [requisitos de tempo de execução](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="e233c-985">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e233c-986">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e233c-986">Requirements</span></span>

| <span data-ttu-id="e233c-987">Requisito</span><span class="sxs-lookup"><span data-stu-id="e233c-987">Requirement</span></span> | <span data-ttu-id="e233c-988">Valor</span><span class="sxs-lookup"><span data-stu-id="e233c-988">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e233c-989">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e233c-989">Minimum supported client</span></span> | <span data-ttu-id="e233c-990">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="e233c-990">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="e233c-991">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e233c-991">Minimum supported server</span></span> | <span data-ttu-id="e233c-992">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="e233c-992">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="e233c-993">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e233c-993">Redistributable</span></span>          | <span data-ttu-id="e233c-994">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e233c-994">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="e233c-995">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e233c-995">Header</span></span>                   | <span data-ttu-id="e233c-996">WinHTTP. h</span><span class="sxs-lookup"><span data-stu-id="e233c-996">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="e233c-997">Confira também</span><span class="sxs-lookup"><span data-stu-id="e233c-997">See also</span></span>

[<span data-ttu-id="e233c-998">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="e233c-998">WinHTTP Versions</span></span>](winhttp-versions.md)
