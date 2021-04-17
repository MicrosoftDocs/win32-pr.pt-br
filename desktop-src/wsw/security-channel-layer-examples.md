---
title: Exemplos de camada de canal de segurança
description: Os exemplos a seguir ilustram a segurança na camada de canal.
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- exemplos de segurança
- exemplos de segurança, instalação
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1283339b1a4af624e118e3f6c76a07449f9274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105773066"
---
# <a name="security-channel-layer-examples"></a>Exemplos de camada de canal de segurança

Os exemplos a seguir ilustram a segurança na [camada de canal](channel-layer-overview.md)

Segurança de transporte do Windows sobre TCP: cliente: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), servidor: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Segurança de transporte do Windows em pipes nomeados: cliente: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), servidor: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Segurança de transporte SSL: cliente: [HttpClientWithSslExample](httpclientwithsslexample.md), servidor: [HttpServerWithSslExample](httpserverwithsslexample.md).

Nome de usuário sobre SSL de modo misto de segurança: cliente: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), servidor: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).

Nome de usuário sobre SSL de modo misto de segurança: cliente: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), servidor: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).

Nome de usuário sobre segurança de modo misto SSL: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Token emitido sobre segurança de modo misto SSL: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). Certificado X509 sobre segurança de modo misto SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="one-time-setup-for-security-samples"></a>Configuração de One-Time para exemplos de segurança

Para executar exemplos de segurança do WWSAPI, você precisa configurar os certificados de cliente e de servidor para SSL, bem como uma conta de usuário local para autenticação de cabeçalho HTTP. Antes de começar, você precisará das seguintes ferramentas:

-   MakeCert.exe (disponível no SDK do Windows 7).
-   CertUtil.exe ou CertMgr.exe (CertUtil.exe está disponível nos SDKs do Windows a partir do Windows Server 2003. CertMgr.exe está disponível no SDK do Windows 7. Você só precisa de uma dessas ferramentas.)
-   HttpCfg.exe: (você só precisará disso se estiver usando o Windows 2003 ou o Windows XP. Essa ferramenta está disponível em ferramentas de suporte do Windows XP SP2 e também vem com o CD do Windows Server 2003 Resource Kit Tools.)

Se você receber os exemplos de WWSAPI instalando o SDK do Windows 7, poderá encontrar o MakeCert.exe e CertMgr.exe em% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ bin.

Execute a seguinte configuração de cinco etapas no prompt de comando (elevado se você estiver usando o Windows Vista e superior):

1.  Gere um certificado autoassinado para ser a autoridade de certificação (CA) ou o emissor: **MakeCert.exe-SS root-Sr LocalMachine-n "CN = falsifique-Test-CA"-Cy Authority-r-SK "CAKeyContainer"**
2.  Gerar um certificado de servidor usando o certificado anterior como o emissor: **MakeCert.exe-SS My-Sr LocalMachine-n "CN = localhost"-céu Exchange-is root-ir LocalMachine-in falsificated-Test-CA-SK "ServerKeyContainer"**
3.  Localize a impressão digital (um hash de 40 caracteres SHA-1) do certificado do servidor executando qualquer um dos comandos a seguir e pesquise o certificado chamado localhost com o emissor falso-Test-CA:
    -   **CertUtil.exe-armazenar meu localhost**
    -   **CertMgr.exe-s-r LocalMachine My**
4.  Registre a impressão digital do certificado do servidor? s sem espaços com HTTP.SYS:
    -   No Windows Vista e superior (a opção "AppID" é um GUID arbitrário): **Netsh.exe http add sslcert IPPORT = 0.0.0.0:8443 AppID = {00112233-4455-6677-8899-AABBCCDDEEFF}** certhash =<40CharacterThumbprint>
    -   No Windows XP ou 2003: **conjunto deHttpCfg.exe SSL-i 0.0.0.0:8443-h <40CharacterThumbprint>**
5.  Criar um usuário local: **net user "TestUserForBasicAuth" "TstPWD@ \* 4Bsic"/Add**

Para limpar os certificados, a associação de certificado SSL e a conta de usuário criada nas etapas anteriores, execute os comandos a seguir. Observe que, se houver vários certificados com o mesmo nome, CertMgr.exe precisarão de sua entrada antes de excluí-los.

-   **CertMgr.exe-del-c-n falsificado-Test-CA-s-r LocalMachine root**
-   **CertMgr.exe-del-c-n localhost-s-r LocalMachine My**
-   **Netsh.exe http Delete SSLCERT IPPORT = 0.0.0.0:8443 (ou HttpCfg.exe Delete SSL-i 0.0.0.0:8443)**
-   **Net user "TestUserForBasicAuth"/Delete**

Verifique se há apenas um certificado raiz chamado falso-Test-CA. Se você não tiver certeza, é sempre seguro tentar limpar esses certificados usando os comandos de limpeza acima (e ignorar erros) antes de iniciar a configuração de cinco etapas.

 

 




