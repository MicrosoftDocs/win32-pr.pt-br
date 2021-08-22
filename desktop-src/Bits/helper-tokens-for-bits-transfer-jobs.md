---
title: Tokens auxiliares para trabalhos de transferência de BITS
description: Tokens auxiliares para trabalhos de transferência de BITS
ms.assetid: f29f9870-e406-472b-9342-203def7453ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a22708b11bd07165166f647454c05663d59f6cfeddde659a9bb5903d5a9606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528676"
---
# <a name="helper-tokens-for-bits-transfer-jobs"></a>Tokens auxiliares para trabalhos de transferência de BITS

No Windows Vista, o serviço Serviço de Transferência Inteligente em Segundo Plano (BITS) permite que um aplicativo associe um único token de segurança a um trabalho de transferência de BITS. O trabalho de transferência de BITS usa esse token para autenticação e para acesso a recursos locais e remotos.

No Windows 7, o serviço BITS associa um token adicional a um trabalho de transferência de BITS. O trabalho de transferência de BITS pode ser configurado com um token de segurança adicional, que é um token de representação criado por um aplicativo que chama a API COM do BITS. Esse modelo de token auxiliar permite que os aplicativos usem simultaneamente dois tokens de segurança diferentes para acessar arquivos locais, certificados do lado do cliente, arquivos remotos e proxies. Por exemplo, um trabalho de transferência de BITS é criado que grava os dados baixados em um diretório local privilegiado e, em seguida, apresenta uma identidade de domínio com direitos baixos para o servidor HTTP e o servidor proxy.

Um aplicativo, normalmente um Windows, especifica um token auxiliar usando a nova interface [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions). Essa interface é implementada pelo objeto de trabalho BITS. O aplicativo chama [**IBackgroundCopyJob::QueryInterface para**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) obter o ponteiro da interface. O aplicativo representa a identidade auxiliar e chama [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) para passar o token para o serviço BITS. Em seguida, o aplicativo especifica os recursos aos quais o token se aplica passando um conjunto de sinalizadores de bits usando [**IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags). O aplicativo limpa todos os sinalizadores (usando **SetHelperTokenFlags** novamente) para reverter o comportamento. O serviço BITS armazena os sinalizadores de bits e o token no trabalho de transferência de BITS.

Quando o proprietário dos trabalhos de transferência bits faz o login, o serviço BITS descarta todos os tokens auxiliares associados ao trabalho de transferência. Se a transferência não for concluída, o serviço BITS coloca o trabalho em um estado de erro com o código de erro **BG \_ E TOKEN \_ \_ REQUIRED** e descarta o token auxiliar. O aplicativo cliente pode atualizar o token chamando [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) e, em seguida, pode retomar o trabalho de transferência de BITS. Como alternativa, o aplicativo cliente pode limpar os sinalizadores de token auxiliar usando [**IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) e retomar o trabalho de transferência sem um token auxiliar.

Da mesma forma, quando o proprietário de uma sessão de serviços de terminal faz o login, o serviço BITS deve descartar todos os tokens auxiliares dessa sessão e colocar os trabalhos de transferência afetados em um estado de erro com o código de erro **BG \_ E TOKEN \_ \_ REQUIRED.**

O modelo de token auxiliar requer uma alteração na política de controle de acesso bits. Versões anteriores do BITS implementaram verificações de acesso em cada chamada de método. A partir Windows 7, a verificação de acesso deve ser executada dentro da chamada [**IBackgroundCopyJob::QueryInterface;**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) caso contrário, o token auxiliar pode não ter acesso ao trabalho de transferência.

> [!Note]  
> Implementações mais antigas exigiam efetivamente que os usuários do BITS tenham privilégios de administrador para definir tokens auxiliares. A partir do Windows 10, versão 1607, os usuários bits não administradores podem usar [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) para definir tokens auxiliares não administradores em trabalhos BITS que eles têm. Essa alteração permite que usuários bits não administradores (como serviços de download em segundo plano em execução na conta [NetworkService](/windows/desktop/Services/networkservice-account)) deem tokens auxiliares.
>
> Especificamente, a implementação foi alterada para permitir que os usuários sem privilégios de administrador deem um conjunto de tokens auxiliares, desde que as seguintes condições sejam atendidas:
>
> -   durante a chamada [**IBackgroundCopyJob::QueryInterface,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) o SID do token do thread do chamador é o mesmo que o SID da conta de usuário do proprietário do trabalho e
> -   quando [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) é chamado, o token auxiliar não tem o SID do administrador (**\_ \_ ADMINISTRADORES RID DO ALIAS \_** DE DOMÍNIO ) habilitado.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> </dl>

 

 