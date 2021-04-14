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
# <a name="select-fd_set-and-fd_xxx-macros"></a><span data-ttu-id="fd630-103">Macros Select, FD \_ set e FD \_ xxx</span><span class="sxs-lookup"><span data-stu-id="fd630-103">Select, FD\_SET, and FD\_XXX Macros</span></span>

<span data-ttu-id="fd630-104">Como os soquetes não são representados pelo inteiro de estilo UNIX, pequeno, não negativo, a implementação da função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) foi alterada no Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="fd630-104">Since sockets are not represented by the UNIX-style, small, non-negative integer, the implementation of the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) function was changed in Windows Sockets.</span></span> <span data-ttu-id="fd630-105">Cada conjunto de soquetes ainda é representado pela estrutura do **\_ conjunto FD** , mas em vez de ser armazenado como uma bitmask, o conjunto é implementado como uma matriz de soquetes.</span><span class="sxs-lookup"><span data-stu-id="fd630-105">Each set of sockets is still represented by the **FD\_SET** structure, but instead of being stored as a bitmask, the set is implemented as an array of sockets.</span></span> <span data-ttu-id="fd630-106">Para evitar possíveis problemas, os aplicativos devem aderir ao uso das \_ macros do FD xxx para definir, inicializar, limpar e verificar as estruturas [**do \_ conjunto de fd**](/windows/desktop/api/winsock/nf-winsock-fd_set) .</span><span class="sxs-lookup"><span data-stu-id="fd630-106">To avoid potential problems, applications must adhere to the use of the FD\_XXX macros to set, initialize, clear, and check the [**FD\_SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) structures.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd630-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd630-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd630-108">Portando aplicativos de soquete para Winsock</span><span class="sxs-lookup"><span data-stu-id="fd630-108">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="fd630-109">Considerações sobre programação do Winsock</span><span class="sxs-lookup"><span data-stu-id="fd630-109">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



