---
title: função glCopyTexImage1D (GL. h)
description: A função glCopyTexImage1D copia os pixels da framebuffer em uma imagem de textura unidimensional.
ms.assetid: 3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd
keywords:
- função glCopyTexImage1D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63180386c094f0c4e4de0f1a361bc3bcb1c6e5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755984"
---
# <a name="glcopyteximage1d-function"></a><span data-ttu-id="958f7-104">função glCopyTexImage1D</span><span class="sxs-lookup"><span data-stu-id="958f7-104">glCopyTexImage1D function</span></span>

<span data-ttu-id="958f7-105">A função **glCopyTexImage1D** copia os pixels da framebuffer em uma imagem de textura unidimensional.</span><span class="sxs-lookup"><span data-stu-id="958f7-105">The **glCopyTexImage1D** function copies pixels from the framebuffer into a one-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="958f7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="958f7-106">Syntax</span></span>


```C++
void WINAPI glCopyTexImage1D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLint   border
);
```



## <a name="parameters"></a><span data-ttu-id="958f7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="958f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="958f7-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="958f7-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="958f7-109">O destino para o qual os dados da imagem serão alterados.</span><span class="sxs-lookup"><span data-stu-id="958f7-109">The target for which the image data will be changed.</span></span> <span data-ttu-id="958f7-110">Deve ter o valor GL \_ Texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="958f7-110">Must have the value GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="958f7-111">*level*</span><span class="sxs-lookup"><span data-stu-id="958f7-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="958f7-112">O número de nível de detalhe.</span><span class="sxs-lookup"><span data-stu-id="958f7-112">The level-of-detail number.</span></span> <span data-ttu-id="958f7-113">Nível 0 é a imagem base.</span><span class="sxs-lookup"><span data-stu-id="958f7-113">Level 0 is the base image.</span></span> <span data-ttu-id="958f7-114">O nível *n* é a imagem de redução *n* º mipmap.</span><span class="sxs-lookup"><span data-stu-id="958f7-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="958f7-115">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="958f7-115">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="958f7-116">O formato interno e a resolução dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="958f7-116">The internal format and resolution of the texture data.</span></span> <span data-ttu-id="958f7-117">Esse parâmetro deve ser um dos valores simbólicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="958f7-117">This parameter must be one of the following symbolic values.</span></span>



