---
description: Contanto que o sistema determine que há atividade de usuário ou aplicativo, ele não entrará em suspensão.
ms.assetid: 83c9394a-1813-405a-802a-0623e5de50d3
title: Critérios de suspensão do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90950b980ec1e0fa06171d7a57d76b410534f96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662177"
---
# <a name="system-sleep-criteria"></a>Critérios de suspensão do sistema

Contanto que o sistema determine que há atividade de usuário ou aplicativo, ele não entrará em suspensão. O sistema pode detectar determinadas atividades, como entrada de usuário ou comunicações de rede. No entanto, há outras atividades que o sistema não pode detectar. Por exemplo, um aplicativo de apresentação requer a tela para exibição. No entanto, pode parecer que o aplicativo está ocioso durante a apresentação, fazendo com que o sistema desative a exibição.

Para notificar o sistema de que seu aplicativo está ocupado, use a função [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) . Essa função impede que o sistema entre em suspensão ou desative a exibição enquanto o aplicativo está em execução.

Os aplicativos de apresentação e multimídia devem chamar a função [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) com a **\_ exibição es \_ necessária** para que o sistema saiba que ele não deve colocar o dispositivo de vídeo em suspensão. Aplicativos de manipulação de eventos, como ferramentas para gerenciar faxes de entrada, devem chamar **SetThreadExecutionState** com o **\_ sistema es \_ necessário**, manipular o evento e, em seguida, limpar o sinalizador para que o sistema possa retornar ao modo de suspensão. Observe que a maioria dos aplicativos de produtividade não precisa usar **SetThreadExecutionState** porque o sistema geralmente pode determinar a atividade por entrada do usuário.

Para manter o tempo desde a última entrada do usuário, o sistema usa um temporizador ocioso de vídeo e um temporizador ocioso do sistema. O sistema compara os temporizadores ociosos com os valores configurados no plano de energia. Se o valor do temporizador ocioso de exibição for maior que o valor de tempo limite de exibição e nenhum thread tiver solicitado a exibição chamando [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) com a **\_ exibição es \_ necessária**, o sistema desligará a exibição. Da mesma forma, se o temporizador ocioso do sistema for maior que o valor do tempo limite do sistema e nenhum aplicativo tiver solicitado o sistema chamando **SetThreadExecutionState** com o **\_ sistema es \_ necessário**, o sistema entrará em suspensão.

O sistema mantém uma contagem de aplicativos que chamaram [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate). O sistema rastreia cada thread que chama **SetThreadExecutionState** e ajusta o contador de acordo. Se esse contador chegar a zero e não houver nenhuma entrada do usuário, o sistema entrará em suspensão.

Se a energia for baixa, um aplicativo poderá solicitar a intervenção do usuário ou solicitar que o sistema se suspenda. Você pode suspender a operação do sistema usando a função [**Setsuspendestate**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

Se o sistema for ativado automaticamente ([PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)), nenhum dos temporizadores será relevante. Para obter mais informações, consulte [eventos de ativação do sistema](system-wake-up-events.md).

## <a name="entering-sleep"></a>Entrando em suspensão

Quando o sistema entra em suspensão, ele preserva automaticamente o estado do sistema inteiro e de todos os aplicativos. Portanto, a maioria dos aplicativos não precisa executar nenhuma ação especial. Os aplicativos que precisam executar ações específicas antes que as transições do sistema possam se registrar para eventos de energia.

Quando o sistema envia um evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) , cada aplicativo tem dois segundos para executar as ações necessárias antes que o sistema inicie a transição para Sleep. Os aplicativos devem limitar a ação que eles levam em resposta a esse evento para garantir que eles concluam todas as operações no tempo alocado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o gerenciamento de energia](about-power-management.md)
</dt> <dt>

[Eventos de ativação do sistema](system-wake-up-events.md)
</dt> </dl>

 

 



