---
title: Criando um ponteiro de objeto
description: Criando um ponteiro de objeto
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f57451e2781a94642e61365d3a6c694758f4056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159646"
---
# <a name="creating-an-object-pointer"></a><span data-ttu-id="82fc8-103">Criando um ponteiro de objeto</span><span class="sxs-lookup"><span data-stu-id="82fc8-103">Creating an Object Pointer</span></span>

<span data-ttu-id="82fc8-104">AVIBall usa a seguinte estrutura como seu ponteiro de objeto.</span><span class="sxs-lookup"><span data-stu-id="82fc8-104">AVIBall uses the following structure as its object pointer.</span></span> <span data-ttu-id="82fc8-105">O primeiro membro dessa estrutura aponta para a tabela de função virtual que o AVIBall usa para acessar suas funções.</span><span class="sxs-lookup"><span data-stu-id="82fc8-105">The first member of this structure points to the virtual function table that AVIBall uses to access its functions.</span></span> <span data-ttu-id="82fc8-106">Os aplicativos podem converter essa estrutura no tipo de dados PAVISTREAM.</span><span class="sxs-lookup"><span data-stu-id="82fc8-106">Applications can cast this structure to the PAVISTREAM data type.</span></span> <span data-ttu-id="82fc8-107">Os métodos que usam o tipo de dados PAVISTREAM usam apenas o ponteiro para a tabela de funções virtuais.</span><span class="sxs-lookup"><span data-stu-id="82fc8-107">Methods that use the PAVISTREAM data type use only the pointer to the virtual function table.</span></span> <span data-ttu-id="82fc8-108">Os membros que seguem o ponteiro para a tabela de funções virtuais são usados internamente pelo AVIBall.</span><span class="sxs-lookup"><span data-stu-id="82fc8-108">The members following the pointer to the virtual function table are used internally by AVIBall.</span></span>


```C++
typedef struct 
{ 
    IAVIStreamVtbl FAR * lpvtbl; 
 
    // Ball instance data. 
    ULONG     ulRefCount; 
    DWORD     fccType;  // is this audio/video? 
    int        width;    // size, in pixels, of each frame 
    int        height; 
    int        length;   // length, in frames 
    int        size; 
    COLORREF    color;    // ball color 
} AVIBALL, FAR * PAVIBALL; 

```



 

 




