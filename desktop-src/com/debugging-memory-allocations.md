---
title: Depurando alocações de memória
description: Depurando alocações de memória
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb6a7dbe313cfe571fa6b4d244df35407fa331e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294523"
---
# <a name="debugging-memory-allocations"></a>Depurando alocações de memória

O COM fornece a interface [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) para que os desenvolvedores usem para depurar suas alocações de memória. Para cada método em [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc), há dois métodos no **IMallocSpy**, um método "pre" e um método "post". Depois que um desenvolvedor o implementa e o publica no sistema, o sistema chama o método "pre" do **IMallocSpy** logo antes do método **IMalloc** correspondente, permitindo efetivamente o código de depuração para "Spy" na operação de alocação e chama o método "post" para liberar o Spy.

Por exemplo, quando o COM detecta que a próxima chamada é uma chamada para [**IMalloc:: Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), ele [**chama IMallocSpy::P realloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), executando quaisquer operações de depuração que o desenvolvedor deseja durante a execução da **alocação** e, em seguida, quando a chamada de **alocação** retorna, chama [**IMallocSpy::P ostalloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) para liberar o Spy e retornar o controle para o código.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando a alocação de memória](managing-memory-allocation.md)
</dt> </dl>

 

 