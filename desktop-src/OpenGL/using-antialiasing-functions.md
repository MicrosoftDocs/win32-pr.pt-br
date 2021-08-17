---
title: Usando funções de anti-aliasing
description: A tabela a seguir lista as funções de anti-aliasing do íris GL e suas funções OpenGL equivalentes.
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- Portabilidade do íris GL, anti-aliasing
- portando do íris GL, antialiasing
- portando para OpenGL do íris GL, antialiasing
- Portabilidade OpenGL do íris GL, antialiasing
- suavização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab36f41e3b639447b4f246d706e11c134d8f920528cde1e946d26af057a95951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980342"
---
# <a name="using-antialiasing-functions"></a>Usando funções de anti-aliasing

A tabela a seguir lista as funções de anti-aliasing do íris GL e suas funções OpenGL equivalentes.



| Função GL de íris | Função OpenGL                                      | Significado                           |
|------------------|------------------------------------------------------|-----------------------------------|
| **pntsmooth**    | [**glEnable**](glenable.md) ( \_ sem ajuste de ponto GL \_ )   | Habilita a anti-aliasing de pontos.   |
| **linesmooth**   | **glEnable**( \_ linha simples de GL \_ )                     | Habilita a anti-aliasing de linhas.    |
| **polismooth**   | [**glEnable**](glenable.md) (uniforme do polígono do GL \_ \_ ) | Habilita a suavização de polígonos. |



 

Use as chamadas [**glDisable**](gldisable.md) equivalentes para desativar a suavização.

No íris GL, você pode controlar a qualidade da suavização chamando:


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



O OpenGL fornece [**glHint**](glhint.md)controluse semelhante:


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



em que *hintmode* é um dos seguintes:

-   GL \_ mais interessante (use a suavização de qualidade mais alta.)
-   GL mais \_ rápido (use a suavização mais eficiente.)
-   GL não se \_ \_ preocupa

O íris GL também permite a correção de fim chamando:


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



O OpenGL não tem nenhum equivalente para essa função.

 

 




