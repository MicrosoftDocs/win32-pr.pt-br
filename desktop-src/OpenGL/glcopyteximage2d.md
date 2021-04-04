---
title: função glCopyTexImage2D (GL. h)
description: A função glCopyTexImage2D copia os pixels da framebuffer em uma imagem de textura bidimensional.
ms.assetid: 4b9d7be6-054d-4590-b3f0-a2a670786c4b
keywords:
- função glCopyTexImage2D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d04a979e9bb026da904687506f3201d12c12c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824494"
---
# <a name="glcopyteximage2d-function"></a><span data-ttu-id="a931f-104">função glCopyTexImage2D</span><span class="sxs-lookup"><span data-stu-id="a931f-104">glCopyTexImage2D function</span></span>

<span data-ttu-id="a931f-105">A função **glCopyTexImage2D** copia os pixels da framebuffer em uma imagem de textura bidimensional.</span><span class="sxs-lookup"><span data-stu-id="a931f-105">The **glCopyTexImage2D** function copies pixels from the framebuffer into a two-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="a931f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a931f-106">Syntax</span></span>


```C++
void WINAPI glCopyTexImage2D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLint   border
);
```



## <a name="parameters"></a><span data-ttu-id="a931f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a931f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a931f-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="a931f-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="a931f-109">O destino para o qual os dados da imagem serão alterados.</span><span class="sxs-lookup"><span data-stu-id="a931f-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="a931f-110">Deve ter o valor GL de \_ textura \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="a931f-110">Must have the value GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="a931f-111">*level*</span><span class="sxs-lookup"><span data-stu-id="a931f-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="a931f-112">O número de nível de detalhe.</span><span class="sxs-lookup"><span data-stu-id="a931f-112">The level-of-detail number.</span></span> <span data-ttu-id="a931f-113">Nível 0 é a imagem base.</span><span class="sxs-lookup"><span data-stu-id="a931f-113">Level 0 is the base image.</span></span> <span data-ttu-id="a931f-114">O nível *n* é a imagem de redução *n* º mipmap.</span><span class="sxs-lookup"><span data-stu-id="a931f-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="a931f-115">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="a931f-115">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="a931f-116">O formato interno e a resolução dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="a931f-116">The internal format and resolution of the texture data.</span></span> <span data-ttu-id="a931f-117">Os valores 1, 2, 3 e 4 não são aceitos para *internalFormat*.</span><span class="sxs-lookup"><span data-stu-id="a931f-117">The values 1, 2, 3, and 4 are not accepted for *internalFormat*.</span></span> <span data-ttu-id="a931f-118">O parâmetro pode assumir um dos valores simbólicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a931f-118">The parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="a931f-119">Constante</span><span class="sxs-lookup"><span data-stu-id="a931f-119">Constant</span></span>                 | <span data-ttu-id="a931f-120">Bits de R</span><span class="sxs-lookup"><span data-stu-id="a931f-120">R Bits</span></span> | <span data-ttu-id="a931f-121">G bits</span><span class="sxs-lookup"><span data-stu-id="a931f-121">G Bits</span></span> | <span data-ttu-id="a931f-122">Bits B</span><span class="sxs-lookup"><span data-stu-id="a931f-122">B Bits</span></span> | <span data-ttu-id="a931f-123">Um bits</span><span class="sxs-lookup"><span data-stu-id="a931f-123">A Bits</span></span> | <span data-ttu-id="a931f-124">Bits L</span><span class="sxs-lookup"><span data-stu-id="a931f-124">L Bits</span></span> | <span data-ttu-id="a931f-125">I bits</span><span class="sxs-lookup"><span data-stu-id="a931f-125">I Bits</span></span> |
|--------------------------|--------|--------|--------|--------|--------|--------|
| <span data-ttu-id="a931f-126">GL \_ alfa</span><span class="sxs-lookup"><span data-stu-id="a931f-126">GL\_ALPHA</span></span>                |        |        |        |        |        |        |
| <span data-ttu-id="a931f-127">\_ALPHA4 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-127">GL\_ALPHA4</span></span>               |        |        |        | <span data-ttu-id="a931f-128">4</span><span class="sxs-lookup"><span data-stu-id="a931f-128">4</span></span>      |        |        |
| <span data-ttu-id="a931f-129">\_ALPHA8 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-129">GL\_ALPHA8</span></span>               |        |        |        | <span data-ttu-id="a931f-130">8</span><span class="sxs-lookup"><span data-stu-id="a931f-130">8</span></span>      |        |        |
| <span data-ttu-id="a931f-131">\_ALPHA12 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-131">GL\_ALPHA12</span></span>              |        |        |        | <span data-ttu-id="a931f-132">12</span><span class="sxs-lookup"><span data-stu-id="a931f-132">12</span></span>     |        |        |
| <span data-ttu-id="a931f-133">\_ALPHA16 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-133">GL\_ALPHA16</span></span>              |        |        |        | <span data-ttu-id="a931f-134">16</span><span class="sxs-lookup"><span data-stu-id="a931f-134">16</span></span>     |        |        |
| <span data-ttu-id="a931f-135">\_luminância GL</span><span class="sxs-lookup"><span data-stu-id="a931f-135">GL\_LUMINANCE</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="a931f-136">\_LUMINANCE4 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-136">GL\_LUMINANCE4</span></span>           |        |        |        |        | <span data-ttu-id="a931f-137">4</span><span class="sxs-lookup"><span data-stu-id="a931f-137">4</span></span>      |        |
| <span data-ttu-id="a931f-138">\_LUMINANCE8 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-138">GL\_LUMINANCE8</span></span>           |        |        |        |        | <span data-ttu-id="a931f-139">8</span><span class="sxs-lookup"><span data-stu-id="a931f-139">8</span></span>      |        |
| <span data-ttu-id="a931f-140">\_LUMINANCE12 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-140">GL\_LUMINANCE12</span></span>          |        |        |        |        | <span data-ttu-id="a931f-141">12</span><span class="sxs-lookup"><span data-stu-id="a931f-141">12</span></span>     |        |
| <span data-ttu-id="a931f-142">\_LUMINANCE16 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-142">GL\_LUMINANCE16</span></span>          |        |        |        |        | <span data-ttu-id="a931f-143">16</span><span class="sxs-lookup"><span data-stu-id="a931f-143">16</span></span>     |        |
| <span data-ttu-id="a931f-144">luminância do GL \_ \_ alfa</span><span class="sxs-lookup"><span data-stu-id="a931f-144">GL\_LUMINANCE\_ALPHA</span></span>     |        |        |        |        |        |        |
| <span data-ttu-id="a931f-145">GL \_ LUMINANCE4 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="a931f-145">GL\_LUMINANCE4\_ALPHA4</span></span>   |        |        |        | <span data-ttu-id="a931f-146">4</span><span class="sxs-lookup"><span data-stu-id="a931f-146">4</span></span>      | <span data-ttu-id="a931f-147">4</span><span class="sxs-lookup"><span data-stu-id="a931f-147">4</span></span>      |        |
| <span data-ttu-id="a931f-148">GL \_ LUMINANCE6 \_ ALPHA2</span><span class="sxs-lookup"><span data-stu-id="a931f-148">GL\_LUMINANCE6\_ALPHA2</span></span>   |        |        |        | <span data-ttu-id="a931f-149">2</span><span class="sxs-lookup"><span data-stu-id="a931f-149">2</span></span>      | <span data-ttu-id="a931f-150">6</span><span class="sxs-lookup"><span data-stu-id="a931f-150">6</span></span>      |        |
| <span data-ttu-id="a931f-151">GL \_ LUMINANCE8 \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="a931f-151">GL\_LUMINANCE8\_ALPHA8</span></span>   |        |        |        | <span data-ttu-id="a931f-152">8</span><span class="sxs-lookup"><span data-stu-id="a931f-152">8</span></span>      | <span data-ttu-id="a931f-153">8</span><span class="sxs-lookup"><span data-stu-id="a931f-153">8</span></span>      |        |
| <span data-ttu-id="a931f-154">GL \_ LUMINANCE12 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="a931f-154">GL\_LUMINANCE12\_ALPHA4</span></span>  |        |        |        | <span data-ttu-id="a931f-155">4</span><span class="sxs-lookup"><span data-stu-id="a931f-155">4</span></span>      | <span data-ttu-id="a931f-156">12</span><span class="sxs-lookup"><span data-stu-id="a931f-156">12</span></span>     |        |
| <span data-ttu-id="a931f-157">GL \_ LUMINANCE12 \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="a931f-157">GL\_LUMINANCE12\_ALPHA12</span></span> |        |        |        | <span data-ttu-id="a931f-158">12</span><span class="sxs-lookup"><span data-stu-id="a931f-158">12</span></span>     | <span data-ttu-id="a931f-159">12</span><span class="sxs-lookup"><span data-stu-id="a931f-159">12</span></span>     |        |
| <span data-ttu-id="a931f-160">GL \_ LUMINANCE16 \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="a931f-160">GL\_LUMINANCE16\_ALPHA16</span></span> |        |        |        | <span data-ttu-id="a931f-161">16</span><span class="sxs-lookup"><span data-stu-id="a931f-161">16</span></span>     | <span data-ttu-id="a931f-162">16</span><span class="sxs-lookup"><span data-stu-id="a931f-162">16</span></span>     |        |
| <span data-ttu-id="a931f-163">intensidade do GL \_</span><span class="sxs-lookup"><span data-stu-id="a931f-163">GL\_INTENSITY</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="a931f-164">\_INTENSITY4 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-164">GL\_INTENSITY4</span></span>           |        |        |        |        |        | <span data-ttu-id="a931f-165">4</span><span class="sxs-lookup"><span data-stu-id="a931f-165">4</span></span>      |
| <span data-ttu-id="a931f-166">\_INTENSITY8 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-166">GL\_INTENSITY8</span></span>           |        |        |        |        |        | <span data-ttu-id="a931f-167">8</span><span class="sxs-lookup"><span data-stu-id="a931f-167">8</span></span>      |
| <span data-ttu-id="a931f-168">\_INTENSITY12 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-168">GL\_INTENSITY12</span></span>          |        |        |        |        |        | <span data-ttu-id="a931f-169">12</span><span class="sxs-lookup"><span data-stu-id="a931f-169">12</span></span>     |
| <span data-ttu-id="a931f-170">\_INTENSITY16 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-170">GL\_INTENSITY16</span></span>          |        |        |        |        |        | <span data-ttu-id="a931f-171">16</span><span class="sxs-lookup"><span data-stu-id="a931f-171">16</span></span>     |
| <span data-ttu-id="a931f-172">GL em \_ RGB</span><span class="sxs-lookup"><span data-stu-id="a931f-172">GL\_RGB</span></span>                  |        |        |        |        |        |        |
| <span data-ttu-id="a931f-173">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="a931f-173">GL\_R3\_G3\_B2</span></span>           | <span data-ttu-id="a931f-174">3</span><span class="sxs-lookup"><span data-stu-id="a931f-174">3</span></span>      | <span data-ttu-id="a931f-175">3</span><span class="sxs-lookup"><span data-stu-id="a931f-175">3</span></span>      | <span data-ttu-id="a931f-176">2</span><span class="sxs-lookup"><span data-stu-id="a931f-176">2</span></span>      |        |        |        |
| <span data-ttu-id="a931f-177">\_RGB4 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-177">GL\_RGB4</span></span>                 | <span data-ttu-id="a931f-178">4</span><span class="sxs-lookup"><span data-stu-id="a931f-178">4</span></span>      | <span data-ttu-id="a931f-179">4</span><span class="sxs-lookup"><span data-stu-id="a931f-179">4</span></span>      | <span data-ttu-id="a931f-180">4</span><span class="sxs-lookup"><span data-stu-id="a931f-180">4</span></span>      |        |        |        |
| <span data-ttu-id="a931f-181">\_RGB5 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-181">GL\_RGB5</span></span>                 | <span data-ttu-id="a931f-182">5</span><span class="sxs-lookup"><span data-stu-id="a931f-182">5</span></span>      | <span data-ttu-id="a931f-183">5</span><span class="sxs-lookup"><span data-stu-id="a931f-183">5</span></span>      | <span data-ttu-id="a931f-184">5</span><span class="sxs-lookup"><span data-stu-id="a931f-184">5</span></span>      |        |        |        |
| <span data-ttu-id="a931f-185">\_RGB8 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-185">GL\_RGB8</span></span>                 | <span data-ttu-id="a931f-186">8</span><span class="sxs-lookup"><span data-stu-id="a931f-186">8</span></span>      | <span data-ttu-id="a931f-187">8</span><span class="sxs-lookup"><span data-stu-id="a931f-187">8</span></span>      | <span data-ttu-id="a931f-188">8</span><span class="sxs-lookup"><span data-stu-id="a931f-188">8</span></span>      |        |        |        |
| <span data-ttu-id="a931f-189">\_RGB10 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-189">GL\_RGB10</span></span>                | <span data-ttu-id="a931f-190">10</span><span class="sxs-lookup"><span data-stu-id="a931f-190">10</span></span>     | <span data-ttu-id="a931f-191">10</span><span class="sxs-lookup"><span data-stu-id="a931f-191">10</span></span>     | <span data-ttu-id="a931f-192">10</span><span class="sxs-lookup"><span data-stu-id="a931f-192">10</span></span>     |        |        |        |
| <span data-ttu-id="a931f-193">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-193">GL\_RGB12</span></span>                | <span data-ttu-id="a931f-194">12</span><span class="sxs-lookup"><span data-stu-id="a931f-194">12</span></span>     | <span data-ttu-id="a931f-195">12</span><span class="sxs-lookup"><span data-stu-id="a931f-195">12</span></span>     | <span data-ttu-id="a931f-196">12</span><span class="sxs-lookup"><span data-stu-id="a931f-196">12</span></span>     |        |        |        |
| <span data-ttu-id="a931f-197">\_RGB16 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-197">GL\_RGB16</span></span>                | <span data-ttu-id="a931f-198">16</span><span class="sxs-lookup"><span data-stu-id="a931f-198">16</span></span>     | <span data-ttu-id="a931f-199">16</span><span class="sxs-lookup"><span data-stu-id="a931f-199">16</span></span>     | <span data-ttu-id="a931f-200">16</span><span class="sxs-lookup"><span data-stu-id="a931f-200">16</span></span>     |        |        |        |
| <span data-ttu-id="a931f-201">Se \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="a931f-201">GL\_RGBA</span></span>                 |        |        |        |        |        |        |
| <span data-ttu-id="a931f-202">\_RGBA2 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-202">GL\_RGBA2</span></span>                | <span data-ttu-id="a931f-203">2</span><span class="sxs-lookup"><span data-stu-id="a931f-203">2</span></span>      | <span data-ttu-id="a931f-204">2</span><span class="sxs-lookup"><span data-stu-id="a931f-204">2</span></span>      | <span data-ttu-id="a931f-205">2</span><span class="sxs-lookup"><span data-stu-id="a931f-205">2</span></span>      | <span data-ttu-id="a931f-206">2</span><span class="sxs-lookup"><span data-stu-id="a931f-206">2</span></span>      |        |        |
| <span data-ttu-id="a931f-207">\_RGBA4 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-207">GL\_RGBA4</span></span>                | <span data-ttu-id="a931f-208">4</span><span class="sxs-lookup"><span data-stu-id="a931f-208">4</span></span>      | <span data-ttu-id="a931f-209">4</span><span class="sxs-lookup"><span data-stu-id="a931f-209">4</span></span>      | <span data-ttu-id="a931f-210">4</span><span class="sxs-lookup"><span data-stu-id="a931f-210">4</span></span>      | <span data-ttu-id="a931f-211">4</span><span class="sxs-lookup"><span data-stu-id="a931f-211">4</span></span>      |        |        |
| <span data-ttu-id="a931f-212">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="a931f-212">GL\_RGB5\_A1</span></span>             | <span data-ttu-id="a931f-213">5</span><span class="sxs-lookup"><span data-stu-id="a931f-213">5</span></span>      | <span data-ttu-id="a931f-214">5</span><span class="sxs-lookup"><span data-stu-id="a931f-214">5</span></span>      | <span data-ttu-id="a931f-215">5</span><span class="sxs-lookup"><span data-stu-id="a931f-215">5</span></span>      | <span data-ttu-id="a931f-216">1</span><span class="sxs-lookup"><span data-stu-id="a931f-216">1</span></span>      |        |        |
| <span data-ttu-id="a931f-217">\_RGBA8 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-217">GL\_RGBA8</span></span>                | <span data-ttu-id="a931f-218">8</span><span class="sxs-lookup"><span data-stu-id="a931f-218">8</span></span>      | <span data-ttu-id="a931f-219">8</span><span class="sxs-lookup"><span data-stu-id="a931f-219">8</span></span>      | <span data-ttu-id="a931f-220">8</span><span class="sxs-lookup"><span data-stu-id="a931f-220">8</span></span>      | <span data-ttu-id="a931f-221">8</span><span class="sxs-lookup"><span data-stu-id="a931f-221">8</span></span>      |        |        |
| <span data-ttu-id="a931f-222">GL \_ RGB10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="a931f-222">GL\_RGB10\_A2</span></span>            | <span data-ttu-id="a931f-223">10</span><span class="sxs-lookup"><span data-stu-id="a931f-223">10</span></span>     | <span data-ttu-id="a931f-224">10</span><span class="sxs-lookup"><span data-stu-id="a931f-224">10</span></span>     | <span data-ttu-id="a931f-225">10</span><span class="sxs-lookup"><span data-stu-id="a931f-225">10</span></span>     | <span data-ttu-id="a931f-226">2</span><span class="sxs-lookup"><span data-stu-id="a931f-226">2</span></span>      |        |        |
| <span data-ttu-id="a931f-227">\_RGBA12 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-227">GL\_RGBA12</span></span>               | <span data-ttu-id="a931f-228">12</span><span class="sxs-lookup"><span data-stu-id="a931f-228">12</span></span>     | <span data-ttu-id="a931f-229">12</span><span class="sxs-lookup"><span data-stu-id="a931f-229">12</span></span>     | <span data-ttu-id="a931f-230">12</span><span class="sxs-lookup"><span data-stu-id="a931f-230">12</span></span>     | <span data-ttu-id="a931f-231">12</span><span class="sxs-lookup"><span data-stu-id="a931f-231">12</span></span>     |        |        |
| <span data-ttu-id="a931f-232">\_RGBA16 GL</span><span class="sxs-lookup"><span data-stu-id="a931f-232">GL\_RGBA16</span></span>               | <span data-ttu-id="a931f-233">16</span><span class="sxs-lookup"><span data-stu-id="a931f-233">16</span></span>     | <span data-ttu-id="a931f-234">16</span><span class="sxs-lookup"><span data-stu-id="a931f-234">16</span></span>     | <span data-ttu-id="a931f-235">16</span><span class="sxs-lookup"><span data-stu-id="a931f-235">16</span></span>     | <span data-ttu-id="a931f-236">16</span><span class="sxs-lookup"><span data-stu-id="a931f-236">16</span></span>     |        |        |



 

