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
# <a name="ssl-in-winhttp"></a>SSL no WinHTTP

O Microsoft Windows HTTP Services (WinHTTP) dá suporte a transações de protocolo SSL (SSL), incluindo certificados de cliente. Este tópico explica os conceitos envolvidos em uma transação SSL e como eles são tratados usando o WinHTTP.

## <a name="secure-sockets-layer"></a>protocolo SSL

O SSL é um padrão estabelecido para garantir transações HTTP seguras. O SSL fornece um mecanismo para executar a criptografia de até 128 bits em todas as transações entre o cliente e o servidor. Ele permite que o cliente Verifique se o servidor pertence a uma entidade confiável por meio do uso de certificados de servidor. Ele também permite que o servidor confirme a identidade do cliente com certificados de cliente.

Cada um desses problemas de criptografia, identidade do servidor e identidade do cliente são negociados no handshake SSL que ocorre quando um cliente solicita pela primeira vez um recurso de um servidor HTTPS (protocolo de transferência de hipertexto) seguro. Essencialmente, o cliente e o servidor apresentam uma lista de configurações necessárias e preferenciais. Se um conjunto comum de requisitos puder ser acordado e atendido, uma conexão SSL será estabelecida.

O WinHTTP fornece uma interface de alto nível para usar SSL. Embora os detalhes do handshake e da transação SSL sejam tratados internamente, o WinHTTP permite que você recupere os níveis de criptografia, especifique o protocolo de segurança e interaja com certificados de cliente e servidor. As seções a seguir fornecem detalhes sobre a criação de aplicativos baseados em WinHTTP que elegem uma versão de protocolo SSL, examinam certificados de servidor e selecionam certificados de cliente para enviar a servidores HTTPS.

## <a name="server-certificates"></a>Certificados do servidor

Os certificados de servidor são enviados do servidor para o cliente para que o cliente possa obter uma chave pública para o servidor e garantir que o servidor tenha sido verificado por uma autoridade de certificação. Os certificados podem conter tipos diferentes de dados. Por exemplo, um certificado X. 509 inclui o formato do certificado, o número de série do certificado, o algoritmo usado para assinar o certificado, o nome da AC (autoridade de certificação) que emitiu o certificado, o nome e a chave pública da entidade que solicita o certificado e a assinatura da autoridade de certificação.

Ao usar a API (interface de programação de aplicativo) do WinHTTP, você pode recuperar um certificado de servidor chamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e especificando o sinalizador de estrutura de certificado de [**segurança da \_ opção \_ \_ \_ WinHTTP**](option-flags.md) . O certificado do servidor é retornado em uma estrutura de [**\_ \_ informações de certificado do WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) . Se você preferir recuperar o contexto de certificado, especifique a [**opção WinHTTP sinalizador de \_ \_ contexto de \_ certificado \_ de servidor**](option-flags.md) .

Se um certificado de servidor contiver erros, os detalhes sobre o erro poderão ser obtidos na função de retorno de chamada de status. A notificação de [**\_ \_ \_ \_ falha segura de status de retorno de chamada WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) indica um erro com um certificado de servidor. O parâmetro *lpvStatusInformation* contém um ou mais sinalizadores de erro detalhados. Consulte [**\_ retorno de \_ chamada de status do WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) para obter mais informações.

## <a name="client-certificates"></a>Certificados do cliente

Durante o handshake de SSL, o servidor pode exigir autenticação. O cliente é autenticado fornecendo um certificado de cliente válido para o servidor. O WinHTTP permite que você selecione e envie um certificado de um [*repositório de certificados*](glossary.md)local. As seções a seguir descrevem o processo que fornece certificados de cliente ao usar a API do WinHTTP ou o objeto [**WinHttpRequest**](winhttprequest.md) .

### <a name="winhttp-api"></a>API do WinHTTP

O [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) e o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) podem falhar ao indicar que uma solicitação não foi bem-sucedida porque o servidor HTTPS requer autenticação. Nesses casos, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para retornar o \_ certificado de autenticação de cliente WinHTTP de erro \_ \_ \_ \_ necessário. Após receber esse erro, use as funções de [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) apropriadas para encontrar um certificado apropriado. Indique que esse certificado deve ser enviado com a próxima solicitação chamando [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) com a [**opção WinHTTP sinalizador de \_ \_ contexto de \_ certificado \_ de cliente**](option-flags.md) .

O exemplo de código a seguir mostra como abrir um [*repositório de certificados*](glossary.md) e localizar um certificado com base no nome da entidade após o erro \_ WinHTTP \_ Client \_ auth \_ CERT \_ necessário ter sido retornado.


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



