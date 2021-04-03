---
title: Convertendo texdef
description: O exemplo de código a seguir é uma definição de textura do íris GL
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- Portabilidade do íris GL, textura
- portando do íris GL, textura
- portando para OpenGL do íris GL, textura
- Portabilidade OpenGL do íris GL, textura
- textura
- Portabilidade do íris GL, texdef
- portando do íris GL, texdef
- portando para OpenGL do íris GL, texdef
- Portabilidade OpenGL do íris GL, texdef
- texdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479af06bcfd3a50daf56fb0629e4c32f24750081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822965"
---
# <a name="translating-texdef"></a><span data-ttu-id="9a2c6-113">Convertendo texdef</span><span class="sxs-lookup"><span data-stu-id="9a2c6-113">Translating texdef</span></span>

<span data-ttu-id="9a2c6-114">O exemplo de código a seguir é uma definição de textura do íris GL:</span><span class="sxs-lookup"><span data-stu-id="9a2c6-114">The following code example is an IRIS GL texture definition:</span></span>


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



<span data-ttu-id="9a2c6-115">No exemplo anterior, **texdef** especifica o filtro de \_ ponto TX como a ampliação e o filtro de minimização, e TX \_ REPEAT como o mecanismo de encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="9a2c6-115">In the preceding example, **texdef** specifies the TX\_POINT filter as both the magnification and the minimizing filter, and TX\_REPEAT as the wrapping mechanism.</span></span> <span data-ttu-id="9a2c6-116">Ele também especifica a imagem de textura **: \_ textura de granito**.</span><span class="sxs-lookup"><span data-stu-id="9a2c6-116">It also specifies the texture image: **granite\_texture**.</span></span>

<span data-ttu-id="9a2c6-117">No OpenGL, [**glTexImage**](glteximage1d.md) especifica a imagem e [glTexParameter](gltexparameter-functions.md) define a propriedade.</span><span class="sxs-lookup"><span data-stu-id="9a2c6-117">In OpenGL, [**glTexImage**](glteximage1d.md) specifies the image and [glTexParameter](gltexparameter-functions.md) sets the property.</span></span> <span data-ttu-id="9a2c6-118">Para converter as definições de textura do íris GL, substitua a função **textdef** por **glTexImage** e uma ou mais chamadas para **glTexParameter**.</span><span class="sxs-lookup"><span data-stu-id="9a2c6-118">To translate IRIS GL texture definitions, replace the **textdef** function with **glTexImage** and one or more calls to **glTexParameter**.</span></span>

<span data-ttu-id="9a2c6-119">O código do íris GL anterior tem esta aparência quando traduzido para OpenGL:</span><span class="sxs-lookup"><span data-stu-id="9a2c6-119">The preceding IRIS GL code looks like this when translated to OpenGL:</span></span>


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



<span data-ttu-id="9a2c6-120">A tabela a seguir lista os parâmetros de textura do íris GL e seus parâmetros OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="9a2c6-120">The following table lists the IRIS GL texture parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="9a2c6-121">Parâmetro de textura do íris GL</span><span class="sxs-lookup"><span data-stu-id="9a2c6-121">IRIS GL texture parameter</span></span> | <span data-ttu-id="9a2c6-122">Parâmetro de textura OpenGL</span><span class="sxs-lookup"><span data-stu-id="9a2c6-122">OpenGL texture parameter</span></span>                                  |
|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9a2c6-123">MINFILTER de TX \_</span><span class="sxs-lookup"><span data-stu-id="9a2c6-123">TX\_MINFILTER</span></span>             | <span data-ttu-id="9a2c6-124">\_filtro de \_ mínimo de textura GL \_</span><span class="sxs-lookup"><span data-stu-id="9a2c6-124">GL\_TEXTURE\_MIN\_FILTER</span></span>                                  |
| <span data-ttu-id="9a2c6-125">MAGFILTER de TX \_</span><span class="sxs-lookup"><span data-stu-id="9a2c6-125">TX\_MAGFILTER</span></span>             | <span data-ttu-id="9a2c6-126">\_ \_ filtro mag de textura GL \_</span><span class="sxs-lookup"><span data-stu-id="9a2c6-126">GL\_TEXTURE\_MAG\_FILTER</span></span>                                  |
| <span data-ttu-id="9a2c6-127">TX \_ encapsulado, \_ S Wrap de TX \_</span><span class="sxs-lookup"><span data-stu-id="9a2c6-127">TX\_WRAP, TX\_WRAP\_S</span></span>     | <span data-ttu-id="9a2c6-128">\_S de \_ encapsulamento de textura GL \_</span><span class="sxs-lookup"><span data-stu-id="9a2c6-128">GL\_TEXTURE\_WRAP\_S</span></span>                                      |
| <span data-ttu-id="9a2c6-129">TX \_ Wrap, \_ encapsulamento TX \_ T</span><span class="sxs-lookup"><span data-stu-id="9a2c6-129">TX\_WRAP, TX\_WRAP\_T</span></span>     | <span data-ttu-id="9a2c6-130">\_cor da \_ \_ borda da \_ textura TGL de \_ codificação \_ de textura GL</span><span class="sxs-lookup"><span data-stu-id="9a2c6-130">GL\_TEXTURE\_WRAP\_TGL\_TEXTURE\_BORDER\_COLOR</span></span><br/> |



 

