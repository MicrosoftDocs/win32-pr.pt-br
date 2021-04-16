---
description: As \_ \_ \_ \_ palavras-chave try e Except são usadas para construir um manipulador de exceção baseado em quadros. O exemplo a seguir mostra a estrutura de um manipulador de exceção.
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Sintaxe de Exception-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eff9e6ca5d16a71b416f79a09f46795592a696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500756"
---
# <a name="exception-handler-syntax"></a>Sintaxe de Exception-Handler

As palavras-chave **\_ \_ try** e **\_ \_ Except** são usadas para construir um manipulador de exceção baseado em quadros. O exemplo a seguir mostra a estrutura de um manipulador de exceção.


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



Observe que o bloco **\_ \_ try** e o bloco de manipulador de exceção exigem chaves ( {} ). Não é permitido usar uma instrução **goto** para saltar no corpo de um bloco **\_ \_ try** ou em um bloco de manipulador de exceção. Essa regra se aplica a manipuladores de exceção e manipuladores de terminação.

O bloco **\_ \_ try** contém o corpo protegido de código que o manipulador de exceção protege. Uma função pode ter qualquer número de manipuladores de exceção, e essas instruções de tratamento de exceções podem ser aninhadas dentro da mesma função ou em funções diferentes. Se ocorrer uma exceção dentro do bloco **\_ \_ try** , o sistema usará o controle e iniciará a pesquisa de um manipulador de exceção. Para obter uma descrição detalhada dessa pesquisa, consulte [manipulação de exceção](exception-handling.md).

O manipulador de exceção recebe apenas exceções que ocorrem em um único thread. Isso significa que, se um bloco **\_ \_ try** contiver uma chamada para a função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ou [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) , as exceções que ocorrerem no novo processo ou thread não serão expedidas para esse manipulador.

O sistema avalia a expressão de filtro de cada manipulador de exceção, protegendo o código no qual a exceção ocorreu até que a exceção seja tratada ou não haja mais manipuladores. Uma expressão de filtro deve ser avaliada como um dos três valores a seguir.



| Valor                              | Significado                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_manipulador de execução de exceção \_**    | O sistema transfere o controle para o manipulador de exceção e a execução continua no registro de ativação no qual o manipulador é encontrado.                                                                                       |
| **EXCEÇÃO de \_ continuação da \_ pesquisa**    | O sistema continua a procurar um manipulador.                                                                                                                                                                          |
| **EXCEÇÃO de \_ continuação de \_ execução** | O sistema interrompe a pesquisa de um manipulador e retorna o controle para o ponto em que a exceção ocorreu. Se a exceção for não continuável, isso resultará em uma exceção de exceção de **\_ \_ não continuável de exceção** . |



 

A expressão de filtro é avaliada no contexto da função na qual o manipulador de exceção está localizado, embora a exceção tenha ocorrido em uma função diferente. Isso significa que a expressão de filtro pode acessar as variáveis locais da função. Da mesma forma, o bloco do manipulador de exceção pode acessar as variáveis locais da função na qual ela está localizada.

Para obter mais exemplos, consulte [usando um manipulador de exceção](using-an-exception-handler.md).

Para obter mais informações sobre expressões de filtro e funções de filtro, consulte [manipulação de exceção baseada em quadros](frame-based-exception-handling.md).

 

 
