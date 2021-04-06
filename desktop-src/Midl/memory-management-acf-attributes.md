---
title: Atributos de ACF de gerenciamento de memória
description: Os atributos listados na tabela a seguir permitem que você execute o gerenciamento de memória do lado do cliente.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- MIDL de ACF, atributos, gerenciamento de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12a0ee6d11a2b10e1c0fad7cd1a42411670b508
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917249"
---
# <a name="memory-management-acf-attributes"></a><span data-ttu-id="27a86-104">Atributos de ACF de gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="27a86-104">Memory Management ACF Attributes</span></span>

<span data-ttu-id="27a86-105">Os atributos listados na tabela a seguir permitem que você execute o gerenciamento de memória do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="27a86-105">The attributes listed in the following table enable you to perform memory management from the client side.</span></span>



| <span data-ttu-id="27a86-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="27a86-106">Attribute</span></span>                                   | <span data-ttu-id="27a86-107">Uso</span><span class="sxs-lookup"><span data-stu-id="27a86-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27a86-108">**aloca**</span><span class="sxs-lookup"><span data-stu-id="27a86-108">**allocate**</span></span>](allocate.md)                | <span data-ttu-id="27a86-109">Especifica a maneira como o aplicativo cliente e o stub alocam e liberam memória para ponteiros.</span><span class="sxs-lookup"><span data-stu-id="27a86-109">Specifies the way the client application and stub allocate and release memory for pointers.</span></span> <span data-ttu-id="27a86-110">Esse atributo é particularmente útil quando você deseja que determinadas estruturas de ponteiro permaneçam acessíveis para o aplicativo de servidor após a chamada de procedimento remoto retornar ao cliente.</span><span class="sxs-lookup"><span data-stu-id="27a86-110">This attribute is particularly useful when you want certain pointer structures to remain accessible to the server application after the remote procedure call returns to the client.</span></span> <span data-ttu-id="27a86-111">Você também pode usar o atributo [**ALLOCATE**](allocate.md) para direcionar o stub para calcular o tamanho de toda a memória referenciada por meio do ponteiro do tipo especificado e fazer uma única chamada para o [**usuário de MIDL \_ \_ alocar**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span><span class="sxs-lookup"><span data-stu-id="27a86-111">You can also use the [**allocate**](allocate.md) attribute to direct the stub to compute the size of all memory referenced through the pointer of the specified type and to make a single call to [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span></span> |
| [<span data-ttu-id="27a86-112">**contagem de bytes \_**</span><span class="sxs-lookup"><span data-stu-id="27a86-112">**byte\_count**</span></span>](byte-count.md)           | <span data-ttu-id="27a86-113">Permite que você crie um bloco persistente e contíguo de memória que pode ser reutilizado em várias chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="27a86-113">Enables you to create a persistent, contiguous block of memory that can be reused over multiple remote procedure calls.</span></span> <span data-ttu-id="27a86-114">Isso libera o aplicativo cliente da sobrecarga de alocar repetidamente e liberar memória que pode incluir vários ponteiros e outras estruturas de dados complexas.</span><span class="sxs-lookup"><span data-stu-id="27a86-114">This frees the client application from the overhead of repeatedly allocating and releasing memory that may include multiple pointers and other complex data structures.</span></span>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="27a86-115">**Habilitar \_ alocação**</span><span class="sxs-lookup"><span data-stu-id="27a86-115">**enable\_allocate**</span></span>](enable-allocate.md) | <span data-ttu-id="27a86-116">Especifica que o código stub do servidor deve habilitar o ambiente de gerenciamento de memória de stub.</span><span class="sxs-lookup"><span data-stu-id="27a86-116">Specifies that the server stub code should enable the stub memory-management environment.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 