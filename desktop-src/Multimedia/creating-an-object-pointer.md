---
title: Criando um ponteiro de objeto
description: Criando um ponteiro de objeto
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586ba0b8c9ee261e29f21ed58c84193f4cc89d1399c62d75d82a2c0a49075dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144679"
---
# <a name="creating-an-object-pointer"></a>Criando um ponteiro de objeto

AVIBall usa a estrutura a seguir como seu ponteiro de objeto. O primeiro membro dessa estrutura aponta para a tabela de funções virtuais que o AVIBall usa para acessar suas funções. Os aplicativos podem lançar essa estrutura para o tipo de dados PAVISTREAM. Os métodos que usam o tipo de dados PAVISTREAM usam apenas o ponteiro para a tabela de funções virtuais. Os membros que seguem o ponteiro para a tabela de funções virtuais são usados internamente por AVIBall.


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



 

 




