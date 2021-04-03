---
title: Atributos de desempenho
description: Use os seguintes atributos em um arquivo IDL para reduzir o tamanho do código stub ou melhorar o desempenho.
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- MIDL, atributos, desempenho de IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbfa518b400d237c9fd3789f61b7e74a0c38276
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006157"
---
# <a name="performance-attributes"></a><span data-ttu-id="58bb6-104">Atributos de desempenho</span><span class="sxs-lookup"><span data-stu-id="58bb6-104">Performance Attributes</span></span>

<span data-ttu-id="58bb6-105">Use os seguintes atributos em um arquivo IDL para reduzir o tamanho do código stub ou melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="58bb6-105">Use the following attributes in an IDL file to reduce the size of the stub code or otherwise improve performance.</span></span>



| <span data-ttu-id="58bb6-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="58bb6-106">Attribute</span></span>                             | <span data-ttu-id="58bb6-107">Uso</span><span class="sxs-lookup"><span data-stu-id="58bb6-107">Usage</span></span>                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58bb6-108">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="58bb6-108">**ignore**</span></span>](ignore.md)              | <span data-ttu-id="58bb6-109">Designa que um ponteiro contido em uma estrutura ou União e o objeto indicado pelo ponteiro não sejam transmitidos.</span><span class="sxs-lookup"><span data-stu-id="58bb6-109">Designates that a pointer contained in a structure or union and the object indicated by the pointer is not to be transmitted.</span></span>                        |
| [<span data-ttu-id="58bb6-110">**local**</span><span class="sxs-lookup"><span data-stu-id="58bb6-110">**local**</span></span>](local.md)                | <span data-ttu-id="58bb6-111">Designa uma função que é local para o aplicativo para o qual MIDL não precisa gerar código stub.</span><span class="sxs-lookup"><span data-stu-id="58bb6-111">Designates a function that is local to the application for which MIDL does not need to generate stub code.</span></span>                                           |
| [<span data-ttu-id="58bb6-112">**\_marshaling de transmissão**</span><span class="sxs-lookup"><span data-stu-id="58bb6-112">**wire\_marshal**</span></span>](wire-marshal.md) | <span data-ttu-id="58bb6-113">Define um tipo de dados como um tipo mais simples para transmissão em uma rede e permite que você implemente rotinas de marshaling e desempacotamento para o tipo.</span><span class="sxs-lookup"><span data-stu-id="58bb6-113">Defines a data type as a simpler type for transmission over a network and allows you to implement marshaling and unmarshaling routines for the type.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="58bb6-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="58bb6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58bb6-115">Atributos de ACF de gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="58bb6-115">Memory Management ACF Attributes</span></span>](memory-management-acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="58bb6-116">Atributos de ACF de otimização de stub</span><span class="sxs-lookup"><span data-stu-id="58bb6-116">Stub Optimization ACF Attributes</span></span>](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 




