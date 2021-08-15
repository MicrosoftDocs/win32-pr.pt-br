---
title: Códigos de erro em COM
description: Códigos de erro em COM
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dd61208c9ae825999ec0dec024a8cc492b81cae426b1cc4143d694034204d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388284"
---
# <a name="error-codes-in-com"></a>Códigos de erro em COM

Para indicar êxito ou falha, os métodos e funções COM retornam um valor do tipo **HRESULT.** Um **HRESULT** é um inteiro de 32 bits. O bit de ordem alta do **HRESULT** sinaliza êxito ou falha. Zero (0) indica êxito e 1 indica falha.

Isso produz os seguintes intervalos numéricos:

-   Códigos de êxito: 0x0-0x7FFFFFFF.
-   Códigos de erro: 0x80000000-0xFFFFFFFF.

Um pequeno número de métodos COM não retornam um **valor HRESULT.** Por exemplo, os [**métodos AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) retornam valores longos não assinados. Mas cada método COM que retorna um código de erro faz isso retornando um **valor HRESULT.**

Para verificar se um método COM é bem-sucedido, examine o bit de ordem alta do **HRESULT retornado.** Os Windows do SDK fornecem duas macros que facilitam isso: a macro [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) e a macro [**FAILED.**](/windows/desktop/api/winerror/nf-winerror-failed) A **macro SUCCEEDED** **retornará TRUE se** um **HRESULT** for um código de êxito e **FALSE** se for um código de erro. O exemplo a seguir verifica se [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) é bem-sucedido.


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    // The function succeeded.
}
else
{
    // Handle the error.
}
```



Às vezes, é mais conveniente testar a condição inversa. A [**macro FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) faz o oposto de [**SUCCEEDED.**](/windows/desktop/api/winerror/nf-winerror-succeeded) Ele retorna **TRUE para** um código de erro e **FALSE** para um código de êxito.


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (FAILED(hr))
{
    // Handle the error.
}
else
{
    // The function succeeded.
}
```



Mais adiante neste módulo, vamos dar uma olhada em alguns conselhos práticos sobre como estruturar seu código para lidar com erros COM. (Consulte [Tratamento de erros em COM](error-handling-in-com.md).)

## <a name="next"></a>Avançar

[Criando um objeto em COM](creating-an-object-in-com.md)

 

 
