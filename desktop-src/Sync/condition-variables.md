---
description: Variáveis de condição são primitivos de sincronização que permitem que os threads aguardem até que ocorra uma determinada condição. Variáveis de condição são objetos de modo de usuário que não podem ser compartilhados entre processos.
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: Variáveis de condição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711fad7d80c1c5e06fc6e496198cd298b190daba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754484"
---
# <a name="condition-variables"></a>Variáveis de condição

Variáveis de condição são primitivos de sincronização que permitem que os threads aguardem até que ocorra uma determinada condição. Variáveis de condição são objetos de modo de usuário que não podem ser compartilhados entre processos.

Variáveis de condição habilitam threads para liberar atomicamente um bloqueio e entrar no estado de suspensão. Eles podem ser usados com seções críticas ou bloqueios de SRW (leitor/gravador) reduzidos. Variáveis de condição dão suporte a operações que "Wake One" ou "Wake All" aguardam threads. Depois que um thread é ativadosdo, ele adquire novamente o bloqueio liberado quando o thread entrou no estado de suspensão.

Observe que o chamador deve alocar uma estrutura de **\_ variável de condição** e inicializá-la chamando [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (para inicializar a estrutura dinamicamente) ou atribuir a variável de **condição constante \_ \_ init** à variável de estrutura (para inicializar a estrutura estaticamente).

**Windows Server 2003 e Windows XP:** Não há suporte para variáveis de condição.

A seguir estão as funções de variável de condição.



| Função de variável de condição                                        | Descrição                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | Inicializa uma variável de condição.                                                                              |
| [**SleepConditionVariableCS**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | Dorme na variável de condição especificada e libera a seção crítica especificada como uma operação atômica. |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | Dorme na variável de condição especificada e libera o bloqueio de SRW especificado como uma operação atômica.         |
| [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | Ativa todos os threads aguardando a variável de condição especificada.                                                 |
| [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | Ativa um único thread Aguardando a variável de condição especificada.                                             |



 

O pseudocódigo a seguir demonstra o padrão de uso típico de variáveis de condição.

``` syntax
CRITICAL_SECTION CritSection;
CONDITION_VARIABLE ConditionVar;

void PerformOperationOnSharedData()
{ 
   EnterCriticalSection(&CritSection);

   // Wait until the predicate is TRUE

   while( TestPredicate() == FALSE )
   {
      SleepConditionVariableCS(&ConditionVar, &CritSection, INFINITE);
   }

   // The data can be changed safely because we own the critical 
   // section and the predicate is TRUE

   ChangeSharedData();

   LeaveCriticalSection(&CritSection);

   // If necessary, signal the condition variable by calling
   // WakeConditionVariable or WakeAllConditionVariable so other
   // threads can wake
}
```

Por exemplo, em uma implementação de um bloqueio de leitor/gravador, a `TestPredicate` função verificaria se a solicitação de bloqueio atual é compatível com os proprietários existentes. Se for, adquira o bloqueio; caso contrário, Sleep. Para obter um exemplo mais detalhado, consulte [usando variáveis de condição](using-condition-variables.md).

Variáveis de condição estão sujeitas a ativações falsas (aquelas não associadas a uma ativação explícita) e ativaçãos roubadas (outro thread gerencia a execução antes do thread ativados). Portanto, você deve verificar novamente um predicado (normalmente em um loop **while** ) depois que uma operação de suspensão retorna.

Você pode ativar outros threads usando [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) ou [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) dentro ou fora do bloqueio associado à variável de condição. Geralmente, é melhor liberar o bloqueio antes de ativar outros threads para reduzir o número de alternâncias de contexto.

Geralmente, é conveniente usar mais de uma variável de condição com o mesmo bloqueio. Por exemplo, uma implementação de um bloqueio de leitor/gravador pode usar uma única seção crítica, mas variáveis de condição separadas para leitores e gravadores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando variáveis de condição](using-condition-variables.md)
</dt> </dl>

 

 