| <span data-ttu-id="958f7-118">Constante</span><span class="sxs-lookup"><span data-stu-id="958f7-118">Constant</span></span>                 | <span data-ttu-id="958f7-119">Bits de R</span><span class="sxs-lookup"><span data-stu-id="958f7-119">R Bits</span></span> | <span data-ttu-id="958f7-120">G bits</span><span class="sxs-lookup"><span data-stu-id="958f7-120">G Bits</span></span> | <span data-ttu-id="958f7-121">Bits B</span><span class="sxs-lookup"><span data-stu-id="958f7-121">B Bits</span></span> | <span data-ttu-id="958f7-122">Um bits</span><span class="sxs-lookup"><span data-stu-id="958f7-122">A Bits</span></span> | <span data-ttu-id="958f7-123">Bits L</span><span class="sxs-lookup"><span data-stu-id="958f7-123">L Bits</span></span> | <span data-ttu-id="958f7-124">I bits</span><span class="sxs-lookup"><span data-stu-id="958f7-124">I Bits</span></span> |
|--------------------------|--------|--------|--------|--------|--------|--------|
| <span data-ttu-id="958f7-125">GL \_ alfa</span><span class="sxs-lookup"><span data-stu-id="958f7-125">GL\_ALPHA</span></span>                |        |        |        |        |        |        |
| <span data-ttu-id="958f7-126">\_ALPHA4 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-126">GL\_ALPHA4</span></span>               |        |        |        | <span data-ttu-id="958f7-127">4</span><span class="sxs-lookup"><span data-stu-id="958f7-127">4</span></span>      |        |        |
| <span data-ttu-id="958f7-128">\_ALPHA8 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-128">GL\_ALPHA8</span></span>               |        |        |        | <span data-ttu-id="958f7-129">8</span><span class="sxs-lookup"><span data-stu-id="958f7-129">8</span></span>      |        |        |
| <span data-ttu-id="958f7-130">\_ALPHA12 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-130">GL\_ALPHA12</span></span>              |        |        |        | <span data-ttu-id="958f7-131">12</span><span class="sxs-lookup"><span data-stu-id="958f7-131">12</span></span>     |        |        |
| <span data-ttu-id="958f7-132">\_ALPHA16 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-132">GL\_ALPHA16</span></span>              |        |        |        | <span data-ttu-id="958f7-133">16</span><span class="sxs-lookup"><span data-stu-id="958f7-133">16</span></span>     |        |        |
| <span data-ttu-id="958f7-134">\_luminância GL</span><span class="sxs-lookup"><span data-stu-id="958f7-134">GL\_LUMINANCE</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="958f7-135">\_LUMINANCE4 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-135">GL\_LUMINANCE4</span></span>           |        |        |        |        | <span data-ttu-id="958f7-136">4</span><span class="sxs-lookup"><span data-stu-id="958f7-136">4</span></span>      |        |
| <span data-ttu-id="958f7-137">\_LUMINANCE8 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-137">GL\_LUMINANCE8</span></span>           |        |        |        |        | <span data-ttu-id="958f7-138">8</span><span class="sxs-lookup"><span data-stu-id="958f7-138">8</span></span>      |        |
| <span data-ttu-id="958f7-139">\_LUMINANCE12 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-139">GL\_LUMINANCE12</span></span>          |        |        |        |        | <span data-ttu-id="958f7-140">12</span><span class="sxs-lookup"><span data-stu-id="958f7-140">12</span></span>     |        |
| <span data-ttu-id="958f7-141">\_LUMINANCE16 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-141">GL\_LUMINANCE16</span></span>          |        |        |        |        | <span data-ttu-id="958f7-142">16</span><span class="sxs-lookup"><span data-stu-id="958f7-142">16</span></span>     |        |
| <span data-ttu-id="958f7-143">luminância do GL \_ \_ alfa</span><span class="sxs-lookup"><span data-stu-id="958f7-143">GL\_LUMINANCE\_ALPHA</span></span>     |        |        |        |        |        |        |
| <span data-ttu-id="958f7-144">GL \_ LUMINANCE4 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="958f7-144">GL\_LUMINANCE4\_ALPHA4</span></span>   |        |        |        | <span data-ttu-id="958f7-145">4</span><span class="sxs-lookup"><span data-stu-id="958f7-145">4</span></span>      | <span data-ttu-id="958f7-146">4</span><span class="sxs-lookup"><span data-stu-id="958f7-146">4</span></span>      |        |
| <span data-ttu-id="958f7-147">GL \_ LUMINANCE6 \_ ALPHA2</span><span class="sxs-lookup"><span data-stu-id="958f7-147">GL\_LUMINANCE6\_ALPHA2</span></span>   |        |        |        | <span data-ttu-id="958f7-148">2</span><span class="sxs-lookup"><span data-stu-id="958f7-148">2</span></span>      | <span data-ttu-id="958f7-149">6</span><span class="sxs-lookup"><span data-stu-id="958f7-149">6</span></span>      |        |
| <span data-ttu-id="958f7-150">GL \_ LUMINANCE8 \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="958f7-150">GL\_LUMINANCE8\_ALPHA8</span></span>   |        |        |        | <span data-ttu-id="958f7-151">8</span><span class="sxs-lookup"><span data-stu-id="958f7-151">8</span></span>      | <span data-ttu-id="958f7-152">8</span><span class="sxs-lookup"><span data-stu-id="958f7-152">8</span></span>      |        |
| <span data-ttu-id="958f7-153">GL \_ LUMINANCE12 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="958f7-153">GL\_LUMINANCE12\_ALPHA4</span></span>  |        |        |        | <span data-ttu-id="958f7-154">4</span><span class="sxs-lookup"><span data-stu-id="958f7-154">4</span></span>      | <span data-ttu-id="958f7-155">12</span><span class="sxs-lookup"><span data-stu-id="958f7-155">12</span></span>     |        |
| <span data-ttu-id="958f7-156">GL \_ LUMINANCE12 \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="958f7-156">GL\_LUMINANCE12\_ALPHA12</span></span> |        |        |        | <span data-ttu-id="958f7-157">12</span><span class="sxs-lookup"><span data-stu-id="958f7-157">12</span></span>     | <span data-ttu-id="958f7-158">12</span><span class="sxs-lookup"><span data-stu-id="958f7-158">12</span></span>     |        |
| <span data-ttu-id="958f7-159">GL \_ LUMINANCE16 \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="958f7-159">GL\_LUMINANCE16\_ALPHA16</span></span> |        |        |        | <span data-ttu-id="958f7-160">16</span><span class="sxs-lookup"><span data-stu-id="958f7-160">16</span></span>     | <span data-ttu-id="958f7-161">16</span><span class="sxs-lookup"><span data-stu-id="958f7-161">16</span></span>     |        |
| <span data-ttu-id="958f7-162">intensidade do GL \_</span><span class="sxs-lookup"><span data-stu-id="958f7-162">GL\_INTENSITY</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="958f7-163">\_INTENSITY4 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-163">GL\_INTENSITY4</span></span>           |        |        |        |        |        | <span data-ttu-id="958f7-164">4</span><span class="sxs-lookup"><span data-stu-id="958f7-164">4</span></span>      |
| <span data-ttu-id="958f7-165">\_INTENSITY8 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-165">GL\_INTENSITY8</span></span>           |        |        |        |        |        | <span data-ttu-id="958f7-166">8</span><span class="sxs-lookup"><span data-stu-id="958f7-166">8</span></span>      |
| <span data-ttu-id="958f7-167">\_INTENSITY12 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-167">GL\_INTENSITY12</span></span>          |        |        |        |        |        | <span data-ttu-id="958f7-168">12</span><span class="sxs-lookup"><span data-stu-id="958f7-168">12</span></span>     |
| <span data-ttu-id="958f7-169">\_INTENSITY16 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-169">GL\_INTENSITY16</span></span>          |        |        |        |        |        | <span data-ttu-id="958f7-170">16</span><span class="sxs-lookup"><span data-stu-id="958f7-170">16</span></span>     |
| <span data-ttu-id="958f7-171">GL em \_ RGB</span><span class="sxs-lookup"><span data-stu-id="958f7-171">GL\_RGB</span></span>                  |        |        |        |        |        |        |
| <span data-ttu-id="958f7-172">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="958f7-172">GL\_R3\_G3\_B2</span></span>           | <span data-ttu-id="958f7-173">3</span><span class="sxs-lookup"><span data-stu-id="958f7-173">3</span></span>      | <span data-ttu-id="958f7-174">3</span><span class="sxs-lookup"><span data-stu-id="958f7-174">3</span></span>      | <span data-ttu-id="958f7-175">2</span><span class="sxs-lookup"><span data-stu-id="958f7-175">2</span></span>      |        |        |        |
| <span data-ttu-id="958f7-176">\_RGB4 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-176">GL\_RGB4</span></span>                 | <span data-ttu-id="958f7-177">4</span><span class="sxs-lookup"><span data-stu-id="958f7-177">4</span></span>      | <span data-ttu-id="958f7-178">4</span><span class="sxs-lookup"><span data-stu-id="958f7-178">4</span></span>      | <span data-ttu-id="958f7-179">4</span><span class="sxs-lookup"><span data-stu-id="958f7-179">4</span></span>      |        |        |        |
| <span data-ttu-id="958f7-180">\_RGB5 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-180">GL\_RGB5</span></span>                 | <span data-ttu-id="958f7-181">5</span><span class="sxs-lookup"><span data-stu-id="958f7-181">5</span></span>      | <span data-ttu-id="958f7-182">5</span><span class="sxs-lookup"><span data-stu-id="958f7-182">5</span></span>      | <span data-ttu-id="958f7-183">5</span><span class="sxs-lookup"><span data-stu-id="958f7-183">5</span></span>      |        |        |        |
| <span data-ttu-id="958f7-184">\_RGB8 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-184">GL\_RGB8</span></span>                 | <span data-ttu-id="958f7-185">8</span><span class="sxs-lookup"><span data-stu-id="958f7-185">8</span></span>      | <span data-ttu-id="958f7-186">8</span><span class="sxs-lookup"><span data-stu-id="958f7-186">8</span></span>      | <span data-ttu-id="958f7-187">8</span><span class="sxs-lookup"><span data-stu-id="958f7-187">8</span></span>      |        |        |        |
| <span data-ttu-id="958f7-188">\_RGB10 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-188">GL\_RGB10</span></span>                | <span data-ttu-id="958f7-189">10</span><span class="sxs-lookup"><span data-stu-id="958f7-189">10</span></span>     | <span data-ttu-id="958f7-190">10</span><span class="sxs-lookup"><span data-stu-id="958f7-190">10</span></span>     | <span data-ttu-id="958f7-191">10</span><span class="sxs-lookup"><span data-stu-id="958f7-191">10</span></span>     |        |        |        |
| <span data-ttu-id="958f7-192">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-192">GL\_RGB12</span></span>                | <span data-ttu-id="958f7-193">12</span><span class="sxs-lookup"><span data-stu-id="958f7-193">12</span></span>     | <span data-ttu-id="958f7-194">12</span><span class="sxs-lookup"><span data-stu-id="958f7-194">12</span></span>     | <span data-ttu-id="958f7-195">12</span><span class="sxs-lookup"><span data-stu-id="958f7-195">12</span></span>     |        |        |        |
| <span data-ttu-id="958f7-196">\_RGB16 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-196">GL\_RGB16</span></span>                | <span data-ttu-id="958f7-197">16</span><span class="sxs-lookup"><span data-stu-id="958f7-197">16</span></span>     | <span data-ttu-id="958f7-198">16</span><span class="sxs-lookup"><span data-stu-id="958f7-198">16</span></span>     | <span data-ttu-id="958f7-199">16</span><span class="sxs-lookup"><span data-stu-id="958f7-199">16</span></span>     |        |        |        |
| <span data-ttu-id="958f7-200">Se \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="958f7-200">GL\_RGBA</span></span>                 |        |        |        |        |        |        |
| <span data-ttu-id="958f7-201">\_RGBA2 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-201">GL\_RGBA2</span></span>                | <span data-ttu-id="958f7-202">2</span><span class="sxs-lookup"><span data-stu-id="958f7-202">2</span></span>      | <span data-ttu-id="958f7-203">2</span><span class="sxs-lookup"><span data-stu-id="958f7-203">2</span></span>      | <span data-ttu-id="958f7-204">2</span><span class="sxs-lookup"><span data-stu-id="958f7-204">2</span></span>      | <span data-ttu-id="958f7-205">2</span><span class="sxs-lookup"><span data-stu-id="958f7-205">2</span></span>      |        |        |
| <span data-ttu-id="958f7-206">\_RGBA4 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-206">GL\_RGBA4</span></span>                | <span data-ttu-id="958f7-207">4</span><span class="sxs-lookup"><span data-stu-id="958f7-207">4</span></span>      | <span data-ttu-id="958f7-208">4</span><span class="sxs-lookup"><span data-stu-id="958f7-208">4</span></span>      | <span data-ttu-id="958f7-209">4</span><span class="sxs-lookup"><span data-stu-id="958f7-209">4</span></span>      | <span data-ttu-id="958f7-210">4</span><span class="sxs-lookup"><span data-stu-id="958f7-210">4</span></span>      |        |        |
| <span data-ttu-id="958f7-211">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="958f7-211">GL\_RGB5\_A1</span></span>             | <span data-ttu-id="958f7-212">5</span><span class="sxs-lookup"><span data-stu-id="958f7-212">5</span></span>      | <span data-ttu-id="958f7-213">5</span><span class="sxs-lookup"><span data-stu-id="958f7-213">5</span></span>      | <span data-ttu-id="958f7-214">5</span><span class="sxs-lookup"><span data-stu-id="958f7-214">5</span></span>      | <span data-ttu-id="958f7-215">1</span><span class="sxs-lookup"><span data-stu-id="958f7-215">1</span></span>      |        |        |
| <span data-ttu-id="958f7-216">\_RGBA8 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-216">GL\_RGBA8</span></span>                | <span data-ttu-id="958f7-217">8</span><span class="sxs-lookup"><span data-stu-id="958f7-217">8</span></span>      | <span data-ttu-id="958f7-218">8</span><span class="sxs-lookup"><span data-stu-id="958f7-218">8</span></span>      | <span data-ttu-id="958f7-219">8</span><span class="sxs-lookup"><span data-stu-id="958f7-219">8</span></span>      | <span data-ttu-id="958f7-220">8</span><span class="sxs-lookup"><span data-stu-id="958f7-220">8</span></span>      |        |        |
| <span data-ttu-id="958f7-221">GL \_ RGB10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="958f7-221">GL\_RGB10\_A2</span></span>            | <span data-ttu-id="958f7-222">10</span><span class="sxs-lookup"><span data-stu-id="958f7-222">10</span></span>     | <span data-ttu-id="958f7-223">10</span><span class="sxs-lookup"><span data-stu-id="958f7-223">10</span></span>     | <span data-ttu-id="958f7-224">10</span><span class="sxs-lookup"><span data-stu-id="958f7-224">10</span></span>     | <span data-ttu-id="958f7-225">2</span><span class="sxs-lookup"><span data-stu-id="958f7-225">2</span></span>      |        |        |
| <span data-ttu-id="958f7-226">\_RGBA12 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-226">GL\_RGBA12</span></span>               | <span data-ttu-id="958f7-227">12</span><span class="sxs-lookup"><span data-stu-id="958f7-227">12</span></span>     | <span data-ttu-id="958f7-228">12</span><span class="sxs-lookup"><span data-stu-id="958f7-228">12</span></span>     | <span data-ttu-id="958f7-229">12</span><span class="sxs-lookup"><span data-stu-id="958f7-229">12</span></span>     | <span data-ttu-id="958f7-230">12</span><span class="sxs-lookup"><span data-stu-id="958f7-230">12</span></span>     |        |        |
| <span data-ttu-id="958f7-231">\_RGBA16 GL</span><span class="sxs-lookup"><span data-stu-id="958f7-231">GL\_RGBA16</span></span>               | <span data-ttu-id="958f7-232">16</span><span class="sxs-lookup"><span data-stu-id="958f7-232">16</span></span>     | <span data-ttu-id="958f7-233">16</span><span class="sxs-lookup"><span data-stu-id="958f7-233">16</span></span>     | <span data-ttu-id="958f7-234">16</span><span class="sxs-lookup"><span data-stu-id="958f7-234">16</span></span>     | <span data-ttu-id="958f7-235">16</span><span class="sxs-lookup"><span data-stu-id="958f7-235">16</span></span>     |        |        |



 

