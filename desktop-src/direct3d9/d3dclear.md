---
description: Esses sinalizadores identificam uma superfície a ser redefinida ao chamar Limpar.
ms.assetid: 5d76e9a3-7afc-4db7-bffe-64bc7b9f83ac
title: D3DCLEAR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4c588fca44f9567dba0c1d2f7b88ba286cb86f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343341"
---
# <a name="d3dclear"></a><span data-ttu-id="bb920-103">D3DCLEAR</span><span class="sxs-lookup"><span data-stu-id="bb920-103">D3DCLEAR</span></span>

<span data-ttu-id="bb920-104">Esses sinalizadores identificam uma superfície a ser redefinida ao chamar [**Limpar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear).</span><span class="sxs-lookup"><span data-stu-id="bb920-104">These flags identify a surface to reset when calling [**Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear).</span></span>



| <span data-ttu-id="bb920-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="bb920-105">\#define</span></span>          | <span data-ttu-id="bb920-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb920-106">Description</span></span>                                                                                                                                 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb920-107">ESTENCIL D3DCLEAR \_</span><span class="sxs-lookup"><span data-stu-id="bb920-107">D3DCLEAR\_STENCIL</span></span> | <span data-ttu-id="bb920-108">Limpe o buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="bb920-108">Clear the stencil buffer.</span></span>                                                                                                                   |
| <span data-ttu-id="bb920-109">DESTINO D3DCLEAR \_</span><span class="sxs-lookup"><span data-stu-id="bb920-109">D3DCLEAR\_TARGET</span></span>  | <span data-ttu-id="bb920-110">Limpe um destino de renderização ou todos os destinos em um destino de renderização múltipla.</span><span class="sxs-lookup"><span data-stu-id="bb920-110">Clear a render target, or all targets in a multiple render target.</span></span> <span data-ttu-id="bb920-111">Consulte [Vários destinos de renderização (Direct3D 9)](multiple-render-targets.md).</span><span class="sxs-lookup"><span data-stu-id="bb920-111">See [Multiple Render Targets (Direct3D 9)](multiple-render-targets.md).</span></span> |
| <span data-ttu-id="bb920-112">D3DCLEAR \_ ZBUFFER</span><span class="sxs-lookup"><span data-stu-id="bb920-112">D3DCLEAR\_ZBUFFER</span></span> | <span data-ttu-id="bb920-113">Limpe o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="bb920-113">Clear the depth buffer.</span></span>                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="bb920-114">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="bb920-114">Constant Information</span></span>



| <span data-ttu-id="bb920-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb920-115">Requirement</span></span>                         |  <span data-ttu-id="bb920-116">Valor</span><span class="sxs-lookup"><span data-stu-id="bb920-116">Value</span></span>           |
|--------------------------|-------------|
| <span data-ttu-id="bb920-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb920-117">Header</span></span>                   | <span data-ttu-id="bb920-118">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="bb920-118">d3d9types.h</span></span> |
| <span data-ttu-id="bb920-119">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="bb920-119">Minimum operating system</span></span> | <span data-ttu-id="bb920-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="bb920-120">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="bb920-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb920-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb920-122">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="bb920-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
