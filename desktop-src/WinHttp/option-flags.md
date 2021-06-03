---
Description: Os seguintes sinalizadores de opção têm suporte de WinHttpQueryOption e WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Sinalizadores de opção (WinHTTP. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: f9405d604318205b4e951d28d5b0c304a5f7ab71
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349975"
---
# <a name="option-flags"></a><span data-ttu-id="b1b50-103">Sinalizadores de opção</span><span class="sxs-lookup"><span data-stu-id="b1b50-103">Option Flags</span></span>

<span data-ttu-id="b1b50-104">Os seguintes sinalizadores de opção têm suporte de [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span><span class="sxs-lookup"><span data-stu-id="b1b50-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="b1b50-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**\_opção WinHTTP \_ garantindo \_ \_ \_ retornos de chamada sem bloqueio**</span><span class="sxs-lookup"><span data-stu-id="b1b50-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-106">O padrão é FALSE.</span><span class="sxs-lookup"><span data-stu-id="b1b50-106">The default is FALSE.</span></span> <span data-ttu-id="b1b50-107">Se definido como TRUE, o WinHTTP não garantirá o progresso se os retornos de chamada de status forem bloqueados pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="b1b50-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="b1b50-108">O aplicativo cliente deve tomar cuidado especial para executar operações mínimas no retorno de chamada sem bloqueio, retornando o mais rápido possível e, em particular, não deve esperar por nenhuma chamada de WinHTTP subsequente.</span><span class="sxs-lookup"><span data-stu-id="b1b50-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="b1b50-109">Se não seguir essas diretrizes, provavelmente haverá um impacto negativo no desempenho ou um possível travamento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b1b50-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="b1b50-110">Se usado da maneira prescrita, essa opção pode melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="b1b50-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**política de WINHTTP da \_ opção de \_ logon automático \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-112">Define um valor inteiro longo sem sinal que especifica a [política de logon automática](authentication-in-winhttp.md) com um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1b50-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="b1b50-113">Termo</span><span class="sxs-lookup"><span data-stu-id="b1b50-113">Term</span></span> | <span data-ttu-id="b1b50-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1b50-114">Description</span></span> |
|-|-|
| <span data-ttu-id="b1b50-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>nível de segurança do WINHTTP \_ AUTOlogonn \_ \_ \_ alto</span><span class="sxs-lookup"><span data-stu-id="b1b50-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="b1b50-116">As credenciais padrão não são usadas.</span><span class="sxs-lookup"><span data-stu-id="b1b50-116">Default credentials are not used.</span></span> <span data-ttu-id="b1b50-117">Observe que esse sinalizador só terá efeito se você especificar o servidor pelo nome real do computador.</span><span class="sxs-lookup"><span data-stu-id="b1b50-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="b1b50-118">Ele não entrará em vigor, se você especificar o servidor por "localhost" ou endereço IP.</span><span class="sxs-lookup"><span data-stu-id="b1b50-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="b1b50-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>nível de segurança do WINHTTP com \_ \_ acesso automático \_ \_ reduzido</span><span class="sxs-lookup"><span data-stu-id="b1b50-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="b1b50-120">Um logon autenticado usando as credenciais padrão é executado para todas as solicitações.</span><span class="sxs-lookup"><span data-stu-id="b1b50-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="b1b50-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>nível de segurança do WINHTTP com \_ logon automático \_ \_ \_ médio</span><span class="sxs-lookup"><span data-stu-id="b1b50-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="b1b50-122">Um logon autenticado usando as credenciais padrão é executado somente para solicitações na intranet local.</span><span class="sxs-lookup"><span data-stu-id="b1b50-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="b1b50-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**retorno de chamada de \_ opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-124">Recupera o ponteiro para a função de retorno de chamada definida com [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span><span class="sxs-lookup"><span data-stu-id="b1b50-124">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**\_contexto de \_ certificado de cliente de opção WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-126">Define o contexto de certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="b1b50-126">Sets the client certificate context.</span></span> <span data-ttu-id="b1b50-127">Se um aplicativo receber [**o \_ certificado de autenticação de cliente WinHTTP de erro \_ \_ \_ \_ necessário**](error-messages.md), ele deverá chamar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para fornecer um certificado antes de repetir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-127">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="b1b50-128">Como parte do processamento dessa opção, o WinHttp chama [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) no contexto de certificado fornecido pelo chamador para que o contexto do certificado possa ser liberado independentemente pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="b1b50-128">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="b1b50-129">O aplicativo não deve tentar fechar o repositório de certificados com o \_ sinalizador de \_ sinalizador de força de armazenamento de fechamento de certificado \_ \_ na chamada para [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) no repositório de certificados do qual o contexto de certificado foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-129">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="b1b50-130">Pode ocorrer uma violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="b1b50-130">An access violation may occur.</span></span>

<span data-ttu-id="b1b50-131">Quando o servidor solicita um certificado de cliente, o [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)ou o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retorna um erro WinHTTP erro de [**certificado de \_ \_ \_ autenticação de \_ \_ cliente**](error-messages.md) .</span><span class="sxs-lookup"><span data-stu-id="b1b50-131">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="b1b50-132">Se o servidor solicitar o certificado, mas não o exigir, o aplicativo poderá especificar essa opção para indicar que ele não tem um certificado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-132">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="b1b50-133">O servidor pode escolher outro esquema de autenticação ou permitir acesso anônimo ao servidor.</span><span class="sxs-lookup"><span data-stu-id="b1b50-133">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="b1b50-134">O aplicativo fornece a macro de **contexto de \_ \_ \_ certificado \_ de cliente do WinHTTP** no parâmetro *lpBuffer* de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1b50-134">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="b1b50-135">Se o servidor exigir um certificado de cliente, ele poderá enviar um código de status HTTP 403 em resposta.</span><span class="sxs-lookup"><span data-stu-id="b1b50-135">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="b1b50-136">Para obter mais informações, consulte **a \_ opção \_ WinHTTP \_ \_ \_ lista de emissor de certificado de cliente** .</span><span class="sxs-lookup"><span data-stu-id="b1b50-136">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_opção WinHTTP \_ \_ lista de emissor de certificado de cliente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-138">Recupera uma [**estrutura SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) quando o erro de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) é um **erro \_ WinHTTP \_ Client \_ auth \_ CERT \_ necessário**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-138">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="b1b50-139">A lista emissor na estrutura contém uma lista de autoridades de certificação aceitáveis (CA) do servidor.</span><span class="sxs-lookup"><span data-stu-id="b1b50-139">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="b1b50-140">O aplicativo cliente pode filtrar a lista de autoridades de certificação para recuperar o certificado do cliente para autenticação SSL.</span><span class="sxs-lookup"><span data-stu-id="b1b50-140">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="b1b50-141">Como alternativa, se o servidor solicitar o certificado do cliente, mas não precisar dele, o aplicativo poderá chamar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) com a opção **WinHTTP de contexto de \_ \_ \_ certificado \_ de cliente** .</span><span class="sxs-lookup"><span data-stu-id="b1b50-141">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="b1b50-142">Para obter mais informações, consulte opção **WinHTTP de contexto de certificado de \_ \_ cliente \_ \_ de opção** .</span><span class="sxs-lookup"><span data-stu-id="b1b50-142">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**página de código da \_ opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-144">Define a [*página de código*](glossary.md) usada para processar a URL (ou seja, a cadeia de caracteres de consulta).</span><span class="sxs-lookup"><span data-stu-id="b1b50-144">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="b1b50-145">O padrão é UTF8.</span><span class="sxs-lookup"><span data-stu-id="b1b50-145">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_opção WinHTTP \_ Configurar \_ autenticação do Passport \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-147">Define um valor inteiro longo sem sinal que especifica se a [autenticação do Passport na autenticação do WinHTTP](passport-authentication-in-winhttp.md) está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-147">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="b1b50-148">O valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="b1b50-148">The value can be one of the following:</span></span>

| <span data-ttu-id="b1b50-149">Termo</span><span class="sxs-lookup"><span data-stu-id="b1b50-149">Term</span></span> | <span data-ttu-id="b1b50-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1b50-150">Description</span></span> |
|-|-|
| <span data-ttu-id="b1b50-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ desabilitar \_ autenticação do Passport \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="b1b50-152">A autenticação Microsoft Passport está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-152">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="b1b50-153">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-153">This is the default.</span></span> |
| <span data-ttu-id="b1b50-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ desabilitar \_ o \_ keyring do Passport</span><span class="sxs-lookup"><span data-stu-id="b1b50-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="b1b50-155">O token de telefone do Passport está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-155">The Passport keyring is disabled.</span></span> <span data-ttu-id="b1b50-156">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-156">This is the default.</span></span> |
| <span data-ttu-id="b1b50-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ habilitar \_ autenticação do Passport \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="b1b50-158">A autenticação do Passport está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-158">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="b1b50-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ habilitar \_ o \_ token de toque do Passport</span><span class="sxs-lookup"><span data-stu-id="b1b50-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="b1b50-160">O token de telefone do Passport está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-160">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="b1b50-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_ \_ novas tentativas de conexão de opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-162">Define ou recupera um valor inteiro longo sem sinal que contém o número de tentativas de timesWinHTTP para se conectar a um host.</span><span class="sxs-lookup"><span data-stu-id="b1b50-162">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="b1b50-163">O Microsoft Windows HTTP Services (WinHTTP) só tenta uma vez por endereço IP (Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="b1b50-163">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="b1b50-164">Por exemplo, se você tentar se conectar a um host de hospedagem múltipla que tem 10 endereços IP e **a \_ opção WinHTTP as \_ \_ repetições de conexão** estiver definida como 7, o WinHTTP tentará se conectar somente com o primeiro endereço IP sete.</span><span class="sxs-lookup"><span data-stu-id="b1b50-164">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="b1b50-165">Dado o mesmo conjunto de 10 endereços IP, se **a \_ opção WinHTTP \_ conectar \_ repetições** estiver definida como 20, o WinHTTP tentará cada uma das 10 somente uma vez.</span><span class="sxs-lookup"><span data-stu-id="b1b50-165">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="b1b50-166">Se uma tentativa de conexão ainda falhar após o número especificado de tentativas ou se o tempo limite de conexão expirar antes de então, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-166">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="b1b50-167">O valor padrão para **as \_ \_ \_ repetições de conexão de opção de WinHTTP** é cinco tentativas.</span><span class="sxs-lookup"><span data-stu-id="b1b50-167">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**\_ \_ tempo limite de conexão da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-169">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="b1b50-169">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="b1b50-170">Definir essa opção como infinito (0xFFFFFFFF) desabilitará esse temporizador.</span><span class="sxs-lookup"><span data-stu-id="b1b50-170">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="b1b50-171">Se uma solicitação de conexão TCP demorar mais do que esse valor de tempo limite, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-171">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="b1b50-172">O tempo limite padrão é de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="b1b50-172">The default timeout is 60 seconds.</span></span> <span data-ttu-id="b1b50-173">Quando você está tentando se conectar a vários endereços IP para um único host (um host de hospedagem múltipla), o tempo limite é para cada conexão individual.</span><span class="sxs-lookup"><span data-stu-id="b1b50-173">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**\_informações de \_ conexão da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-175">Recupera o endereço IP de origem e de destino e a porta da solicitação que gerou a resposta quando [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retorna.</span><span class="sxs-lookup"><span data-stu-id="b1b50-175">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="b1b50-176">O aplicativo chama [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) com a opção de **\_ informações de \_ conexão \_ da opção WinHTTP** e fornece a estrutura de [**informações de \_ conexão \_ WinHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) no parâmetro *lpBuffer* .</span><span class="sxs-lookup"><span data-stu-id="b1b50-176">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="b1b50-177">Para obter mais informações, **consulte \_ \_ informações de conexão do WinHTTP**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-177">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="b1b50-178">**Windows Server 2003 com SP1 e Windows XP com SP2:** Este sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="b1b50-178">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**\_V0 de \_ Estatísticas de conexão da opção WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-180">Recupera o [**struct \_ \_ V0 de informações de TCP**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) para a conexão subjacente usada pela solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-180">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="b1b50-181">A estrutura retornada pode conter estatísticas de solicitações anteriores enviadas pela mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-181">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="b1b50-182">Esta opção foi substituída por **WinHTTP \_ Option \_ Connection \_ stats \_ v1**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-182">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**\_Estatísticas de conexão da opção WinHTTP \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="b1b50-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-184">Recupera a estrutura de [**informações do TCP \_ \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) para a conexão subjacente usada pela solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-184">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="b1b50-185">A estrutura retornada pode conter estatísticas de solicitações anteriores enviadas pela mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**\_valor de \_ contexto da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-187">Define ou recupera um **\_ PTR de DWORD** que contém um ponteiro para o valor de contexto associado a esse identificador [HINTERNET](hinternet-handles-in-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="b1b50-187">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="b1b50-188">O valor armazenado no buffer é usado e o sinalizador de opção de **\_ valor de \_ contexto \_ de opção WinHTTP** recebe um novo valor.</span><span class="sxs-lookup"><span data-stu-id="b1b50-188">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**\_DEScompactação da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-190">Define um DWORD de sinalizadores que determinam se o WinHTTP irá descompactar automaticamente os corpos de resposta com codificações de conteúdo compactadas.</span><span class="sxs-lookup"><span data-stu-id="b1b50-190">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="b1b50-191">O WinHTTP também definirá um cabeçalho de Accept-Encoding apropriado, substituindo qualquer um fornecido pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="b1b50-191">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="b1b50-192">Os valores com suporte são:</span><span class="sxs-lookup"><span data-stu-id="b1b50-192">Supported values are:</span></span>

| <span data-ttu-id="b1b50-193">Termo</span><span class="sxs-lookup"><span data-stu-id="b1b50-193">Term</span></span> | <span data-ttu-id="b1b50-194">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1b50-194">Description</span></span> |
|-|-|
| <span data-ttu-id="b1b50-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_sinalizador de DEScompactação de WinHTTP \_ \_ gzip</span><span class="sxs-lookup"><span data-stu-id="b1b50-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="b1b50-196">Descompactar conteúdo-codificação: respostas gzip.</span><span class="sxs-lookup"><span data-stu-id="b1b50-196">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="b1b50-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>\_sinalizador de DEScompactação WinHTTP \_ \_ deflate</span><span class="sxs-lookup"><span data-stu-id="b1b50-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="b1b50-198">Descompactar conteúdo-codificação: reinflar respostas.</span><span class="sxs-lookup"><span data-stu-id="b1b50-198">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="b1b50-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_sinalizador de DEScompactação de WinHTTP \_ \_ All</span><span class="sxs-lookup"><span data-stu-id="b1b50-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="b1b50-200">Descompacte as respostas com qualquer codificação de conteúdo com suporte.</span><span class="sxs-lookup"><span data-stu-id="b1b50-200">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="b1b50-201">Por padrão, o WinHTTP fornecerá respostas compactadas para o chamador sem modificações.</span><span class="sxs-lookup"><span data-stu-id="b1b50-201">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**\_recurso de \_ desabilitação da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-203">Define um valor inteiro longo sem sinal que especifica quais recursos estão desabilitados com um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1b50-203">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="b1b50-204">Lembre-se de que esse recurso só deve ser passado para [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) em identificadores de solicitação depois que o identificador de solicitação for criado com [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)e antes que a solicitação seja enviada com [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="b1b50-204">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="b1b50-205">Termo</span><span class="sxs-lookup"><span data-stu-id="b1b50-205">Term</span></span> | <span data-ttu-id="b1b50-206">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1b50-206">Description</span></span> |
|-|-|
| <span data-ttu-id="b1b50-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ desabilitar \_ autenticação</span><span class="sxs-lookup"><span data-stu-id="b1b50-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="b1b50-208">A autenticação automática está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-208">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="b1b50-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ desabilitar \_ cookies</span><span class="sxs-lookup"><span data-stu-id="b1b50-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="b1b50-210">A adição automática de cabeçalhos de cookie a solicitações está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-210">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="b1b50-211">Além disso, os cookies retornados não são adicionados automaticamente ao banco de dados do cookie.</span><span class="sxs-lookup"><span data-stu-id="b1b50-211">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="b1b50-212">A desabilitação de cookies pode resultar em baixo desempenho para autenticação do Passport.</span><span class="sxs-lookup"><span data-stu-id="b1b50-212">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="b1b50-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>\_desabilitar \_ Keep \_ Alive do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="b1b50-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="b1b50-214">Desabilita a semântica Keep-Alive para a conexão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-214">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="b1b50-215">A semântica Keep-Alive é necessária para o MSN, o NTLM e outros tipos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-215">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="b1b50-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP \_ desabilitar \_ redirecionamentos</span><span class="sxs-lookup"><span data-stu-id="b1b50-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="b1b50-217">O redirecionamento automático é desabilitado ao enviar solicitações com o [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="b1b50-217">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="b1b50-218">Se o redirecionamento automático estiver desabilitado, um aplicativo deverá registrar uma função de retorno de chamada para que a autenticação do Passport tenha sucesso.</span><span class="sxs-lookup"><span data-stu-id="b1b50-218">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="b1b50-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_opção WinHTTP \_ desabilitar \_ \_ FALLBACK de protocolo seguro \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-220">Impede que o WinHTTP tente novamente uma conexão com uma versão inferior do protocolo de segurança quando a negociação de protocolo inicial falhar.</span><span class="sxs-lookup"><span data-stu-id="b1b50-220">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**\_opção WinHTTP \_ desabilitar \_ fila de fluxos \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-222">Permite que novas solicitações abram uma conexão HTTP/2 adicional quando o limite máximo de fluxo simultâneo for atingido, em vez de aguardar o próximo fluxo disponível em uma conexão existente.</span><span class="sxs-lookup"><span data-stu-id="b1b50-222">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**\_opção WinHTTP \_ habilitar \_ recurso**</span><span class="sxs-lookup"><span data-stu-id="b1b50-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-224">Define um valor inteiro longo sem sinal que especifica os recursos atualmente habilitados.</span><span class="sxs-lookup"><span data-stu-id="b1b50-224">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="b1b50-225">Pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1b50-225">Can be one of the following values.</span></span>

| <span data-ttu-id="b1b50-226">Termo</span><span class="sxs-lookup"><span data-stu-id="b1b50-226">Term</span></span> | <span data-ttu-id="b1b50-227">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1b50-227">Description</span></span> |
|-|-|
| <span data-ttu-id="b1b50-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ habilitar \_ a \_ representação de reversão SSL \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="b1b50-229">Se habilitada, o WinHTTP reverte temporariamente a representação do cliente durante as operações de autenticação do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="b1b50-229">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="b1b50-230">Esse valor só pode ser definido no identificador de sessão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-230">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="b1b50-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ habilitar \_ \_ revogação de SSL</span><span class="sxs-lookup"><span data-stu-id="b1b50-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="b1b50-232">Se habilitada, o WinHTTP permitirá a revogação de SSL.</span><span class="sxs-lookup"><span data-stu-id="b1b50-232">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="b1b50-233">Esse valor só pode ser definido no identificador de solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-233">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**\_opção WinHTTP \_ habilitar \_ \_ protocolo http**</span><span class="sxs-lookup"><span data-stu-id="b1b50-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-235">Define um bitmask DWORD de versões HTTP avançadas aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="b1b50-235">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="b1b50-236">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="b1b50-236">Possible values are:</span></span>

| <span data-ttu-id="b1b50-237">Termo</span><span class="sxs-lookup"><span data-stu-id="b1b50-237">Term</span></span> | <span data-ttu-id="b1b50-238">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1b50-238">Description</span></span> |
|-|-|
| <span data-ttu-id="b1b50-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_ \_ Sinalizador de protocolo WinHTTP \_ HTTP2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="b1b50-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="b1b50-240">Habilita HTTP/2 para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-240">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="b1b50-241">Nenhum (0x0)</span><span class="sxs-lookup"><span data-stu-id="b1b50-241">None (0x0)</span></span> | <span data-ttu-id="b1b50-242">Restringe a solicitação para HTTP/1.1 e anterior.</span><span class="sxs-lookup"><span data-stu-id="b1b50-242">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="b1b50-243">As versões herdadas do HTTP (1,1 e anteriores) não podem ser desabilitadas usando essa opção.</span><span class="sxs-lookup"><span data-stu-id="b1b50-243">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="b1b50-244">O padrão é 0x0.</span><span class="sxs-lookup"><span data-stu-id="b1b50-244">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-245"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**opção de WINHTTP \_ \_ ENABLETRACING**</span><span class="sxs-lookup"><span data-stu-id="b1b50-245"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-246">Define um valor **bool** que especifica se o rastreamento está habilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="b1b50-246">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="b1b50-247">Para obter mais informações sobre o recurso de rastreamento no WinHTTP, consulte [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="b1b50-247">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="b1b50-248">Essa opção só pode ser definida em um identificador **HINTERNET** **nulo** .</span><span class="sxs-lookup"><span data-stu-id="b1b50-248">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="b1b50-249"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**codificação de opção de WINHTTP \_ \_ \_ extra**</span><span class="sxs-lookup"><span data-stu-id="b1b50-249"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-250">Habilita a codificação de porcentagem de URL para o caminho e a cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="b1b50-250">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="b1b50-251">Como alternativa, você pode codificar por porcentagem antes de chamar o WinHttp.</span><span class="sxs-lookup"><span data-stu-id="b1b50-251">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="b1b50-252"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**a \_ opção WinHTTP \_ expira a \_ conexão**</span><span class="sxs-lookup"><span data-stu-id="b1b50-252"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-253">Essa opção só pode ser definida em um identificador de solicitação que ainda está ativo (enviando ou recebendo).</span><span class="sxs-lookup"><span data-stu-id="b1b50-253">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="b1b50-254">Definir essa opção indicará ao WinHttp para parar de atender solicitações na conexão associada ao identificador de solicitação passado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-254">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="b1b50-255">A conexão será fechada depois que o identificador de solicitação essa opção for chamada com for concluído.</span><span class="sxs-lookup"><span data-stu-id="b1b50-255">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="b1b50-256">Essa opção não assume nenhum parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b1b50-256">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-257"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**\_ \_ erro estendido da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-257"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-258">Recupera um valor inteiro longo sem sinal que contém um código de erro do Microsoft Windows Sockets que foi mapeado para o erro \_ WinHTTP \_ \* mensagens de erro retornadas pela última vez neste contexto de thread.</span><span class="sxs-lookup"><span data-stu-id="b1b50-258">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="b1b50-259">Você pode passar **NULL** como o valor do identificador.</span><span class="sxs-lookup"><span data-stu-id="b1b50-259">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-260"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**\_credenciais de \_ \_ proxy global de opção \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="b1b50-260"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-261">Usa um ponteiro para uma estrutura do [**WinHTTP \_ creds \_ ex**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) com o parâmetro de função *hInternet* definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-261">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="b1b50-262">Essa opção requer a chave do registro **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-262">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="b1b50-263">Se essa chave do registro não estiver definida, o WinHTTP retornará a **\_ \_ \_ opção erro inválido de WinHTTP**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-263">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="b1b50-264">Essa chave do registro não está presente por padrão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-264">This registry key is not present by default.</span></span> <span data-ttu-id="b1b50-265">Quando definido, o WinINet enviará as credenciais para o WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b1b50-265">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="b1b50-266">Sempre que o WinHttp obtiver um desafio de autenticação e se não houver nenhuma credencial definida no identificador atual, ele usará as credenciais fornecidas pelo WinINet.</span><span class="sxs-lookup"><span data-stu-id="b1b50-266">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="b1b50-267">Para compartilhar as credenciais do servidor, além das credenciais de proxy, os usuários precisam definir a **\_ opção WinHTTP \_ usar \_ \_ \_ credenciais do servidor global** .</span><span class="sxs-lookup"><span data-stu-id="b1b50-267">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-268"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**\_ \_ \_ credenciais do servidor global da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-268"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-269">Usa um ponteiro para uma estrutura do [**WinHTTP \_ creds \_ ex**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) com o parâmetro de função *hInternet* definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-269">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="b1b50-270">Essa opção requer a chave do registro **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-270">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="b1b50-271">Se essa chave do registro não estiver definida, o WinHTTP retornará a **\_ \_ \_ opção erro inválido de WinHTTP**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-271">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="b1b50-272">Essa chave do registro não está presente por padrão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-272">This registry key is not present by default.</span></span> <span data-ttu-id="b1b50-273">Quando definido, o WinINet enviará as credenciais para o WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b1b50-273">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="b1b50-274">Sempre que o WinHttp obtiver um desafio de autenticação e se não houver nenhuma credencial definida no identificador atual, ele usará as credenciais fornecidas pelo WinINet.</span><span class="sxs-lookup"><span data-stu-id="b1b50-274">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="b1b50-275">Para compartilhar as credenciais do servidor, além das credenciais de proxy, os usuários precisam definir a **\_ opção WinHTTP \_ usar \_ \_ \_ credenciais do servidor global** .</span><span class="sxs-lookup"><span data-stu-id="b1b50-275">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-276"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**\_tipo de \_ identificador de opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-276"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-277">Recupera um valor inteiro longo sem sinal que contém o tipo do identificador [HINTERNET](hinternet-handles-in-winhttp.md) passado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-277">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="b1b50-278">O valor de retorno pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="b1b50-278">The return value can be one of the following:</span></span>

| <span data-ttu-id="b1b50-279">Termo</span><span class="sxs-lookup"><span data-stu-id="b1b50-279">Term</span></span> | <span data-ttu-id="b1b50-280">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1b50-280">Description</span></span> |
|-|-|
| <span data-ttu-id="b1b50-281"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>\_tipo de identificador WinHTTP \_ \_ Connect</span><span class="sxs-lookup"><span data-stu-id="b1b50-281"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="b1b50-282">O identificador é um identificador de conexão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-282">The handle is a connection handle.</span></span> |
| <span data-ttu-id="b1b50-283"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_solicitação de \_ tipo de identificador WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-283"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="b1b50-284">O identificador é um identificador de solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-284">The handle is a request handle.</span></span> |
| <span data-ttu-id="b1b50-285"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>\_sessão de \_ tipo de identificador WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-285"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="b1b50-286">O identificador é um identificador de sessão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-286">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="b1b50-287"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**\_protocolo http de opção WinHTTP \_ \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="b1b50-287"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-288">Impede que versões de protocolo diferentes daquelas habilitadas pela **\_ opção WinHTTP \_ habilitem o \_ \_ protocolo http** de serem usados para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-288">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**\_protocolo http de opção WinHTTP \_ \_ \_ usado**</span><span class="sxs-lookup"><span data-stu-id="b1b50-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-290">Obtém um DWORD que indica qual versão HTTP avançada foi usada em uma determinada solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-290">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="b1b50-291">Para obter uma lista de valores possíveis, consulte a **\_ opção WinHTTP \_ Enable \_ http \_ Protocol**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-291">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-292"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_versão de \_ http da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-292"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-293">Define ou recupera uma estrutura de [**\_ \_ informações de versão http**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) que contém a versão http com suporte.</span><span class="sxs-lookup"><span data-stu-id="b1b50-293">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="b1b50-294">Essa é uma opção de todo o processo; Use **NULL** para o identificador.</span><span class="sxs-lookup"><span data-stu-id="b1b50-294">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-295"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**\_opção WinHTTP \_ ignorar \_ \_ revogação de certificado \_ offline**</span><span class="sxs-lookup"><span data-stu-id="b1b50-295"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-296">Permite conexões seguras para usar certificados de segurança para os quais a lista de certificados revogados não pôde ser baixada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-296">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-297"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**\_Opção WinHTTP \_ IPv6 \_ Fast \_ FALLBACK**</span><span class="sxs-lookup"><span data-stu-id="b1b50-297"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-298">Habilita o fallback rápido IPv6 (mais feliz olhos) para a conexão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-298">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="b1b50-299">Esse comportamento é semelhante ao comportamento feliz olhos descrito na [RFC 6555](https://tools.ietf.org/html/rfc6555) para melhorar os tempos de conexão em redes em que o IPv6 não é confiável.</span><span class="sxs-lookup"><span data-stu-id="b1b50-299">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="b1b50-300">Se os endereços IPv6 e IPv4 forem resolvidos para um determinado host, o WinHttp será iniciado conectando-se ao primeiro endereço IPv6 resolvido com um tempo limite curto (300 MS).</span><span class="sxs-lookup"><span data-stu-id="b1b50-300">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="b1b50-301">Se essa conexão falhar, o WinHttp tentará se conectar ao primeiro endereço IPv4 resolvido com o tempo limite padrão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-301">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="b1b50-302">Se a segunda conexão falhar, o WinHttp tentará novamente o primeiro endereço IPv6 resolvido com o tempo limite padrão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-302">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="b1b50-303">Se a terceira conexão falhar, o WinHttp reverterá para o comportamento padrão de todos os endereços restantes, tentando uma conexão com cada um com o tempo limite padrão até que uma conexão seja estabelecida ou nenhum endereço permaneça.</span><span class="sxs-lookup"><span data-stu-id="b1b50-303">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-304"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**a \_ opção WinHTTP \_ é uma resposta de \_ conexão de proxy \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-304"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-305">Obtém se uma resposta de conexão de retorno de proxy pode ou não ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-305">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-306"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**Opção de WINHTTP \_ \_ Max \_ Conns \_ por \_ servidor de 1 \_ 0 \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-306"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-307">Define ou recupera um valor inteiro longo sem sinal que contém o número máximo de conexões permitidas por servidor HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="b1b50-307">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="b1b50-308">O valor padrão é **infinito**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-308">The default value is **INFINITE**.</span></span>

<span data-ttu-id="b1b50-309">**Windows Vista com SP1 e Windows Server 2008:** Este sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="b1b50-309">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-310"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**opção de WINHTTP \_ \_ Max \_ Conns \_ por \_ servidor**</span><span class="sxs-lookup"><span data-stu-id="b1b50-310"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-311">Define ou recupera um valor inteiro longo sem sinal que contém o número máximo de conexões permitidas por servidor.</span><span class="sxs-lookup"><span data-stu-id="b1b50-311">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="b1b50-312">O valor padrão é **infinito**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-312">The default value is **INFINITE**.</span></span>

<span data-ttu-id="b1b50-313">Quando essa opção é definida como zero, o WinHTTP define o limite no número de conexões como 2.</span><span class="sxs-lookup"><span data-stu-id="b1b50-313">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-314"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**opção WINHTTP máx. de \_ \_ \_ \_ redirecionamentos automáticos de http \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-314"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-315">Define o número máximo de redirecionamentos que o WinHTTP segue; o padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="b1b50-315">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="b1b50-316">Esse limite impede que sites não autorizados façam a pausa do cliente WinHTTP após um grande número de redirecionamentos.</span><span class="sxs-lookup"><span data-stu-id="b1b50-316">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="b1b50-317">**Windows XP com SP1 e windows 2000 com SP3:** Este sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="b1b50-317">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-318"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_máximo de \_ status HTTP da opção WinHTTP \_ \_ \_ continuar**</span><span class="sxs-lookup"><span data-stu-id="b1b50-318"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-319">O número máximo de respostas de código de status 100-199 informativas ignoradas antes de retornar o código de status final para o cliente WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b1b50-319">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="b1b50-320">Os códigos de status informativos 100-199 podem ser enviados pelo servidor antes do código de status final e são descritos na especificação para HTTP/1.1 (para obter mais informações, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span><span class="sxs-lookup"><span data-stu-id="b1b50-320">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="b1b50-321">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="b1b50-321">The default is 10.</span></span>

<span data-ttu-id="b1b50-322">**Windows XP com SP1 e windows 2000 com SP3:** Este sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="b1b50-322">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-323"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**\_tamanho de \_ \_ dreno de resposta máx da opção \_ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-323"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-324">Um limite na quantidade de dados drenados de respostas para reutilizar uma conexão, especificada em bytes.</span><span class="sxs-lookup"><span data-stu-id="b1b50-324">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="b1b50-325">O padrão é 1MB.</span><span class="sxs-lookup"><span data-stu-id="b1b50-325">The default is 1MB.</span></span>

<span data-ttu-id="b1b50-326">**Windows XP com SP1 e windows 2000 com SP3:** Este sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="b1b50-326">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-327"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**\_ \_ tamanho máximo do \_ cabeçalho de resposta da \_ opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-327"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-328">Um conjunto associado no tamanho máximo da parte do cabeçalho da resposta do servidor, especificado em bytes.</span><span class="sxs-lookup"><span data-stu-id="b1b50-328">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="b1b50-329">Essa ligação protege o cliente de um servidor não autorizado tentando paralisar o cliente enviando uma resposta com uma quantidade infinita de dados de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="b1b50-329">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="b1b50-330">O valor padrão é 64 KB.</span><span class="sxs-lookup"><span data-stu-id="b1b50-330">The default value is 64KB.</span></span>

<span data-ttu-id="b1b50-331">**Windows XP com SP1 e windows 2000 com SP3:** Este sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="b1b50-331">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-332"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**\_ \_ identificador pai da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-332"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-333">Recupera o identificador pai para esse identificador.</span><span class="sxs-lookup"><span data-stu-id="b1b50-333">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-334"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**opção WINHTTP de \_ \_ \_ texto de comarcação do Passport \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-334"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-335">Recupera uma cadeia de caracteres que contém o texto de [*comarcação*](glossary.md) fornecido pelo servidor de logon do Passport.</span><span class="sxs-lookup"><span data-stu-id="b1b50-335">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="b1b50-336">Essa opção deve ser recuperada imediatamente após o servidor de logon responder com um código de status 401.</span><span class="sxs-lookup"><span data-stu-id="b1b50-336">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="b1b50-337">Um aplicativo deve passar um tamanho de buffer, em bytes, que seja grande o suficiente para manter a cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-337">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-338"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_URL de \_ \_ comarcação do passaporte da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-338"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-339">Recupera uma cadeia de caracteres que contém uma URL para um gráfico de [*comarcação*](glossary.md) fornecido pelo servidor de logon do Passport.</span><span class="sxs-lookup"><span data-stu-id="b1b50-339">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="b1b50-340">Essa opção deve ser recuperada imediatamente após o servidor de logon responder com um código de status 401.</span><span class="sxs-lookup"><span data-stu-id="b1b50-340">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="b1b50-341">Um aplicativo deve passar um tamanho de buffer, em bytes, que seja grande o suficiente para manter a cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-341">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-342"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_opção WinHTTP \_ URL de retorno do Passport \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-342"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-343">Define uma opção somente leitura em um identificador de solicitação que recupera a URL de retorno do Passport.</span><span class="sxs-lookup"><span data-stu-id="b1b50-343">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-344"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**opção WINHTTP sair do \_ \_ Passport \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-344"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-345">Define a opção em um identificador de sessão para sair de quaisquer logons do Passport.</span><span class="sxs-lookup"><span data-stu-id="b1b50-345">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="b1b50-346">Um aplicativo deve passar na URL de retorno do Passport que foi recuperada com a **\_ opção WinHTTP URL de \_ \_ retorno \_ do Passport**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-346">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="b1b50-347">Todos os cookies relacionados à URL de retorno são apagados.</span><span class="sxs-lookup"><span data-stu-id="b1b50-347">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-348"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_senha da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-348"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-349">Define ou recupera um valor de cadeia de caracteres que contém a senha associada a um identificador de solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-349">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-350"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_proxy de opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-350"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-351">Define ou recupera uma estrutura de [**\_ \_ informações de proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contém os dados de proxy em um identificador de sessão existente ou identificador de solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-351">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="b1b50-352">Ao recuperar dados de proxy, um aplicativo deve liberar as cadeias de caracteres **lpszProxy** e **lpszProxyBypass** contidas nessa estrutura (se elas não forem **nulas**) usando a função [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="b1b50-352">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="b1b50-353">Um aplicativo pode consultar os dados do proxy global (o proxy padrão) passando um identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="b1b50-353">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-354"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_senha do \_ proxy da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-354"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-355">Define ou recupera um valor de cadeia de caracteres que contém a senha usada para acessar o proxy.</span><span class="sxs-lookup"><span data-stu-id="b1b50-355">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-356"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**SPN de proxy de opção de WINHTTP \_ \_ \_ \_ usado**</span><span class="sxs-lookup"><span data-stu-id="b1b50-356"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-357">Obtém o nome da entidade de segurança do servidor proxy que o WinHTTP forneceu ao SSPI durante a autenticação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-357">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="b1b50-358">Esse valor de cadeia de caracteres é usefor passando para [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) após uma falha de autenticação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-358">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-359"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_nome de \_ usuário do proxy de opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-359"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-360">Define ou recupera um valor de cadeia de caracteres que contém o nome de usuário usado para acessar o proxy.</span><span class="sxs-lookup"><span data-stu-id="b1b50-360">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-361"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_tamanho do \_ buffer de leitura da opção WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-361"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-362">Esta opção foi preterida; Ele não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="b1b50-362">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-363"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**a \_ opção \_ WinHTTP \_ recebe \_ resposta de conexão proxy \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-363"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-364">Define se a entidade de resposta de proxy pode ou não ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-364">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="b1b50-365">Essa opção está desabilitada por padrão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-365">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-366"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**a \_ opção \_ WinHTTP \_ recebe \_ tempo limite de resposta**</span><span class="sxs-lookup"><span data-stu-id="b1b50-366"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-367">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos, para aguardar a recepção de todos os cabeçalhos de resposta a uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-367">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="b1b50-368">Se o WinHTTP não receber todos os cabeçalhos dentro desse período de tempo limite, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-368">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="b1b50-369">O valor de tempo limite padrão é 90 segundos.</span><span class="sxs-lookup"><span data-stu-id="b1b50-369">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="b1b50-370">Esse tempo limite é verificado somente quando os dados são recebidos do soquete.</span><span class="sxs-lookup"><span data-stu-id="b1b50-370">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="b1b50-371">Como resultado, quando o tempo limite expira, o aplicativo cliente não é notificado até que mais dados cheguem do servidor.</span><span class="sxs-lookup"><span data-stu-id="b1b50-371">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="b1b50-372">Se nenhum dado chega do servidor, o atraso entre a expiração do tempo limite e a notificação do aplicativo cliente pode ser tão grande quanto o valor de tempo limite definido usando o parâmetro *dwReceiveTimeout* da função [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) .</span><span class="sxs-lookup"><span data-stu-id="b1b50-372">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-373"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_ \_ tempo limite de recebimento da opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-373"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-374">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos, para receber uma resposta parcial a uma solicitação ou ler alguns dados.</span><span class="sxs-lookup"><span data-stu-id="b1b50-374">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="b1b50-375">Se a resposta demorar mais do que esse valor de tempo limite, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-375">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="b1b50-376">O valor do tempo limite padrão é de 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="b1b50-376">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-377"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**\_política de \_ redirecionamento de opção WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-377"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-378">Define o comportamento do WinHTTP em relação ao tratamento de um código de status de redirecionamento HTTP 30 vezes.</span><span class="sxs-lookup"><span data-stu-id="b1b50-378">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="b1b50-379">Essa opção pode ser definida em uma sessão ou identificador de solicitação para um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b1b50-379">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="b1b50-380">Termo</span><span class="sxs-lookup"><span data-stu-id="b1b50-380">Term</span></span> | <span data-ttu-id="b1b50-381">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1b50-381">Description</span></span> |
|-|-|
| <span data-ttu-id="b1b50-382"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>\_política de \_ redirecionamento de opção de WinHTTP \_ \_ sempre</span><span class="sxs-lookup"><span data-stu-id="b1b50-382"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="b1b50-383">Todos os redirecionamentos são seguidos automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b1b50-383">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="b1b50-384"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>\_ \_ a política de redirecionamento de opção WinHTTP não \_ \_ permite \_ https \_ para \_ http</span><span class="sxs-lookup"><span data-stu-id="b1b50-384"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="b1b50-385">Todos os redirecionamentos são seguidos, exceto aqueles que se originam de uma URL segura (https) para uma URL não segura (http).</span><span class="sxs-lookup"><span data-stu-id="b1b50-385">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="b1b50-386">Essa é a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-386">This is the default setting.</span></span> |
| <span data-ttu-id="b1b50-387"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>\_política de \_ redirecionamento de opção WinHTTP \_ \_ nunca</span><span class="sxs-lookup"><span data-stu-id="b1b50-387"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="b1b50-388">Redirecionamentos nunca são seguidos.</span><span class="sxs-lookup"><span data-stu-id="b1b50-388">Redirects are never followed.</span></span> <span data-ttu-id="b1b50-389">O status de 30 vezes é retornado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b1b50-389">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-390"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**a \_ opção WinHTTP \_ rejeita \_ USERPWD \_ na \_ URL**</span><span class="sxs-lookup"><span data-stu-id="b1b50-390"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-391">Rejeita URLs que contêm um nome de usuário e senha.</span><span class="sxs-lookup"><span data-stu-id="b1b50-391">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="b1b50-392">Essa opção também rejeita URLs que contêm a semântica de *nome de usuário: senha* , mesmo que nenhum nome de usuário ou senha seja especificado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-392">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="b1b50-393">Por exemplo, " u:p@hostname ", " :@hostname ", " u:@hostname " e " :p@hostname " todos seriam sinalizados como inválidos.</span><span class="sxs-lookup"><span data-stu-id="b1b50-393">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="b1b50-394">Se uma URL inválida for passada para a função, ela retornará o [erro \_ WinHTTP \_ Invalid \_ URL](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="b1b50-394">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="b1b50-395">Essa opção é desativada por padrão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-395">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-396"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**\_prioridade de \_ solicitação de opção de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-396"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-397">Esta opção foi preterida; Ele não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="b1b50-397">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-398"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**\_Estatísticas de \_ solicitação de opção de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-398"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-399">Recupera estatísticas para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-399">Retreives statistics for the request.</span></span>  <span data-ttu-id="b1b50-400">Para obter uma lista das estatísticas disponíveis, consulte [**\_ \_ Estatísticas de solicitação do WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span><span class="sxs-lookup"><span data-stu-id="b1b50-400">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-401"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**TEMPOS DE \_ SOLICITAÇÃO DA OPÇÃO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-401"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-402">Retreive informações de tempo para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-402">Retreives timing information for the request.</span></span> <span data-ttu-id="b1b50-403">Para ver uma lista dos tempos disponíveis, consulte [**TEMPOS DE \_ SOLICITAÇÃO \_ WINHTTP.**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)</span><span class="sxs-lookup"><span data-stu-id="b1b50-403">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-404"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP \_ OPTION \_ RESOLVE \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="b1b50-404"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-405">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo-máximo, em milissegundos, para resolver um nome de host.</span><span class="sxs-lookup"><span data-stu-id="b1b50-405">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="b1b50-406">O valor de tempo-máximo padrão é **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="b1b50-406">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="b1b50-407">Se um valor não padrão for especificado, haverá uma sobrecarga de uma criação de thread por resolução de nome.</span><span class="sxs-lookup"><span data-stu-id="b1b50-407">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-408"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**PROTOCOLOS SEGUROS DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-408"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-409">Define um valor inteiro longo sem sinal que especifica quais protocolos seguros são aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="b1b50-409">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="b1b50-410">Por padrão, somente SSL3 e TLS1 estão habilitados no Windows 7 e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b1b50-410">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="b1b50-411">Por padrão, somente SSL3, TLS1.0, TLS1.1 e TLS1.2 são habilitados em Windows 8.1 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b1b50-411">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="b1b50-412">O valor pode ser uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1b50-412">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="b1b50-413">Termo</span><span class="sxs-lookup"><span data-stu-id="b1b50-413">Term</span></span> | <span data-ttu-id="b1b50-414">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1b50-414">Description</span></span> |
|-|-|
| <span data-ttu-id="b1b50-415"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>PROTOCOLO DE SEGURANÇA DO SINALIZADOR WINHTTP \_ \_ \_ \_ TODOS</span><span class="sxs-lookup"><span data-stu-id="b1b50-415"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="b1b50-416">Os protocolos protocolo SSL (SSL) 2.0, SSL 3.0 e TLS (Transport Layer Security) 1.0 podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="b1b50-416">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="b1b50-417"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>SINALIZADOR WINHTTP \_ \_ SECURE PROTOCOL \_ \_ SSL2</span><span class="sxs-lookup"><span data-stu-id="b1b50-417"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="b1b50-418">O protocolo SSL 2.0 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-418">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="b1b50-419"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>PROTOCOLO \_ \_ \_ SSL3 DO SINALIZADOR \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="b1b50-419"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="b1b50-420">O protocolo SSL 3.0 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-420">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="b1b50-421"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>PROTOCOLO SEGURO DE SINALIZADOR \_ \_ WINHTTP \_ \_ TLS1</span><span class="sxs-lookup"><span data-stu-id="b1b50-421"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="b1b50-422">O protocolo TLS 1.0 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-422">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="b1b50-423"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>PROTOCOLO SEGURO DE SINALIZADOR WINHTTP \_ \_ \_ \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b1b50-423"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="b1b50-424">O protocolo TLS 1.1 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-424">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="b1b50-425"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>PROTOCOLO SEGURO DE SINALIZADOR WINHTTP \_ \_ \_ \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="b1b50-425"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="b1b50-426">O protocolo TLS 1.2 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-426">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="b1b50-427"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**STRUCT DO CERTIFICADO \_ \_ DE SEGURANÇA DA \_ OPÇÃO WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-427"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-428">Recupera o certificado de um servidor SSL/TLS na estrutura [**WINHTTP \_ CERTIFICATE \_ INFO.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)</span><span class="sxs-lookup"><span data-stu-id="b1b50-428">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="b1b50-429">O aplicativo deve liberar **os membros lpszSubjectInfo** e **lpszIssuerInfo** com [**LocalFree.**](/windows/desktop/api/winbase/nf-winbase-localfree)</span><span class="sxs-lookup"><span data-stu-id="b1b50-429">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-430"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**SINALIZADORES DE SEGURANÇA DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-430"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-431">Define ou recupera um valor inteiro longo sem sinal que contém os sinalizadores de segurança para um handle.</span><span class="sxs-lookup"><span data-stu-id="b1b50-431">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="b1b50-432">Pode ser uma combinação desses valores:</span><span class="sxs-lookup"><span data-stu-id="b1b50-432">It can be a combination of these values:</span></span>

| <span data-ttu-id="b1b50-433">Termo</span><span class="sxs-lookup"><span data-stu-id="b1b50-433">Term</span></span> | <span data-ttu-id="b1b50-434">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1b50-434">Description</span></span> |
|-|-|
| <span data-ttu-id="b1b50-435"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SINALIZADOR \_ DE SEGURANÇA IGNORAR CERTIFICADO CN \_ \_ \_ \_ INVÁLIDO</span><span class="sxs-lookup"><span data-stu-id="b1b50-435"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="b1b50-436">Permite um nome comum inválido em um certificado; ou seja, o nome do servidor especificado pelo aplicativo não corresponderá ao nome comum no certificado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-436">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="b1b50-437">Se esse sinalizador for definido, o aplicativo não receberá um retorno de chamada **WINHTTP \_ CALLBACK \_ STATUS FLAG CERT CN \_ \_ \_ \_ INVALID.**</span><span class="sxs-lookup"><span data-stu-id="b1b50-437">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="b1b50-438"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SINALIZADOR DE \_ SEGURANÇA IGNORAR DATA DE CERTIFICADO \_ \_ \_ \_ INVÁLIDA</span><span class="sxs-lookup"><span data-stu-id="b1b50-438"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="b1b50-439">Permite uma data de certificado inválida, ou seja, um certificado expirado ou ainda não efetivo.</span><span class="sxs-lookup"><span data-stu-id="b1b50-439">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="b1b50-440">Se esse sinalizador for definido, o aplicativo não receberá um retorno de chamada **WINHTTP \_ CALLBACK STATUS FLAG \_ CERT \_ DATE \_ \_ \_ INVALID.**</span><span class="sxs-lookup"><span data-stu-id="b1b50-440">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="b1b50-441"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SINALIZADOR \_ DE SEGURANÇA IGNORAR AC \_ \_ \_ DESCONHECIDA</span><span class="sxs-lookup"><span data-stu-id="b1b50-441"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="b1b50-442">Permite uma autoridade de certificação inválida.</span><span class="sxs-lookup"><span data-stu-id="b1b50-442">Allows an invalid certificate authority.</span></span> <span data-ttu-id="b1b50-443">Se esse sinalizador for definido, o aplicativo não receberá um retorno de chamada DE CA INVÁLIDO DO SINALIZADOR DE STATUS DE RETORNO DE CHAMADA **WINHTTP. \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-443">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="b1b50-444"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SINALIZADOR DE \_ SEGURANÇA IGNORAR O USO ERRADO DO \_ \_ \_ \_ CERTIFICADO</span><span class="sxs-lookup"><span data-stu-id="b1b50-444"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="b1b50-445">Permite que a identidade de um servidor seja estabelecida com um certificado não servidor (por exemplo, um certificado do cliente).</span><span class="sxs-lookup"><span data-stu-id="b1b50-445">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="b1b50-446"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SINALIZADOR DE \_ SEGURANÇA \_ IGNORAR ASSINATURA \_ \_ FRACA</span><span class="sxs-lookup"><span data-stu-id="b1b50-446"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="b1b50-447">Permite que uma assinatura fraca seja ignorada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-447">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="b1b50-448">Esse sinalizador está disponível na atualização de rollup para cada sistema operacional, começando com o Windows 7 e o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="b1b50-448">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="b1b50-449"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SINALIZADOR \_ DE \_ SEGURANÇA SEGURO</span><span class="sxs-lookup"><span data-stu-id="b1b50-449"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="b1b50-450">Usa transferências seguras.</span><span class="sxs-lookup"><span data-stu-id="b1b50-450">Uses secure transfers.</span></span> <span data-ttu-id="b1b50-451">Isso só é retornado em uma chamada para [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="b1b50-451">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="b1b50-452"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>MEIO DE \_ FORÇA DO SINALIZADOR DE \_ \_ SEGURANÇA</span><span class="sxs-lookup"><span data-stu-id="b1b50-452"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="b1b50-453">Usa criptografia média (56 bits).</span><span class="sxs-lookup"><span data-stu-id="b1b50-453">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="b1b50-454">Isso só é retornado em uma chamada para [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="b1b50-454">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="b1b50-455"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>FORÇA FORTE \_ DO \_ SINALIZADOR DE \_ SEGURANÇA</span><span class="sxs-lookup"><span data-stu-id="b1b50-455"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="b1b50-456">Usa criptografia forte (128 bits).</span><span class="sxs-lookup"><span data-stu-id="b1b50-456">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="b1b50-457">Isso só é retornado em uma chamada para [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="b1b50-457">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="b1b50-458"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>FORÇA DO \_ SINALIZADOR \_ DE SEGURANÇA \_ FRACA</span><span class="sxs-lookup"><span data-stu-id="b1b50-458"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="b1b50-459">Usa criptografia fraca (40 bits).</span><span class="sxs-lookup"><span data-stu-id="b1b50-459">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="b1b50-460">Isso só é retornado em uma chamada para [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="b1b50-460">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="b1b50-461"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**INFORMAÇÕES DE SEGURANÇA DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-461"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-462">Retreive a conexão SChannel e informações de codificação para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-462">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-463"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**BITNESS \_ DA CHAVE \_ DE SEGURANÇA DA \_ \_ OPÇÃO WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="b1b50-463"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-464">Recupera um valor inteiro longo sem sinal que contém a força da criptografia da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b1b50-464">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="b1b50-465">Um número maior indica criptografia de força de codificação mais forte.</span><span class="sxs-lookup"><span data-stu-id="b1b50-465">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-466"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP \_ OPTION \_ SEND \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="b1b50-466"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-467">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo-máximo, em milissegundos, para enviar uma solicitação ou gravar alguns dados.</span><span class="sxs-lookup"><span data-stu-id="b1b50-467">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="b1b50-468">Se o envio da solicitação demorar mais do que o tempo de vida, a operação de envio será cancelada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-468">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="b1b50-469">O tempo de vida padrão é de 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="b1b50-469">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-470"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**CBT DO \_ SERVIDOR DE OPÇÕES \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="b1b50-470"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-471">Obtém um ponteiro para a estrutura de Vinculações [**SecPkgContext \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) que especifica um CBT (Token de Associação de Canal).</span><span class="sxs-lookup"><span data-stu-id="b1b50-471">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="b1b50-472">Um Token de Associação de Canal é uma propriedade de um canal de transporte seguro e é usado para vincular um canal de autenticação ao canal de transporte seguro.</span><span class="sxs-lookup"><span data-stu-id="b1b50-472">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="b1b50-473">Esse token só pode ser obtido por essa opção depois que uma conexão SSL é estabelecida.</span><span class="sxs-lookup"><span data-stu-id="b1b50-473">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="b1b50-474">Passar essa opção  e um valor nulo para *lpBuffer* para [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) retornarão ERROR INSUFFICIENT BUFFER e o tamanho de byte necessário para o buffer no parâmetro \_ \_ *lpdwBufferLength.*</span><span class="sxs-lookup"><span data-stu-id="b1b50-474">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="b1b50-475">Esse valor de tamanho de buffer retornado pode ser passado em uma chamada subsequente para consulta para o Token de Associação de Canal.</span><span class="sxs-lookup"><span data-stu-id="b1b50-475">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="b1b50-476">Essas etapas são necessárias ao lidar com a SOLICITAÇÃO DE STATUS DE RETORNO DE CHAMADA WINHTTP se você quiser modificar os títulos de solicitação com \_ base no Token de Associação de \_ \_ Canal.</span><span class="sxs-lookup"><span data-stu-id="b1b50-476">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="b1b50-477">Observe que o Windows XP e o Vista não são suportados para modificar os headers de solicitação durante esse retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-477">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-478"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**CONTEXTO DA CADEIA DE \_ \_ CERTIFICADOS \_ DO SERVIDOR WINHTTP OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-478"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-479">Recupera o contexto da cadeia de certificação do servidor.</span><span class="sxs-lookup"><span data-stu-id="b1b50-479">Retrieves the server certification chain context.</span></span> <span data-ttu-id="b1b50-480">**WINHTTP \_ OPTION \_ SERVER CERT CHAIN \_ \_ \_ CONTEXT** pode ser passado para obter um ponteiro duplicado para o **CONTEXTO DE \_ CADEIA \_** DE CERTIFICADOs de uma cadeia de certificados de servidor recebida durante uma conexão SSL negociada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-480">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="b1b50-481">O cliente deve chamar [**CertFreeCertificateContext no**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) ponteiro CONTEXT PCCERT retornado que \_ é preenchido no buffer.</span><span class="sxs-lookup"><span data-stu-id="b1b50-481">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-482"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**CONTEXTO DE CERTIFICADO \_ DO \_ SERVIDOR WINHTTP OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-482"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-483">Recupera o contexto de certificação do servidor.</span><span class="sxs-lookup"><span data-stu-id="b1b50-483">Retrieves the server certification context.</span></span> <span data-ttu-id="b1b50-484">**WINHTTP \_ OPTION \_ SERVER CERT CONTEXT \_ \_ pode** ser passado para obter um ponteiro duplicado para o [**CONTEXTO DE CERTIFICADO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) para um certificado do servidor recebido durante uma conexão SSL negociada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-484">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="b1b50-485">O cliente deve chamar [**CertFreeCertificateContext no**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) ponteiro CONTEXT PCCERT retornado que \_ é preenchido no buffer.</span><span class="sxs-lookup"><span data-stu-id="b1b50-485">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-486"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**SPN DO \_ SERVIDOR DE OPÇÕES \_ \_ WINHTTP \_ USADO**</span><span class="sxs-lookup"><span data-stu-id="b1b50-486"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-487">Obtém o nome principal do servidor que o WinHTTP forneceu ao SSPI durante a autenticação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-487">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="b1b50-488">Esse valor de cadeia de caracteres pode ser passado [**para SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) após uma falha de autenticação.</span><span class="sxs-lookup"><span data-stu-id="b1b50-488">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-489"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**SPN DA \_ OPÇÃO \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="b1b50-489"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-490">Inclui ou remove o número da porta do servidor quando o SPN (nome da entidade de serviço) é criado para autenticação Kerberos ou Negotiate Kerberos.</span><span class="sxs-lookup"><span data-stu-id="b1b50-490">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="b1b50-491">Esse sinalizador é um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b1b50-491">This flag is one of the following values:</span></span>

| <span data-ttu-id="b1b50-492">Termo</span><span class="sxs-lookup"><span data-stu-id="b1b50-492">Term</span></span> | <span data-ttu-id="b1b50-493">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1b50-493">Description</span></span> |
|-|-|
| <span data-ttu-id="b1b50-494"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ DESABILITAR \_ A PORTA DO SERVIDOR SPN \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-494"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="b1b50-495">Remove o número da porta do servidor.</span><span class="sxs-lookup"><span data-stu-id="b1b50-495">Removes the server port number.</span></span> |
| <span data-ttu-id="b1b50-496"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ ENABLE \_ SPN \_ SERVER \_ PORT</span><span class="sxs-lookup"><span data-stu-id="b1b50-496"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="b1b50-497">Inclui o número da porta do servidor.</span><span class="sxs-lookup"><span data-stu-id="b1b50-497">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="b1b50-498"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP \_ OPTION \_ TCP \_ FAST \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="b1b50-498"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-499">Habilita o TCP Fast Open para a conexão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-499">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-500"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP \_ OPTION \_ TLS \_ FALSE \_ START**</span><span class="sxs-lookup"><span data-stu-id="b1b50-500"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-501">Habilita o Início Falso do TLS para a conexão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-501">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-502"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**EVENTO DE \_ NOTIFICAÇÃO \_ DE DESCARREGAMENTO DE OPÇÃO \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="b1b50-502"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-503">Recebe um evento que será definido quando o último retorno de chamada for concluído para uma sessão específica.</span><span class="sxs-lookup"><span data-stu-id="b1b50-503">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="b1b50-504">Esse sinalizador deve ser usado em um alça de sessão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-504">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="b1b50-505">O evento não pode ser fechado até que ele tenha sido definido pelo WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b1b50-505">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-506"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**ANÁLISE DE TÍTULO NÃO SEGURO DA OPÇÃO WINHTTP \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-506"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-507">Essa opção é reservada para uso interno e não deve ser chamada.</span><span class="sxs-lookup"><span data-stu-id="b1b50-507">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-508"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**ATUALIZAÇÃO DA OPÇÃO WINHTTP \_ \_ PARA O \_ \_ SOQUETE DA \_ WEB**</span><span class="sxs-lookup"><span data-stu-id="b1b50-508"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-509">Instrui a pilha a iniciar um processo de handshake do WebSocket com [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="b1b50-509">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="b1b50-510">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b1b50-510">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-511"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**URL DA OPÇÃO \_ WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-511"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-512">Recupera um valor de cadeia de caracteres que contém a URL completa de um recurso baixado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-512">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="b1b50-513">Se a URL original contiver dados extras, como cadeias de caracteres de pesquisa ou âncoras, ou se a chamada tiver sido redirecionada, a URL retornada será diferente da original.</span><span class="sxs-lookup"><span data-stu-id="b1b50-513">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="b1b50-514">O aplicativo deve passar um buffer, dimensionado em bytes, que é grande o suficiente para manter a URL retornada em caractere largo.</span><span class="sxs-lookup"><span data-stu-id="b1b50-514">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-515"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**OPÇÃO WINHTTP \_ \_ USAR CREDENCIAIS DE \_ \_ SERVIDOR GLOBAL \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-515"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-516">Aceita um **BOOL** e pode ser definido apenas como um alça de sessão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-516">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="b1b50-517">Ele só será propagado para os alças criados a partir do alça de sessão depois que a opção tiver sido definida.</span><span class="sxs-lookup"><span data-stu-id="b1b50-517">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="b1b50-518">Se **TRUE**, essa opção causará como último recurso o uso de credenciais de servidor global que foram pressionadas do WinInet.</span><span class="sxs-lookup"><span data-stu-id="b1b50-518">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="b1b50-519">O padrão para essa opção é **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="b1b50-519">The default for this option is **FALSE**.</span></span> <span data-ttu-id="b1b50-520">Essa opção requer a chave do Registro **HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp.**</span><span class="sxs-lookup"><span data-stu-id="b1b50-520">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="b1b50-521">Essa chave do Registro não está presente por padrão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-521">This registry key is not present by default.</span></span> <span data-ttu-id="b1b50-522">Quando estiver definido, o WinINet enviará credenciais para WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b1b50-522">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="b1b50-523">Sempre que o WinHttp receber um desafio de autenticação e se não houver credenciais definidas no alçamento atual, ele usará as credenciais fornecidas pelo WinINet.</span><span class="sxs-lookup"><span data-stu-id="b1b50-523">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-524"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**AGENTE DO USUÁRIO DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-524"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-525">Define ou recupera [](glossary.md) a cadeia de caracteres do agente do usuário em alças fornecidas por [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) e usadas em funções [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) subsequentes, desde que ela não seja substituído por um header adicionado por [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) ou **WinHttpSendRequest.**</span><span class="sxs-lookup"><span data-stu-id="b1b50-525">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="b1b50-526">Ao recuperar um agente de usuário, o aplicativo deve passar um buffer, dimensionado em bytes, que é grande o suficiente para manter a URL retornada em caractere largo.</span><span class="sxs-lookup"><span data-stu-id="b1b50-526">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="b1b50-527">Ao definir o agente do usuário, o tamanho do buffer é o comprimento da cadeia de caracteres, em caracteres, mais o **terminador NULL.**</span><span class="sxs-lookup"><span data-stu-id="b1b50-527">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-528"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**NOME DE USUÁRIO DA OPÇÃO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-528"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-529">Define ou recupera uma cadeia de caracteres que contém o nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="b1b50-529">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-530"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ CLOSE \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="b1b50-530"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-531">Define o tempo, em milissegundos, que [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) deve aguardar para concluir o handshake de fechamento.</span><span class="sxs-lookup"><span data-stu-id="b1b50-531">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="b1b50-532">O padrão é 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="b1b50-532">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-533"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ KEEPALIVE \_ INTERVAL**</span><span class="sxs-lookup"><span data-stu-id="b1b50-533"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-534">Define o intervalo, em milissegundos, para enviar um pacote keep alive pela conexão.</span><span class="sxs-lookup"><span data-stu-id="b1b50-534">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="b1b50-535">O intervalo padrão é 30000 (30 segundos).</span><span class="sxs-lookup"><span data-stu-id="b1b50-535">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="b1b50-536">O intervalo mínimo é 15000 (15 segundos).</span><span class="sxs-lookup"><span data-stu-id="b1b50-536">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="b1b50-537">O [**uso de WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para definir um valor inferior a 15000 retornará com **ERROR INVALID \_ \_ PARAMETER**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-537">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="b1b50-538">O valor padrão para **WINHTTP \_ OPTION WEB SOCKET \_ \_ \_ KEEPALIVE \_ INTERVAL** é lido de **HKLM: \\ SOFTWARE Microsoft \\ \\ WebSocket \\ KeepaliveInterval**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-538">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="b1b50-539">Se um valor não for definido, o valor padrão de 30000 será usado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-539">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="b1b50-540">Não é possível ter um intervalo keepalive inferior a 15000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="b1b50-540">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-541"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ RECEIVE \_ BUFFER \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="b1b50-541"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-542">Define ou recupera um DWORD que especifica o tamanho do buffer de recebimento a ser usado em conexões WebSocket.</span><span class="sxs-lookup"><span data-stu-id="b1b50-542">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-543"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ SEND \_ BUFFER \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="b1b50-543"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-544">Define ou recupera um DWORD que especifica o tamanho do buffer de envio a ser usado em conexões WebSocket.</span><span class="sxs-lookup"><span data-stu-id="b1b50-544">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-545"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**CONTAGEM DE \_ \_ THREADS DE TRABALHO DA OPÇÃO \_ WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-545"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-546">Define um valor inteiro longo sem sinal que especifica o número de threads de trabalho que o pool de threads deve usar para preenchimentos assíncronos.</span><span class="sxs-lookup"><span data-stu-id="b1b50-546">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="b1b50-547">O valor padrão dessa opção é zero, que especifica que o número de threads de trabalho é igual ao número de CPUs no sistema.</span><span class="sxs-lookup"><span data-stu-id="b1b50-547">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="b1b50-548">Essa opção só pode ser definida em um manipular **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) antes que uma operação assíncrona tenha ocorrido.</span><span class="sxs-lookup"><span data-stu-id="b1b50-548">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="b1b50-549">Essa opção só pode ser definida uma vez.</span><span class="sxs-lookup"><span data-stu-id="b1b50-549">This option can only be set once.</span></span>

<span data-ttu-id="b1b50-550">**Windows Server 2008 R2 e Windows 7:** Esse sinalizador está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="b1b50-550">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b50-551"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**TAMANHO DO \_ BUFFER DE GRAVAÇÃO DA OPÇÃO WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-551"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b1b50-552">Essa opção foi preterida; ele não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="b1b50-552">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1b50-553">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1b50-553">Remarks</span></span>

<span data-ttu-id="b1b50-554">A tabela a seguir lista os sinalizadores de opção especificando quais identificador eles podem agir, se eles podem ser consultados e definidos e o tipo de dados usado.</span><span class="sxs-lookup"><span data-stu-id="b1b50-554">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="b1b50-555">Um "X" indica que o sinalizador de opção é válido para uso com a função ou o handle, enquanto um "-" especifica que o sinalizador de opção é inválido.</span><span class="sxs-lookup"><span data-stu-id="b1b50-555">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="b1b50-556">Tentar definir ou consultar um sinalizador de opção em uma versão do Windows em que não há suporte resultará em **ERRO \_ WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="b1b50-556">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="b1b50-557">Sinalizador de opção e tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b1b50-557">Option flag, and data type</span></span> | <span data-ttu-id="b1b50-558">Alça de sessão</span><span class="sxs-lookup"><span data-stu-id="b1b50-558">Session handle</span></span> | <span data-ttu-id="b1b50-559">Alça de solicitação</span><span class="sxs-lookup"><span data-stu-id="b1b50-559">Request handle</span></span> | <span data-ttu-id="b1b50-560">Opção de consulta</span><span class="sxs-lookup"><span data-stu-id="b1b50-560">Query option</span></span> | <span data-ttu-id="b1b50-561">Opção Set</span><span class="sxs-lookup"><span data-stu-id="b1b50-561">Set option</span></span> | <span data-ttu-id="b1b50-562">Versão mínima do Windows</span><span class="sxs-lookup"><span data-stu-id="b1b50-562">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="b1b50-563">OPÇÃO WINHTTP \_ COM \_ CERTEZA \_ \_ \_ RETORNOS DE CHAMADA SEM BLOQUEIO</span><span class="sxs-lookup"><span data-stu-id="b1b50-563">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="b1b50-564">**Bool**</span><span class="sxs-lookup"><span data-stu-id="b1b50-564">**BOOL**</span></span> | <span data-ttu-id="b1b50-565">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-565">X</span></span> | \- | \- | <span data-ttu-id="b1b50-566">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-566">X</span></span> | \- |
| <span data-ttu-id="b1b50-567">POLÍTICA DE LOGOM AUTOMÁTICO DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-567">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="b1b50-568">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-568">**DWORD**</span></span> | \- | <span data-ttu-id="b1b50-569">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-569">X</span></span> | \- | <span data-ttu-id="b1b50-570">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-570">X</span></span> | \- |
| <span data-ttu-id="b1b50-571">RETORNO DE CHAMADA DA OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-571">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="b1b50-572">**Lpvoid**</span><span class="sxs-lookup"><span data-stu-id="b1b50-572">**LPVOID**</span></span> | <span data-ttu-id="b1b50-573">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-573">X</span></span> | <span data-ttu-id="b1b50-574">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-574">X</span></span> | <span data-ttu-id="b1b50-575">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-575">X</span></span> | <span data-ttu-id="b1b50-576">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-576">X</span></span> | \- |
| <span data-ttu-id="b1b50-577">CONTEXTO DE CERTIFICADO \_ \_ DO CLIENTE WINHTTP OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-577">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="b1b50-578">**CONTEXTO DO \_ CERTIFICADO**</span><span class="sxs-lookup"><span data-stu-id="b1b50-578">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="b1b50-579">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-579">X</span></span> | \- | <span data-ttu-id="b1b50-580">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-580">X</span></span> | <span data-ttu-id="b1b50-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1b50-581">Windows Vista</span></span> |
| <span data-ttu-id="b1b50-582">LISTA DO EMISSOR DO CERTIFICADO \_ \_ DO \_ CLIENTE \_ \_ WINHTTP OPTION</span><span class="sxs-lookup"><span data-stu-id="b1b50-582">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="b1b50-583">**IssuerListInfoEx de SecPkgContext \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-583">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="b1b50-584">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-584">X</span></span> | <span data-ttu-id="b1b50-585">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-585">X</span></span> | \- | <span data-ttu-id="b1b50-586">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1b50-586">Windows Vista</span></span> |
| <span data-ttu-id="b1b50-587">PÁGINA DE CÓDIGO DA OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-587">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="b1b50-588">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-588">**DWORD**</span></span> | <span data-ttu-id="b1b50-589">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-589">X</span></span> | \- | \- | <span data-ttu-id="b1b50-590">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-590">X</span></span> | \- |
| <span data-ttu-id="b1b50-591">OPÇÃO WINHTTP \_ \_ CONFIGURAR O PASSPORT \_ \_ AUTH</span><span class="sxs-lookup"><span data-stu-id="b1b50-591">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="b1b50-592">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-592">**DWORD**</span></span> | <span data-ttu-id="b1b50-593">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-593">X</span></span> | \- | \- | <span data-ttu-id="b1b50-594">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-594">X</span></span> | \- |
| <span data-ttu-id="b1b50-595">WINHTTP \_ OPTION \_ CONNECT \_ RETRIES</span><span class="sxs-lookup"><span data-stu-id="b1b50-595">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="b1b50-596">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-596">**DWORD**</span></span> | <span data-ttu-id="b1b50-597">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-597">X</span></span> | <span data-ttu-id="b1b50-598">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-598">X</span></span> | <span data-ttu-id="b1b50-599">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-599">X</span></span> | <span data-ttu-id="b1b50-600">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-600">X</span></span> | \- |
| <span data-ttu-id="b1b50-601">\_ \_ tempo limite de conexão da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-601">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="b1b50-602">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-602">**DWORD**</span></span> | <span data-ttu-id="b1b50-603">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-603">X</span></span> | <span data-ttu-id="b1b50-604">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-604">X</span></span> | <span data-ttu-id="b1b50-605">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-605">X</span></span> | <span data-ttu-id="b1b50-606">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-606">X</span></span> | \- |
| <span data-ttu-id="b1b50-607">\_informações de \_ conexão da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-607">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="b1b50-608">**\_informações de conexão WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-608">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="b1b50-609">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-609">X</span></span> | <span data-ttu-id="b1b50-610">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-610">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-611">\_V0 de \_ Estatísticas de conexão da opção WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-611">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="b1b50-612">**\_V0 de informações TCP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-612">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="b1b50-613">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-613">X</span></span> | <span data-ttu-id="b1b50-614">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-614">X</span></span> | \- | <span data-ttu-id="b1b50-615">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="b1b50-615">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="b1b50-616">\_Estatísticas de conexão da opção WinHTTP \_ \_ \_ v1</span><span class="sxs-lookup"><span data-stu-id="b1b50-616">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="b1b50-617">**Informações de TCP \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="b1b50-617">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="b1b50-618">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-618">X</span></span> | <span data-ttu-id="b1b50-619">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-619">X</span></span> | \- | <span data-ttu-id="b1b50-620">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="b1b50-620">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="b1b50-621">\_valor de \_ contexto da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-621">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="b1b50-622">**PTR de DWORD \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-622">**DWORD\_PTR**</span></span> | <span data-ttu-id="b1b50-623">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-623">X</span></span> | <span data-ttu-id="b1b50-624">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-624">X</span></span> | <span data-ttu-id="b1b50-625">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-625">X</span></span> | <span data-ttu-id="b1b50-626">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-626">X</span></span> | \- |
| <span data-ttu-id="b1b50-627">\_DEScompactação da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-627">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="b1b50-628">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-628">**DWORD**</span></span> | <span data-ttu-id="b1b50-629">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-629">X</span></span> | <span data-ttu-id="b1b50-630">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-630">X</span></span> | \- | <span data-ttu-id="b1b50-631">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-631">X</span></span> | <span data-ttu-id="b1b50-632">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b1b50-632">Windows 8.1</span></span> |
| <span data-ttu-id="b1b50-633">\_recurso de \_ desabilitação da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-633">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="b1b50-634">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-634">**DWORD**</span></span> | \- | <span data-ttu-id="b1b50-635">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-635">X</span></span> | \- | <span data-ttu-id="b1b50-636">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-636">X</span></span> | \- |
| <span data-ttu-id="b1b50-637">\_opção WinHTTP \_ desabilitar \_ \_ FALLBACK de protocolo seguro \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-637">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="b1b50-638">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="b1b50-638">**BOOL**</span></span> | <span data-ttu-id="b1b50-639">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-639">X</span></span> | \- | \- | <span data-ttu-id="b1b50-640">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-640">X</span></span> | <span data-ttu-id="b1b50-641">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="b1b50-641">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="b1b50-642">\_opção WinHTTP \_ desabilitar \_ fila de fluxos \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-642">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="b1b50-643">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="b1b50-643">**BOOL**</span></span> | <span data-ttu-id="b1b50-644">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-644">X</span></span> | <span data-ttu-id="b1b50-645">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-645">X</span></span> | \- | <span data-ttu-id="b1b50-646">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-646">X</span></span> | <span data-ttu-id="b1b50-647">Windows 10 versão 1809</span><span class="sxs-lookup"><span data-stu-id="b1b50-647">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="b1b50-648">\_opção WinHTTP \_ habilitar \_ recurso</span><span class="sxs-lookup"><span data-stu-id="b1b50-648">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="b1b50-649">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-649">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="b1b50-650">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-650">X</span></span> | \- |
| <span data-ttu-id="b1b50-651">\_opção WinHTTP \_ habilitar \_ \_ protocolo http</span><span class="sxs-lookup"><span data-stu-id="b1b50-651">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="b1b50-652">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-652">**DWORD**</span></span> | <span data-ttu-id="b1b50-653">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-653">X</span></span> | <span data-ttu-id="b1b50-654">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-654">X</span></span> | \- | <span data-ttu-id="b1b50-655">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-655">X</span></span> | <span data-ttu-id="b1b50-656">Windows 10, versão 1607</span><span class="sxs-lookup"><span data-stu-id="b1b50-656">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="b1b50-657">opção de WINHTTP \_ \_ ENABLETRACING</span><span class="sxs-lookup"><span data-stu-id="b1b50-657">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="b1b50-658">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-658">**DWORD**</span></span> | \- | \- | <span data-ttu-id="b1b50-659">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-659">X</span></span> | <span data-ttu-id="b1b50-660">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-660">X</span></span> | \- |
| <span data-ttu-id="b1b50-661">codificação de opção de WINHTTP \_ \_ \_ extra</span><span class="sxs-lookup"><span data-stu-id="b1b50-661">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="b1b50-662">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="b1b50-662">**BOOL**</span></span> | <span data-ttu-id="b1b50-663">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-663">X</span></span> | <span data-ttu-id="b1b50-664">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-664">X</span></span> | \- | <span data-ttu-id="b1b50-665">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-665">X</span></span> | <span data-ttu-id="b1b50-666">Windows 10 versão 1803</span><span class="sxs-lookup"><span data-stu-id="b1b50-666">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="b1b50-667">a \_ opção WinHTTP \_ expira a \_ conexão</span><span class="sxs-lookup"><span data-stu-id="b1b50-667">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="b1b50-668">N/D</span><span class="sxs-lookup"><span data-stu-id="b1b50-668">N/A</span></span> | \- | <span data-ttu-id="b1b50-669">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-669">X</span></span> | \- | <span data-ttu-id="b1b50-670">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-670">X</span></span> | <span data-ttu-id="b1b50-671">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="b1b50-671">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="b1b50-672">\_ \_ erro estendido da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-672">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="b1b50-673">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-673">**DWORD**</span></span> | <span data-ttu-id="b1b50-674">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-674">X</span></span> | <span data-ttu-id="b1b50-675">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-675">X</span></span> | <span data-ttu-id="b1b50-676">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-676">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-677">\_credenciais de \_ \_ proxy global de opção \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="b1b50-677">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="b1b50-678">**credenciais de WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-678">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="b1b50-679">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-679">X</span></span> | <span data-ttu-id="b1b50-680">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-680">X</span></span> | \- | <span data-ttu-id="b1b50-681">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-681">X</span></span> | \- |
| <span data-ttu-id="b1b50-682">\_ \_ \_ credenciais do servidor global da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-682">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="b1b50-683">**WINHTTP \_ creds \_ ex**</span><span class="sxs-lookup"><span data-stu-id="b1b50-683">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="b1b50-684">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-684">X</span></span> | <span data-ttu-id="b1b50-685">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-685">X</span></span> | \- | <span data-ttu-id="b1b50-686">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-686">X</span></span> | \- |
| <span data-ttu-id="b1b50-687">\_tipo de \_ identificador de opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-687">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="b1b50-688">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-688">**DWORD**</span></span> | <span data-ttu-id="b1b50-689">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-689">X</span></span> | <span data-ttu-id="b1b50-690">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-690">X</span></span> | <span data-ttu-id="b1b50-691">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-691">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-692">\_protocolo http de opção WinHTTP \_ \_ \_ necessário</span><span class="sxs-lookup"><span data-stu-id="b1b50-692">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="b1b50-693">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="b1b50-693">**BOOL**</span></span> | <span data-ttu-id="b1b50-694">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-694">X</span></span> | <span data-ttu-id="b1b50-695">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-695">X</span></span> | \- | <span data-ttu-id="b1b50-696">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-696">X</span></span> | <span data-ttu-id="b1b50-697">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="b1b50-697">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="b1b50-698">\_protocolo http de opção WinHTTP \_ \_ \_ usado</span><span class="sxs-lookup"><span data-stu-id="b1b50-698">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="b1b50-699">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-699">**DWORD**</span></span> | \- | <span data-ttu-id="b1b50-700">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-700">X</span></span> | <span data-ttu-id="b1b50-701">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-701">X</span></span> | \- | <span data-ttu-id="b1b50-702">Windows 10, versão 1607</span><span class="sxs-lookup"><span data-stu-id="b1b50-702">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="b1b50-703">\_versão de \_ http da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-703">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="b1b50-704">**\_informações de versão de http \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-704">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="b1b50-705">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-705">X</span></span> | <span data-ttu-id="b1b50-706">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-706">X</span></span> | <span data-ttu-id="b1b50-707">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-707">X</span></span> | <span data-ttu-id="b1b50-708">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-708">X</span></span> | \- |
| <span data-ttu-id="b1b50-709">\_opção WinHTTP \_ ignorar \_ \_ revogação de certificado \_ offline</span><span class="sxs-lookup"><span data-stu-id="b1b50-709">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="b1b50-710">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="b1b50-710">**BOOL**</span></span> | \- | <span data-ttu-id="b1b50-711">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-711">X</span></span> | \- | <span data-ttu-id="b1b50-712">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-712">X</span></span> | <span data-ttu-id="b1b50-713">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="b1b50-713">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="b1b50-714">\_Opção WinHTTP \_ IPv6 \_ Fast \_ FALLBACK</span><span class="sxs-lookup"><span data-stu-id="b1b50-714">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="b1b50-715">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="b1b50-715">**BOOL**</span></span> | <span data-ttu-id="b1b50-716">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-716">X</span></span> | \- | \- | <span data-ttu-id="b1b50-717">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-717">X</span></span> | <span data-ttu-id="b1b50-718">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="b1b50-718">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="b1b50-719">a \_ opção WinHTTP \_ é uma resposta de \_ conexão de proxy \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-719">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="b1b50-720">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="b1b50-720">**BOOL**</span></span> | <span data-ttu-id="b1b50-721">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-721">X</span></span> | <span data-ttu-id="b1b50-722">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-722">X</span></span> | <span data-ttu-id="b1b50-723">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-723">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-724">Opção de WINHTTP \_ \_ Max \_ Conns \_ por \_ servidor de 1 \_ 0 \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-724">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="b1b50-725">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-725">**DWORD**</span></span> | <span data-ttu-id="b1b50-726">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-726">X</span></span> | \- | <span data-ttu-id="b1b50-727">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-727">X</span></span> | <span data-ttu-id="b1b50-728">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-728">X</span></span> | \- |
| <span data-ttu-id="b1b50-729">opção de WINHTTP \_ \_ Max \_ Conns \_ por \_ servidor</span><span class="sxs-lookup"><span data-stu-id="b1b50-729">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="b1b50-730">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-730">**DWORD**</span></span> | <span data-ttu-id="b1b50-731">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-731">X</span></span> | \- | <span data-ttu-id="b1b50-732">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-732">X</span></span> | <span data-ttu-id="b1b50-733">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-733">X</span></span> | \- |
| <span data-ttu-id="b1b50-734">opção WINHTTP máx. de \_ \_ \_ \_ redirecionamentos automáticos de http \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-734">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="b1b50-735">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-735">**DWORD**</span></span> | <span data-ttu-id="b1b50-736">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-736">X</span></span> | <span data-ttu-id="b1b50-737">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-737">X</span></span> | <span data-ttu-id="b1b50-738">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-738">X</span></span> | <span data-ttu-id="b1b50-739">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-739">X</span></span> | \- |
| <span data-ttu-id="b1b50-740">\_máximo de \_ status HTTP da opção WinHTTP \_ \_ \_ continuar</span><span class="sxs-lookup"><span data-stu-id="b1b50-740">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="b1b50-741">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-741">**DWORD**</span></span> | <span data-ttu-id="b1b50-742">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-742">X</span></span> | <span data-ttu-id="b1b50-743">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-743">X</span></span> | <span data-ttu-id="b1b50-744">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-744">X</span></span> | <span data-ttu-id="b1b50-745">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-745">X</span></span> | \- |
| <span data-ttu-id="b1b50-746">\_tamanho de \_ \_ dreno de resposta máx da opção \_ WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-746">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="b1b50-747">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-747">**DWORD**</span></span> | <span data-ttu-id="b1b50-748">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-748">X</span></span> | <span data-ttu-id="b1b50-749">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-749">X</span></span> | <span data-ttu-id="b1b50-750">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-750">X</span></span> | <span data-ttu-id="b1b50-751">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-751">X</span></span> | \- |
| <span data-ttu-id="b1b50-752">\_ \_ tamanho máximo do \_ cabeçalho de resposta da \_ opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-752">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="b1b50-753">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-753">**DWORD**</span></span> | <span data-ttu-id="b1b50-754">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-754">X</span></span> | <span data-ttu-id="b1b50-755">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-755">X</span></span> | <span data-ttu-id="b1b50-756">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-756">X</span></span> | <span data-ttu-id="b1b50-757">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-757">X</span></span> | \- |
| <span data-ttu-id="b1b50-758">\_ \_ identificador pai da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-758">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="b1b50-759">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="b1b50-759">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="b1b50-760">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-760">X</span></span> | <span data-ttu-id="b1b50-761">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-761">X</span></span> | <span data-ttu-id="b1b50-762">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-762">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-763">opção WINHTTP de \_ \_ \_ texto de comarcação do Passport \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-763">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="b1b50-764">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="b1b50-764">**LPWSTR**</span></span> | \- | <span data-ttu-id="b1b50-765">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-765">X</span></span> | <span data-ttu-id="b1b50-766">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-766">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-767">\_URL de \_ \_ comarcação do passaporte da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-767">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="b1b50-768">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="b1b50-768">**LPWSTR**</span></span> | \- | <span data-ttu-id="b1b50-769">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-769">X</span></span> | <span data-ttu-id="b1b50-770">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-770">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-771">\_opção WinHTTP \_ URL de retorno do Passport \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-771">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="b1b50-772">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="b1b50-772">**LPVOID**</span></span> | \- | <span data-ttu-id="b1b50-773">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-773">X</span></span> | <span data-ttu-id="b1b50-774">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-774">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-775">opção WINHTTP sair do \_ \_ Passport \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-775">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="b1b50-776">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="b1b50-776">**LPVOID**</span></span> | <span data-ttu-id="b1b50-777">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-777">X</span></span> | \- | \- | <span data-ttu-id="b1b50-778">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-778">X</span></span> | \- |
| <span data-ttu-id="b1b50-779">\_senha da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-779">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="b1b50-780">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="b1b50-780">**LPWSTR**</span></span> | \- | <span data-ttu-id="b1b50-781">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-781">X</span></span> | <span data-ttu-id="b1b50-782">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-782">X</span></span> | <span data-ttu-id="b1b50-783">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-783">X</span></span> | \- |
| <span data-ttu-id="b1b50-784">\_proxy de opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-784">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="b1b50-785">**\_informações de proxy WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-785">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="b1b50-786">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-786">X</span></span> | <span data-ttu-id="b1b50-787">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-787">X</span></span> | <span data-ttu-id="b1b50-788">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-788">X</span></span> | <span data-ttu-id="b1b50-789">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-789">X</span></span> | \- |
| <span data-ttu-id="b1b50-790">\_senha do \_ proxy da opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-790">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="b1b50-791">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="b1b50-791">**LPWSTR**</span></span> | \- | <span data-ttu-id="b1b50-792">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-792">X</span></span> | <span data-ttu-id="b1b50-793">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-793">X</span></span> | <span data-ttu-id="b1b50-794">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-794">X</span></span> | \- |
| <span data-ttu-id="b1b50-795">SPN de proxy de opção de WINHTTP \_ \_ \_ \_ usado</span><span class="sxs-lookup"><span data-stu-id="b1b50-795">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="b1b50-796">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="b1b50-796">**LPWSTR**</span></span> | \- | <span data-ttu-id="b1b50-797">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-797">X</span></span> | <span data-ttu-id="b1b50-798">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-798">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-799">\_nome de \_ usuário do proxy de opção WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-799">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="b1b50-800">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="b1b50-800">**LPWSTR**</span></span> | \- | <span data-ttu-id="b1b50-801">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-801">X</span></span> | <span data-ttu-id="b1b50-802">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-802">X</span></span> | <span data-ttu-id="b1b50-803">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-803">X</span></span> | \- |
| <span data-ttu-id="b1b50-804">TAMANHO DO \_ BUFFER DE LEITURA DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-804">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="b1b50-805">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-805">**DWORD**</span></span> | \- | <span data-ttu-id="b1b50-806">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-806">X</span></span> | <span data-ttu-id="b1b50-807">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-807">X</span></span> | <span data-ttu-id="b1b50-808">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-808">X</span></span> | \- |
| <span data-ttu-id="b1b50-809">RESPOSTA DE CONEXÃO DE \_ \_ PROXY DE RECEBIMENTO DA \_ \_ \_ OPÇÃO WINHTTP</span><span class="sxs-lookup"><span data-stu-id="b1b50-809">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="b1b50-810">**Bool**</span><span class="sxs-lookup"><span data-stu-id="b1b50-810">**BOOL**</span></span> | <span data-ttu-id="b1b50-811">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-811">X</span></span> | <span data-ttu-id="b1b50-812">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-812">X</span></span> | \- | <span data-ttu-id="b1b50-813">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-813">X</span></span> | \- |
| <span data-ttu-id="b1b50-814">WINHTTP \_ OPTION \_ RECEIVE \_ RESPONSE \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b1b50-814">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="b1b50-815">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-815">**DWORD**</span></span> | <span data-ttu-id="b1b50-816">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-816">X</span></span> | <span data-ttu-id="b1b50-817">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-817">X</span></span> | <span data-ttu-id="b1b50-818">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-818">X</span></span> | <span data-ttu-id="b1b50-819">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-819">X</span></span> | \- |
| <span data-ttu-id="b1b50-820">WINHTTP \_ OPTION \_ RECEIVE \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b1b50-820">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="b1b50-821">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-821">**DWORD**</span></span> | <span data-ttu-id="b1b50-822">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-822">X</span></span> | <span data-ttu-id="b1b50-823">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-823">X</span></span> | <span data-ttu-id="b1b50-824">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-824">X</span></span> | <span data-ttu-id="b1b50-825">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-825">X</span></span> | \- |
| <span data-ttu-id="b1b50-826">POLÍTICA DE \_ REDIRECIONAMENTO DE OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-826">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="b1b50-827">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-827">**DWORD**</span></span> | <span data-ttu-id="b1b50-828">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-828">X</span></span> | <span data-ttu-id="b1b50-829">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-829">X</span></span> | <span data-ttu-id="b1b50-830">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-830">X</span></span> | <span data-ttu-id="b1b50-831">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-831">X</span></span> | \- |
| <span data-ttu-id="b1b50-832">OPÇÃO WINHTTP \_ REJEITAR \_ \_ USERPWD \_ NA \_ URL</span><span class="sxs-lookup"><span data-stu-id="b1b50-832">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="b1b50-833">**Bool**</span><span class="sxs-lookup"><span data-stu-id="b1b50-833">**BOOL**</span></span> | \- | <span data-ttu-id="b1b50-834">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-834">X</span></span> | \- | <span data-ttu-id="b1b50-835">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-835">X</span></span> | \- |
| <span data-ttu-id="b1b50-836">PRIORIDADE DE \_ SOLICITAÇÃO DE OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-836">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="b1b50-837">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-837">**DWORD**</span></span> | \- | <span data-ttu-id="b1b50-838">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-838">X</span></span> | <span data-ttu-id="b1b50-839">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-839">X</span></span> | <span data-ttu-id="b1b50-840">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-840">X</span></span> | \- |
| <span data-ttu-id="b1b50-841">ESTATÍSTICAS DE \_ SOLICITAÇÃO DE OPÇÃO \_ WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-841">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="b1b50-842">**ESTATÍSTICAS DE \_ SOLICITAÇÃO \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="b1b50-842">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="b1b50-843">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-843">X</span></span> | <span data-ttu-id="b1b50-844">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-844">X</span></span> | \- | <span data-ttu-id="b1b50-845">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="b1b50-845">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="b1b50-846">TEMPOS DE \_ SOLICITAÇÃO DA OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-846">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="b1b50-847">**TEMPOS DE \_ SOLICITAÇÃO WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-847">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="b1b50-848">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-848">X</span></span> | <span data-ttu-id="b1b50-849">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-849">X</span></span> | \- | <span data-ttu-id="b1b50-850">Windows 10 versão 1903</span><span class="sxs-lookup"><span data-stu-id="b1b50-850">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="b1b50-851">WINHTTP \_ OPTION \_ RESOLVE \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b1b50-851">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="b1b50-852">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-852">**DWORD**</span></span> | <span data-ttu-id="b1b50-853">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-853">X</span></span> | <span data-ttu-id="b1b50-854">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-854">X</span></span> | <span data-ttu-id="b1b50-855">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-855">X</span></span> | <span data-ttu-id="b1b50-856">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-856">X</span></span> | \- |
| <span data-ttu-id="b1b50-857">PROTOCOLOS SEGUROS DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-857">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="b1b50-858">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-858">**DWORD**</span></span> | <span data-ttu-id="b1b50-859">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-859">X</span></span> | \- | \- | <span data-ttu-id="b1b50-860">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-860">X</span></span> | \- |
| <span data-ttu-id="b1b50-861">STRUCT DO CERTIFICADO \_ \_ DE SEGURANÇA DA \_ OPÇÃO WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-861">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="b1b50-862">**INFORMAÇÕES DE CERTIFICADO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1b50-862">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="b1b50-863">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-863">X</span></span> | <span data-ttu-id="b1b50-864">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-864">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-865">SINALIZADORES DE SEGURANÇA DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-865">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="b1b50-866">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-866">**DWORD**</span></span> | \- | <span data-ttu-id="b1b50-867">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-867">X</span></span> | <span data-ttu-id="b1b50-868">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-868">X</span></span> | <span data-ttu-id="b1b50-869">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-869">X</span></span> | \- |
| <span data-ttu-id="b1b50-870">INFORMAÇÕES DE SEGURANÇA DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-870">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="b1b50-871">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="b1b50-871">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="b1b50-872">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-872">X</span></span> | <span data-ttu-id="b1b50-873">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-873">X</span></span> | \- | <span data-ttu-id="b1b50-874">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="b1b50-874">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="b1b50-875">BITNESS \_ DA CHAVE \_ DE SEGURANÇA DA \_ \_ OPÇÃO WINHTTP</span><span class="sxs-lookup"><span data-stu-id="b1b50-875">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="b1b50-876">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-876">**DWORD**</span></span> | \- | <span data-ttu-id="b1b50-877">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-877">X</span></span> | <span data-ttu-id="b1b50-878">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-878">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-879">WINHTTP \_ OPTION \_ SEND \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b1b50-879">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="b1b50-880">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-880">**DWORD**</span></span> | <span data-ttu-id="b1b50-881">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-881">X</span></span> | <span data-ttu-id="b1b50-882">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-882">X</span></span> | <span data-ttu-id="b1b50-883">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-883">X</span></span> | <span data-ttu-id="b1b50-884">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-884">X</span></span> | \- |
| <span data-ttu-id="b1b50-885">CBT DO \_ SERVIDOR DE OPÇÕES \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="b1b50-885">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="b1b50-886">[**Vinculações SecPkgContext \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="b1b50-886">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="b1b50-887">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-887">X</span></span> | <span data-ttu-id="b1b50-888">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-888">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-889">CONTEXTO DA CADEIA DE \_ \_ CERTIFICADOS \_ DO SERVIDOR WINHTTP OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-889">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="b1b50-890">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="b1b50-890">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="b1b50-891">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-891">X</span></span> | <span data-ttu-id="b1b50-892">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-892">X</span></span> | \- | <span data-ttu-id="b1b50-893">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="b1b50-893">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="b1b50-894">CONTEXTO DE CERTIFICADO \_ DO \_ SERVIDOR WINHTTP OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-894">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="b1b50-895">**CONTEXTO DO CERTIFICADO**</span><span class="sxs-lookup"><span data-stu-id="b1b50-895">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="b1b50-896">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-896">X</span></span> | <span data-ttu-id="b1b50-897">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-897">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-898">SPN DO \_ SERVIDOR DE OPÇÕES \_ \_ WINHTTP \_ USADO</span><span class="sxs-lookup"><span data-stu-id="b1b50-898">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="b1b50-899">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="b1b50-899">**LPWSTR**</span></span> | \- | <span data-ttu-id="b1b50-900">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-900">X</span></span> | <span data-ttu-id="b1b50-901">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-901">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-902">SPN DA \_ OPÇÃO \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="b1b50-902">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="b1b50-903">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-903">**DWORD**</span></span> | \- | <span data-ttu-id="b1b50-904">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-904">X</span></span> | \- | <span data-ttu-id="b1b50-905">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-905">X</span></span> | \- |
| <span data-ttu-id="b1b50-906">WINHTTP \_ OPTION \_ TCP \_ FAST \_ OPEN</span><span class="sxs-lookup"><span data-stu-id="b1b50-906">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="b1b50-907">**Bool**</span><span class="sxs-lookup"><span data-stu-id="b1b50-907">**BOOL**</span></span> | <span data-ttu-id="b1b50-908">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-908">X</span></span> | \- | \- | <span data-ttu-id="b1b50-909">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-909">X</span></span> | <span data-ttu-id="b1b50-910">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="b1b50-910">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="b1b50-911">WINHTTP \_ OPTION \_ TLS \_ FALSE \_ START</span><span class="sxs-lookup"><span data-stu-id="b1b50-911">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="b1b50-912">**Bool**</span><span class="sxs-lookup"><span data-stu-id="b1b50-912">**BOOL**</span></span> | <span data-ttu-id="b1b50-913">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-913">X</span></span> | \- | \- | <span data-ttu-id="b1b50-914">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-914">X</span></span> | <span data-ttu-id="b1b50-915">Windows 10 versão 2004</span><span class="sxs-lookup"><span data-stu-id="b1b50-915">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="b1b50-916">EVENTO DE \_ NOTIFICAÇÃO \_ DE DESCARREGAMENTO DE OPÇÃO \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="b1b50-916">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="b1b50-917">Hinternet</span><span class="sxs-lookup"><span data-stu-id="b1b50-917">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="b1b50-918">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-918">X</span></span> | \- | \- | <span data-ttu-id="b1b50-919">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-919">X</span></span> | \- |
| <span data-ttu-id="b1b50-920">ANÁLISE DE TÍTULO NÃO SEGURO DA OPÇÃO WINHTTP \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-920">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="b1b50-921">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-921">**DWORD**</span></span> | \- | <span data-ttu-id="b1b50-922">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-922">X</span></span> | \- | <span data-ttu-id="b1b50-923">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-923">X</span></span> | \- |
| <span data-ttu-id="b1b50-924">ATUALIZAÇÃO DA OPÇÃO WINHTTP \_ \_ PARA O \_ \_ SOQUETE DA \_ WEB</span><span class="sxs-lookup"><span data-stu-id="b1b50-924">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="b1b50-925">N/D</span><span class="sxs-lookup"><span data-stu-id="b1b50-925">N/A</span></span> | \- | <span data-ttu-id="b1b50-926">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-926">X</span></span> | \- | <span data-ttu-id="b1b50-927">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-927">X</span></span> | \- |
| <span data-ttu-id="b1b50-928">URL DA OPÇÃO \_ WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-928">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="b1b50-929">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="b1b50-929">**LPWSTR**</span></span> | \- | <span data-ttu-id="b1b50-930">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-930">X</span></span> | <span data-ttu-id="b1b50-931">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-931">X</span></span> | \- | \- |
| <span data-ttu-id="b1b50-932">OPÇÃO WINHTTP \_ \_ USAR CREDENCIAIS DE \_ \_ SERVIDOR GLOBAL \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-932">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="b1b50-933">**Bool**</span><span class="sxs-lookup"><span data-stu-id="b1b50-933">**BOOL**</span></span> | <span data-ttu-id="b1b50-934">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-934">X</span></span> | <span data-ttu-id="b1b50-935">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-935">X</span></span> | \- | <span data-ttu-id="b1b50-936">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-936">X</span></span> | \- |
| <span data-ttu-id="b1b50-937">AGENTE DO USUÁRIO DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-937">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="b1b50-938">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="b1b50-938">**LPWSTR**</span></span> | <span data-ttu-id="b1b50-939">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-939">X</span></span> | \- | <span data-ttu-id="b1b50-940">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-940">X</span></span> | <span data-ttu-id="b1b50-941">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-941">X</span></span> | \- |
| <span data-ttu-id="b1b50-942">NOME DE USUÁRIO DA OPÇÃO WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-942">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="b1b50-943">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="b1b50-943">**LPWSTR**</span></span> | \- | <span data-ttu-id="b1b50-944">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-944">X</span></span> | <span data-ttu-id="b1b50-945">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-945">X</span></span> | <span data-ttu-id="b1b50-946">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-946">X</span></span> | \- |
| <span data-ttu-id="b1b50-947">WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ CLOSE \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b1b50-947">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="b1b50-948">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-948">**DWORD**</span></span> | \- | \- | <span data-ttu-id="b1b50-949">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-949">X</span></span> | <span data-ttu-id="b1b50-950">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-950">X</span></span> | \- |
| <span data-ttu-id="b1b50-951">WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ KEEPALIVE \_ INTERVAL</span><span class="sxs-lookup"><span data-stu-id="b1b50-951">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="b1b50-952">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-952">**DWORD**</span></span> | \- | \- | <span data-ttu-id="b1b50-953">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-953">X</span></span> | <span data-ttu-id="b1b50-954">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-954">X</span></span> | \- |
| <span data-ttu-id="b1b50-955">WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ RECEIVE \_ BUFFER \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="b1b50-955">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="b1b50-956">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-956">**DWORD**</span></span> | <span data-ttu-id="b1b50-957">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-957">X</span></span> | <span data-ttu-id="b1b50-958">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-958">X</span></span> | <span data-ttu-id="b1b50-959">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-959">X</span></span> | <span data-ttu-id="b1b50-960">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-960">X</span></span> | <span data-ttu-id="b1b50-961">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b1b50-961">Windows 8.1</span></span> |
| <span data-ttu-id="b1b50-962">WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ SEND \_ BUFFER \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="b1b50-962">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="b1b50-963">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-963">**DWORD**</span></span> | <span data-ttu-id="b1b50-964">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-964">X</span></span> | <span data-ttu-id="b1b50-965">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-965">X</span></span> | <span data-ttu-id="b1b50-966">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-966">X</span></span> | <span data-ttu-id="b1b50-967">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-967">X</span></span> | <span data-ttu-id="b1b50-968">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b1b50-968">Windows 8.1</span></span> |
| <span data-ttu-id="b1b50-969">CONTAGEM DE \_ \_ THREADS DE TRABALHO DA OPÇÃO \_ WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-969">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="b1b50-970">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-970">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="b1b50-971">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-971">X</span></span> | \- |
| <span data-ttu-id="b1b50-972">TAMANHO DO \_ BUFFER DE GRAVAÇÃO DA OPÇÃO WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1b50-972">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="b1b50-973">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1b50-973">**DWORD**</span></span> | \- | <span data-ttu-id="b1b50-974">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-974">X</span></span> | <span data-ttu-id="b1b50-975">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-975">X</span></span> | <span data-ttu-id="b1b50-976">X</span><span class="sxs-lookup"><span data-stu-id="b1b50-976">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="b1b50-977">Para Windows XP e Windows 2000, consulte [Requisitos de tempo de executar](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="b1b50-977">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1b50-978">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1b50-978">Requirements</span></span>

| <span data-ttu-id="b1b50-979">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1b50-979">Requirement</span></span> | <span data-ttu-id="b1b50-980">Valor</span><span class="sxs-lookup"><span data-stu-id="b1b50-980">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="b1b50-981">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1b50-981">Minimum supported client</span></span> | <span data-ttu-id="b1b50-982">Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1b50-982">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="b1b50-983">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1b50-983">Minimum supported server</span></span> | <span data-ttu-id="b1b50-984">Windows Server 2003, Windows 2000 Server somente com aplicativos da área de trabalho SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1b50-984">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="b1b50-985">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b1b50-985">Redistributable</span></span>          | <span data-ttu-id="b1b50-986">WinHTTP 5.0 e Internet Explorer 5.01 ou posterior no Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b1b50-986">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="b1b50-987">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b1b50-987">Header</span></span>                   | <span data-ttu-id="b1b50-988">Winhttp.h</span><span class="sxs-lookup"><span data-stu-id="b1b50-988">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="b1b50-989">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1b50-989">See also</span></span>

[<span data-ttu-id="b1b50-990">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="b1b50-990">WinHTTP Versions</span></span>](winhttp-versions.md)