</dd> <dt>

<span data-ttu-id="958f7-236">*x*</span><span class="sxs-lookup"><span data-stu-id="958f7-236">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="958f7-237">A coordenada do plano x da janela do canto inferior esquerdo da linha de pixels a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="958f7-237">The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="958f7-238">*y*</span><span class="sxs-lookup"><span data-stu-id="958f7-238">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="958f7-239">A coordenada de plano y da janela do canto inferior esquerdo da linha de pixels a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="958f7-239">The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="958f7-240">*width*</span><span class="sxs-lookup"><span data-stu-id="958f7-240">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="958f7-241">A largura da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="958f7-241">The width of the texture image.</span></span> <span data-ttu-id="958f7-242">Deve ser zero ou 2n + 2 (*Border*) para algum número inteiro *n*.</span><span class="sxs-lookup"><span data-stu-id="958f7-242">Must be zero or 2n + 2(*border*) for some integer *n*.</span></span> <span data-ttu-id="958f7-243">A altura da imagem de textura é 1.</span><span class="sxs-lookup"><span data-stu-id="958f7-243">The height of the texture image is 1.</span></span>

</dd> <dt>

<span data-ttu-id="958f7-244">*borda*</span><span class="sxs-lookup"><span data-stu-id="958f7-244">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="958f7-245">A largura da borda.</span><span class="sxs-lookup"><span data-stu-id="958f7-245">The width of the border.</span></span> <span data-ttu-id="958f7-246">Deve ser zero ou 1.</span><span class="sxs-lookup"><span data-stu-id="958f7-246">Must be either zero or 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="958f7-247">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="958f7-247">Return value</span></span>

