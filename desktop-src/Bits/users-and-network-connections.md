---
title: Usuários e conexões de rede
description: O BITS transfere arquivos somente quando o proprietário do trabalho é conectado e uma conexão de rede é estabelecida.
ms.assetid: b31fc04f-8fa8-407f-9380-ca6b09589c46
keywords:
- BITS de conexões de rede
- transferir BITS de trabalho, Propriedade
- transferir BITS de trabalho, propriedade, conta de usuário
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 54e346590cac90b8d896a9a45c86aee5ae241d7d299bb055cf9ff55db88b8668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679878"
---
# <a name="users-and-network-connections"></a>Usuários e conexões de rede

O BITS transfere arquivos somente quando o proprietário do trabalho é conectado e uma conexão de rede é estabelecida. O BITS processa o trabalho de transferência usando o contexto de segurança do proprietário do trabalho. O usuário que criou o trabalho é considerado o proprietário do trabalho. No entanto, um usuário com privilégios de administrador pode apropriar- [**se**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) do trabalho de outro usuário.

O BITS suspende um trabalho quando o proprietário faz logoff ou se a conexão de rede é perdida (o BITS não forçará uma conexão de rede). O BITS retoma o trabalho quando o proprietário faz logon novamente e uma conexão de rede é estabelecida. Depois que a conexão de rede é estabelecida, pode ocorrer um pequeno atraso antes que o BITS comece a transferir dados.

Se a conexão de rede for perdida, todos os trabalhos cujo estado for [**BG \_ estado de trabalho \_ \_ na fila**](/windows/desktop/api/Bits/ne-bits-bg_job_state) ou **BG \_ transferência de \_ estado \_ de trabalho** serão movidos para o estado de **\_ \_ \_ \_ erro temporário de estado do trabalho** com um código de erro BG [ \_ E \_ \_ desconectado pela rede](bits-return-values.md) . Quando uma conexão de rede é estabelecida, todos os trabalhos em um BG estado de **\_ \_ \_ \_ erro transitório de estado de trabalho** , que podem incluir qualquer código de erro, são movidos para o estado de **\_ \_ \_ fila de estado de trabalho BG** .

Para que o BITS detecte que um usuário está conectado, o usuário deve usar uma das seguintes opções de logon interativo:

-   Faça logon na tela de boas-vindas.
-   Faça logon em um cliente de [serviço de terminal](../termserv/terminal-services-portal.md) .
-   Use a [troca rápida de usuário](../shell/fast-user-switching.md).
-   a partir do Windows 10, versão 1607, faça logon de outro dispositivo usando o Powershell remoto. Consulte [para gerenciar sessões remotas do PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md) para obter detalhes.

Executar um aplicativo como outro usuário (usando o comando **runas** ) não é um logon interativo; O BITS não executará trabalhos associados ao usuário especificado.

As contas do sistema LocalSystem, LocalService e NetworkService estão sempre conectadas; Portanto, os trabalhos enviados por um serviço usando essas contas sempre são executados. Para obter informações e limitações sobre o uso de contas de serviço, consulte [contas de serviço e bits](service-accounts-and-bits.md).

Os proprietários de trabalho podem fornecer um token auxiliar a ser usado em situações em que vários tokens são necessários para concluir uma transferência, como para autenticação com um host remoto. Consulte [tokens auxiliares para trabalhos de transferência de bits](helper-tokens-for-bits-transfer-jobs.md) para obter detalhes. em versões anteriores do Windows, o proprietário do trabalho efetivamente tinha que ter privilégios de administrador para iniciar um trabalho que usava um token auxiliar. no Windows 10, a versão 1607, agora é possível que um proprietário do trabalho do BITS defina tokens auxiliares sem ser um administrador, desde que o token auxiliar não tenha recursos de administrador. Isso reduz a superfície de vulnerabilidade de download em segundo plano ou de ferramentas de atualização, permitindo sua execução com a conta NetworkService com menos privilégios, em vez de uma conta com privilégios administrativos.

Os usuários com um [token restrito](../secauthz/restricted-tokens.md) (um token que contém SIDs de restrição) não podem criar ou modificar trabalhos.
 

 