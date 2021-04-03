---
title: Portando funções de textura
description: Portando funções de textura
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- Portabilidade do íris GL, textura
- portando do íris GL, textura
- portando para OpenGL do íris GL, textura
- Portabilidade OpenGL do íris GL, textura
- textura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cba8b105089553084a93f997517d19cf371e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005744"
---
# <a name="porting-texture-functions"></a><span data-ttu-id="75d81-108">Portando funções de textura</span><span class="sxs-lookup"><span data-stu-id="75d81-108">Porting Texture Functions</span></span>

<span data-ttu-id="75d81-109">Ao portar funções de textura do íris GL para OpenGL, tenha em mente os seguintes pontos:</span><span class="sxs-lookup"><span data-stu-id="75d81-109">When porting IRIS GL texture functions to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="75d81-110">O OpenGL não mantém tabelas de texturas; Ele usa textura de 1-D e somente textura de 2D.</span><span class="sxs-lookup"><span data-stu-id="75d81-110">OpenGL doesn't maintain tables of textures; it uses either 1-D texture and 2-D texture only.</span></span> <span data-ttu-id="75d81-111">Para reutilizar as texturas do código da íris GL, coloque-as em uma lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="75d81-111">To reuse the textures from your IRIS GL code, put them in a display list.</span></span>
-   <span data-ttu-id="75d81-112">O OpenGL não gera mipmaps automaticamente.</span><span class="sxs-lookup"><span data-stu-id="75d81-112">OpenGL doesn't automatically generate mipmaps.</span></span> <span data-ttu-id="75d81-113">Se você estiver usando mipmaps, deverá primeiro chamar a função [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) .</span><span class="sxs-lookup"><span data-stu-id="75d81-113">If you're using mipmaps, you must first call the [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) function.</span></span>
-   <span data-ttu-id="75d81-114">No OpenGL, você usa [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) para ativar e desativar os recursos de texturing.</span><span class="sxs-lookup"><span data-stu-id="75d81-114">In OpenGL, you use [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) to turn texturing capabilities on and off.</span></span>
-   <span data-ttu-id="75d81-115">No OpenGL, o tamanho da textura é mais estritamente regulamentado do que no íris GL.</span><span class="sxs-lookup"><span data-stu-id="75d81-115">In OpenGL, texture size is more strictly regulated than in IRIS GL.</span></span> <span data-ttu-id="75d81-116">O tamanho de uma textura OpenGL deve ser:</span><span class="sxs-lookup"><span data-stu-id="75d81-116">The size of an OpenGL texture must be:</span></span>

    <span data-ttu-id="75d81-117">2 *n* + 2 *b*</span><span class="sxs-lookup"><span data-stu-id="75d81-117">2 *n* + 2 *b*</span></span>

    <span data-ttu-id="75d81-118">onde *n* é um inteiro e *b* é:</span><span class="sxs-lookup"><span data-stu-id="75d81-118">where *n* is an integer and *b* is:</span></span>

    -   <span data-ttu-id="75d81-119">0, se a textura não tiver borda</span><span class="sxs-lookup"><span data-stu-id="75d81-119">0, if the texture has no border</span></span>
    -   <span data-ttu-id="75d81-120">1, se a textura tiver um pixel de borda (texturas OpenGL podem ter bordas de 1 pixel).</span><span class="sxs-lookup"><span data-stu-id="75d81-120">1, if the texture has a border pixel (OpenGL textures can have 1-pixel borders.)</span></span>

<span data-ttu-id="75d81-121">A tabela a seguir lista as funções de textura do íris GL e seus equivalentes em OpenGL gerais.</span><span class="sxs-lookup"><span data-stu-id="75d81-121">The following table lists IRIS GL texture functions and their general OpenGL equivalents.</span></span>