<span data-ttu-id="958f7-248">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="958f7-248">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="958f7-249">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="958f7-249">Error codes</span></span>

<span data-ttu-id="958f7-250">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="958f7-250">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="958f7-251">Nome</span><span class="sxs-lookup"><span data-stu-id="958f7-251">Name</span></span>                                                                                                  | <span data-ttu-id="958f7-252">Significado</span><span class="sxs-lookup"><span data-stu-id="958f7-252">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="958f7-253"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="958f7-253"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="958f7-254">o *destino* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="958f7-254">*target* was not an accepted value.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="958f7-255"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="958f7-255"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="958f7-256">o *nível* era menor que zero ou maior que log2 *Max*, em que *Max* é o valor RETORNADO de \_ tamanho de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="958f7-256">*level* was less than zero or greater than log2 *max*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                           |
| <dl> <span data-ttu-id="958f7-257"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="958f7-257"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="958f7-258">a *borda* não era zero ou 1.</span><span class="sxs-lookup"><span data-stu-id="958f7-258">*border* was not zero or 1.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="958f7-259"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="958f7-259"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="958f7-260">*a largura* era menor que zero, maior que 2 + \_ GL tamanho máximo de \_ textura \_ ou a *largura* não pode ser representada como 2n + (*Border*) para algum número inteiro *n*.</span><span class="sxs-lookup"><span data-stu-id="958f7-260">*width* was less than zero, greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or *width* cannot be represented as 2n +(*border*) for some integer *n*.</span></span><br/> |
| <dl> <span data-ttu-id="958f7-261"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="958f7-261"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="958f7-262">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="958f7-262">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                    |



