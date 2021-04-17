---
description: A natureza interativa de telefonia exige que a TAPI seja um ambiente operacional em tempo real.
ms.assetid: b8512588-ec28-4fbe-b47f-b900e2dba1f2
title: Modelo síncrono/assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b3d3b58e9704719e502fa3efc11bc4dc216479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813049"
---
# <a name="synchronousasynchronous-model"></a>Modelo síncrono/assíncrono

A natureza interativa de telefonia exige que a TAPI seja um ambiente operacional em tempo real. Muitas das funções TAPI precisam ser concluídas rapidamente e retornar seus resultados para o aplicativo de forma síncrona. Outras funções (como discagem) podem não ser capazes de concluir tão rapidamente e, portanto, operar de forma assíncrona.

As operações de telefonia são concluídas de forma síncrona ou assíncrona. Esses dois modelos diferem da seguinte maneira. As *funções síncronas* executam toda a solicitação antes que o thread do chamador tenha permissão para retornar da chamada de função. As *funções assíncronas* retornam antes que a solicitação seja executada em sua totalidade. Quando a solicitação assíncrona for concluída mais tarde, o provedor de serviços relatará a conclusão chamando um procedimento de retorno de chamada que a TAPI forneceu originalmente a ela no início da sequência de inicialização.

-   Operações assíncronas têm um parâmetro chamado *dwRequestID* do tipo definido [drv \_ REQUESTID](./drv-requestid.md) como seu primeiro parâmetro. Tal operação executa parte de seu processamento na chamada de função e o restante de seu processamento em um thread de execução independente depois que a chamada de função é retornada. Quando a função retorna, ela retorna um resultado de erro negativo ou o *dwRequestID* (positivo) que foi passado na chamada de função. O resultado de erro negativo indica que a operação está concluída (e falhou). O *dwRequestID* positivo retornado indica que a operação continua no thread independente. Nesse caso, o provedor de serviço eventualmente chama o procedimento [**de \_ conclusão assíncrona**](/windows/win32/api/tspi/nc-tspi-async_completion) , passando o *dwRequestID* e um código de resultado para indicar o resultado da operação. O código de resultado é zero para êxito ou um do mesmo conjunto de resultados de erro (negativo). De qualquer forma, o provedor de serviços nunca deve retornar zero ou qualquer valor positivo diferente de *dwRequestID* de uma função designada como assíncrona porque fazer isso pode produzir resultados inesperados. Os provedores de serviço sempre devem copiar dados de entrada da memória do aplicativo para a memória do provedor de serviços antes de retornar de uma função assíncrona.
-   As operações síncronas não têm *dwRequestID* como seu primeiro parâmetro. Tal operação executa todo o seu processamento no thread de execução do chamador, retornando o resultado final quando ele retorna. O resultado é zero para êxito ou um código de erro negativo para falha. O provedor de serviços não chama [**a \_ conclusão assíncrona**](/windows/win32/api/tspi/nc-tspi-async_completion) para operações síncronas.

É interessante considerar o tempo de um retorno de chamada de "conclusão" relativo ao quando a solicitação original retorna. Uma solicitação assíncrona típica seria implementada pelo provedor de serviços como no seguinte pseudocódigo:

``` syntax
Some_request(Request_ID, ...) {
  check parameters for validity
  check device state for validity
  store Request_ID for Completion Interrupt Handler's use
  manipulate device registers to start physical operation
  return Request_ID  // to indicate asynch operation
}
Operation Completion Interrupt Handler: {
  if operation was successful then
    call "completion" callback passing Request_ID and "success"
  else
    call "completion" callback passing Request_ID and "error num"
  endif
}
```

Se a operação for concluída muito rapidamente (ou a solicitação original retornar muito lentamente), é possível que o manipulador de interrupção que é executado quando uma operação física é concluída possa ser disparado antes que a solicitação original retorne ao aplicativo ou mesmo à TAPI. Esse comportamento é permitido. A TAPI garante que a notificação eventual de conclusão para o aplicativo seja entregue após o retorno da solicitação original.

**TAPI 2. x:** Lista o estado em que cada função é concluída de forma síncrona ou assíncrona aparece na [referência de função rápida TAPI](./tapi-quick-function-reference.md).

 

 
