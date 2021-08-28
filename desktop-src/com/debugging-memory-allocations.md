---
title: Depurando alocações de memória
description: Depurando alocações de memória
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b3376b2ffee17ce747197eb57fecbdae18e086d5252dd5f4721975181885
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993446"
---
# <a name="debugging-memory-allocations"></a>Depurando alocações de memória

O COM fornece a interface [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) para os desenvolvedores usarem para depurar suas alocações de memória. Para cada método em [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc), há dois métodos em **IMallocSpy**, um método "pre" e um método "post". Depois que um desenvolvedor o implementa e o publica no sistema, o sistema chama o método **"pre" do IMallocSpy** logo antes do método **IMalloc** correspondente, permitindo efetivamente que o código de depuração "espiar" na operação de alocação e chama o método "post" para liberar o spy.

Por exemplo, quando COM detecta que a próxima chamada é uma chamada para [**IMalloc::Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), ele chama [**IMallocSpy::P reAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), executando as  operações de depuração que o desenvolvedor deseja durante a execução de Alloc e, em seguida, quando a chamada **Alloc** retorna, chama [**IMallocSpy::P ostAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) para liberar o spy e retornar o controle para o código.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando alocação de memória](managing-memory-allocation.md)
</dt> </dl>

 

 