---
title: Padrões de segurança COM
description: Você pode usar os padrões de segurança COM para seu aplicativo em vez de especificar suas próprias configurações de segurança.
ms.assetid: 6f1f6925-a6ab-4cfa-b0b4-b4b4012979f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6287e00971eca3afe94e598555225943709d1c42546fccb76a442a0dfe3be4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550590"
---
# <a name="com-security-defaults"></a>Padrões de segurança COM

Você pode usar os padrões de segurança COM para seu aplicativo em vez de especificar suas próprias configurações de segurança. Nesse caso, o COM inicializa e gerencia a segurança para você. Você não precisa configurar o Registro nem chamar nenhuma função de segurança em seu programa.

No entanto, se determinados valores nomeados do Registro foram definidos ou modificados, os padrões de segurança que o COM usa serão afetados. A lista a seguir descreve os valores padrão de segurança COM e explica como alguns valores são influenciados pelas configurações do Registro.

A seguir estão os valores de segurança padrão que o COM usa:

-   O provedor de serviços de segurança padrão é aquele determinado pelo COM para ser o mais compatível com o ambiente. COM escolhe o protocolo Kerberos v5 ou NTLMSSP, com o protocolo Kerberos sendo a opção padrão. Nenhum dos protocolos fornecidos pelo Schannel é escolhido como o padrão.
-   O sistema identifica um chamador por meio de nome de usuário e senha e cria automaticamente um token de identificação usado pelo sistema de segurança.
-   Se o [valor nomeado LegacyAuthenticationLevel](legacyauthenticationlevel.md) existir e se seu valor tiver sido definido, esse valor será usado. Caso contrário, o nível de autenticação será definido em connect (RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT). Esse nível significa que, na primeira chamada que um cliente faz ao servidor, o COM faz uma verificação de autenticação. Se o cliente passar na verificação, nenhuma autenticação será feita. O valor AuthenticationLevel também pode ser definido na [chave AppID.](appid-key.md)
-   Se o [valor nomeado LegacyImpersonationLevel](legacyimpersonationlevel.md) existir e se seu valor tiver sido definido, esse valor será usado. Caso contrário, o nível de representação será definido para identificar (RPC \_ C \_ IMP LEVEL \_ \_ IDENTIFY). Os direitos de representação são concedidos pelo cliente ao servidor. Identificar nível significa que o servidor pode obter a identidade do cliente. O servidor pode representar o cliente para verificação de ACL (lista de controle de acesso), mas não pode acessar objetos do sistema como o cliente. Para obter mais informações, consulte [Níveis de representação](impersonation-levels.md) e [Desproporção.](cloaking.md)
-   Se o [valor nomeado AccessPermission](accesspermission.md) em **AppID** existir e tiver sido definido, esse valor será usado. Caso contrário, o COM verifica se [há uma entrada DefaultAccessPermission.](defaultaccesspermission.md) Se estiver presente, esse valor será usado. Se esse valor não estiver presente, o COM construirá uma ACL que concede permissões à identidade do servidor e ao sistema local.
-   Se o [valor nomeado SRPTrustLevel](srptrustlevel.md) em **AppID** existir e tiver sido definido, esse valor será usado. Caso contrário, o nível de confiança da Política de Restrição de Software (SRP) será definido como Não permitido (SAFER \_ LEVELID DISALLOWED), o que indica que o aplicativo é executado em um ambiente restrito e não é permitido acessar quaisquer privilégios de usuário sensíveis à segurança do \_ usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 




