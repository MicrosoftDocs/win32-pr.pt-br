---
description: O Microsoft Windows HTTP Services (WinHTTP) dá suporte a transações de protocolo SSL (SSL), incluindo certificados de cliente. Este tópico explica os conceitos envolvidos em uma transação SSL e como eles são tratados usando o WinHTTP.
ms.assetid: cb0a04f5-1026-4ad5-bb5b-c854064a5167
title: SSL no WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7952bb9a0227017927452502352c0354e69079c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170009"
---
# <a name="ssl-in-winhttp"></a><span data-ttu-id="4f6f4-104">SSL no WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4f6f4-104">SSL in WinHTTP</span></span>

<span data-ttu-id="4f6f4-105">O Microsoft Windows HTTP Services (WinHTTP) dá suporte a transações de protocolo SSL (SSL), incluindo certificados de cliente.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-105">Microsoft Windows HTTP Services (WinHTTP) supports Secure Sockets Layer (SSL) transactions including client certificates.</span></span> <span data-ttu-id="4f6f4-106">Este tópico explica os conceitos envolvidos em uma transação SSL e como eles são tratados usando o WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-106">This topic explains concepts involved in an SSL transaction and how they are handled using WinHTTP.</span></span>

## <a name="secure-sockets-layer"></a><span data-ttu-id="4f6f4-107">protocolo SSL</span><span class="sxs-lookup"><span data-stu-id="4f6f4-107">Secure Sockets Layer</span></span>

<span data-ttu-id="4f6f4-108">O SSL é um padrão estabelecido para garantir transações HTTP seguras.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-108">SSL is an established standard for ensuring secure HTTP transactions.</span></span> <span data-ttu-id="4f6f4-109">O SSL fornece um mecanismo para executar a criptografia de até 128 bits em todas as transações entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-109">SSL provides a mechanism to perform up to 128-bit encryption on all transactions between the client and server.</span></span> <span data-ttu-id="4f6f4-110">Ele permite que o cliente Verifique se o servidor pertence a uma entidade confiável por meio do uso de certificados de servidor.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-110">It enables the client to verify that the server belongs to a trusted entity through the use of server certificates.</span></span> <span data-ttu-id="4f6f4-111">Ele também permite que o servidor confirme a identidade do cliente com certificados de cliente.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-111">It also enables the server to confirm the identity of the client with client certificates.</span></span>

<span data-ttu-id="4f6f4-112">Cada um desses problemas de criptografia, identidade do servidor e identidade do cliente são negociados no handshake SSL que ocorre quando um cliente solicita pela primeira vez um recurso de um servidor HTTPS (protocolo de transferência de hipertexto) seguro.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-112">Each of these issues encryption, server identity, and client identity are negotiated in the SSL handshake that occurs when a client first requests a resource from a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span> <span data-ttu-id="4f6f4-113">Essencialmente, o cliente e o servidor apresentam uma lista de configurações necessárias e preferenciais.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-113">Essentially, the client and server each present a list of required and preferred settings.</span></span> <span data-ttu-id="4f6f4-114">Se um conjunto comum de requisitos puder ser acordado e atendido, uma conexão SSL será estabelecida.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-114">If a common set of requirements can be agreed upon and met, an SSL connection is established.</span></span>

<span data-ttu-id="4f6f4-115">O WinHTTP fornece uma interface de alto nível para usar SSL.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-115">WinHTTP provides a high level interface for using SSL.</span></span> <span data-ttu-id="4f6f4-116">Embora os detalhes do handshake e da transação SSL sejam tratados internamente, o WinHTTP permite que você recupere os níveis de criptografia, especifique o protocolo de segurança e interaja com certificados de cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-116">While the details of the SSL handshake and transaction are handled internally, WinHTTP enables you to retrieve encryption levels, specify the security protocol, and interact with server and client certificates.</span></span> <span data-ttu-id="4f6f4-117">As seções a seguir fornecem detalhes sobre a criação de aplicativos baseados em WinHTTP que elegem uma versão de protocolo SSL, examinam certificados de servidor e selecionam certificados de cliente para enviar a servidores HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-117">The following sections provide details on creating WinHTTP based applications that elect an SSL protocol version, examine server certificates, and select client certificates to send to HTTPS servers.</span></span>

## <a name="server-certificates"></a><span data-ttu-id="4f6f4-118">Certificados do servidor</span><span class="sxs-lookup"><span data-stu-id="4f6f4-118">Server Certificates</span></span>

