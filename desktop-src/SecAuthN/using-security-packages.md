---
description: Lista os pacotes de segurança que podem ser usados com SSPI.
ms.assetid: f5999d41-b334-49be-8883-d9b9042d20dc
title: Usando pacotes de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df24bba0f910ba74a633e8a43f961cee4fb505db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762920"
---
# <a name="using-security-packages"></a>Usando pacotes de segurança

A [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) (SSPI) pode ser usada com os seguintes [*pacotes de segurança*](../secgloss/s-gly.md):

-   [Pacote de segurança Kerberos](#kerberos-security-package)
-   [Pacote de segurança do NTLM](#ntlm-security-package)

Os protocolos [*Kerberos*](../secgloss/k-gly.md) e NTLM são implementados como pacotes de segurança do SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) Secur32.dll fornecido com o sistema operacional. Por padrão, o suporte para autenticação Kerberos e NTLM é carregado pela [*autoridade de segurança local*](../secgloss/l-gly.md) (LSA) em um computador quando o sistema é iniciado. No Windows Server ou em domínios do Windows, qualquer pacote pode ser usado para autenticar logons de rede e conexões de cliente/servidor. Qual delas é usada depende dos recursos do computador no outro lado da conexão. O protocolo Kerberos é sempre preferencial, se disponível.

Depois que um contexto de segurança para um usuário interativo tiver sido estabelecido, outra instância do pacote Kerberos ou NTLM poderá ser carregada por um processo em execução no contexto de segurança do usuário para dar suporte à troca, à assinatura, à verificação, à criptografia e à descriptografia de mensagens. No entanto, nenhum processo diferente da LSA tem permissão para acessar [*chaves de sessão*](../secgloss/s-gly.md) ou tíquetes no cache de credenciais.

Os serviços do sistema e os aplicativos de nível de transporte acessam um SSP por meio de SSPI, que fornece funções para enumerar os pacotes de segurança disponíveis em um sistema, selecionar um pacote e usar esse pacote para obter uma conexão autenticada.

Os métodos no SSPI são rotinas genéricas que os desenvolvedores podem usar sem saber os detalhes de um determinado [*protocolo de segurança*](../secgloss/s-gly.md). Por exemplo, quando uma conexão de cliente/servidor é autenticada:

1.  O aplicativo no lado do cliente da conexão envia [*credenciais*](../secgloss/c-gly.md) para o servidor usando a função SSPI [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
2.  O aplicativo no lado do servidor da conexão responde com a função SSPI [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).
3.  Depois que a conexão for autenticada, a LSA no servidor usará as informações do cliente para criar um [*token de acesso*](../secgloss/a-gly.md).
4.  O servidor pode então chamar a função SSPI [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) para anexar o token de acesso a um thread de representação para o serviço.

## <a name="kerberos-security-package"></a>Pacote de segurança Kerberos

O [*pacote de segurança*](../secgloss/s-gly.md) do Kerberos é baseado no [*protocolo de autenticação Kerberos*](../secgloss/k-gly.md).

Se o protocolo Kerberos estiver sendo usado para autenticar uma conexão de cliente/servidor, [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) gerará uma mensagem GSSAPI que inclui uma \_ \_ mensagem de req KRB AP do cliente. [**AcceptSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) , em seguida, gera uma mensagem GSSAPI que inclui uma \_ \_ mensagem de rep KRB AP do servidor.

Para obter informações básicas sobre as etapas que ocorrem em segundo plano na implementação de um protocolo Kerberos, consulte [Microsoft Kerberos](microsoft-kerberos.md).

Todos os serviços distribuídos usam SSPI para acessar o protocolo Kerberos. Uma lista parcial das maneiras como o protocolo Kerberos é usado para autenticação inclui:

-   Serviços de spooler de impressão
-   Acesso a arquivos remotos CIFS/SMB
-   Consultas [*LDAP*](../secgloss/l-gly.md) para o Active Directory
-   Gerenciamento e referências do sistema de arquivos distribuído
-   Autenticação de autoridade de segurança de host para host IPsec
-   Solicitações de reserva para a qualidade de serviço da rede
-   Autenticação de intranet para Serviços de Informações da Internet
-   Gerenciamento de servidor remoto ou estação de trabalho usando RPC autenticado
-   [*Solicitações de certificado*](../secgloss/c-gly.md) para serviços de certificados para usuários e computadores do domínio

## <a name="ntlm-security-package"></a>Pacote de segurança do NTLM

O pacote de segurança NTLM é baseado no protocolo de autenticação NTLM.

 

 
