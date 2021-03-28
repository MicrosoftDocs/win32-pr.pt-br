---
title: defi-PS
description: Define um valor constante inteiro, que deve ser carregado sempre que um sombreador for definido como um dispositivo.
ms.assetid: c51982a1-45b4-48db-a49a-93165d61efd3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3552d5cfe322dd384e1c6bd219e35af19b469a56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084762"
---
# <a name="defi---ps"></a><span data-ttu-id="c1bba-103">defi-PS</span><span class="sxs-lookup"><span data-stu-id="c1bba-103">defi - ps</span></span>

<span data-ttu-id="c1bba-104">Define um valor constante inteiro, que deve ser carregado sempre que um sombreador for definido como um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1bba-104">Defines an integer constant value, which should be loaded any time a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1bba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1bba-105">Syntax</span></span>



| <span data-ttu-id="c1bba-106">defi DST, inteirovalue</span><span class="sxs-lookup"><span data-stu-id="c1bba-106">defi dst, integerValue</span></span> |
|------------------------|



 

-   <span data-ttu-id="c1bba-107">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="c1bba-107">dst is the destination register.</span></span>
-   <span data-ttu-id="c1bba-108">integerValue é um valor inteiro constante.</span><span class="sxs-lookup"><span data-stu-id="c1bba-108">integerValue is a constant integer value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1bba-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1bba-109">Remarks</span></span>



| <span data-ttu-id="c1bba-110">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c1bba-110">Pixel shader versions</span></span> | <span data-ttu-id="c1bba-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="c1bba-111">1\_1</span></span> | <span data-ttu-id="c1bba-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="c1bba-112">1\_2</span></span> | <span data-ttu-id="c1bba-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c1bba-113">1\_3</span></span> | <span data-ttu-id="c1bba-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="c1bba-114">1\_4</span></span> | <span data-ttu-id="c1bba-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c1bba-115">2\_0</span></span> | <span data-ttu-id="c1bba-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c1bba-116">2\_x</span></span> | <span data-ttu-id="c1bba-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c1bba-117">2\_sw</span></span> | <span data-ttu-id="c1bba-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c1bba-118">3\_0</span></span> | <span data-ttu-id="c1bba-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c1bba-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c1bba-120">defi</span><span class="sxs-lookup"><span data-stu-id="c1bba-120">defi</span></span>                  |      |      |      |      |      | <span data-ttu-id="c1bba-121">x</span><span class="sxs-lookup"><span data-stu-id="c1bba-121">x</span></span>    | <span data-ttu-id="c1bba-122">x</span><span class="sxs-lookup"><span data-stu-id="c1bba-122">x</span></span>     | <span data-ttu-id="c1bba-123">x</span><span class="sxs-lookup"><span data-stu-id="c1bba-123">x</span></span>    | <span data-ttu-id="c1bba-124">x</span><span class="sxs-lookup"><span data-stu-id="c1bba-124">x</span></span>     |



 

<span data-ttu-id="c1bba-125">A instrução defi define uma constante de sombreador cujo valor é carregado sempre que um sombreador é definido como um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1bba-125">The defi instruction defines a shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="c1bba-126">Elas são chamadas de constantes imediatas.</span><span class="sxs-lookup"><span data-stu-id="c1bba-126">These are called immediate constants.</span></span> <span data-ttu-id="c1bba-127">Constantes imediatas têm precedência sobre constantes definidas pelo método de API SetPixelShaderConstantB.</span><span class="sxs-lookup"><span data-stu-id="c1bba-127">Immediate constants take precedence over constants set by the API method SetPixelShaderConstantB.</span></span>

<span data-ttu-id="c1bba-128">Há duas maneiras de definir uma constante em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="c1bba-128">There are two ways to set a constant in a shader.</span></span>

1.  <span data-ttu-id="c1bba-129">Use defi para definir a constante diretamente dentro de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="c1bba-129">Use defi to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="c1bba-130">Use os métodos de API para definir uma constante.</span><span class="sxs-lookup"><span data-stu-id="c1bba-130">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="c1bba-131">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) para definir uma constante booliana.</span><span class="sxs-lookup"><span data-stu-id="c1bba-131">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) to set a Boolean constant.</span></span>
    -   <span data-ttu-id="c1bba-132">Use [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) para definir uma constante de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="c1bba-132">Use [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) to set a floating-point constant.</span></span>
    -   <span data-ttu-id="c1bba-133">Use [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) para definir uma constante de inteiro.</span><span class="sxs-lookup"><span data-stu-id="c1bba-133">Use [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) to set an integer constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1bba-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1bba-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1bba-135">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c1bba-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 