## <a name="remarks"></a><span data-ttu-id="958f7-263">Comentários</span><span class="sxs-lookup"><span data-stu-id="958f7-263">Remarks</span></span>

<span data-ttu-id="958f7-264">A função **glCopyTexImage1D** define uma imagem de textura unidimensional usando pixels do framebuffer atual, em vez de memória principal, como é o caso para [**glTexImage1D**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="958f7-264">The **glCopyTexImage1D** function defines a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexImage1D**](glteximage1d.md).</span></span>

<span data-ttu-id="958f7-265">Usando o nível de mipmap especificado com o *nível*, as matrizes de textura são definidas como uma linha de pixel alinhada ao canto inferior esquerdo da janela nas coordenadas especificadas por *x* e *y*, com um comprimento igual à *largura* + 2 \* *borda*.</span><span class="sxs-lookup"><span data-stu-id="958f7-265">Using the mipmap level specified with *level*, texture arrays are defined as a pixel row aligned with the lower-left corner of the window at the coordinates specified by *x* and *y*, with a length equal to *width* + 2 \* *border*.</span></span> <span data-ttu-id="958f7-266">O formato interno da matriz de textura é especificado com o parâmetro *internalFormat* .</span><span class="sxs-lookup"><span data-stu-id="958f7-266">The internal format of the texture array is specified with the *internalFormat* parameter.</span></span>