</dd> <dt>

<span data-ttu-id="a931f-237">*x*</span><span class="sxs-lookup"><span data-stu-id="a931f-237">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="a931f-238">A coordenada de plano x do canto inferior esquerdo da região retangular de pixels a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="a931f-238">The window x-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="a931f-239">*y*</span><span class="sxs-lookup"><span data-stu-id="a931f-239">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="a931f-240">A coordenada de plano y da janela do canto inferior esquerdo da região retangular de pixels a serem copiados.</span><span class="sxs-lookup"><span data-stu-id="a931f-240">The window y-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="a931f-241">*width*</span><span class="sxs-lookup"><span data-stu-id="a931f-241">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="a931f-242">A largura da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="a931f-242">The width of the texture image.</span></span> <span data-ttu-id="a931f-243">Deve ser 2n + 2 \* *Border* para um inteiro *n*.</span><span class="sxs-lookup"><span data-stu-id="a931f-243">Must be 2n + 2 \* *border* for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="a931f-244">*altura*</span><span class="sxs-lookup"><span data-stu-id="a931f-244">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="a931f-245">A altura da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="a931f-245">The height of the texture image.</span></span> <span data-ttu-id="a931f-246">Deve ser 2n + 2 \* *Border* para um inteiro *n*.</span><span class="sxs-lookup"><span data-stu-id="a931f-246">Must be 2n + 2 \* *border* for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="a931f-247">*borda*</span><span class="sxs-lookup"><span data-stu-id="a931f-247">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="a931f-248">A largura da borda.</span><span class="sxs-lookup"><span data-stu-id="a931f-248">The width of the border.</span></span> <span data-ttu-id="a931f-249">Deve ser zero ou 1.</span><span class="sxs-lookup"><span data-stu-id="a931f-249">Must be either zero or 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a931f-250">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a931f-250">Return value</span></span>

