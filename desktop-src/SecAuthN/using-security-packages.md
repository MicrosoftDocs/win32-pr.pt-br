---
description: Lista os pacotes de segurança que podem ser usados com SSPI.
ms.assetid: f5999d41-b334-49be-8883-d9b9042d20dc
title: Usando pacotes de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9253ee2ac4cec98e3c68a1f3dab80a71b216e6235af78722864ee0e0958897c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915188"
---
# <a name="using-security-packages"></a>Usando pacotes de segurança

A [*SSPI (Interface*](../secgloss/s-gly.md) do Provedor de Suporte de Segurança) pode ser usada com os seguintes pacotes [*de segurança:*](../secgloss/s-gly.md)

-   [Pacote de segurança Kerberos](#kerberos-security-package)
-   [Pacote de segurança NTLM](#ntlm-security-package)

Os [*protocolos Kerberos*](../secgloss/k-gly.md) e NTLM são implementados como pacotes de segurança do SSP [*(provedor*](../secgloss/s-gly.md) de suporte de segurança) do Secur32.dll fornecido com o sistema operacional. Por padrão, o suporte para autenticação Kerberos e NTLM é carregado pela LSA (autoridade de segurança [*local)*](../secgloss/l-gly.md) em um computador quando o sistema é iniciado. No Windows server ou Windows, qualquer pacote pode ser usado para autenticar logons de rede e conexões de cliente/servidor. Qual deles é usado depende dos recursos do computador do outro lado da conexão. O protocolo Kerberos sempre é preferencial, se disponível.

Depois que um contexto de segurança para um usuário interativo tiver sido estabelecido, outra instância do pacote Kerberos ou NTLM poderá ser carregada por um processo em execução no contexto de segurança do usuário para dar suporte à troca, assinatura, verificação, criptografia e descriptografia de mensagens. No entanto, nenhum processo diferente do LSA tem permissão de acesso a chaves [*de*](../secgloss/s-gly.md) sessão ou tíquetes no cache de credenciais.

Os serviços do sistema e os aplicativos de nível de transporte acessam um SSP por meio do SSPI, que fornece funções para enumerar os pacotes de segurança disponíveis em um sistema, selecionar um pacote e usar esse pacote para obter uma conexão autenticada.

Os métodos no SSPI são rotinas genéricas que os desenvolvedores podem usar sem conhecer os detalhes de um protocolo [*de segurança específico.*](../secgloss/s-gly.md) Por exemplo, quando uma conexão cliente/servidor é autenticada:

1.  O aplicativo no lado do [](../secgloss/c-gly.md) cliente da conexão envia credenciais para o servidor usando a função SSPI [**InitializeSecurityContext (Geral).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
2.  O aplicativo no lado do servidor da conexão responde com a função SSPI [**AcceptSecurityContext (Geral).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
3.  Depois que a conexão tiver sido autenticada, o LSA no servidor usará informações do cliente para criar um [*token de acesso*](../secgloss/a-gly.md).
4.  O servidor pode chamar a função SSPI [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) para anexar o token de acesso a um thread de representação para o serviço.

## <a name="kerberos-security-package"></a>Pacote de segurança Kerberos

O pacote [](../secgloss/s-gly.md) de segurança Kerberos baseia-se no protocolo [*de autenticação Kerberos*](../secgloss/k-gly.md).

Se o protocolo Kerberos estiver sendo usado para autenticar uma conexão de cliente/servidor, [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) gerará uma mensagem GSSAPI que inclui uma mensagem REQ de AP do KRB do \_ \_ cliente. [**AcceptSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) gera uma mensagem GSSAPI que inclui uma mensagem de \_ REP de AP \_ KRB do servidor.

Para obter informações em segundo plano sobre as etapas que ocorrem nos bastidores na implementação de um protocolo Kerberos, consulte [Microsoft Kerberos](microsoft-kerberos.md).

Todos os serviços distribuídos usam SSPI para acessar o protocolo Kerberos. Uma lista parcial das maneiras pelas quais o protocolo Kerberos é usado para autenticação inclui:

-   Serviços de spooler de impressão
-   Acesso a arquivos remotos CIFS/SMB
-   [*Consultas LDAP*](../secgloss/l-gly.md) para o Active Directory
-   Indicações e gerenciamento de sistema de arquivos distribuídos
-   Autenticação da autoridade de segurança de host para host IPsec
-   Solicitações de reserva para qualidade de serviço de rede
-   Autenticação de intranet para Serviços de Informações da Internet
-   Gerenciamento de servidor remoto ou estação de trabalho usando RPC autenticado
-   [*Solicitações de certificado*](../secgloss/c-gly.md) para serviços de certificado para usuários e computadores de domínio

## <a name="ntlm-security-package"></a>Pacote de segurança NTLM

O pacote de segurança NTLM baseia-se no protocolo de autenticação NTLM.

 

 