<span data-ttu-id="9a2c6-131">A tabela a seguir lista os possíveis valores dos parâmetros de textura do íris GL e seus parâmetros OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="9a2c6-131">The following table lists the possible values of the IRIS GL texture parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="9a2c6-132">Parâmetro de textura do íris GL</span><span class="sxs-lookup"><span data-stu-id="9a2c6-132">IRIS GL texture parameter</span></span> | <span data-ttu-id="9a2c6-133">Parâmetro de textura OpenGL</span><span class="sxs-lookup"><span data-stu-id="9a2c6-133">OpenGL texture parameter</span></span>     |
|---------------------------|------------------------------|
| <span data-ttu-id="9a2c6-134">ponto de TX \_</span><span class="sxs-lookup"><span data-stu-id="9a2c6-134">TX\_POINT</span></span>                 | <span data-ttu-id="9a2c6-135">GL \_ mais próximo</span><span class="sxs-lookup"><span data-stu-id="9a2c6-135">GL\_NEAREST</span></span>                  |
| <span data-ttu-id="9a2c6-136">TX \_ BIlinear</span><span class="sxs-lookup"><span data-stu-id="9a2c6-136">TX\_BILINEAR</span></span>              | <span data-ttu-id="9a2c6-137">GL \_ linear</span><span class="sxs-lookup"><span data-stu-id="9a2c6-137">GL\_LINEAR</span></span>                   |
| <span data-ttu-id="9a2c6-138">\_ponto de MIPMAP de TX \_</span><span class="sxs-lookup"><span data-stu-id="9a2c6-138">TX\_MIPMAP\_POINT</span></span>         | <span data-ttu-id="9a2c6-139">GL \_ mais próximo \_ MIPMAP \_ mais próximo</span><span class="sxs-lookup"><span data-stu-id="9a2c6-139">GL\_NEAREST\_MIPMAP\_NEAREST</span></span> |
| <span data-ttu-id="9a2c6-140">\_MIPMAP TX \_ bilinear</span><span class="sxs-lookup"><span data-stu-id="9a2c6-140">TX\_MIPMAP\_BILINEAR</span></span>      | <span data-ttu-id="9a2c6-141">GL \_ linear \_ MIPMAP \_ mais próximo</span><span class="sxs-lookup"><span data-stu-id="9a2c6-141">GL\_LINEAR\_MIPMAP\_NEAREST</span></span>  |
| <span data-ttu-id="9a2c6-142">MIPMAP de TX \_ \_ linear</span><span class="sxs-lookup"><span data-stu-id="9a2c6-142">TX\_MIPMAP\_LINEAR</span></span>        | <span data-ttu-id="9a2c6-143">GL \_ mais próximo \_ MIPMAP \_ linear</span><span class="sxs-lookup"><span data-stu-id="9a2c6-143">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>  |
| <span data-ttu-id="9a2c6-144">TX \_ TRIlinear</span><span class="sxs-lookup"><span data-stu-id="9a2c6-144">TX\_TRILINEAR</span></span>             | <span data-ttu-id="9a2c6-145">GL \_ linear \_ MIPMAP \_ linear</span><span class="sxs-lookup"><span data-stu-id="9a2c6-145">GL\_LINEAR\_MIPMAP\_LINEAR</span></span>   |



 

 

 





