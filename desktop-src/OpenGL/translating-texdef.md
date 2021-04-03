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
# <a name="translating-texdef"></a>Convertendo texdef

O exemplo de código a seguir é uma definição de textura do íris GL:


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



No exemplo anterior, **texdef** especifica o filtro de \_ ponto TX como a ampliação e o filtro de minimização, e TX \_ REPEAT como o mecanismo de encapsulamento. Ele também especifica a imagem de textura **: \_ textura de granito**.

No OpenGL, [**glTexImage**](glteximage1d.md) especifica a imagem e [glTexParameter](gltexparameter-functions.md) define a propriedade. Para converter as definições de textura do íris GL, substitua a função **textdef** por **glTexImage** e uma ou mais chamadas para **glTexParameter**.

O código do íris GL anterior tem esta aparência quando traduzido para OpenGL:


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



A tabela a seguir lista os parâmetros de textura do íris GL e seus parâmetros OpenGL equivalentes.



| Parâmetro de textura do íris GL | Parâmetro de textura OpenGL                                  |
|---------------------------|-----------------------------------------------------------|
| MINFILTER de TX \_             | \_filtro de \_ mínimo de textura GL \_                                  |
| MAGFILTER de TX \_             | \_ \_ filtro mag de textura GL \_                                  |
| TX \_ encapsulado, \_ S Wrap de TX \_     | \_S de \_ encapsulamento de textura GL \_                                      |
| TX \_ Wrap, \_ encapsulamento TX \_ T     | \_cor da \_ \_ borda da \_ textura TGL de \_ codificação \_ de textura GL<br/> |



 

A tabela a seguir lista os possíveis valores dos parâmetros de textura do íris GL e seus parâmetros OpenGL equivalentes.



| Parâmetro de textura do íris GL | Parâmetro de textura OpenGL     |
|---------------------------|------------------------------|
| ponto de TX \_                 | GL \_ mais próximo                  |
| TX \_ BIlinear              | GL \_ linear                   |
| \_ponto de MIPMAP de TX \_         | GL \_ mais próximo \_ MIPMAP \_ mais próximo |
| \_MIPMAP TX \_ bilinear      | GL \_ linear \_ MIPMAP \_ mais próximo  |
| MIPMAP de TX \_ \_ linear        | GL \_ mais próximo \_ MIPMAP \_ linear  |
| TX \_ TRIlinear             | GL \_ linear \_ MIPMAP \_ linear   |



 

 

 





