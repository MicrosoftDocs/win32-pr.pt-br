---
description: As \_ \_ \_ \_ palavras-chave try e finally são usadas para construir um manipulador de terminação. O exemplo a seguir mostra a estrutura de um manipulador de encerramento.
ms.assetid: fbaf8890-2516-4b60-be57-464f91f2a38a
title: Sintaxe de Termination-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3a6322bbcf86f56a75c62eaba03d50827edcd71a57addf48ef3777c7687796
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984456"
---
# <a name="termination-handler-syntax"></a>Sintaxe de Termination-Handler

As palavras-chave **\_ \_ try** e **\_ \_ finally** são usadas para construir um manipulador de terminação. O exemplo a seguir mostra a estrutura de um manipulador de encerramento.


```C++
__try 
{ 
    // guarded body of code 
 
} 
__finally 
{ 
    // __finally block 
 
}
```



Para obter exemplos, consulte [usando um manipulador de encerramento](using-a-termination-handler.md).

Assim como ocorre com o manipulador de exceção, o bloco **\_ \_ try** e o bloco **\_ \_ finally** exigem chaves ( {} ) e o uso de uma instrução **goto** para saltar em um dos blocos não é permitido.

O bloco **\_ \_ try** contém o corpo protegido de código que é protegido pelo manipulador de encerramento. Uma função pode ter qualquer número de manipuladores de terminação e esses blocos de tratamento de terminação podem ser aninhados dentro da mesma função ou em funções diferentes.

O bloco **\_ \_ finally** é executado sempre que o fluxo de controle deixa o bloco **\_ \_ try** . No entanto, o bloco **\_ \_ finally** não será executado se você chamar qualquer uma das funções a seguir dentro do bloco **\_ \_ try** : [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)ou **Abort**.

O bloco **\_ \_ finally** é executado no contexto da função na qual o manipulador de terminação está localizado. Isso significa que o bloco **\_ \_ finally** pode acessar as variáveis locais da função. A execução do bloco **\_ \_ finally** pode terminar por qualquer um dos seguintes meios.

-   Execução da última instrução no bloco e continuação para a próxima instrução
-   Uso de uma instrução de controle (**Return**, **Break**, **continue** ou **goto**)
-   Uso de **longjmp** ou um salto para um manipulador de exceção

Se a execução do bloco **\_ \_ try** for encerrada devido a uma exceção que invoca o bloco de tratamento de exceção de um manipulador de exceção baseado em quadro, o bloco **\_ \_ finally** será executado antes que o bloco de tratamento de exceção seja executado. Da mesma forma, uma chamada para a função de biblioteca de tempo de execução **longjmp** C do bloco **\_ \_ try** causa a execução do bloco **\_ \_ finally** antes da execução ser retomada no destino da operação **longjmp** . Se a execução do bloco **\_ \_ try** for encerrada devido a uma instrução de controle (**Return**, **Break**, **continue** ou **goto**), o bloco **\_ \_ finally** será executado.

A função [**AbnormalTermination**](abnormaltermination.md) pode ser usada no bloco **\_ \_ finally** para determinar se o bloco **\_ \_ try** foi encerrado sequencialmente – ou seja, se ele atingiu a chave de fechamento (}). Deixar o bloco **\_ \_ try** devido a uma chamada para **longjmp**, um salto para um manipulador de exceção ou uma instrução **Return**, **Break**, **continue** ou **goto** , é considerado um encerramento anormal. Observe que a falha ao terminar sequencialmente faz com que o sistema Pesquise todos os quadros de pilha em ordem inversa para determinar se os manipuladores de encerramento devem ser chamados. Isso pode resultar em degradação do desempenho devido à execução de centenas de instruções.

Para evitar o encerramento anormal do manipulador de encerramento, a execução deve continuar no final do bloco. Você também pode executar a instrução **\_ \_ Leave** . A instrução **\_ \_ Leave** permite o encerramento imediato do bloco **\_ \_ try** sem causar um encerramento anormal e sua penalidade de desempenho. Verifique a documentação do compilador para determinar se a instrução **\_ \_ Leave** tem suporte.

Se a execução do bloco **\_ \_ finally** terminar devido à instrução de controle de **retorno** , será equivalente a **goto** para a chave de fechamento na função de circunscrição. Portanto, a função de circunscrição será retornada.

 

 
