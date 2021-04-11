---
description: Essas constantes são usadas ao criar um efeito para definir o comportamento de compilação ou o comportamento de efeito de tempo de execução.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: D3D10_EFFECT constantes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c12b7a458bb7c97bb53436565513673006a2884
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296081"
---
# <a name="d3d10_effect-constants"></a><span data-ttu-id="8a768-103">Constantes de efeito de D3D10 \_</span><span class="sxs-lookup"><span data-stu-id="8a768-103">D3D10\_EFFECT Constants</span></span>

<span data-ttu-id="8a768-104">Essas constantes são usadas ao criar um efeito para definir o comportamento de compilação ou o comportamento de efeito de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="8a768-104">These constants used when creating an effect to define either compilation behavior or runtime effect behavior.</span></span>



| <span data-ttu-id="8a768-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="8a768-105">\#define</span></span>                                 | <span data-ttu-id="8a768-106">Valor</span><span class="sxs-lookup"><span data-stu-id="8a768-106">Value</span></span>        | <span data-ttu-id="8a768-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a768-107">Description</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a768-108">Efeito \_ \_ filho de compilação de efeitos d3d10 \_ \_</span><span class="sxs-lookup"><span data-stu-id="8a768-108">D3D10\_EFFECT\_COMPILE\_CHILD\_EFFECT</span></span>    | <span data-ttu-id="8a768-109">1 << 0</span><span class="sxs-lookup"><span data-stu-id="8a768-109">1 << 0</span></span> | <span data-ttu-id="8a768-110">Compile o arquivo. FX para um efeito filho.</span><span class="sxs-lookup"><span data-stu-id="8a768-110">Compile the .fx file to a child effect.</span></span> <span data-ttu-id="8a768-111">Os efeitos filho não têm inicializações para nenhum valor compartilhado porque eles são inicializados no pool de efeitos.</span><span class="sxs-lookup"><span data-stu-id="8a768-111">Child effects have no initializes for any shared values because these are initialized in the effect pool.</span></span>                                                                                                           |
| <span data-ttu-id="8a768-112">D3D10 de \_ efeito de \_ compilação \_ permitir \_ operações lentas \_</span><span class="sxs-lookup"><span data-stu-id="8a768-112">D3D10\_EFFECT\_COMPILE\_ALLOW\_SLOW\_OPS</span></span> | <span data-ttu-id="8a768-113">1 << 1</span><span class="sxs-lookup"><span data-stu-id="8a768-113">1 << 1</span></span> | <span data-ttu-id="8a768-114">Por padrão, o modo de desempenho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8a768-114">By default, performance mode is enabled.</span></span> <span data-ttu-id="8a768-115">O modo de desempenho não permite objetos de estado mutável, impedindo que expressões não literais apareçam nas definições de objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="8a768-115">Performance mode disallows mutable state objects by preventing non-literal expressions from appearing in state object definitions.</span></span> <span data-ttu-id="8a768-116">A especificação desse sinalizador desabilitará o modo e permitirá objetos de estado mutável.</span><span class="sxs-lookup"><span data-stu-id="8a768-116">Specifying this flag will disable the mode and allow for mutable state objects.</span></span> |
| <span data-ttu-id="8a768-117">\_Efeito de \_ d3d10 \_ thread único</span><span class="sxs-lookup"><span data-stu-id="8a768-117">D3D10\_EFFECT\_SINGLE\_THREADED</span></span>          | <span data-ttu-id="8a768-118">1 << 3</span><span class="sxs-lookup"><span data-stu-id="8a768-118">1 << 3</span></span> | <span data-ttu-id="8a768-119">Não tente sincronizar com outros threads que carregam efeitos no mesmo pool.</span><span class="sxs-lookup"><span data-stu-id="8a768-119">Do not attempt to synchronize with other threads loading effects into the same pool.</span></span>                                                                                                                                                                        |



 

<span data-ttu-id="8a768-120">Essas constantes são definidas como macros em d3d10effect. h.</span><span class="sxs-lookup"><span data-stu-id="8a768-120">These constants are defined as macros in d3d10effect.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a768-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a768-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a768-122">Constantes de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8a768-122">Effect Constants (Direct3D 10)</span></span>](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



