---
title: Impedindo o logoff ou a suspensão durante uma gravação
description: Se as precauções adequadas não forem feitas em um aplicativo, é possível que um usuário faça logoff durante uma operação de gravação. Isso leva à interrupção do processo de gravação, o que pode resultar em perda de dados e possivelmente renderizar o disco inutilizável.
ms.assetid: 5223c9f6-30f6-43ce-b46c-267da0a53d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5922fbe6dbc27303cee82e7ed745cbaaf2744781
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454004"
---
# <a name="preventing-logoff-or-suspend-during-a-burn"></a>Impedindo o logoff ou a suspensão durante uma gravação

Se as precauções adequadas não forem feitas em um aplicativo, é possível que um usuário faça logoff durante uma operação de gravação. Isso leva à interrupção do processo de gravação, o que pode resultar em perda de dados e possivelmente renderizar o disco inutilizável.

Para evitar esse problema, o aplicativo deve processar a mensagem do [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) , que é entregue antes do logoff. Se o aplicativo receber essa mensagem durante a execução de uma operação de gravação, retorne **false** para cancelar o procedimento de logoff. Se o aplicativo permitir que o usuário decida se deseja continuar o logoff, será fornecido um aviso indicando que o usuário perderá os dados.

As transições de energia durante o processo de gravação também podem criar possíveis problemas no sucesso de uma atividade de gravação. Impedir essas complicações durante o processo de gravação exige que um aplicativo esteja ciente de quando as transições de energia estão prestes a ocorrer. Isso é feito por meio da habilitação do aplicativo para processar a mensagem [**\_ POWERBROADCAST do WM**](/windows/desktop/Power/wm-powerbroadcast) . Os aplicativos desenvolvidos para o Windows XP ou o Windows Server 2003 podem retornar a **\_ \_ negação de consulta de difusão** em resposta ao [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend), impedindo a suspensão durante o processo de gravação.

Devido a alterações no modelo de gerenciamento de energia para Windows Vista e Windows Server 2008, o evento [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend) não é mais entregue aos aplicativos. Em vez disso, o evento [**PBT \_ APMSUSPEND**](/windows/desktop/Power/pbt-apmsuspend) é entregue, fornecendo dois segundos para um aplicativo se preparar para a transição.

Como resultado dessas alterações, é recomendável que os aplicativos chamem a função [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) para evitar um tempo limite ocioso do sistema que normalmente resulta na transição para suspender. É importante lembrar que a chamada dessa função com os sinalizadores apropriados definidos só impedirá o sistema ocioso, e não uma suspensão em andamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o IMAPi](using-imapi.md)
</dt> <dt>

[**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate)
</dt> </dl>

 

 