<span data-ttu-id="958f7-267">A função **glCopyTexImage1D** processa os pixels em uma linha da mesma maneira que [**glCopyPixels**](glcopypixels.md), exceto que antes da conversão final dos pixels, todos os valores de componentes de pixel são clamped para o intervalo de \[ 0, 1 \] e convertidos para o formato interno da textura para armazenamento na matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="958f7-267">The **glCopyTexImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md), except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="958f7-268">A ordenação de pixels é determinada com coordenadas *x* inferiores correspondentes às coordenadas de textura inferiores.</span><span class="sxs-lookup"><span data-stu-id="958f7-268">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="958f7-269">Se qualquer um dos pixels dentro de uma linha especificada da framebuffer atual estiver fora da janela associada ao contexto de renderização atual, seus valores serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="958f7-269">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="958f7-270">Você não pode incluir chamadas para **glCopyTexImage1D** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="958f7-270">You cannot include calls to **glCopyTexImage1D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="958f7-271">A função **glCopyTexImage1D** só está disponível no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="958f7-271">The **glCopyTexImage1D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="958f7-272">Texturing não tem efeito no modo de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="958f7-272">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="958f7-273">As funções [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) afetam as imagens de textura exatamente como elas afetam o [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="958f7-273">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="958f7-274">A função a seguir recupera informações relacionadas a **glCopyTexImage1D**:</span><span class="sxs-lookup"><span data-stu-id="958f7-274">The following function retrieves information related to **glCopyTexImage1D**:</span></span>

<span data-ttu-id="958f7-275">[**glIsEnabled**](glisenabled.md) com a textura do argumento GL \_ \_ 1D</span><span class="sxs-lookup"><span data-stu-id="958f7-275">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="958f7-276">Requisitos</span><span class="sxs-lookup"><span data-stu-id="958f7-276">Requirements</span></span>



| <span data-ttu-id="958f7-277">Requisito</span><span class="sxs-lookup"><span data-stu-id="958f7-277">Requirement</span></span> | <span data-ttu-id="958f7-278">Valor</span><span class="sxs-lookup"><span data-stu-id="958f7-278">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="958f7-279">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="958f7-279">Minimum supported client</span></span><br/> | <span data-ttu-id="958f7-280">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="958f7-280">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="958f7-281">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="958f7-281">Minimum supported server</span></span><br/> | <span data-ttu-id="958f7-282">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="958f7-282">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="958f7-283">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="958f7-283">Header</span></span><br/>                   | <dl> <span data-ttu-id="958f7-284"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="958f7-284"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="958f7-285">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="958f7-285">Library</span></span><br/>                  | <dl> <span data-ttu-id="958f7-286"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="958f7-286"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="958f7-287">DLL</span><span class="sxs-lookup"><span data-stu-id="958f7-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="958f7-288"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="958f7-288"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="958f7-289">Confira também</span><span class="sxs-lookup"><span data-stu-id="958f7-289">See also</span></span>

<dl> <dt>

[<span data-ttu-id="958f7-290">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="958f7-290">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="958f7-291">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="958f7-291">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="958f7-292">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="958f7-292">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="958f7-293">**glFog**</span><span class="sxs-lookup"><span data-stu-id="958f7-293">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="958f7-294">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="958f7-294">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="958f7-295">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="958f7-295">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="958f7-296">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="958f7-296">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="958f7-297">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="958f7-297">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="958f7-298">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="958f7-298">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="958f7-299">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="958f7-299">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="958f7-300">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="958f7-300">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