| <span data-ttu-id="75d81-122">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="75d81-122">IRIS GL function</span></span> | <span data-ttu-id="75d81-123">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="75d81-123">OpenGL function</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="75d81-124">Significado</span><span class="sxs-lookup"><span data-stu-id="75d81-124">Meaning</span></span>                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d81-125">**textdef2d**</span><span class="sxs-lookup"><span data-stu-id="75d81-125">**textdef2d**</span></span>    | <span data-ttu-id="75d81-126">[**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)</span><span class="sxs-lookup"><span data-stu-id="75d81-126">[**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)</span></span><br/> [<span data-ttu-id="75d81-127">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="75d81-127">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)<br/>                                                                                                           | <span data-ttu-id="75d81-128">Especifica uma imagem de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="75d81-128">Specifies a 2-D texture image.</span></span>                                                              |
| <span data-ttu-id="75d81-129">**textbind**</span><span class="sxs-lookup"><span data-stu-id="75d81-129">**textbind**</span></span>     | <span data-ttu-id="75d81-130">**glTexImage2DglTexParameter**</span><span class="sxs-lookup"><span data-stu-id="75d81-130">**glTexImage2DglTexParameter**</span></span><br/> <span data-ttu-id="75d81-131">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="75d81-131">**gluBuild2DMipmaps**</span></span><br/>                                                                                                                                                                                            | <span data-ttu-id="75d81-132">Seleciona uma função de textura.</span><span class="sxs-lookup"><span data-stu-id="75d81-132">Selects a texture function.</span></span>                                                                 |
| <span data-ttu-id="75d81-133">**tevdef**</span><span class="sxs-lookup"><span data-stu-id="75d81-133">**tevdef**</span></span>       | [<span data-ttu-id="75d81-134">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="75d81-134">**glTexEnv**</span></span>](gltexenv-functions.md)                                                                                                                                                                                                                                | <span data-ttu-id="75d81-135">Define um ambiente de mapeamento de textura.</span><span class="sxs-lookup"><span data-stu-id="75d81-135">Defines a texture-mapping environment.</span></span>                                                      |
| <span data-ttu-id="75d81-136">**tevbind**</span><span class="sxs-lookup"><span data-stu-id="75d81-136">**tevbind**</span></span>      | <span data-ttu-id="75d81-137">**glTexEnv**[**glTexImage1D**](glteximage1d.md)</span><span class="sxs-lookup"><span data-stu-id="75d81-137">**glTexEnv**[**glTexImage1D**](glteximage1d.md)</span></span><br/>                                                                                                                                                                                                           | <span data-ttu-id="75d81-138">Seleciona um ambiente de textura.</span><span class="sxs-lookup"><span data-stu-id="75d81-138">Selects a texture environment.</span></span>                                                              |
| <span data-ttu-id="75d81-139">**T2**</span><span class="sxs-lookup"><span data-stu-id="75d81-139">**t2**</span></span>           | [<span data-ttu-id="75d81-140">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="75d81-140">**glTexCoord**</span></span>](gltexcoord-functions.md)                                                                                                                                                                                                                            | <span data-ttu-id="75d81-141">Define as coordenadas de textura atuais.</span><span class="sxs-lookup"><span data-stu-id="75d81-141">Sets the current texture coordinates.</span></span>                                                       |
| <span data-ttu-id="75d81-142">**texgen**</span><span class="sxs-lookup"><span data-stu-id="75d81-142">**texgen**</span></span>       | <span data-ttu-id="75d81-143">[**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)</span><span class="sxs-lookup"><span data-stu-id="75d81-143">[**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)</span></span><br/> [<span data-ttu-id="75d81-144">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="75d81-144">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)<br/> [<span data-ttu-id="75d81-145">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="75d81-145">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)<br/> [<span data-ttu-id="75d81-146">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="75d81-146">**gluScaleImage**</span></span>](gluscaleimage.md)<br/> | <span data-ttu-id="75d81-147">Controla a geração de coordenadas de textura. Dimensiona uma imagem para um tamanho arbitrário.</span><span class="sxs-lookup"><span data-stu-id="75d81-147">Controls generation of texture coordinates.Scales an image to an arbitrary size.</span></span><br/> |



 

<span data-ttu-id="75d81-148">Para obter mais informações sobre o texturing, consulte o *Guia de programação OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="75d81-148">For more information on texturing, see the *OpenGL Programming Guide*.</span></span>

<span data-ttu-id="75d81-149">Este tópico inclui informações sobre o seguinte.</span><span class="sxs-lookup"><span data-stu-id="75d81-149">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="75d81-150">Convertendo tevdef</span><span class="sxs-lookup"><span data-stu-id="75d81-150">Translating tevdef</span></span>](translating-tevdef.md)
-   [<span data-ttu-id="75d81-151">Convertendo texdef</span><span class="sxs-lookup"><span data-stu-id="75d81-151">Translating texdef</span></span>](translating-texdef.md)
-   [<span data-ttu-id="75d81-152">Convertendo texgen</span><span class="sxs-lookup"><span data-stu-id="75d81-152">Translating texgen</span></span>](translating-texgen.md)

 

 





