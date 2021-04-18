---
title: Portando defs, associações e conjuntos
description: Portando defs, associações e conjuntos
ms.assetid: 971feb14-ed39-4492-a62b-9930bdc506e9
keywords:
- Portabilidade do íris GL, definições
- portando do íris GL, definições
- portando para OpenGL do íris GL, definições
- Portabilidade OpenGL do íris GL, definições
- Portabilidade do íris GL, associações
- portando do íris GL, associações
- portando para OpenGL do íris GL, associações
- Portabilidade OpenGL do íris GL, associações
- Portabilidade do íris GL, conjuntos
- portando do íris GL, conjuntos
- portando para OpenGL do íris GL, conjuntos
- Portabilidade OpenGL do íris GL, conjuntos
- definitions
- associa
- conjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f9a88253390ee99f5b5870fd7a09e272f1c549
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756710"
---
# <a name="porting-defs-binds-and-sets"></a><span data-ttu-id="5551e-118">Portando defs, associações e conjuntos</span><span class="sxs-lookup"><span data-stu-id="5551e-118">Porting Defs, Binds, and Sets</span></span>

<span data-ttu-id="5551e-119">O OpenGL não tem tabelas de definições armazenadas; Você não pode definir modelos de iluminação, material, texturas, estilos de linha ou padrões como objetos separados como você pode no íris GL.</span><span class="sxs-lookup"><span data-stu-id="5551e-119">OpenGL doesn't have tables of stored definitions; you can't define lighting models, material, textures, line styles, or patterns as separate objects as you can in IRIS GL.</span></span> <span data-ttu-id="5551e-120">Portanto, o OpenGL não tem equivalentes diretos às seguintes funções do íris GL:</span><span class="sxs-lookup"><span data-stu-id="5551e-120">Thus OpenGL has no direct equivalents to the following IRIS GL functions:</span></span>

-   <span data-ttu-id="5551e-121">**Imdef** e **imassociação**</span><span class="sxs-lookup"><span data-stu-id="5551e-121">**Imdef** and **Imbind**</span></span>
-   <span data-ttu-id="5551e-122">**tevdef** e **tevbind**</span><span class="sxs-lookup"><span data-stu-id="5551e-122">**tevdef** and **tevbind**</span></span>
-   <span data-ttu-id="5551e-123">**textdef** e **textbind**</span><span class="sxs-lookup"><span data-stu-id="5551e-123">**textdef** and **textbind**</span></span>
-   <span data-ttu-id="5551e-124">**refinastyle** e **SetStyle**</span><span class="sxs-lookup"><span data-stu-id="5551e-124">**definestyle** and **setstyle**</span></span>
-   <span data-ttu-id="5551e-125">**defpattern** e **setpattern**</span><span class="sxs-lookup"><span data-stu-id="5551e-125">**defpattern** and **setpattern**</span></span>

<span data-ttu-id="5551e-126">Você pode usar as listas de exibição do OpenGL para imitar o mecanismo de Def/BIND GL da íris.</span><span class="sxs-lookup"><span data-stu-id="5551e-126">You can use OpenGL display lists to mimic the IRIS GL def/bind mechanism.</span></span> <span data-ttu-id="5551e-127">Por exemplo, aqui está uma definição de material no íris GL:</span><span class="sxs-lookup"><span data-stu-id="5551e-127">For example, here is a material definition in IRIS GL:</span></span>


```C++
float mat() = { 
    AMBIENT, .1, .1, .1, 
    DIFFUSE, 0, .369, .165, 
    SPECULAR, .5, .5, .5, 
    SHININESS, 10, 
    LMNULL 
}; 
lmdef(DEFMATERIAL, 1, 0, mat); 
lmbind(MATERIAL, 1);
```



<span data-ttu-id="5551e-128">O exemplo de código OpenGL a seguir define o mesmo material em uma lista de exibição que é referenciada pelo número da lista definido pelo **mymaterial**.</span><span class="sxs-lookup"><span data-stu-id="5551e-128">The following OpenGL code sample defines the same material in a display list that is referred to by the list number defined by **MYMATERIAL**.</span></span>


```C++
#define MYMATERIAL 10 
 
GLfloat        mat_amb[] = {.1, .1, .1, 1.0}; 
GLfloat        mat_dif[] = {0, .369, .165, 1.0}; 
GLfloat        mat_spec[] = {.5, .5, .5, 1.0}; 
 
glNewList(MYMATERIAL, GL_COMPILE); 
    glMaterialfv(GL_FRONT, GL_AMBIENT, mat_amb); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_dif); 
    glMaterialfv(GL_FRONT, GL_SHININESS, 10); 
glEndList(); 
 
glCallList( MYMATERIAL );
```



 

 




