---
description: A função MyHandleError é um exemplo de uma função de ferramenta usada para imprimir uma mensagem de erro e sair do programa de chamada.
ms.assetid: 7b28509f-a77f-4b60-90d4-18edaa6d1a2d
title: MyHandleError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 047c9642a1b19c2af4a6e5ef2134ca305c472c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753219"
---
# <a name="myhandleerror"></a>MyHandleError

A função **MyHandleError** é um exemplo de uma função de ferramenta usada para imprimir uma mensagem de erro e sair do programa de chamada. Os exemplos de várias funções de CryptoAPI na [referência de criptografia](cryptography-reference.md) e os exemplos mais estendidos no uso da [criptografia](using-cryptography.md) implementam essa função. Aplicativos reais podem exigir um recurso de tratamento de erros mais complexo.


```C++
#include <stdio.h>
#include <tchar.h>
#include <windows.h>

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError

```



 

 