<span data-ttu-id="a931f-251">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a931f-251">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a931f-252">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a931f-252">Error codes</span></span>

<span data-ttu-id="a931f-253">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a931f-253">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a931f-254">Nome</span><span class="sxs-lookup"><span data-stu-id="a931f-254">Name</span></span>                                                                                                  | <span data-ttu-id="a931f-255">Significado</span><span class="sxs-lookup"><span data-stu-id="a931f-255">Meaning</span></span>                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a931f-256"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="a931f-256"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a931f-257">o *destino* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="a931f-257">*target* was not an accepted value.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="a931f-258"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a931f-258"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a931f-259">o *nível* era menor que zero ou maior que log2 *Max*, em que *Max* é o valor RETORNADO de \_ tamanho de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a931f-259">*level* was less than zero or greater than log2 *max*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                               |
| <dl> <span data-ttu-id="a931f-260"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a931f-260"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a931f-261">a *borda* não era zero ou 1.</span><span class="sxs-lookup"><span data-stu-id="a931f-261">*border* was not zero or 1.</span></span><br/>                                                                                                                       |
| <dl> <span data-ttu-id="a931f-262"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a931f-262"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a931f-263">a *largura* era menor que zero, maior que 2 + GL \_ tamanho máximo de \_ textura \_ ou a *largura* não pode ser representada como 2n + 2 \* *Border* para um inteiro *n*.</span><span class="sxs-lookup"><span data-stu-id="a931f-263">*width* was less than zero, greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or *width* cannot be represented as 2n + 2 \* *border* for some integer *n*.</span></span><br/> |
| <dl> <span data-ttu-id="a931f-264"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a931f-264"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a931f-265">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a931f-265">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="a931f-266">Comentários</span><span class="sxs-lookup"><span data-stu-id="a931f-266">Remarks</span></span>

