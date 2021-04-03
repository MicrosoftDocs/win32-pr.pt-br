---
title: Autenticação mútua em um serviço de soquetes do Windows com o SCP
description: Os tópicos nesta seção incluem exemplos de código que mostram como executar a autenticação mútua com um serviço que se publica usando um SCP (ponto de conexão de serviço).
ms.assetid: f730464c-95ac-4285-960c-18862f6f7852
ms.tgt_platform: multiple
keywords:
- Autenticação mútua em um serviço de soquetes do Windows com um SCP AD
- Active Directory, usando a autenticação mútua, o Windows Sockets Service com um SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527715c4a35dc15cd67f5820e6fa891b56452399
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823648"
---
# <a name="mutual-authentication-in-a-windows-sockets-service-with-scp"></a>Autenticação mútua em um serviço de soquetes do Windows com o SCP

Os tópicos nesta seção incluem exemplos de código que mostram como executar a autenticação mútua com um serviço que se publica usando um SCP (ponto de conexão de serviço). Os exemplos são baseados em um Microsoft Windows Sockets Service que usa um pacote SSPI para lidar com a negociação de autenticação mútua entre um cliente e o serviço. Use os procedimentos a seguir para implementar a autenticação mútua nesse cenário.

**Para registrar SPNs em um diretório quando um serviço é instalado**

1.  Chame a função [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para compor SPNs (nomes da entidade de serviço) para o serviço.
2.  Chame a função [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) para registrar os SPNs na conta de serviço ou conta de computador em cujo contexto o serviço será executado. Esta etapa deve ser executada por um administrador de domínio; uma exceção é que um serviço em execução na conta LocalSystem pode registrar seu SPN no formato " <service class> / <host> " na conta de computador do host de serviço.

**Para verificar a configuração na inicialização do serviço**

-   Verifique se os SPNs apropriados estão registrados na conta sob a qual o serviço está sendo executado. Para obter mais informações, consulte [tarefas de manutenção de conta de logon](logon-account-maintenance-tasks.md).

**Para autenticar o serviço na inicialização do cliente**

1.  Recuperar dados de conexão do ponto de conexão de serviço do serviço.
2.  Estabeleça uma conexão com o serviço.
3.  Chame a função [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) para compor um SPN para o serviço. Redija o SPN da cadeia de caracteres de classe de serviço conhecida e os dados recuperados do ponto de conexão de serviço. Esses dados incluem o nome do host do servidor no qual o serviço está em execução. Lembre-se de que o nome do host deve ser um nome DNS.
4.  Use um pacote de segurança SSPI para executar a autenticação:
    1.  Chame a função [**falha AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) para adquirir as credenciais do cliente.
    2.  Passe as credenciais do cliente e o SPN para a função [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) para gerar um blob de segurança a ser enviado ao serviço para autenticação. Defina o sinalizador de **\_ \_ \_ autenticação mútua de req do ISC** para solicitar autenticação mútua.
    3.  Troque os BLOBs pelo serviço até que a autenticação seja concluída.
5.  Verifique a máscara de recursos retornados para o sinalizador de **\_ \_ \_ autenticação mútua de req do ISC** para verificar se a autenticação mútua foi executada.
6.  Se a autenticação tiver sido bem-sucedida, troque o tráfego com o serviço autenticado. Use a assinatura digital para garantir que as mensagens entre o cliente e o serviço não tenham sido violadas. A menos que os requisitos de desempenho sejam graves, use a criptografia. Para obter mais informações e um exemplo de código que mostra como usar as funções [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)e [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) em um pacote SSPI, consulte [garantindo a integridade da comunicação durante a troca de mensagens](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

**Para autenticar o cliente pelo serviço quando um cliente se conecta**

1.  Carregue um pacote de segurança SSPI que dê suporte à autenticação mútua.
2.  Quando um cliente se conecta, use o pacote de segurança para executar a autenticação:
    1.  Chame a função [**falha AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) para adquirir as credenciais de serviço.
    2.  Passe as credenciais de serviço e o blob de segurança recebido do cliente para a função [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) para gerar um blob de segurança para enviar de volta para o cliente.
    3.  Troque os BLOBs pelo cliente até que a autenticação seja concluída.
3.  Verifique a máscara de recursos retornados para o sinalizador de **\_ \_ \_ autenticação mútua de ASC RET** para verificar se a autenticação mútua foi executada.
4.  Se a autenticação tiver sido bem-sucedida, troque o tráfego com o cliente autenticado. Use a assinatura digital e a criptografia, a menos que o desempenho seja um problema.

Para obter mais informações e um exemplo de código para esse cenário de autenticação mútua, consulte:

-   [Como um cliente autentica um serviço Windows Sockets baseado em SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md)
-   [Compor e registrar SPNs para um serviço de soquetes do Windows baseado em SCP](composing-and-registering-spns-for-an-scp-based-windows-sockets-service.md)
-   [Como um serviço do Windows Sockets autentica um cliente](how-a-windows-sockets-service-authenticates-a-client.md)

Para obter mais informações, consulte:

-   [Publicando com pontos de conexão de serviço](publishing-with-service-connection-points.md)
-   [Documentação do SSPI](/windows/desktop/SecAuthN/sspi)
-   [Documentação do Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)

 

 