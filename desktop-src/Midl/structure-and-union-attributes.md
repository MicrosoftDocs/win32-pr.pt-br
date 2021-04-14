---
title: Atributos de estrutura e União
description: Use os \_ atributos switch \ para especificar a característica de uma União em uma chamada de procedimento remoto. Use o atributo ignorar para designar determinados membros da estrutura ou da União como locais para o aplicativo cliente.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- MIDL, atributos, estrutura e União de IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2a7764d56c8557bd71923021a9f324a118ac81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453571"
---
# <a name="structure-and-union-attributes"></a><span data-ttu-id="00249-105">Atributos de estrutura e União</span><span class="sxs-lookup"><span data-stu-id="00249-105">Structure and Union Attributes</span></span>

<span data-ttu-id="00249-106">Use os **atributos \_ switch** \* para especificar a característica de uma União em uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="00249-106">Use the **switch\_**\* attributes to specify the characteristic of a union in a remote procedure call.</span></span> <span data-ttu-id="00249-107">Use o atributo [**ignorar**](ignore.md) para designar determinados membros da estrutura ou da União como locais para o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="00249-107">Use the [**ignore**](ignore.md) attribute to designate certain structure or union members as local to the client application.</span></span>



| <span data-ttu-id="00249-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="00249-108">Attribute</span></span>                           | <span data-ttu-id="00249-109">Uso</span><span class="sxs-lookup"><span data-stu-id="00249-109">Usage</span></span>                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00249-110">**comutador**</span><span class="sxs-lookup"><span data-stu-id="00249-110">**switch**</span></span>](switch.md)            | <span data-ttu-id="00249-111">Seleciona o discriminante para uma União encapsulada.</span><span class="sxs-lookup"><span data-stu-id="00249-111">Selects the discriminant for an encapsulated union.</span></span>                                                                           |
| [<span data-ttu-id="00249-112">**switch \_ é**</span><span class="sxs-lookup"><span data-stu-id="00249-112">**switch\_is**</span></span>](switch-is.md)     | <span data-ttu-id="00249-113">Identifica o discriminante para uma União não encapsulada.</span><span class="sxs-lookup"><span data-stu-id="00249-113">Identifies the discriminant for a nonencapsulated union.</span></span>                                                                      |
| [<span data-ttu-id="00249-114">**tipo de comutador \_**</span><span class="sxs-lookup"><span data-stu-id="00249-114">**switch\_type**</span></span>](switch-type.md) | <span data-ttu-id="00249-115">Identifica o tipo de discriminante para uma União não encapsulada.</span><span class="sxs-lookup"><span data-stu-id="00249-115">Identifies the type of the discriminant for a nonencapsulated union.</span></span>                                                          |
| [<span data-ttu-id="00249-116">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="00249-116">**ignore**</span></span>](ignore.md)            | <span data-ttu-id="00249-117">Designa que um ponteiro contido em uma estrutura ou União e o objeto indicado pelo ponteiro não sejam transmitidos.</span><span class="sxs-lookup"><span data-stu-id="00249-117">Designates that a pointer contained in a structure or union and the object indicated by the pointer is not to be transmitted.</span></span> |



 

<span data-ttu-id="00249-118">Você também pode usar os [atributos de ponteiro de matriz e dimensionamento](array-and-sized-pointer-attributes.md) para especificar características de estrutura ou membros de União.</span><span class="sxs-lookup"><span data-stu-id="00249-118">You can also use the [array and sized pointer attributes](array-and-sized-pointer-attributes.md) to specify characteristics of structure or union members.</span></span>

 

 




