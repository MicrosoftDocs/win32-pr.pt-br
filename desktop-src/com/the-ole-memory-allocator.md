---
title: O alocador de memória OLE
description: O alocador de memória OLE
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64fedd610fd8fd6dab0bcd14deb37e04f6df74d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084922"
---
# <a name="the-ole-memory-allocator"></a>O alocador de memória OLE

A biblioteca COM fornece uma implementação de um alocador de memória que é thread-safe. (Ou seja, isso não pode causar problemas em situações multi-threaded). Sempre que a propriedade de um bloco alocado de memória é passada por meio de uma interface COM ou entre um cliente e a biblioteca COM, você deve usar esse alocador de COM para alocar a memória. A alocação interna a um objeto pode usar qualquer esquema de alocação desejado, mas o alocador de memória COM é um alocador útil, eficiente e seguro para thread.

Uma chamada para a função de API [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) fornece um ponteiro para o alocador OLE, que é uma implementação da interface [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) . No entanto, é mais eficiente chamar as funções auxiliares [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)e [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), que encapsulam a obtenção de um ponteiro para o alocador de memória da tarefa, chamando o método **IMalloc** correspondente e, em seguida, liberando o ponteiro para o alocador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando a alocação de memória](managing-memory-allocation.md)
</dt> <dt>

[A biblioteca COM](the-com-library.md)
</dt> </dl>

 

 