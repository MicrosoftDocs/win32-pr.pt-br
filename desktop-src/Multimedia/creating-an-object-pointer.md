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
# <a name="creating-an-object-pointer"></a>Criando um ponteiro de objeto

AVIBall usa a seguinte estrutura como seu ponteiro de objeto. O primeiro membro dessa estrutura aponta para a tabela de função virtual que o AVIBall usa para acessar suas funções. Os aplicativos podem converter essa estrutura no tipo de dados PAVISTREAM. Os métodos que usam o tipo de dados PAVISTREAM usam apenas o ponteiro para a tabela de funções virtuais. Os membros que seguem o ponteiro para a tabela de funções virtuais são usados internamente pelo AVIBall.


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



 

 




