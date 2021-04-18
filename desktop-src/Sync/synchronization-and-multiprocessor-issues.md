---
description: Os aplicativos podem encontrar problemas quando executados em sistemas de multiprocessadores devido a suposições que eles fazem são válidos somente em sistemas de processador único.
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: Sincronização e problemas de multiprocessador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3896dc240e76f1506bac2a6a2e95f101b05beca7
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/21/2021
ms.locfileid: "105755536"
---
# <a name="synchronization-and-multiprocessor-issues"></a>Sincronização e problemas de multiprocessador

Os aplicativos podem encontrar problemas quando executados em sistemas de multiprocessadores devido a suposições que eles fazem são válidos somente em sistemas de processador único.

## <a name="thread-priorities"></a>Prioridades do thread

Considere um programa com dois threads, um com prioridade mais alta do que o outro. Em um sistema de processador único, o thread de prioridade mais alta não cederá o controle ao thread de prioridade mais baixa, pois o Agendador dá preferência a threads de prioridade mais alta. Em um sistema multiprocessador, ambos os threads podem ser executados simultaneamente, cada um em seu próprio processador.

Os aplicativos devem sincronizar o acesso a estruturas de dados para evitar condições de corrida. O código que pressupõe que threads de prioridade mais alta sejam executados sem interferência de threads de prioridade inferior falhará em sistemas de multiprocessadores.

## <a name="memory-ordering"></a>Ordenação de memória

Quando um processador grava em um local de memória, o valor é armazenado em cache para melhorar o desempenho. Da mesma forma, o processador tenta atender às solicitações de leitura do cache para melhorar o desempenho. Além disso, os processadores começam a buscar valores da memória antes de serem solicitados pelo aplicativo. Isso pode acontecer como parte da execução especulativa ou devido a problemas de linha de cache.

Os caches de CPU podem ser particionados em bancos que podem ser acessados em paralelo. Isso significa que as operações de memória podem ser concluídas fora de ordem. Para garantir que as operações de memória sejam concluídas na ordem, a maioria dos processadores fornece instruções de barreira de memória. Uma *barreira de memória total* garante que as operações de leitura e gravação de memória que aparecem antes da instrução de barreira de memória sejam confirmadas na memória antes de qualquer operação de leitura e gravação de memória que apareça após a instrução de barreira de memória. Uma *barreira de leitura de memória* solicita apenas as operações de leitura de memória e uma *barreira de memória de gravação* solicita apenas as operações de gravação de memória. Essas instruções também garantem que o compilador desabilite as otimizações que poderiam reordenar as operações de memória entre as barreiras.

Os processadores podem dar suporte a instruções para barreiras de memória com semântica de aquisição, liberação e isolamento. Essas semânticas descrevem a ordem na qual os resultados de uma operação são disponibilizados. Com a semântica de aquisição, os resultados da operação estão disponíveis antes dos resultados de qualquer operação que aparece depois dele no código. Com a semântica de versão, os resultados da operação estão disponíveis após os resultados de qualquer operação que aparece antes dele no código. A semântica de isolamento combina a semântica de aquisição e liberação. Os resultados de uma operação com semântica de cerca estão disponíveis antes das de qualquer operação que aparece depois dele no código e após as de qualquer operação que aparece antes dela.

Em processadores x86 e x64 que dão suporte a SSE2, as instruções são **mfence** (limite de memória), **lfence** (limite de carga) e **sfence** (limite de armazenamento). Em processadores ARM, as instruts são **DMB** e **DSB**. Para obter mais informações, consulte a documentação do processador.

As seguintes funções de sincronização usam as barreiras apropriadas para garantir a ordenação de memória:

-   Funções que inserem ou deixam seções críticas
-   Funções que adquirem ou liberam bloqueios de SRW
-   Início e conclusão de inicialização única
-   Função **EnterSynchronizationBarrier**
-   Funções que sinalizam objetos de sincronização
-   Funções de espera
-   Funções interbloqueadas (exceto funções com sufixo _nolimite_ ou intrínsecos com sufixo de _\_ NF_ )

## <a name="fixing-a-race-condition"></a>Corrigindo uma condição de corrida

O código a seguir tem uma condição de corrida em sistemas de multiprocessadores porque o processador que é executado `CacheComputedValue` pela primeira vez pode gravar na `fValueHasBeenComputed` memória principal antes `iValue` de gravar na memória principal. Consequentemente, um segundo processador `FetchComputedValue` em execução ao mesmo tempo `fValueHasBeenComputed` é lido como **verdadeiro**, mas o novo valor de `iValue` ainda está no cache do primeiro processador e não foi gravado na memória.

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

Essa condição de corrida acima pode ser reparada usando a palavra-chave **volatile** ou a função [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) para garantir que o valor de `iValue` seja atualizado para todos os processadores antes que o valor de `fValueHasBeenComputed` seja definido como **true**.

Iniciando o Visual Studio 2005, se compilado em **/volatile: MS** Mode, o compilador usa a semântica de aquisição para operações de leitura em variáveis **voláteis** e semântica de liberação para operações de gravação em variáveis **voláteis** (quando há suporte pela CPU). Portanto, você pode corrigir o exemplo da seguinte maneira:

``` syntax
volatile int iValue;
volatile BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

Com o Visual Studio 2003, as referências **voláteis** a **volátil** são ordenadas; o compilador não solicitará o acesso à variável **volátil** novamente. No entanto, essas operações podem ser reordenadas pelo processador. Portanto, você pode corrigir o exemplo da seguinte maneira:

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          FALSE, FALSE)==FALSE) 
  {
    InterlockedExchange ((LONG*)&iValue, (LONG)ComputeValue());
    InterlockedExchange ((LONG*)&fValueHasBeenComputed, TRUE);
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          TRUE, TRUE)==TRUE) 
  {
    InterlockedExchange((LONG*)piResult, (LONG)iValue);
    return TRUE;
  } 

  else return FALSE;
}
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de seção crítica](critical-section-objects.md)
</dt> <dt>

[Acesso de variável interbloqueada](interlocked-variable-access.md)
</dt> <dt>

[Funções de espera](wait-functions.md)
</dt> </dl>

 

 



