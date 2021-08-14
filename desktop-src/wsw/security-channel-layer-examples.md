---
title: Exemplos de camada de canal de segurança
description: Os exemplos a seguir ilustram a segurança na Camada de Canal.
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- exemplos de segurança
- exemplos de segurança, instalação
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d130bc7e0e4250107c6e331a43f7d5a13786929c37bd998177ee587c2f29049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192767"
---
# <a name="security-channel-layer-examples"></a>Exemplos de camada de canal de segurança

Os exemplos a seguir ilustram a segurança na camada [de canal](channel-layer-overview.md)

Windows de transporte em TCP: Cliente: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), Servidor: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Windows segurança de transporte em pipes nomeados: Cliente: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Servidor: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Segurança de transporte SSL: Cliente: [HttpClientWithSslExample](httpclientwithsslexample.md), Servidor: [HttpServerWithSslExample](httpserverwithsslexample.md).

Nome de usuário sobre segurança de modo misto SSL: Cliente: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), Servidor: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).

Nome de usuário sobre segurança de modo misto SSL: Cliente: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), Servidor: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).

Nome de usuário sobre segurança de modo misto SSL: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Token emitido pela segurança de modo misto SSL: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). Certificado X509 sobre segurança de modo misto SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="one-time-setup-for-security-samples"></a>One-Time configuração para exemplos de segurança

Para executar exemplos de segurança WWSAPI, você precisa configurar os certificados de cliente e servidor para SSL, bem como uma conta de usuário local para autenticação de cabeçalho HTTP. Antes de começar, você precisa das seguintes ferramentas:

-   MakeCert.exe (disponível no SDK Windows 7.)
-   CertUtil.exe ou CertMgr.exe (CertUtil.exe está disponível nos SDKs do Windows a partir do Windows Server 2003. CertMgr.exe está disponível no SDK Windows 7. Você só precisa de uma dessas ferramentas.)
-   HttpCfg.exe: (Você precisará disso somente se estiver usando Windows 2003 ou Windows XP. Essa ferramenta está disponível no Windows ferramentas de suporte do XP SP2 e também vem com o CD Windows Server 2003 Resource Kit Tools.)

Se você obter os exemplos de WWSAPI instalando o SDK do Windows 7, poderá encontrar o MakeCert.exe e o CertMgr.exe em %ProgramFiles% \\ SDKs da Microsoft \\ Windows \\ v7.0 \\ bin.

Execute a seguinte configuração de cinco etapas no prompt de comando (elevada se você estiver usando Windows Vista e superior):

1.  Gerar um certificado auto-assinado para ser a AC (autoridade de certificação) ou emissor: **MakeCert.exe -ss Root -sr LocalMachine -n "CN=Fake-Test-CA" -cy authority -r -sk "CAKeyContainer"**
2.  Gere um certificado do servidor usando o certificado anterior como emissor: **MakeCert.exe -ss My -sr LocalMachine -n "CN=localhost" -sky exchange -is Root -ir LocalMachine -in Fake-Test-CA -sk "ServerKeyContainer"**
3.  Encontre a impressão digital (um hash SHA-1 de 40 caracteres) do certificado do servidor executando um dos comandos a seguir e pesquise o certificado chamado localhost com o emissor Fake-Test-CA:
    -   **CertUtil.exe -store Meu localhost**
    -   **CertMgr.exe -s -r LocalMachine My**
4.  Registre a impressão digital do certificado do servidor sem espaços com HTTP.SYS:
    -   No Windows Vista e superior (a opção "appid" é um GUID **arbitrário):Netsh.exe http add sslcert ipport=0.0.0.0:8443 appid={00 112233-4455-6677-8899-AABBCCDDEEFF}** certhash=<40CharacterThumbprint>
    -   No Windows XP ou 2003: **HttpCfg.exe set ssl -i 0.0.0.0:8443 -h <40CharacterThumbprint>**
5.  Criar um usuário local: **Usuário net "TestUserForBasicAuth" "TstPWD@ \* 4Bsic" /add**

Para limpar os certificados, a associação de certificado SSL e a conta de usuário criada nas etapas anteriores, execute os comandos a seguir. Observe que, se houver vários certificados com o mesmo nome, CertMgr.exe precisará de sua entrada antes de excluí-los.

-   **CertMgr.exe -del -c -n Fake-Test-CA -s -r Raiz localMachine**
-   **CertMgr.exe -del -c -n localhost -s -r LocalMachine My**
-   **Netsh.exe http delete sslcert ipport=0.0.0.0:8443 (ou HttpCfg.exe delete ssl -i 0.0.0.0:8443)**
-   **Usuário net "TestUserForBasicAuth" /delete**

Certifique-se de que haja apenas um certificado raiz chamado Fake-Test-CA. Se você não tiver certeza, é sempre seguro tentar limpar esses certificados usando os comandos de limpeza acima (e ignorar erros) antes de iniciar a configuração de cinco etapas.

 

 




