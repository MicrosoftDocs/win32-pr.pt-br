---
title: Tokens auxiliares para trabalhos de transferência de BITS
description: Tokens auxiliares para trabalhos de transferência de BITS
ms.assetid: f29f9870-e406-472b-9342-203def7453ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52925a6e0d5a9601e21848d514214bfb843f6246
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454334"
---
# <a name="helper-tokens-for-bits-transfer-jobs"></a>Tokens auxiliares para trabalhos de transferência de BITS

No Windows Vista, o serviço de Serviço de Transferência Inteligente em Segundo Plano (BITS) permite que um aplicativo associe um único token de segurança a um trabalho de transferência de BITS. O trabalho de transferência de BITS usa esse token para autenticação e para acesso a recursos locais e remotos.

No Windows 7, o serviço BITS associa um token adicional a um trabalho de transferência de BITS. O trabalho de transferência do BITS pode ser configurado com um token de segurança adicional, que é um token de representação criado por um aplicativo que chama a API COM do BITS. Esse modelo de token auxiliar permite que os aplicativos usem simultaneamente dois tokens de segurança diferentes para acessar arquivos locais, certificados do lado do cliente, arquivos remotos e proxies. Por exemplo, um trabalho de transferência de BITS é criado para gravar os dados baixados em um diretório local com privilégios e, em seguida, apresenta uma identidade de domínio de direitos limitados ao servidor HTTP e ao servidor proxy.

Um aplicativo, normalmente um serviço do Windows, especifica um token auxiliar usando a nova interface [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions). Essa interface é implementada pelo objeto de trabalho BITS. O aplicativo chama [**método ibackgroundcopyjob:: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) para obter o ponteiro de interface. O aplicativo representa a identidade auxiliar e chama [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) para passar o token para o serviço bits. Em seguida, o aplicativo especifica os recursos aos quais o token se aplica passando um conjunto de sinalizadores de bit usando [**IBitsTokenOptions:: SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags). O aplicativo limpa todos os sinalizadores (usando **SetHelperTokenFlags** novamente) para reverter o comportamento. O serviço BITS armazena os sinalizadores de bit e o token no trabalho de transferência BITS.

Quando o proprietário dos trabalhos de transferência de BITS faz logoff, o serviço BITS descarta os tokens auxiliares associados ao trabalho de transferência. Se a transferência não for concluída, o serviço BITS colocará o trabalho em um estado de erro com o **token BG e o código de erro \_ \_ \_ necessário** e descartará o token auxiliar. O aplicativo cliente pode atualizar o token chamando [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) e, em seguida, pode retomar o trabalho de transferência do bits. Como alternativa, o aplicativo cliente pode limpar os sinalizadores do token auxiliar usando [**IBitsTokenOptions:: SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) e, em seguida, retomar o trabalho de transferência sem um token auxiliar.

Da mesma forma, quando o proprietário de uma sessão dos serviços de terminal faz logoff, o serviço BITS deve descartar os tokens auxiliares dessa sessão e posicionar os trabalhos de transferência afetados em um estado de erro com o código de erro **BG \_ E \_ token \_ necessário** .

O modelo de token auxiliar requer uma alteração na política de controle de acesso do BITS. Versões anteriores de BITS implementaram verificações de acesso em cada chamada de método. A partir do Windows 7, a verificação de acesso deve ser executada dentro da chamada [**método ibackgroundcopyjob:: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) ; caso contrário, o token auxiliar pode não ter acesso ao trabalho de transferência.

> [!Note]  
> As implementações mais antigas exigiam efetivamente que os usuários do BITS tenham privilégios de administrador para definir os tokens auxiliares. A partir do Windows 10, versão 1607, os usuários que não são administradores podem usar [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) para definir tokens auxiliares não administradores em trabalhos bits que eles possuem. Essa alteração permite que usuários não administradores de BITS (como serviços de download de segundo plano em execução na [conta NetworkService](/windows/desktop/Services/networkservice-account)) definam tokens auxiliares.
>
> Especificamente, a implementação foi alterada para permitir que usuários sem privilégios de administrador definam tokens auxiliares, desde que as seguintes condições sejam atendidas:
>
> -   durante a chamada [**método ibackgroundcopyjob:: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , o SID do token thread's do chamador é o mesmo que o SID da conta de usuário do proprietário do trabalho e
> -   Quando [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) é chamado, o token auxiliar não tem o Sid de administrador (**\_ \_ \_ Administradores RID de alias de domínio**) habilitado.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> </dl>

 

 