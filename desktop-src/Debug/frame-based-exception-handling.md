---
description: Um manipulador de exceção baseado em quadros permite que você lide com a possibilidade de que uma exceção ocorra em uma determinada sequência de código. Um manipulador de exceção baseado em quadros consiste nos seguintes elementos.
ms.assetid: 07aac772-f917-48b7-91a9-3b5d4cb43600
title: Manipulação de exceção baseada em quadros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb72118aca7653e9bc15e7f4ff4b75e46b1abad5bab7dee4a3397ae5f98e1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573116"
---
# <a name="frame-based-exception-handling"></a>Manipulação de exceção baseada em quadros

Um *manipulador de exceção baseado em quadros* permite que você lide com a possibilidade de que uma exceção ocorra em uma determinada sequência de código. Um manipulador de exceção baseado em quadros consiste nos seguintes elementos.

-   Um corpo de código protegido
-   Uma expressão de filtro
-   Um bloco de manipulador de exceção

Os manipuladores de exceção baseados em quadros são declarados na sintaxe específica do idioma. Por exemplo, no compilador de otimização do Microsoft C/C++, eles são implementados usando **\_ \_ try** e **\_ \_ Except**. Para obter mais informações, consulte [sintaxe do manipulador](handler-syntax.md).

O *corpo de código protegido* é um conjunto de uma ou mais instruções para as quais a expressão de filtro e o bloco de manipulador de exceção fornecem proteção de manipulação de exceção. O corpo protegido pode ser um bloco de código, um conjunto de blocos aninhados ou um procedimento ou uma função inteira. Usando o compilador de otimização do Microsoft C/C++, um corpo protegido é incluído entre chaves ( {} ) após a palavra-chave **\_ \_ try** .

A *expressão de filtro* de um manipulador de exceção com base em quadros é uma expressão que é avaliada pelo sistema quando ocorre uma exceção dentro do corpo protegido. Essa avaliação resulta em uma das seguintes ações pelo sistema.

-   O sistema interrompe sua pesquisa por um manipulador de exceção, restaura o estado da máquina e continua a execução do thread no ponto em que a exceção ocorreu.
-   O sistema continua sua pesquisa por um manipulador de exceção.
-   O sistema transfere o controle para o manipulador de exceção e a execução do thread continua sequencialmente no registro de ativação no qual o manipulador de exceção é encontrado. Se o manipulador não estiver no registro de ativação no qual a exceção ocorreu, o sistema desenrolará a pilha, deixando o registro de ativação atual e quaisquer outros quadros de pilha até que ele volte ao quadro de pilha do manipulador de exceções. Antes de um manipulador de exceção ser executado, os manipuladores de terminação são executados para qualquer corpo de código protegido que foi encerrado como resultado da transferência de controle para o manipulador de exceção. Para obter mais informações sobre manipuladores de terminação, consulte [tratamento de terminação](termination-handling.md).

A expressão de filtro pode ser uma expressão simples ou pode invocar uma *função de filtro* que tenta manipular a exceção. Você pode chamar as funções [**GetExceptionCode**](getexceptioncode.md) e [**GetExceptionInformation**](getexceptioninformation.md) de dentro de uma expressão de filtro para obter informações sobre a exceção que está sendo filtrada. **GetExceptionCode** retorna um código que identifica o tipo de exceção e **GetExceptionInformation** retorna um ponteiro para uma estrutura [**de \_ ponteiros de exceção**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) que contém ponteiros para estruturas de [**\_ registro**](/windows/desktop/api/WinNT/ns-winnt-exception_record) de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) e de exceção.

Essas funções não podem ser chamadas de dentro de uma função de filtro, mas seus valores de retorno podem ser passados como parâmetros para uma função de filtro. [**GetExceptionCode**](getexceptioncode.md) pode ser usado dentro do bloco de manipulador de exceção, mas [**GetExceptionInformation**](getexceptioninformation.md) não pode porque as informações para as quais ele aponta estão normalmente na pilha e são destruídas quando o controle é transferido para um manipulador de exceção. No entanto, um aplicativo pode copiar as informações para o armazenamento seguro para torná-lo disponível para o manipulador de exceção.

A vantagem de uma função de filtro é que ela pode manipular uma exceção e retornar um valor que faz com que o sistema continue a execução a partir do ponto em que a exceção ocorreu. Com um bloco de manipulador de exceção, por outro lado, a execução continua sequencialmente do manipulador de exceção em vez do ponto da exceção.

Manipular uma exceção pode ser tão simples quanto observar um erro e definir um sinalizador que será examinado posteriormente, imprimindo uma mensagem de aviso ou de erro ou tomando alguma outra ação limitada. Se a execução puder ser continuada, também poderá ser necessário alterar o estado da máquina modificando o registro de contexto. Para obter um exemplo de uma função de filtro que manipula uma exceção de falha de página, consulte [usando as funções de memória virtual](../memory/using-the-memory-management-functions.md).

A função [**UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) pode ser usada como uma função de filtro em uma expressão de filtro. Ele retorna \_ \_ o manipulador de execução de exceção, a menos que o processo esteja sendo depurado; nesse caso, ele retorna uma exceção de \_ continuação da \_ pesquisa.

 

 