Antes de reenviar uma solicitação que contenha um certificado de cliente, você pode determinar se o nível de criptografia com suporte é aceitável para seu aplicativo. Chame [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e especifique o sinalizador de [**\_ sinalizadores de \_ segurança \_ da opção WinHTTP**](option-flags.md) para determinar o nível de criptografia usado.

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a>Recuperação da lista de emissores para autenticação de cliente SSL

Quando o aplicativo cliente WinHttp envia uma solicitação para um servidor HTTP seguro que exige a autenticação de cliente SSL, o WinHttp retorna um erro de certificado de **\_ autenticação de \_ cliente WinHTTP \_ \_ \_ necessário** se o aplicativo não tiver fornecido uma certificação de cliente. Para computadores em execução no Windows Server 2008 e no Windows Vista, o WinHttp permite que o aplicativo recupere a lista de emissores do certificado fornecida pelo servidor no desafio de autenticação. A lista emissor especifica uma lista de autoridades de certificação (CAs) que são autorizadas pelo servidor a emitir certificados de cliente. O aplicativo filtra a lista de emissores para obter o certificado necessário.

O aplicativo cliente WinHttp recupera a lista de emissores quando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)ou [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retorna um **certificado de autenticação de \_ cliente WinHTTP de erro \_ \_ \_ \_ necessário**. Quando esse erro é retornado, o aplicativo chama [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) com a opção **WinHTTP de lista de \_ \_ emissor de \_ certificado \_ \_ de cliente** . O parâmetro *lpBuffer* deve ser grande o suficiente para conter um ponteiro para a estrutura [ \_ IssuerListInfoEx SecPkgContext](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) . O exemplo de código a seguir mostra como recuperar a lista de emissores.


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



As informações na estrutura [SecPkgContext \_ IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , *cIssuers* e *aIssuers*, podem ser usadas para pesquisar o certificado, conforme mostrado no exemplo de código abaixo. Para obter mais informações, consulte [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).


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



### <a name="optional-client-ssl-certificates"></a>Certificados SSL de cliente opcionais

A partir do Windows Server 2008 e do Windows Vista, a API do WinHttp dá suporte a certificados de cliente opcionais. Quando o servidor solicita um certificado de cliente, o [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)ou o [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retorna um erro WinHTTP erro de **certificado de \_ \_ \_ autenticação de \_ \_ cliente** . Se o servidor solicitar o certificado, mas não precisar dele, o aplicativo poderá especificar essa opção para indicar que ele não tem um certificado. O servidor pode escolher outro esquema de autenticação ou permitir acesso anônimo ao servidor. O aplicativo especifica a macro de **\_ \_ \_ \_ contexto não certificado de cliente do WinHTTP** no parâmetro *lpBuffer* de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , conforme mostrado no exemplo de código a seguir.

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

Se o **\_ nenhum \_ contexto de \_ certificado \_ de cliente WinHTTP** for definido e o servidor ainda exigir um certificado de cliente, ele poderá enviar um código de status HTTP 403. Para obter mais informações, consulte **a \_ opção \_ WinHTTP \_ \_ \_ lista de emissor de certificado de cliente** .

### <a name="winhttprequest-object"></a>Objeto WinHttpRequest

Use o método [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) do objeto [**WinHttpRequest**](winhttprequest.md) para selecionar certificados de cliente para enviar ao servidor com uma solicitação. Selecione um certificado especificando uma cadeia de seleção de certificado com o método [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) . A cadeia de seleção de certificado consiste no local do certificado, no [*repositório de certificados*](glossary.md)e no nome da entidade delimitada por barras invertidas. A tabela a seguir lista os componentes dessa cadeia de seleção.



| Componente                                                  | Descrição                                                                                                                                                                                        | Valores possíveis                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Local                                                   | Determina a chave do registro sob a qual os certificados são armazenados.                                                                                                                               | Os valores possíveis são " \_ máquina local" para indicar que o [*repositório de certificados*](glossary.md) está em **HKEY \_ local \_ Machine**<br/> e " \_ usuário atual" para indicar que o *repositório de certificados* está sob o **usuário atual hKey não \_ representado \_ .**<br/> Este componente diferencia maiúsculas de minúsculas. |
| [*Repositório de certificados*](glossary.md) | Indica o nome do [*repositório de certificados*](glossary.md) que contém o certificado relevante.                                                                       | Os [*repositórios de certificados*](glossary.md) típicos são "My", "root" e "TrustedPeople". Este componente diferencia maiúsculas de minúsculas.                                                                                                                                                                                          |
| Nome da entidade                                               | Identifica um certificado dentro do [*repositório de certificados*](glossary.md)especificado. O primeiro certificado que contém a cadeia de caracteres especificada para esse componente é selecionado. | O nome da entidade pode ser qualquer cadeia de caracteres. Uma cadeia de caracteres em branco indica que o primeiro certificado no [*repositório de certificados*](glossary.md) deve ser usado. Este componente não diferencia maiúsculas de minúsculas.                                                                                                                         |



 

O nome e o local do [*repositório de certificados*](glossary.md) são componentes opcionais. No entanto, se você especificar um *repositório de certificados*, também deverá especificar o local desse *repositório de certificados*. O local padrão é o \_ usuário atual e o *repositório de certificados* padrão é "My".

O exemplo de código a seguir mostra como especificar que um certificado com o assunto "meu certificado de Middle-Tier" deve ser escolhido no repositório de [*certificados*](glossary.md) "pessoal" no registro, em **HKEY \_ local \_ Machine**.

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> Em alguns idiomas, a barra invertida é um caractere de escape. Lembre-se de modificar a cadeia de seleção de certificado para considerar isso. Por exemplo, no Microsoft JScript, use duas barras invertidas adjacentes em vez de uma.

 

Se você não especificar um certificado e um servidor HTTPS exigir um certificado de cliente, o WinHTTP selecionará o primeiro certificado no [*repositório de certificados*](glossary.md)padrão. Se não houver nenhum certificado, um erro será gerado. Se o certificado não for aceito, o servidor retornará um código de status 403 para indicar que a solicitação não pode ser atendida. Você pode escolher um certificado mais apropriado com [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) e reenviar a solicitação.

 

