---
title: Códigos de erro em COM
description: Códigos de erro em COM
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733cbe0799a22b0f0c01ee9cb226ad7e0b8660da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103954"
---
# <a name="error-codes-in-com"></a>Códigos de erro em COM

Para indicar êxito ou falha, métodos COM e funções retornam um valor do tipo **HRESULT**. Um **HRESULT** é um inteiro de 32 bits. O bit de ordem superior do **HRESULT** sinaliza êxito ou falha. Zero (0) indica êxito e 1 indica falha.

Isso produz os seguintes intervalos numéricos:

-   Códigos de êxito: 0x0 – 0x7FFFFFFF.
-   Códigos de erro: 0x80000000 – 0xFFFFFFFF.

Um pequeno número de métodos COM não retorna um valor **HRESULT** . Por exemplo, os métodos [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) retornam valores longos não assinados. Mas cada método COM que retorna um código de erro faz isso retornando um valor **HRESULT** .

Para verificar se um método COM é executado COM sucesso, examine o bit de ordem superior do **HRESULT** retornado. Os cabeçalhos de SDK do Windows fornecem duas macros que tornam isso mais fácil: a macro com [**êxito**](/windows/desktop/api/winerror/nf-winerror-succeeded) e a macro [**com falha**](/windows/desktop/api/winerror/nf-winerror-failed) . A macro **Succeeded** retornará **true** se um **HRESULT** for um código de êxito e **false** se for um código de erro. O exemplo a seguir verifica se [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) tem sucesso.


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



Às vezes, é mais conveniente testar a condição inversa. A macro [**com falha**](/windows/desktop/api/winerror/nf-winerror-failed) faz o oposto do [**êxito**](/windows/desktop/api/winerror/nf-winerror-succeeded). Retorna **true** para um código de erro e **false** para um código de êxito.


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



Mais adiante neste módulo, veremos alguns conselhos práticos sobre como estruturar seu código para manipular erros COM. (Consulte [tratamento de erros no com](error-handling-in-com.md).)

## <a name="next"></a>Avançar

[Criando um objeto em COM](creating-an-object-in-com.md)

 

 
