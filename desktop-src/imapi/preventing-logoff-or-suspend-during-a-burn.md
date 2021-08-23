---
title: Impedindo o logoff ou a suspensão durante uma gravação
description: Se as precauções adequadas não forem feitas em um aplicativo, é possível que um usuário faça logoff durante uma operação de gravação. Isso leva à interrupção do processo de gravação, o que pode resultar em perda de dados e possivelmente renderizar o disco inutilizável.
ms.assetid: 5223c9f6-30f6-43ce-b46c-267da0a53d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f3dd6980db72854ff65d657cc58730335febcb1dbc8c4a467eedead88f5eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977126"
---
# <a name="preventing-logoff-or-suspend-during-a-burn"></a>Impedindo o logoff ou a suspensão durante uma gravação

Se as precauções adequadas não forem feitas em um aplicativo, é possível que um usuário faça logoff durante uma operação de gravação. Isso leva à interrupção do processo de gravação, o que pode resultar em perda de dados e possivelmente renderizar o disco inutilizável.

Para evitar esse problema, o aplicativo deve processar a mensagem do [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) , que é entregue antes do logoff. Se o aplicativo receber essa mensagem durante a execução de uma operação de gravação, retorne **false** para cancelar o procedimento de logoff. Se o aplicativo permitir que o usuário decida se deseja continuar o logoff, será fornecido um aviso indicando que o usuário perderá os dados.

As transições de energia durante o processo de gravação também podem criar possíveis problemas no sucesso de uma atividade de gravação. Impedir essas complicações durante o processo de gravação exige que um aplicativo esteja ciente de quando as transições de energia estão prestes a ocorrer. Isso é feito por meio da habilitação do aplicativo para processar a mensagem [**\_ POWERBROADCAST do WM**](/windows/desktop/Power/wm-powerbroadcast) . os aplicativos desenvolvidos para Windows XP ou Windows Server 2003 podem retornar a **\_ \_ negação de consulta de difusão** em resposta ao [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend), impedindo a suspensão durante o processo de gravação.

devido a alterações no modelo de gerenciamento de energia para Windows Vista e Windows Server 2008, o evento [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend) não é mais entregue aos aplicativos. Em vez disso, o evento [**PBT \_ APMSUSPEND**](/windows/desktop/Power/pbt-apmsuspend) é entregue, fornecendo dois segundos para um aplicativo se preparar para a transição.

Como resultado dessas alterações, é recomendável que os aplicativos chamem a função [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) para evitar um tempo limite ocioso do sistema que normalmente resulta na transição para suspender. É importante lembrar que a chamada dessa função com os sinalizadores apropriados definidos só impedirá o sistema ocioso, e não uma suspensão em andamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o IMAPi](using-imapi.md)
</dt> <dt>

[**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate)
</dt> </dl>

 

 