---
description: A API do Direct3D define vários elementos de API para ajudá-lo a criar e gerenciar o sistema de efeitos.
ms.assetid: d3b0b7a2-0820-4bb1-8b9e-c6b55a039963
title: Referência de efeito (gráficos do Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c903959096e1192555fd813a256d03fb1969fa9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920331"
---
# <a name="effect-reference-direct3d-10-graphics"></a><span data-ttu-id="a7782-103">Referência de efeito (gráficos do Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="a7782-103">Effect Reference (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="a7782-104">A API do Direct3D define vários elementos de API para ajudá-lo a criar e gerenciar o sistema de efeitos.</span><span class="sxs-lookup"><span data-stu-id="a7782-104">The Direct3D API defines several API elements to help you create and manage the effect system.</span></span>

-   [<span data-ttu-id="a7782-105">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a7782-105">Interfaces</span></span>](d3d10-graphics-reference-effect-interfaces.md)
-   [<span data-ttu-id="a7782-106">Funções</span><span class="sxs-lookup"><span data-stu-id="a7782-106">Functions</span></span>](d3d10-graphics-reference-effect-functions.md)
-   [<span data-ttu-id="a7782-107">Estruturas</span><span class="sxs-lookup"><span data-stu-id="a7782-107">Structures</span></span>](d3d10-graphics-reference-effect-structures.md)
-   [<span data-ttu-id="a7782-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="a7782-108">Constants</span></span>](d3d10-graphics-reference-effect-constants.md)

<span data-ttu-id="a7782-109">O sistema de efeitos encapsula as atribuições de estado em um efeito.</span><span class="sxs-lookup"><span data-stu-id="a7782-109">The effect system encapsulates state assignments in an effect.</span></span> <span data-ttu-id="a7782-110">Cada efeito é uma coleção de estado do pipeline que pode ser dividido em atribuições de estado usando blocos de estado, recursos e sombreadores.</span><span class="sxs-lookup"><span data-stu-id="a7782-110">Each effect is a collection of pipeline state which can be broken down into state assignments using state blocks, resources, and shaders.</span></span> <span data-ttu-id="a7782-111">Dependendo do tamanho de um efeito, você pode optar por implementar um em uma cadeia de caracteres de texto ASCII ou um arquivo de efeito (. FX).</span><span class="sxs-lookup"><span data-stu-id="a7782-111">Depending on the size of an effect, you can choose to implement one in an ASCII text string or an effect file (.fx).</span></span> <span data-ttu-id="a7782-112">Para organizar as informações em um efeito, consulte o [formato de efeito](d3d10-effect-format.md).</span><span class="sxs-lookup"><span data-stu-id="a7782-112">To organize information in an effect, see the [effect format](d3d10-effect-format.md).</span></span>

<span data-ttu-id="a7782-113">Tendo criado um efeito, use a API de efeito para definir o estado no dispositivo durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="a7782-113">Having designed an effect, use the effect API to set state in the device during rendering.</span></span> <span data-ttu-id="a7782-114">Também, o sistema de efeitos dá suporte a uma série de APIs de reflexão para obter e definir dados de efeito.</span><span class="sxs-lookup"><span data-stu-id="a7782-114">As well, the effect system supports a series of reflection API's for getting and setting effect data.</span></span> <span data-ttu-id="a7782-115">Para obter mais informações, consulte [interfaces do sistema de efeito (Direct3D 10)](d3d10-graphics-programming-guide-effects-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="a7782-115">For more information, see [Effect System Interfaces (Direct3D 10)](d3d10-graphics-programming-guide-effects-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7782-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7782-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7782-117">Referência do Direct3D</span><span class="sxs-lookup"><span data-stu-id="a7782-117">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 



