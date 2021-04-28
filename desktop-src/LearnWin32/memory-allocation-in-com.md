---
title: Alocação de memória em COM
description: Alocação de memória em COM
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cb9913da55fab82f699ac05dae3998f7582224
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103884"
---
# <a name="memory-allocation-in-com"></a>Alocação de memória em COM

Às vezes, um método aloca um buffer de memória no heap e retorna o endereço do buffer para o chamador. COM define um par de funções para alocar e liberar memória no heap.

-   A função [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) aloca um bloco de memória.
-   A função [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) libera um bloco de memória que foi alocado com [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).

Vimos um exemplo desse padrão no [exemplo de caixa de diálogo abrir](example--the-open-dialog-box.md):


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



O método [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) aloca memória para uma cadeia de caracteres. Internamente, o método chama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para alocar a cadeia de caracteres. Quando o método retorna, *pszFilePath* aponta para o local da memória do novo buffer. O chamador é responsável por chamar [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória.

Por que o COM define suas próprias funções de alocação de memória? Um motivo é fornecer uma camada de abstração sobre o alocador de heap. Caso contrário, alguns métodos poderão chamar **malloc** enquanto outros chamarem **New**. Em seguida, seu programa precisaria chamar **gratuitamente** em alguns casos e **excluir** em outros, e manter o controle da ti tudo rapidamente se tornaria impossível. As funções de alocação COM criam uma abordagem uniforme.

Outra consideração é o fato de que COM é um padrão *binário* , portanto, ele não está vinculado a uma linguagem de programação específica. Portanto, o COM não pode contar com qualquer forma específica de linguagem de alocação de memória.

## <a name="next"></a>Avançar

[Práticas de codificação COM](com-coding-practices.md)

 

 
