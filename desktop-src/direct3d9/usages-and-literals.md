---
description: O uso é semelhante ao escopo de um parâmetro, pois ele define o escopo no qual o parâmetro é válido.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Usos e literais (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ca6f010d2c1e05055fd4427b8b5f7d4ab445ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105793847"
---
# <a name="usages-and-literals-direct3d-9"></a><span data-ttu-id="0efed-103">Usos e literais (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0efed-103">Usages and Literals (Direct3D 9)</span></span>

<span data-ttu-id="0efed-104">O uso é semelhante ao escopo de um parâmetro, pois ele define o escopo no qual o parâmetro é válido.</span><span class="sxs-lookup"><span data-stu-id="0efed-104">Usage is similar to a parameter's scope, because it defines the scope in which the parameter is valid.</span></span>



|        |                                                                                                                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0efed-105">Valor</span><span class="sxs-lookup"><span data-stu-id="0efed-105">Value</span></span>  | <span data-ttu-id="0efed-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="0efed-106">Description</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="0efed-107">const</span><span class="sxs-lookup"><span data-stu-id="0efed-107">const</span></span>  | <span data-ttu-id="0efed-108">O parâmetro será constante dentro do escopo de todas as funções.</span><span class="sxs-lookup"><span data-stu-id="0efed-108">The parameter will be constant within the scope of all functions.</span></span> <span data-ttu-id="0efed-109">(Observe que esses parâmetros ainda podem ser gravados com o [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), pois isso ocorre fora do escopo de todas as funções.)</span><span class="sxs-lookup"><span data-stu-id="0efed-109">(Note that such parameters can still be written to with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), because this occurs outside the scope of all functions.)</span></span> |
| <span data-ttu-id="0efed-110">shared</span><span class="sxs-lookup"><span data-stu-id="0efed-110">shared</span></span> | <span data-ttu-id="0efed-111">O parâmetro será compartilhado no pool de efeitos.</span><span class="sxs-lookup"><span data-stu-id="0efed-111">The parameter will be shared in the effect pool.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="0efed-112">static</span><span class="sxs-lookup"><span data-stu-id="0efed-112">static</span></span> | <span data-ttu-id="0efed-113">O parâmetro será invisível para o aplicativo, ou seja, você não poderá acessá-los de [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="0efed-113">The parameter will be invisible to the application, that is, you cannot access them from [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>                                                                                                  |



 

<span data-ttu-id="0efed-114">Marcar um parâmetro como literal indica que seu valor nunca será alterado.</span><span class="sxs-lookup"><span data-stu-id="0efed-114">Marking a parameter as literal indicates that its value will never change.</span></span> <span data-ttu-id="0efed-115">Isso permite que o compilador de efeito faça uma otimização extra.</span><span class="sxs-lookup"><span data-stu-id="0efed-115">This enables the effect compiler to do extra optimization.</span></span>

<span data-ttu-id="0efed-116">Somente os parâmetros de nível superior não compartilhados podem ser marcados como literais.</span><span class="sxs-lookup"><span data-stu-id="0efed-116">Only non-shared top-level parameters can be marked as literal.</span></span> <span data-ttu-id="0efed-117">Os parâmetros só podem ser marcados como literais com [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="0efed-117">Parameters can only be marked as literal with [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span> <span data-ttu-id="0efed-118">Valores literais não podem ser definidos com [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="0efed-118">Literal values cannot be set with [**ID3DXEffect**](id3dxeffect.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0efed-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0efed-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0efed-120">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="0efed-120">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



