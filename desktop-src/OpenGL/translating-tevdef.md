---
title: Convertendo tevdef
description: O exemplo de código a seguir é uma definição de ambiente de textura do íris GL que especifica o parâmetro de ambiente de textura de decal de TV \_
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- Portabilidade do íris GL, textura
- portando do íris GL, textura
- portando para OpenGL do íris GL, textura
- Portabilidade OpenGL do íris GL, textura
- textura
- Portabilidade do íris GL, tevdef
- portando do íris GL, tevdef
- portando para OpenGL do íris GL, tevdef
- Portabilidade OpenGL do íris GL, tevdef
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac2610d1467adb6faa1ea105fc8e8734bfb9c4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916588"
---
# <a name="translating-tevdef"></a><span data-ttu-id="aa6f2-113">Convertendo tevdef</span><span class="sxs-lookup"><span data-stu-id="aa6f2-113">Translating tevdef</span></span>

<span data-ttu-id="aa6f2-114">O exemplo de código a seguir é uma definição de ambiente de textura do íris GL que especifica o parâmetro de ambiente de textura de decal de TV \_ :</span><span class="sxs-lookup"><span data-stu-id="aa6f2-114">The following code example is an IRIS GL texture-environment definition that specifies the TV\_DECAL texture-environment parameter:</span></span>


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



<span data-ttu-id="aa6f2-115">e o mesmo código traduzido para OpenGL:</span><span class="sxs-lookup"><span data-stu-id="aa6f2-115">and the same code translated to OpenGL:</span></span>


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



<span data-ttu-id="aa6f2-116">A tabela a seguir lista os parâmetros de ambiente de textura do íris GL e seus parâmetros OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-116">The following table lists the IRIS GL texture-environment parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="aa6f2-117">Parâmetro do íris GL</span><span class="sxs-lookup"><span data-stu-id="aa6f2-117">IRIS GL parameter</span></span>     | <span data-ttu-id="aa6f2-118">Parâmetro OpenGL</span><span class="sxs-lookup"><span data-stu-id="aa6f2-118">OpenGL parameter</span></span>             |
|-----------------------|------------------------------|
| <span data-ttu-id="aa6f2-119">\_modular de TV</span><span class="sxs-lookup"><span data-stu-id="aa6f2-119">TV\_MODULATE</span></span>          | <span data-ttu-id="aa6f2-120">GL \_ modular</span><span class="sxs-lookup"><span data-stu-id="aa6f2-120">GL\_MODULATE</span></span>                 |
| <span data-ttu-id="aa6f2-121">DECAL de TV \_</span><span class="sxs-lookup"><span data-stu-id="aa6f2-121">TV\_DECAL</span></span>             | <span data-ttu-id="aa6f2-122">\_Decal GL</span><span class="sxs-lookup"><span data-stu-id="aa6f2-122">GL\_DECAL</span></span>                    |
| <span data-ttu-id="aa6f2-123">TV \_ Blend</span><span class="sxs-lookup"><span data-stu-id="aa6f2-123">TV\_BLEND</span></span>             | <span data-ttu-id="aa6f2-124">a \_ combinação GL</span><span class="sxs-lookup"><span data-stu-id="aa6f2-124">GL\_BLEND</span></span>                    |
| <span data-ttu-id="aa6f2-125">cor da TV \_</span><span class="sxs-lookup"><span data-stu-id="aa6f2-125">TV\_COLOR</span></span>             | <span data-ttu-id="aa6f2-126">cor do GL \_ Texture \_ env \_</span><span class="sxs-lookup"><span data-stu-id="aa6f2-126">GL\_TEXTURE\_ENV\_COLOR</span></span>      |
| <span data-ttu-id="aa6f2-127">Alfa da TV \_</span><span class="sxs-lookup"><span data-stu-id="aa6f2-127">TV\_ALPHA</span></span>             | <span data-ttu-id="aa6f2-128">Nenhum equivalente OpenGL direto.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-128">No direct OpenGL equivalent.</span></span> |
| <span data-ttu-id="aa6f2-129">\_seleção de componente de TV \_</span><span class="sxs-lookup"><span data-stu-id="aa6f2-129">TV\_COMPONENT\_SELECT</span></span> | <span data-ttu-id="aa6f2-130">Nenhum equivalente OpenGL direto.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-130">No direct OpenGL equivalent.</span></span> |



 

<span data-ttu-id="aa6f2-131">Para obter mais informações sobre os parâmetros de ambiente de textura, consulte [**glTexEnv**](gltexenv-functions.md).</span><span class="sxs-lookup"><span data-stu-id="aa6f2-131">For more information about texture-environment parameters, see [**glTexEnv**](gltexenv-functions.md).</span></span>

 

 