<span data-ttu-id="a931f-267">A função **glCopyTexImage2D** define uma imagem de textura bidimensional usando pixels do framebuffer atual, em vez de memória principal, como é o caso para [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="a931f-267">The **glCopyTexImage2D** function defines a two-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexImage2D**](glteximage2d.md).</span></span>

<span data-ttu-id="a931f-268">Usando o nível de mipmap especificado com o *nível*, as matrizes de textura são definidas como um retângulo de pixels com o canto inferior esquerdo localizado nas coordenadas *x* e *y*, largura igual à *largura* + (2 \* *borda*) e uma altura igual à *altura* + (2 \* *borda*).</span><span class="sxs-lookup"><span data-stu-id="a931f-268">Using the mipmap level specified with *level*, texture arrays are defined as a rectangle of pixels with the lower-left corner located at the coordinates *x* and *y*, width equal to *width* + (2 \* *border*), and a height equal to *height* + (2 \* *border*).</span></span> <span data-ttu-id="a931f-269">O formato interno da matriz de textura é especificado com o parâmetro *internalFormat* .</span><span class="sxs-lookup"><span data-stu-id="a931f-269">The internal format of the texture array is specified with the *internalFormat* parameter.</span></span>

<span data-ttu-id="a931f-270">A função **glCopyTexImage2D** processa os pixels em uma linha da mesma maneira que [**glCopyPixels**](glcopypixels.md) , exceto que antes da conversão final dos pixels, todos os valores de componentes de pixel são clamped para o intervalo de \[ 0, 1 \] e convertidos para o formato interno da textura para armazenamento na matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="a931f-270">The **glCopyTexImage2D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="a931f-271">A ordenação de pixels é determinada com coordenadas *x* e *y* inferiores correspondentes às coordenadas de textura *s* e *t* inferiores.</span><span class="sxs-lookup"><span data-stu-id="a931f-271">Pixel ordering is determined with lower *x* and *y* coordinates corresponding to lower *s* and *t* texture coordinates.</span></span> <span data-ttu-id="a931f-272">Se qualquer um dos pixels dentro de uma linha especificada da framebuffer atual estiver fora da janela associada ao contexto de renderização atual, seus valores serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="a931f-272">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="a931f-273">Você não pode incluir chamadas para **glCopyTexImage2D** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="a931f-273">You cannot include calls to **glCopyTexImage2D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="a931f-274">A função **glCopyTexImage2D** só está disponível no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a931f-274">The **glCopyTexImage2D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="a931f-275">Texturing não tem efeito no modo de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="a931f-275">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="a931f-276">As funções [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) afetam as imagens de textura exatamente como elas afetam o [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="a931f-276">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="a931f-277">A função a seguir recupera informações relacionadas a **glCopyTexImage2D**:</span><span class="sxs-lookup"><span data-stu-id="a931f-277">The following function retrieves information related to **glCopyTexImage2D**:</span></span>

