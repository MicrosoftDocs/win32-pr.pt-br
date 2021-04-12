---
title: Padrões de segurança COM
description: Você pode usar os padrões de segurança COM para seu aplicativo em vez de especificar suas próprias configurações de segurança.
ms.assetid: 6f1f6925-a6ab-4cfa-b0b4-b4b4012979f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cba607044d6e93c9f01243809feae6e5a600851
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291815"
---
# <a name="com-security-defaults"></a>Padrões de segurança COM

Você pode usar os padrões de segurança COM para seu aplicativo em vez de especificar suas próprias configurações de segurança. Nesse caso, COM irá inicializar e gerenciar a segurança para você. Você não precisa configurar o registro nem chamar nenhuma função de segurança em seu programa.

No entanto, se determinados valores nomeados do registro tiverem sido definidos ou modificados, os padrões de segurança usados COM serão afetados. A lista a seguir descreve os valores padrão de segurança COM e explica como alguns valores são influenciados pelas configurações do registro.

A seguir estão os valores de segurança padrão que o COM usa:

-   O provedor de serviços de segurança padrão é aquele que é determinado pelo COM para ser o mais compatível com o ambiente. COM escolhe o protocolo Kerberos V5 ou NTLMSSP, com o protocolo Kerberos sendo a opção padrão. Nenhum dos protocolos fornecidos pelo Schannel é escolhido como o padrão.
-   O sistema identifica um chamador por meio de nome de usuário e senha e cria automaticamente um token de identificação usado pelo sistema de segurança.
-   Se o valor nomeado [LegacyAuthenticationLevel](legacyauthenticationlevel.md) existir e se seu valor tiver sido definido, esse valor será usado. Caso contrário, o nível de autenticação será definido em conectar (RPC \_ C \_ Authn \_ nível \_ Connect). Esse nível significa que na primeira chamada que um cliente faz para o servidor, COM faz uma verificação de autenticação. Se o cliente passar a verificação, nenhuma outra autenticação será feita. O valor AuthenticationLevel também pode ser definido sob a chave [AppID](appid-key.md) .
-   Se o valor nomeado [LegacyImpersonationLevel](legacyimpersonationlevel.md) existir e se seu valor tiver sido definido, esse valor será usado. Caso contrário, o nível de representação será definido como identificar (o nível de Requery do RPC \_ C é \_ \_ \_ identificado). Os direitos de representação são concedidos pelo cliente ao servidor. O nível de identificação significa que o servidor pode obter a identidade do cliente. O servidor pode representar o cliente para a verificação da ACL (lista de controle de acesso), mas não pode acessar objetos do sistema como o cliente do. Para obter mais informações, consulte [níveis de representação](impersonation-levels.md) e [encobrimento](cloaking.md).
-   Se o valor nomeado [AccessPermission](accesspermission.md) em **AppID** existir e tiver sido definido, esse valor será usado. Caso contrário, COM verifica uma entrada [DefaultAccessPermission](defaultaccesspermission.md) . Se estiver presente, esse valor será usado. Se esse valor não estiver presente, o COM construirá uma ACL que concede permissões para a identidade do servidor e o sistema local.
-   Se o valor nomeado [SRPTrustLevel](srptrustlevel.md) em **AppID** existir e tiver sido definido, esse valor será usado. Caso contrário, o nível de confiança SRP (política de restrição de software) é definido como não permitido (nível de segurança não \_ \_ permitido), que indica que o aplicativo é executado em um ambiente restrito e não é permitido de acessar quaisquer privilégios de usuário sensíveis à segurança do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 




