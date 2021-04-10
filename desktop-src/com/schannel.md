---
title: SChannel
description: O pacote de segurança do Schannel (canal seguro), cujo identificador de serviço de autenticação é RPC \_ C \_ Authn \_ GSS \_ Schannel, dá suporte aos seguintes protocolos baseados em chave pública SSL (protocolo SSL) 2,0 e 3,0, protocolo TLS 1,0 e tecnologia de comunicação privada (PCT) 1,0. O TLS 1,0 é uma versão padronizada e ligeiramente modificada do SSL 3,0 que foi emitida pelo IETF (Internet Engineering Task Force) em 1999 de Janeiro, no documento RFC 2246. Como o TLS foi padronizado, os desenvolvedores são incentivados a usar TLS em vez de SSL. O PCT é incluído apenas para fins de compatibilidade com versões anteriores e não deve ser usado para um novo desenvolvimento. Quando o pacote de segurança Schannel é usado, o DCOM negocia automaticamente o melhor protocolo, dependendo dos recursos do cliente e do servidor.
ms.assetid: 03a5f987-f668-4f19-9b58-d62711f58734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccc9f82a05d1542e7585426128f10cdf452d31d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294538"
---
# <a name="schannel"></a>SChannel

O pacote de segurança do Schannel (canal seguro), cujo identificador do serviço de autenticação é RPC \_ C \_ Authn \_ GSS \_ Schannel, dá suporte aos seguintes protocolos baseados em chave pública: SSL (protocolo SSL) versões 2,0 e 3,0, TLS (Transport Layer Security) 1,0 e PCT (tecnologia de comunicação privada) 1,0. O TLS 1,0 é uma versão padronizada e ligeiramente modificada do SSL 3,0 que foi emitida pelo IETF (Internet Engineering Task Force) em 1999 de Janeiro, no documento [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt). Como o TLS foi padronizado, os desenvolvedores são incentivados a usar TLS em vez de SSL. O PCT é incluído apenas para fins de compatibilidade com versões anteriores e não deve ser usado para um novo desenvolvimento. Quando o pacote de segurança Schannel é usado, o DCOM negocia automaticamente o melhor protocolo, dependendo dos recursos do cliente e do servidor.

Os tópicos a seguir descrevem brevemente o protocolo TLS e como ele funciona com o DCOM.

