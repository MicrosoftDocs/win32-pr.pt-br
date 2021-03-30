---
title: Uma porta de exemplo de uma lista de exibição
description: Este tópico fornece um exemplo de código do íris GL que define três listas de exibição; uma das listas de exibição refere-se às outras em sua definição. Seguindo o exemplo do íris GL há um exemplo de como o código é semelhante ao portado para OpenGL.
ms.assetid: 03283b00-fb5b-4e89-9384-171b38f141ee
keywords:
- Portabilidade do íris GL, listas de exibição
- portando do íris GL, listas de exibição
- portando para OpenGL do íris GL, listas de exibição
- Portabilidade OpenGL do íris GL, listas de exibição
- Exibir listas, portando do íris GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a856350a0a248bf7dcac51c36b9d35cf114956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635879"
---
# <a name="a-sample-port-of-a-display-list"></a><span data-ttu-id="34f9b-109">Uma porta de exemplo de uma lista de exibição</span><span class="sxs-lookup"><span data-stu-id="34f9b-109">A Sample Port of a Display List</span></span>

<span data-ttu-id="34f9b-110">Este tópico fornece um exemplo de código do íris GL que define três listas de exibição; uma das listas de exibição refere-se às outras em sua definição.</span><span class="sxs-lookup"><span data-stu-id="34f9b-110">This topic gives an IRIS GL sample of code that defines three display lists; one of the display lists refers to the others in its definition.</span></span> <span data-ttu-id="34f9b-111">Seguindo o exemplo do íris GL há um exemplo de como o código é semelhante ao portado para OpenGL.</span><span class="sxs-lookup"><span data-stu-id="34f9b-111">Following the IRIS GL sample is a sample of what the code looks like when ported to OpenGL.</span></span>

## <a name="iris-gl-sample-display-list-code"></a><span data-ttu-id="34f9b-112">Código da lista de exibição de exemplo do íris GL</span><span class="sxs-lookup"><span data-stu-id="34f9b-112">IRIS GL Sample Display List Code</span></span>


```C++
makeobj(10);  // 10 object  
    cpack(0x0000FF); 
    recti(164, 33, 364, 600);   // Hollow rectangle  
closeobj(); 
 
makeobj(20);  // 20 object  
    cpack(0xFFFF00); 
    circle(0, 0, 25);           // Unfilled circle  
    recti(100, 100, 200, 200);  // Filled rectangle  
closeobj(); 
 
makeobj(30);  // 30 object  
    callobj(10); 
    cpack(0xFFFFFF); 
    recti(400, 100, 500, 300);  // Draw filled rectangle  
    callobj(20); 
closeobj(); 
 
// Now draw by calling the lists  
call(30);
```



## <a name="opengl-sample-display-list-code"></a><span data-ttu-id="34f9b-113">Exemplo de código de lista de exibição do OpenGL</span><span class="sxs-lookup"><span data-stu-id="34f9b-113">OpenGL Sample Display List Code</span></span>

<span data-ttu-id="34f9b-114">Aqui está o código do íris GL anterior convertido em OpenGL:</span><span class="sxs-lookup"><span data-stu-id="34f9b-114">Here is the preceding IRIS GL code translated to OpenGL:</span></span>


```C++
glNewList(10, GL_COMPILE);            // List #10  
    glColor3f(1, 0, 0); 
    glRecti(164, 33, 364, 600); 
glEndList(); 
 
glNewList(20, GL_COMPILE);            //List #20  
    glColor3f(1, 1, 0);               // Set color to YELLOW  
    glPolygonMode(GL_BOTH, GL_LINE);  // Unfilled mode  
    glBegin(GL_POLYGON);  // Use polygon to approximate a circle  
        for(i=0; i<100; i++) { 
            cosine = 25 * cos(i * 2 * PI/100.0); 
            sine =   25 * sin(i * 2 * PI/100.0); 
            glVertex2f(cosine, sine); 
        } 
    glEnd(); 
    glBegin(GL_QUADS); 
        glColorf(0, 1, 1);            // Set color to CYAN  
        glVertex2i(100, 100); 
        glVertex2i(100, 200); 
        glVertex2i(200, 200); 
        glVertex2i(100, 200); 
    glEnd(); 
glEndList(); 
 
glNewList(30, GL_COMPILE);            // List #30  
    glCallList(10); 
        glColorf(1, 1, 1);            // Set color to WHITE  
        glRecti(400, 100, 500, 300); 
    glCallList(20); 
glEndList(); 
 
// Execute the display lists  
glCallList(30);
```



 

 