<span data-ttu-id="a931f-278">[**glIsEnabled**](glisenabled.md) com a textura do argumento GL \_ \_ 2D</span><span class="sxs-lookup"><span data-stu-id="a931f-278">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="a931f-279">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a931f-279">Requirements</span></span>



| <span data-ttu-id="a931f-280">Requisito</span><span class="sxs-lookup"><span data-stu-id="a931f-280">Requirement</span></span> | <span data-ttu-id="a931f-281">Valor</span><span class="sxs-lookup"><span data-stu-id="a931f-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a931f-282">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a931f-282">Minimum supported client</span></span><br/> | <span data-ttu-id="a931f-283">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a931f-283">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a931f-284">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a931f-284">Minimum supported server</span></span><br/> | <span data-ttu-id="a931f-285">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a931f-285">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a931f-286">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a931f-286">Header</span></span><br/>                   | <dl> <span data-ttu-id="a931f-287"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a931f-287"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a931f-288">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a931f-288">Library</span></span><br/>                  | <dl> <span data-ttu-id="a931f-289"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a931f-289"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a931f-290">DLL</span><span class="sxs-lookup"><span data-stu-id="a931f-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a931f-291"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a931f-291"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a931f-292">Confira também</span><span class="sxs-lookup"><span data-stu-id="a931f-292">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a931f-293">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a931f-293">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a931f-294">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="a931f-294">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="a931f-295">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="a931f-295">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="a931f-296">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a931f-296">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a931f-297">**glFog**</span><span class="sxs-lookup"><span data-stu-id="a931f-297">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="a931f-298">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="a931f-298">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="a931f-299">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="a931f-299">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="a931f-300">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="a931f-300">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="a931f-301">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="a931f-301">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="a931f-302">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="a931f-302">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="a931f-303">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="a931f-303">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="a931f-304">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="a931f-304">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





