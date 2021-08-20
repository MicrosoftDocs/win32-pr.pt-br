---
title: Traduzindo o texdef
description: O exemplo de código a seguir é uma definição de textura IRIS GL
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- Portação IRIS GL, textura
- portando de IRIS GL, textura
- portando para OpenGL de IRIS GL, textura
- Portação openGL de IRIS GL, textura
- textura
- Portação IRIS GL, texdef
- portando de IRIS GL, texdef
- portando para OpenGL de IRIS GL, texdef
- Portação openGL de IRIS GL, texdef
- texdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92955b2b49d6960afc661d467da42a4ebcd7aff6caaf7c0bd386093968413f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980548"
---
# <a name="translating-texdef"></a>Traduzindo o texdef

O exemplo de código a seguir é uma definição de textura IRIS GL:


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



No exemplo anterior, **o texdef** especifica o filtro TX POINT como a ampliação e o filtro de minimização e TX REPEAT como o \_ mecanismo de \_ empacotamento. Ele também especifica a imagem de textura: **textura de \_ granito.**

No OpenGL, [**glTexImage**](glteximage1d.md) especifica a imagem e [glTexParameter define](gltexparameter-functions.md) a propriedade . Para converter definições de textura IRIS GL, substitua a função **textdef** por **glTexImage** e uma ou mais chamadas para **glTexParameter.**

O código IRIS GL anterior tem esta aparência quando convertido em OpenGL:


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



A tabela a seguir lista os parâmetros de textura IRIS GL e seus parâmetros OpenGL equivalentes.



| Parâmetro de textura IRIS GL | Parâmetro de textura OpenGL                                  |
|---------------------------|-----------------------------------------------------------|
| TX \_ MINFILTER             | FILTRO MIN \_ \_ DE TEXTURA \_ GL                                  |
| TX \_ MAGFILTER             | FILTRO GL \_ TEXTURE \_ MAG \_                                  |
| TX \_ WRAP, TX \_ WRAP \_ S     | GL \_ TEXTURE \_ WRAP \_ S                                      |
| TX \_ WRAP, TX \_ WRAP \_ T     | COR \_ DA BORDA DA TEXTURA GL TEXTURE WRAP \_ \_ TGL \_ \_ \_<br/> |



 

A tabela a seguir lista os valores possíveis dos parâmetros de textura IRIS GL e seus parâmetros OpenGL equivalentes.



| Parâmetro de textura IRIS GL | Parâmetro de textura OpenGL     |
|---------------------------|------------------------------|
| TX \_ POINT                 | GL \_ MAIS PRÓXIMO                  |
| TX \_ BILINEAR              | GL \_ LINEAR                   |
| TX \_ MIPMAP \_ POINT         | GL \_ MAIS PRÓXIMO DE \_ MIPMAP \_ |
| TX \_ MIPMAP \_ BILINEAR      | GL \_ LINEAR \_ MIPMAP \_ MAIS PRÓXIMO  |
| TX \_ MIPMAP \_ LINEAR        | GL \_ NEAREST \_ MIPMAP \_ LINEAR  |
| TX \_ TRILINEAR             | GL \_ LINEAR \_ MIPMAP \_ LINEAR   |



 

 

 





