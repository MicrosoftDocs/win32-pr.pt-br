---
description: Como os soquetes não são representados pelo inteiro de estilo UNIX, pequeno, não negativo, a implementação da função Select foi alterada no Windows Sockets.
ms.assetid: 97c7996c-c541-4673-b26f-d66f3fc0b62e
title: Macros Select, FD_SET e FD_XXX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9bce15e921bf6566717a30114af73530406e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505719"
---
# <a name="select-fd_set-and-fd_xxx-macros"></a>Macros Select, FD \_ set e FD \_ xxx

Como os soquetes não são representados pelo inteiro de estilo UNIX, pequeno, não negativo, a implementação da função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) foi alterada no Windows Sockets. Cada conjunto de soquetes ainda é representado pela estrutura do **\_ conjunto FD** , mas em vez de ser armazenado como uma bitmask, o conjunto é implementado como uma matriz de soquetes. Para evitar possíveis problemas, os aplicativos devem aderir ao uso das \_ macros do FD xxx para definir, inicializar, limpar e verificar as estruturas [**do \_ conjunto de fd**](/windows/desktop/api/winsock/nf-winsock-fd_set) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Portando aplicativos de soquete para Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerações sobre programação do Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