-   [Quando usar o TLS](#when-to-use-tls)
-   [Breve visão geral de como o TLS funciona](#brief-overview-of-how-tls-works)
-   [Certificados X. 509](#x509-certificates)
    -   [Certificados do cliente](#client-certificates)
-   [Usando o TLS no COM](#using-tls-in-com)
    -   [Como um servidor define a cobertura de segurança](#how-a-server-sets-the-security-blanket)
    -   [Como um cliente define a cobertura de segurança](#how-a-client-sets-the-security-blanket)
    -   [Como um cliente altera a cobertura de segurança](#how-a-client-changes-the-security-blanket)
    -   [Exemplo: o cliente altera a cobertura de segurança](#example-client-changes-the-security-blanket)
-   [Tópicos relacionados](#related-topics)

> [!Note]  
> Todas as informações sobre o protocolo TLS nessas seções também se aplicam aos protocolos SSL e PCT.

 

## <a name="when-to-use-tls"></a>Quando usar o TLS

O TLS é a única opção de segurança disponível quando os servidores precisam provar sua identidade para clientes anônimos. Isso é particularmente importante para sites que desejam participar do comércio eletrônico porque ele ajuda a proteger a transmissão de informações confidenciais, como números de cartão de crédito. O TLS garante que os clientes de comércio eletrônico possam ter certeza de quem eles estão fazendo negócios, pois recebem uma prova da identidade do servidor. Ele também dá ao servidor de comércio eletrônico a eficiência de não ter que se preocupar com a autenticação da identidade de cada um de seus clientes.

O TLS requer que todos os servidores comprovem sua identidade aos clientes. Além disso, o TLS fornece a opção de fazer com que os clientes comprovem sua identidade aos servidores. Essa autenticação mútua pode ser útil para restringir o acesso de determinadas páginas da Web em uma grande intranet corporativa.

O TLS dá suporte aos níveis de autenticação mais fortes e oferece uma arquitetura aberta que permite que a segurança de criptografia aumente ao longo do tempo para acompanhar a inovação tecnológica. O TLS é a melhor opção para ambientes em que o nível mais alto de segurança é desejado para os dados em trânsito.

## <a name="brief-overview-of-how-tls-works"></a>Breve visão geral de como o TLS funciona

O TLS é criado com base em uma PKI (infraestrutura de chave pública), que usa pares de chaves públicas/privadas para habilitar a criptografia de dados e estabelecer a integridade dos dados, e usa certificados X. 509 para autenticação.

Muitos protocolos de segurança, como o protocolo Kerberos V5, dependem de uma única chave para criptografar e descriptografar dados. Portanto, esses protocolos dependem da troca segura de chaves de criptografia; no protocolo Kerberos, isso é feito por meio de tíquetes obtidos do centro de distribuição de chaves (KDC). Isso exige que todos que usam o protocolo Kerberos sejam registrados com o KDC, o que seria uma limitação impraticável para um servidor Web de comércio eletrônico destinado a atrair milhões de clientes de todo o mundo. Portanto, o TLS depende de uma PKI, que usa duas chaves para data encryptionâ € "quando uma chave do par criptografa os dados, somente a outra chave do par pode descriptografá-lo. O benefício principal desse design é que a criptografia pode ser executada sem a necessidade da troca segura de chaves de criptografia.

Uma PKI usa uma técnica em que uma das chaves é mantida privada e está disponível somente para a entidade para a qual ela está registrada, enquanto a outra chave é pública para qualquer pessoa acessar. Se alguém quiser enviar uma mensagem privada para o proprietário de um par de chaves, a mensagem poderá ser criptografada com a chave pública e somente a chave privada poderá ser usada para descriptografar a mensagem.

Os pares de chaves também são usados para verificar a integridade dos dados que estão sendo enviados. Para fazer isso, o proprietário do par de chaves pode anexar uma assinatura digital aos dados antes de enviá-la. A criação de uma assinatura digital envolve o cálculo de um hash dos dados e a criptografia do hash com a chave privada. Qualquer pessoa que usa a chave pública para descriptografar a assinatura digital é garantida de que a assinatura digital deve ter vindo apenas da pessoa que possui a chave privada. Além disso, o destinatário pode calcular um hash dos dados usando o mesmo algoritmo que o remetente e, se o hash calculado corresponder ao enviado na assinatura digital, o destinatário poderá ter certeza de que os dados não foram modificados após serem assinados digitalmente.

Uma desvantagem de usar uma PKI para a criptografia de dados de alto volume é o desempenho relativamente lento. Devido à intensa matemática envolvida, a criptografia e a descriptografia de dados usando uma codificação assimétrica que depende de um par de chaves pode ser de até 1.000 vezes mais lenta do que a criptografia e a descriptografia usando uma criptografia simétrica que depende apenas de uma única chave. Portanto, o TLS usa uma PKI somente para gerar assinaturas digitais e para negociar a única chave específica da sessão que será usada pelo cliente e pelo servidor para criptografia e descriptografia de dados em massa. O TLS dá suporte a uma ampla variedade de codificações simétricas de chave única, e codificações adicionais podem ser adicionadas no futuro.

Para obter mais informações sobre o protocolo de handshake de TLS, consulte [protocolo de handshake TLS](/windows/desktop/SecAuthN/tls-handshake-protocol).

Para obter mais detalhes sobre a criptografia por trás do protocolo TLS, consulte [princípios básicos de criptografia](/windows/desktop/SecCrypto/cryptography-essentials).

## <a name="x509-certificates"></a>Certificados X. 509

Um problema crítico que deve ser tratado por uma PKI é a capacidade de confiar na autenticidade da chave pública que está sendo usada. Ao usar uma chave pública emitida para uma empresa com a qual você deseja fazer negócios, você deve ter certeza de que a chave realmente pertence à empresa, e não a um ladrão que deseja descobrir seu número de cartão de crédito.

Para garantir a identidade de uma entidade de segurança que contém um par de chaves, o principal recebe um certificado X. 509 por uma autoridade de certificação (CA). Esse certificado contém informações que identificam a entidade de segurança, contém a chave pública da entidade de segurança e são assinadas digitalmente pela autoridade de certificação. Essa assinatura digital indica que a autoridade de certificação acredita que a chave pública contida no certificado realmente pertence à entidade de segurança identificada pelo certificado.

E como você confia na autoridade de certificação? Como a própria CA contém um certificado X. 509 que foi assinado por uma autoridade de certificação de nível superior. Essa cadeia de assinaturas de certificado continua até atingir uma CA raiz, que é uma autoridade de certificação que assina seus próprios certificados. Se você confiar na integridade da autoridade de certificação raiz de um certificado, deverá ser capaz de confiar na autenticidade do certificado em si. Portanto, selecionar CAs raiz nas quais você está disposto a confiar é um direito importante para um administrador do sistema.

### <a name="client-certificates"></a>Certificados do cliente

Quando os protocolos de camada de transporte de segurança surgem pela primeira vez, sua principal finalidade era garantir que um cliente estivesse se conectando a um servidor autêntico e ajudasse a proteger a privacidade dos dados em trânsito. No entanto, o SSL 3,0 e o TLS 1,0 também incluem suporte para a transmissão do certificado de um cliente durante o handshake do protocolo. Esse recurso opcional permite a autenticação mútua do cliente e do servidor.

A decisão de usar um certificado de cliente deve ser feita no contexto do aplicativo. Certificados de cliente são desnecessários se o requisito primário está Autenticando o servidor. No entanto, se a autenticação de cliente for essencial, o certificado de um cliente poderá ser usado em vez de depender da autenticação personalizada dentro do aplicativo. O uso de certificados de cliente é preferível em relação à autenticação personalizada porque fornece aos usuários um cenário de logon único.

## <a name="using-tls-in-com"></a>Usando o TLS no COM

O TLS dá suporte apenas ao nível de representação personificar (RPC \_ C \_ imp. de \_ nível de redistribuição \_ ). Se COM negociar o TLS como o serviço de autenticação em um proxy, o COM definirá o nível de representação para representar, independentemente do padrão do processo. Para que a representação funcione corretamente no TLS, o cliente deve fornecer um certificado X. 509 para o servidor e o servidor deve ter esse certificado mapeado para uma conta de usuário específica no servidor. Para obter mais informações, consulte o [guia passo a passo para mapear certificados para contas de usuário](https://www.microsoft.com/isapi/redir.dll?prd=windows2000&sbp=technicallibrary&ar=security&sba=mappingcertificates).

O TLS não oferece suporte ao [encobrimento](cloaking.md). Se um sinalizador de encobrimento e o TLS forem especificados em um [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou em uma chamada [**IClientSecurity:: setampla**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) , e \_ INVALIDARG serão retornados.

O TLS não funciona com o nível de autenticação definido como nenhum. O handshake entre o cliente e o servidor examina o nível de autenticação definido por cada um e escolhe a configuração de segurança mais alta para a conexão.

Os parâmetros de segurança para TLS podem ser definidos chamando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket). As seções a seguir descrevem as nuances envolvidas na realização dessas chamadas.

### <a name="how-a-server-sets-the-security-blanket"></a>Como um servidor define a cobertura de segurança

Se um servidor quiser usar o TLS, ele deverá especificar Schannel (RPC \_ C \_ Authn \_ GSS \_ Schannel) como um serviço de autenticação no parâmetro *asAuthSvc* de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Para impedir que os clientes se conectem ao servidor usando um serviço de autenticação menos seguro, o servidor deve especificar apenas o Schannel como um serviço de autenticação ao chamar **CoInitializeSecurity**. O servidor não pode alterar a cobertura de segurança depois de ter chamado **CoInitializeSecurity**.

Para usar o TLS, os seguintes parâmetros devem ser especificados quando um servidor chama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity):

-   *pVoid* deve ser um ponteiro para um objeto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) ou um ponteiro para um [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor). Ele não deve ser **nulo** ou um ponteiro para uma AppID.
-   *cAuthSvc* não pode ser 0 ou-1. Os servidores COM nunca escolhem Schannel quando *cAuthSvc* é-1.
-   *asAuthSvc* deve especificar Schannel como um serviço de autenticação possível. Isso é feito definindo os seguintes parâmetros [**de \_ \_ serviço de autenticação únicos**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) para o membro Schannel da [**\_ \_ lista exclusiva de autenticação**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list):
    -   *dwAuthnSvc* deve ser RPC \_ C \_ Authn \_ GSS \_ Schannel.
    -   *dwAuthzSvc* deve ser RPC \_ C \_ AUTHZ \_ None. No momento, ele é ignorado.
    -   *pPrincipalName* deve ser um ponteiro para um [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), Cast como um ponteiro para OLECHAR, que representa o certificado X. 509 do servidor.
-   *dwAuthnLevel* indica o nível de autenticação mínimo que será aceito de clientes para uma conexão bem-sucedida. Não pode ser RPC \_ C \_ Authn \_ nível \_ None.
-   *dwCapabilities* não deve ter o \_ sinalizador AppID EOAC definido. O \_ sinalizador de controle de acesso EOAC \_ deve ser definido se *pVoid* aponta para um objeto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) ; ele não deve ser definido se *pVoid* aponta para um \_ descritor de segurança. Para outros sinalizadores que podem ser definidos, consulte [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Para obter mais informações sobre como usar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), consulte [Configurando a segurança do processwide com CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

### <a name="how-a-client-sets-the-security-blanket"></a>Como um cliente define a cobertura de segurança

Se um cliente quiser usar o TLS, ele deverá especificar Schannel (RPC \_ C \_ Authn \_ GSS \_ Schannel) em sua lista de serviços de autenticação no parâmetro *pAuthList* de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Se Schannel não for especificado como um possível serviço de autenticação quando **CoInitializeSecurity** for chamado, uma chamada posterior para [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) (ou [**IClientSecurity:: setampla**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)) falhará se tentar especificar Schannel como o serviço de autenticação.

Os parâmetros a seguir devem ser especificados quando um cliente chama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity):

-   *dwAuthnLevel* especifica o nível de autenticação padrão que o cliente deseja usar. Não pode ser RPC \_ C \_ Authn \_ nível \_ None.
-   *dwImpLevel* deve ser a \_ representação de nível de imp do RPC C \_ \_ \_ .
-   *pAuthList* deve ter os seguintes parâmetros de [**\_ \_ informações de autenticação exclusivas**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) como um membro da lista:
    -   *dwAuthnSvc* deve ser RPC \_ C \_ Authn \_ GSS \_ Schannel.
    -   *dwAuthzSvc* deve ser RPC \_ C \_ AUTHZ \_ None.
    -   *pAuthInfo* é um ponteiro para um [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), convertido como um ponteiro para void, que representa o certificado X. 509 do cliente. Se o cliente não tiver um certificado ou não quiser apresentar seu certificado ao servidor, o *pAuthInfo* deverá ser **nulo** e será feita uma tentativa de conexão anônima com o servidor.
-   *dwCapabilities* é um conjunto de sinalizadores que indicam recursos adicionais do cliente. Consulte [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para obter informações sobre quais sinalizadores devem ser definidos.

Para obter mais informações sobre como usar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), consulte [Configurando a segurança do processwide com CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

### <a name="how-a-client-changes-the-security-blanket"></a>Como um cliente altera a cobertura de segurança

Se um cliente quiser usar o TLS, mas alterar a cobertura de segurança depois de chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), ele deverá chamar [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) ou [**IClientSecurity:: setampla**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) com parâmetros semelhantes aos usados na chamada para **CoInitializeSecurity**, com as seguintes diferenças:

-   *pServerPrincName* indica o nome da entidade de segurança do servidor, no formato msstd ou fullsic. Para obter informações sobre esses formatos, consulte [nomes de entidade de segurança](/windows/desktop/Rpc/principal-names). Se o cliente tiver o certificado X. 509 do servidor, ele poderá encontrar o nome da entidade de segurança chamando [**RpcCertGeneratePrincipalName**](/windows/desktop/api/rpcssl/nf-rpcssl-rpccertgenerateprincipalname).
-   *pAuthInfo* é um ponteiro para um [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), convertido como um ponteiro para \_ identificador de identidade de autenticação RPC \_ \_ , que representa o certificado X. 509 do cliente. Se o cliente não tiver um certificado ou não quiser apresentar seu certificado ao servidor, o *pAuthInfo* deverá ser **nulo** e será feita uma tentativa de conexão anônima com o servidor.
-   *dwCapabilities* consiste em sinalizadores que indicam recursos adicionais do cliente. Somente quatro sinalizadores podem ser usados para alterar as configurações de ampla segurança: EOAC \_ padrão, EOAC \_ Mutual \_ auth, EOAC \_ qualquer \_ autoridade (esse sinalizador é preterido) e EOAC \_ Make \_ FULLSIC. Para obter mais informações, consulte [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

Para obter mais informações sobre como usar o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), consulte [definindo a segurança no nível de proxy da interface](setting-security-at-the-interface-proxy-level.md).

### <a name="example-client-changes-the-security-blanket"></a>Exemplo: o cliente altera a cobertura de segurança

O exemplo a seguir demonstra como um cliente pode alterar a cobertura de segurança para acomodar uma solicitação do servidor para o cliente fornecer seu certificado X. 509. O código de tratamento de erros é omitido para fins de brevidade.


```C++
void ClientChangesSecurity ()
{
  HCRYPTPROV                   provider           = 0;
  HCERTSTORE                   cert_store         = NULL;
  PCCERT_CONTEXT               client_cert        = NULL;
  PCCERT_CONTEXT               server_cert        = NULL;
  WCHAR                        *server_princ_name = NULL;
  ISecret                      *pSecret           = NULL;
  MULTI_QI                     server_instance;
  COSERVERINFO                 server_machine;
  SOLE_AUTHENTICATION_LIST     auth_list;
  SOLE_AUTHENTICATION_INFO     auth_info[1];



  // Specify all the authentication info. 
  // The client is willing to connect using SChannel,
  //   with no client certificate.
  auth_list.cAuthInfo     = 1;
  auth_list.aAuthInfo     = auth_info;
  auth_info[0].dwAuthnSvc = RPC_C_AUTHN_GSS_SCHANNEL;
  auth_info[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
  auth_info[0].pAuthInfo  = NULL;  // No certificate

  // Initialize client security with no client certificate.
  CoInitializeSecurity( NULL, -1, NULL, NULL,
                        RPC_C_AUTHN_LEVEL_PKT,
                        RPC_C_IMP_LEVEL_IMPERSONATE, &auth_list,
                        EOAC_NONE, NULL );
  
  // Specify info for the proxy.
  server_instance = {&IID_ISecret, NULL, S_OK};
  server_machine  = {0, L"ServerMachineName", NULL, 0};
  
  // Create a proxy.
  CoCreateInstanceEx( CLSID_Secret, NULL, CLSCTX_REMOTE_SERVER, 
                      &server_machine, 1, &server_instance);
  pSecret = (ISecret *) server_instance.pItf;

  //** The client obtained the server's certificate during the handshake.
  //** The server requests a certificate from the client.

  // Get the default certificate provider.
  CryptAcquireContext( &provider, NULL, NULL, PROV_RSA_SCHANNEL, 0 );

  // Open the certificate store.
  cert_store = CertOpenSystemStore( provider, L"my" );

  // Find the client's certificate.
  client_cert = 
    CertFindCertificateInStore( cert_store,
                                X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
                                0,
                                CERT_FIND_SUBJECT_STR,
                                L"ClientName",  // Use the principal name
                                NULL );

  // Find the fullsic principal name of the server.
  RpcCertGeneratePrincipalName( server_cert, RPC_C_FULL_CERT_CHAIN, 
                                &server_princ_name );

  // Change the client's security: 
  // Increase the authentication level and attach a certificate.
  CoSetProxyBlanket( pSecret, RPC_C_AUTHN_GSS_SCHANNEL,
                     RPC_C_AUTHZ_NONE,
                     server_princ_name, RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
                     RPC_C_IMP_LEVEL_IMPERSONATE, 
                     (RPC_AUTH_IDENTITY_HANDLE *) client_cert,
                     EOAC_NONE );

  cleanup:
  if (server_princ_name != NULL)
    RpcStringFree( &server_princ_name );
  if (client_cert != NULL)
    CertFreeCertificateContext(client_cert);
  if (server_cert != NULL)
    CertFreeCertificateContext(server_cert);
  if (cert_store != NULL)
    CertCloseStore( cert_store, CERT_CLOSE_STORE_CHECK_FLAG );
  if (provider != 0 )
    CryptReleaseContext( provider, 0 );
  if (pSecret != NULL)
    pSecret->Release();
  CoUninitialize();
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pacotes de segurança e COM](com-and-security-packages.md)
</dt> </dl>

 

 