<span data-ttu-id="4f6f4-119">Os certificados de servidor são enviados do servidor para o cliente para que o cliente possa obter uma chave pública para o servidor e garantir que o servidor tenha sido verificado por uma autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-119">Server certificates are sent from the server to the client so that the client can obtain a public key for the server and ensure that the server has been verified by a certification authority.</span></span> <span data-ttu-id="4f6f4-120">Os certificados podem conter tipos diferentes de dados.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-120">Certificates can contain different types of data.</span></span> <span data-ttu-id="4f6f4-121">Por exemplo, um certificado X. 509 inclui o formato do certificado, o número de série do certificado, o algoritmo usado para assinar o certificado, o nome da AC (autoridade de certificação) que emitiu o certificado, o nome e a chave pública da entidade que solicita o certificado e a assinatura da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-121">For example, an X.509 certificate includes the format of the certificate, the serial number of the certificate, the algorithm used to sign the certificate, the name of the certification authority (CA) that issued the certificate, the name and public key of the entity that requests the certificate, and the CA's signature.</span></span>

<span data-ttu-id="4f6f4-122">Ao usar a API (interface de programação de aplicativo) do WinHTTP, você pode recuperar um certificado de servidor chamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e especificando o sinalizador de estrutura de certificado de [**segurança da \_ opção \_ \_ \_ WinHTTP**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="4f6f4-122">When using the WinHTTP  application programming interface (API), you can retrieve a server certificate by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and specifying the [**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**](option-flags.md) flag.</span></span> <span data-ttu-id="4f6f4-123">O certificado do servidor é retornado em uma estrutura de [**\_ \_ informações de certificado do WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) .</span><span class="sxs-lookup"><span data-stu-id="4f6f4-123">The server certificate is returned in a [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="4f6f4-124">Se você preferir recuperar o contexto de certificado, especifique a [**opção WinHTTP sinalizador de \_ \_ contexto de \_ certificado \_ de servidor**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="4f6f4-124">If you prefer to retrieve the certificate context, specify the [**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**](option-flags.md) flag instead.</span></span>

<span data-ttu-id="4f6f4-125">Se um certificado de servidor contiver erros, os detalhes sobre o erro poderão ser obtidos na função de retorno de chamada de status.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-125">If a server certificate contains errors, details about the error can be obtained in the status callback function.</span></span> <span data-ttu-id="4f6f4-126">A notificação de [**\_ \_ \_ \_ falha segura de status de retorno de chamada WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) indica um erro com um certificado de servidor.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-126">The [**WINHTTP\_CALLBACK\_STATUS\_SECURE\_FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) notification indicates an error with a server certificate.</span></span> <span data-ttu-id="4f6f4-127">O parâmetro *lpvStatusInformation* contém um ou mais sinalizadores de erro detalhados.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-127">The *lpvStatusInformation* parameter contains one or more detailed error flags.</span></span> <span data-ttu-id="4f6f4-128">Consulte [**\_ retorno de \_ chamada de status do WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-128">See [**WINHTTP\_STATUS\_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) for more information.</span></span>

## <a name="client-certificates"></a><span data-ttu-id="4f6f4-129">Certificados do cliente</span><span class="sxs-lookup"><span data-stu-id="4f6f4-129">Client Certificates</span></span>

<span data-ttu-id="4f6f4-130">Durante o handshake de SSL, o servidor pode exigir autenticação.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-130">During the SSL handshake, the server might require authentication.</span></span> <span data-ttu-id="4f6f4-131">O cliente é autenticado fornecendo um certificado de cliente válido para o servidor.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-131">The client is authenticated by supplying a valid client certificate to the server.</span></span> <span data-ttu-id="4f6f4-132">O WinHTTP permite que você selecione e envie um certificado de um [*repositório de certificados*](glossary.md)local.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-132">WinHTTP enables you to select and send a certificate from a local [*certificate store*](glossary.md).</span></span> <span data-ttu-id="4f6f4-133">As seções a seguir descrevem o processo que fornece certificados de cliente ao usar a API do WinHTTP ou o objeto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="4f6f4-133">The following sections describe the process that provides client certificates when using either the WinHTTP API or the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

### <a name="winhttp-api"></a><span data-ttu-id="4f6f4-134">API do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4f6f4-134">WinHTTP API</span></span>

<span data-ttu-id="4f6f4-135">O [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) e o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) podem falhar ao indicar que uma solicitação não foi bem-sucedida porque o servidor HTTPS requer autenticação.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-135">Both [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) and [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) can fail to indicate that a request was unsuccessful because the HTTPS server requires authentication.</span></span> <span data-ttu-id="4f6f4-136">Nesses casos, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para retornar o \_ certificado de autenticação de cliente WinHTTP de erro \_ \_ \_ \_ necessário.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-136">In these cases, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to returns ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED.</span></span> <span data-ttu-id="4f6f4-137">Após receber esse erro, use as funções de [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) apropriadas para encontrar um certificado apropriado.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-137">Upon receiving this error, use the appropriate [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) functions to find an appropriate certificate.</span></span> <span data-ttu-id="4f6f4-138">Indique que esse certificado deve ser enviado com a próxima solicitação chamando [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) com a [**opção WinHTTP sinalizador de \_ \_ contexto de \_ certificado \_ de cliente**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="4f6f4-138">Indicate that this certificate should be sent with the next request by calling [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the [**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**](option-flags.md) flag.</span></span>

<span data-ttu-id="4f6f4-139">O exemplo de código a seguir mostra como abrir um [*repositório de certificados*](glossary.md) e localizar um certificado com base no nome da entidade após o erro \_ WinHTTP \_ Client \_ auth \_ CERT \_ necessário ter sido retornado.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-139">The following code example shows how to open a [*certificate store*](glossary.md) and locate a certificate based on subject name after the ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED error has been returned.</span></span>


```C++
  if( !WinHttpReceiveResponse( hRequest, NULL ) )
  {
    if( GetLastError( ) == ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED )
    {
      //MY is the store the certificate is in.
      hMyStore = CertOpenSystemStore( 0, TEXT("MY") );
      if( hMyStore )
      {
        pCertContext = CertFindCertificateInStore( hMyStore,
             X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
             0,
             CERT_FIND_SUBJECT_STR,
             (LPVOID) szCertName, //Subject string in the certificate.
             NULL );
        if( pCertContext )
        {
          WinHttpSetOption( hRequest, 
                            WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                            (LPVOID) pCertContext, 
                            sizeof(CERT_CONTEXT) );
          CertFreeCertificateContext( pCertContext );
        }
        CertCloseStore( hMyStore, 0 );

        // NOTE: Application should now resend the request.
      }
    }
  }
```



<span data-ttu-id="4f6f4-140">Antes de reenviar uma solicitação que contenha um certificado de cliente, você pode determinar se o nível de criptografia com suporte é aceitável para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-140">Before resending a request that contains a client certificate, you can determine if the supported level of encryption is acceptable for your application.</span></span> <span data-ttu-id="4f6f4-141">Chame [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e especifique o sinalizador de [**\_ sinalizadores de \_ segurança \_ da opção WinHTTP**](option-flags.md) para determinar o nível de criptografia usado.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-141">Call [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and specify the [**WINHTTP\_OPTION\_SECURITY\_FLAGS**](option-flags.md) flag to determine the level of encryption that is used.</span></span>

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a><span data-ttu-id="4f6f4-142">Recuperação da lista de emissores para autenticação de cliente SSL</span><span class="sxs-lookup"><span data-stu-id="4f6f4-142">Issuer List Retrieval for SSL Client Authentication</span></span>

<span data-ttu-id="4f6f4-143">Quando o aplicativo cliente WinHttp envia uma solicitação para um servidor HTTP seguro que exige a autenticação de cliente SSL, o WinHttp retorna um erro de certificado de **\_ autenticação de \_ cliente WinHTTP \_ \_ \_ necessário** se o aplicativo não tiver fornecido uma certificação de cliente.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-143">When the WinHttp client application sends a request to a secure HTTP server that requires SSL client authentication, WinHttp returns an **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED** if the application has not supplied a client certificate.</span></span> <span data-ttu-id="4f6f4-144">Para computadores em execução no Windows Server 2008 e no Windows Vista, o WinHttp permite que o aplicativo recupere a lista de emissores do certificado fornecida pelo servidor no desafio de autenticação.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-144">For computers running on Windows Server 2008 and Windows Vista, WinHttp enables the application to retrieve the certificate issuer list supplied by the server in the authentication challenge.</span></span> <span data-ttu-id="4f6f4-145">A lista emissor especifica uma lista de autoridades de certificação (CAs) que são autorizadas pelo servidor a emitir certificados de cliente.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-145">The Issuer List specifies a list of Certificate Authorities (CAs) that are authorized by the server to issue client certificates.</span></span> <span data-ttu-id="4f6f4-146">O aplicativo filtra a lista de emissores para obter o certificado necessário.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-146">The application filters the issuer list to obtain the required certificate.</span></span>

<span data-ttu-id="4f6f4-147">O aplicativo cliente WinHttp recupera a lista de emissores quando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)ou [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retorna um **certificado de autenticação de \_ cliente WinHTTP de erro \_ \_ \_ \_ necessário**.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-147">The WinHttp client application retrieves the issuer list when [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="4f6f4-148">Quando esse erro é retornado, o aplicativo chama [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) com a opção **WinHTTP de lista de \_ \_ emissor de \_ certificado \_ \_ de cliente** .</span><span class="sxs-lookup"><span data-stu-id="4f6f4-148">When this error is returned, the application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span> <span data-ttu-id="4f6f4-149">O parâmetro *lpBuffer* deve ser grande o suficiente para conter um ponteiro para a estrutura [ \_ IssuerListInfoEx SecPkgContext](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) .</span><span class="sxs-lookup"><span data-stu-id="4f6f4-149">The *lpBuffer* parameter must be large enough to contain a pointer to the [SecPkgContext\_IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure.</span></span> <span data-ttu-id="4f6f4-150">O exemplo de código a seguir mostra como recuperar a lista de emissores.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-150">The following code example shows how to retrieve the issuer list.</span></span>


```C++
#include <windows.h>
#include <winhttp.h>
#include <schannel.h>

//...

void GetIssuerList(HINTERNET hRequest)
{
  SecPkgContext_IssuerListInfoEx* pIssuerList = NULL;
  DWORD dwBufferSize = sizeof(SecPkgContext_IssuerListInfoEx*);

  if (WinHttpQueryOption(hRequest,
           WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST,
           &pIssuerList,
           &dwBufferSize) == TRUE)
  {
    // Use the pIssuerList for cert store filtering.
    GlobalFree(pIssuerList); // Free the issuer list when done.
  }
}
```



<span data-ttu-id="4f6f4-151">As informações na estrutura [SecPkgContext \_ IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , *cIssuers* e *aIssuers*, podem ser usadas para pesquisar o certificado, conforme mostrado no exemplo de código abaixo.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-151">The information in the [SecPkgContext\_IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure, *cIssuers* and *aIssuers*, can be used to search for the certificate as shown in the code example below.</span></span> <span data-ttu-id="4f6f4-152">Para obter mais informações, consulte [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).</span><span class="sxs-lookup"><span data-stu-id="4f6f4-152">For more information, see [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).</span></span>


```C++
PCERT_CONTEXT pClientCert = NULL;
PCCERT_CHAIN_CONTEXT pClientCertChain = NULL;

CERT_CHAIN_FIND_BY_ISSUER_PARA SrchCriteria;
::ZeroMemory(&SrchCriteria, sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA));
SrchCriteria.cbSize = sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA);

SrchCriteria.cIssuer = pIssuerList->cIssuers;
SrchCriteria.rgIssuer = pIssuerList->aIssuers;

pClientCertChain = CertFindChainInStore(
            hClientCertStore,
            X509_ASN_ENCODING,
            CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_URL_FLAG |
            // Do not perform wire download when building chains.
            CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_FLAG,
            // Do not search pCacheEntry->_ClientCertStore 
            // for issuer certs.
            CERT_CHAIN_FIND_BY_ISSUER,
            &SrchCriteria,
            NULL);

if (pClientCertChain)
{
    pClientCert = (PCERT_CONTEXT) pClientCertChain->rgpChain[0]->rgpElement[0]->pCertContext;

    CertDuplicateCertificateContext(pClientCert);

    CertFreeCertificateChain(pClientCertChain);

    pClientCertChain = NULL;
}
```



### <a name="optional-client-ssl-certificates"></a><span data-ttu-id="4f6f4-153">Certificados SSL de cliente opcionais</span><span class="sxs-lookup"><span data-stu-id="4f6f4-153">Optional Client SSL Certificates</span></span>

<span data-ttu-id="4f6f4-154">A partir do Windows Server 2008 e do Windows Vista, a API do WinHttp dá suporte a certificados de cliente opcionais.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-154">Starting in Windows Server 2008 and Windows Vista, the WinHttp API supports optional client certificates.</span></span> <span data-ttu-id="4f6f4-155">Quando o servidor solicita um certificado de cliente, o [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)ou o [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retorna um erro WinHTTP erro de **certificado de \_ \_ \_ autenticação de \_ \_ cliente** .</span><span class="sxs-lookup"><span data-stu-id="4f6f4-155">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED** error.</span></span> <span data-ttu-id="4f6f4-156">Se o servidor solicitar o certificado, mas não precisar dele, o aplicativo poderá especificar essa opção para indicar que ele não tem um certificado.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-156">If the server requests the certificate, but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="4f6f4-157">O servidor pode escolher outro esquema de autenticação ou permitir acesso anônimo ao servidor.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-157">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="4f6f4-158">O aplicativo especifica a macro de **\_ \_ \_ \_ contexto não certificado de cliente do WinHTTP** no parâmetro *lpBuffer* de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-158">The application specifies the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

<span data-ttu-id="4f6f4-159">Se o **\_ nenhum \_ contexto de \_ certificado \_ de cliente WinHTTP** for definido e o servidor ainda exigir um certificado de cliente, ele poderá enviar um código de status HTTP 403.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-159">If the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** is set, and the server still requires a client certificate, it may send a 403 HTTP status code.</span></span> <span data-ttu-id="4f6f4-160">Para obter mais informações, consulte **a \_ opção \_ WinHTTP \_ \_ \_ lista de emissor de certificado de cliente** .</span><span class="sxs-lookup"><span data-stu-id="4f6f4-160">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>

### <a name="winhttprequest-object"></a><span data-ttu-id="4f6f4-161">Objeto WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="4f6f4-161">WinHttpRequest Object</span></span>

<span data-ttu-id="4f6f4-162">Use o método [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) do objeto [**WinHttpRequest**](winhttprequest.md) para selecionar certificados de cliente para enviar ao servidor com uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-162">Use the [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) method of the [**WinHttpRequest**](winhttprequest.md) object to select client certificates to send to the server with a request.</span></span> <span data-ttu-id="4f6f4-163">Selecione um certificado especificando uma cadeia de seleção de certificado com o método [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="4f6f4-163">Select a certificate by specifying a certificate selection string with the [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) method.</span></span> <span data-ttu-id="4f6f4-164">A cadeia de seleção de certificado consiste no local do certificado, no [*repositório de certificados*](glossary.md)e no nome da entidade delimitada por barras invertidas.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-164">The certificate selection string consists of the certificate location, [*certificate store*](glossary.md), and subject name delimited by backslashes.</span></span> <span data-ttu-id="4f6f4-165">A tabela a seguir lista os componentes dessa cadeia de seleção.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-165">The following table lists components for this selection string.</span></span>



| <span data-ttu-id="4f6f4-166">Componente</span><span class="sxs-lookup"><span data-stu-id="4f6f4-166">Component</span></span>                                                  | <span data-ttu-id="4f6f4-167">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f6f4-167">Description</span></span>                                                                                                                                                                                        | <span data-ttu-id="4f6f4-168">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="4f6f4-168">Possible values</span></span>                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f6f4-169">Local</span><span class="sxs-lookup"><span data-stu-id="4f6f4-169">Location</span></span>                                                   | <span data-ttu-id="4f6f4-170">Determina a chave do registro sob a qual os certificados são armazenados.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-170">Determines the registry key under which the certificates are stored.</span></span>                                                                                                                               | <span data-ttu-id="4f6f4-171">Os valores possíveis são " \_ máquina local" para indicar que o [*repositório de certificados*](glossary.md) está em **HKEY \_ local \_ Machine**</span><span class="sxs-lookup"><span data-stu-id="4f6f4-171">The possible values are "LOCAL\_MACHINE" to indicate that the [*certificate store*](glossary.md) is under **HKEY\_LOCAL\_MACHINE**</span></span><br/> <span data-ttu-id="4f6f4-172">e " \_ usuário atual" para indicar que o *repositório de certificados* está sob o **usuário atual hKey não \_ representado \_ .**</span><span class="sxs-lookup"><span data-stu-id="4f6f4-172">and "CURRENT\_USER" to indicate that the *certificate store* is under the non-impersonated **HKEY\_CURRENT\_USER.**</span></span><br/> <span data-ttu-id="4f6f4-173">Este componente diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-173">This component is case-sensitive.</span></span> |
| [<span data-ttu-id="4f6f4-174">*Repositório de certificados*</span><span class="sxs-lookup"><span data-stu-id="4f6f4-174">*Certificate store*</span></span>](glossary.md) | <span data-ttu-id="4f6f4-175">Indica o nome do [*repositório de certificados*](glossary.md) que contém o certificado relevante.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-175">Indicates the name of the [*certificate store*](glossary.md) that contains the relevant certificate.</span></span>                                                                       | <span data-ttu-id="4f6f4-176">Os [*repositórios de certificados*](glossary.md) típicos são "My", "root" e "TrustedPeople".</span><span class="sxs-lookup"><span data-stu-id="4f6f4-176">Typical [*certificate stores*](glossary.md) are "MY", "Root", and "TrustedPeople".</span></span> <span data-ttu-id="4f6f4-177">Este componente diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-177">This component is case-sensitive.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="4f6f4-178">Nome da entidade</span><span class="sxs-lookup"><span data-stu-id="4f6f4-178">Subject name</span></span>                                               | <span data-ttu-id="4f6f4-179">Identifica um certificado dentro do [*repositório de certificados*](glossary.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-179">Identifies a certificate within the specified [*certificate store*](glossary.md).</span></span> <span data-ttu-id="4f6f4-180">O primeiro certificado que contém a cadeia de caracteres especificada para esse componente é selecionado.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-180">The first certificate that contains the string specified for this component is selected.</span></span> | <span data-ttu-id="4f6f4-181">O nome da entidade pode ser qualquer cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-181">The subject name can be any string.</span></span> <span data-ttu-id="4f6f4-182">Uma cadeia de caracteres em branco indica que o primeiro certificado no [*repositório de certificados*](glossary.md) deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-182">A blank string indicates that the first certificate in the [*certificate store*](glossary.md) should be used.</span></span> <span data-ttu-id="4f6f4-183">Este componente não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-183">This component is case-insensitive.</span></span>                                                                                                                         |



 

<span data-ttu-id="4f6f4-184">O nome e o local do [*repositório de certificados*](glossary.md) são componentes opcionais.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-184">The [*certificate store*](glossary.md) name and location are optional components.</span></span> <span data-ttu-id="4f6f4-185">No entanto, se você especificar um *repositório de certificados*, também deverá especificar o local desse *repositório de certificados*.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-185">However, if you specify a *certificate store*, you must also specify the location of that *certificate store*.</span></span> <span data-ttu-id="4f6f4-186">O local padrão é o \_ usuário atual e o *repositório de certificados* padrão é "My".</span><span class="sxs-lookup"><span data-stu-id="4f6f4-186">The default location is CURRENT\_USER and the default *certificate store* is "MY".</span></span>

<span data-ttu-id="4f6f4-187">O exemplo de código a seguir mostra como especificar que um certificado com o assunto "meu certificado de Middle-Tier" deve ser escolhido no repositório de [*certificados*](glossary.md) "pessoal" no registro, em **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-187">The following code example shows how to specify that a certificate with the subject "My Middle-Tier Certificate" should be chosen from the "Personal" [*certificate store*](glossary.md) in the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> <span data-ttu-id="4f6f4-188">Em alguns idiomas, a barra invertida é um caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-188">In some languages the backslash is an escape character.</span></span> <span data-ttu-id="4f6f4-189">Lembre-se de modificar a cadeia de seleção de certificado para considerar isso.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-189">Remember to modify the certificate selection string to account for this.</span></span> <span data-ttu-id="4f6f4-190">Por exemplo, no Microsoft JScript, use duas barras invertidas adjacentes em vez de uma.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-190">For example, in Microsoft JScript, use two adjacent backslashes instead of one.</span></span>

 

<span data-ttu-id="4f6f4-191">Se você não especificar um certificado e um servidor HTTPS exigir um certificado de cliente, o WinHTTP selecionará o primeiro certificado no [*repositório de certificados*](glossary.md)padrão.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-191">If you do not specify a certificate and an HTTPS server requires a client certificate, WinHTTP selects the first certificate in the default [*certificate store*](glossary.md).</span></span> <span data-ttu-id="4f6f4-192">Se não houver nenhum certificado, um erro será gerado.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-192">If no certificates exist, an error is raised.</span></span> <span data-ttu-id="4f6f4-193">Se o certificado não for aceito, o servidor retornará um código de status 403 para indicar que a solicitação não pode ser atendida.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-193">If the certificate is not accepted, the server returns a 403 status code to indicate that the request cannot be fulfilled.</span></span> <span data-ttu-id="4f6f4-194">Você pode escolher um certificado mais apropriado com [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) e reenviar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="4f6f4-194">You can then choose a more appropriate certificate with [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) and resend the request.</span></span>

 

