---
title: Armazenamento persistente no servidor
description: Você pode otimizar seu aplicativo para que o stub do servidor não Libere memória no servidor na conclusão de uma chamada de procedimento remoto.
ms.assetid: 340334e2-94ac-4be2-a16d-38bc4c64e7db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7237fe6136918e5495ee1f22bac0991d71c5dbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916453"
---
# <a name="persistent-storage-on-the-server"></a><span data-ttu-id="8fc38-103">Armazenamento persistente no servidor</span><span class="sxs-lookup"><span data-stu-id="8fc38-103">Persistent Storage on the Server</span></span>

<span data-ttu-id="8fc38-104">Você pode otimizar seu aplicativo para que o stub do servidor não Libere memória no servidor na conclusão de uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="8fc38-104">You can optimize your application so the server stub does not free memory on the server at the conclusion of a remote procedure call.</span></span> <span data-ttu-id="8fc38-105">Por exemplo, quando um identificador de contexto será manipulado por vários procedimentos remotos, você poderá usar o atributo ACF **\[ ALLOCATE (não \_ livre \] )** para manter a memória alocada no servidor.</span><span class="sxs-lookup"><span data-stu-id="8fc38-105">For example, when a context handle will be manipulated by several remote procedures, you can use the ACF attribute **\[allocate(dont\_free)\]** to retain the allocated memory on the server.</span></span>

<span data-ttu-id="8fc38-106">O atributo **\[ ALLOCATE (não \_ livre \] )** é adicionado à declaração de **typedef** de ACF no ACF.</span><span class="sxs-lookup"><span data-stu-id="8fc38-106">The **\[allocate(dont\_free)\]** attribute is added to the ACF **typedef** declaration in the ACF.</span></span> <span data-ttu-id="8fc38-107">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8fc38-107">For example:</span></span>

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes, dont_free)] P_TREE_TYPE;
```

<span data-ttu-id="8fc38-108">Quando o atributo **\[ ALLOCATE (não \_ livre \] )** é especificado, a estrutura de dados de árvore é alocada, mas não liberada, pelo stub do servidor.</span><span class="sxs-lookup"><span data-stu-id="8fc38-108">When the **\[allocate(dont\_free)\]** attribute is specified, the tree data structure is allocated, but not freed, by the server stub.</span></span> <span data-ttu-id="8fc38-109">Quando você torna os ponteiros para essas áreas de dados persistentes disponíveis para outras rotinas — por exemplo, copiando os ponteiros para variáveis globais — os dados retidos podem ser acessados por outras funções de servidor.</span><span class="sxs-lookup"><span data-stu-id="8fc38-109">When you make the pointers to such persistent data areas available to other routines—for example, by copying the pointers to global variables—the retained data is accessible to other server functions.</span></span> <span data-ttu-id="8fc38-110">O atributo **\[ ALLOCATE (não \_ livre \] )** é particularmente útil para manter estruturas de ponteiro persistentes como parte das informações de estado do servidor associadas a um tipo de identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="8fc38-110">The **\[allocate(dont\_free)\]** attribute is particularly useful for maintaining persistent pointer structures as part of the server state information associated with a context-handle type.</span></span>

 

 




