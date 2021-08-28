---
description: As \_ \_ palavras-chave try \_ \_ e except são usadas para construir um manipulador de exceção baseado em quadro. O exemplo a seguir mostra a estrutura de um manipulador de exceção.
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Sintaxe Exception-Handler dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd24b3ffc84a3469c7c8d97ce505a0292ee538ea8f0b9c1d604bf34f65203ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912736"
---
# <a name="exception-handler-syntax"></a>Sintaxe Exception-Handler dados

As **\_ \_ palavras-chave try** **\_ \_ e except** são usadas para construir um manipulador de exceção baseado em quadro. O exemplo a seguir mostra a estrutura de um manipulador de exceção.


```C++
__try 
{
    // guarded body of code 
 
} 
__except (filter-expression) 
{ 
    // exception-handler block 
 
}
```



Observe que o **\_ \_ bloco try** e o bloco do manipulador de exceção exigem chaves ( {} ). Não é permitido usar uma instrução **goto** para ir para o corpo de um bloco **\_ \_ try** ou para um bloco de manipulador de exceção. Essa regra se aplica a manipuladores de exceção e manipuladores de encerramento.

O **\_ \_ bloco try** contém o corpo protegido do código que o manipulador de exceção protege. Uma função pode ter qualquer número de manipuladores de exceção, e essas instruções de tratamento de exceção podem ser aninhadas dentro da mesma função ou em funções diferentes. Se ocorrer uma exceção dentro do **\_ \_ bloco try,** o sistema terá controle e iniciará a pesquisa por um manipulador de exceção. Para ver uma descrição detalhada dessa pesquisa, consulte Tratamento [de exceções.](exception-handling.md)

O manipulador de exceção recebe apenas exceções que ocorrem em um único thread. Isso significa que, se um bloco **\_ \_ try** contiver uma chamada para a função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ou [**CreateThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) as exceções que ocorrem dentro do novo processo ou thread não serão expedidas para esse manipulador.

O sistema avalia a expressão de filtro de cada manipulador de exceção que está protegido pelo código no qual a exceção ocorreu até que a exceção seja tratada ou não haja mais manipuladores. Uma expressão de filtro deve ser avaliada como um dos três valores a seguir.



| Valor                              | Significado                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MANIPULADOR DE \_ EXECUÇÃO DE \_ EXCEÇÃO**    | O sistema transfere o controle para o manipulador de exceção e a execução continua no quadro de pilha no qual o manipulador é encontrado.                                                                                       |
| **PESQUISA DE \_ \_ CONTINUAÇÃO DE EXCEÇÃO**    | O sistema continua a procurar um manipulador.                                                                                                                                                                          |
| **EXCEÇÃO \_ CONTINUAR \_ EXECUÇÃO** | O sistema interrompe sua pesquisa por um manipulador e retorna o controle para o ponto em que a exceção ocorreu. Se a exceção não forcontinuável, isso resulta em uma **exceção EXCEPTION \_ NONCONTINUABLE \_ EXCEPTION.** |



 

A expressão de filtro é avaliada no contexto da função na qual o manipulador de exceção está localizado, mesmo que a exceção possa ter ocorrido em uma função diferente. Isso significa que a expressão de filtro pode acessar as variáveis locais da função. Da mesma forma, o bloco do manipulador de exceção pode acessar as variáveis locais da função na qual ele está localizado.

Para obter mais exemplos, consulte [Usando um manipulador de exceção](using-an-exception-handler.md).

Para obter mais informações sobre expressões de filtro e funções de filtro, consulte [Tratamento de exceção baseado em quadro.](frame-based-exception-handling.md)

 

 
