---
title: Função glPixelMapuiv (Gl.h)
description: A função glPixelMapuiv configura mapas de transferência de pixel.
ms.assetid: dd0f7881-fdd1-49c2-b68c-21e2f9e5ecd2
keywords:
- Função glPixelMapuiv OpenGL
topic_type:
- apiref
api_name:
- glPixelMapuiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a353e15ec5fb67fd8d7f876cf0bdb119228ae69f8f68c14a880e5d53375a5a7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980835"
---
# <a name="glpixelmapuiv-function"></a>Função glPixelMapuiv

A **função glPixelMapuiv** configura mapas de transferência de pixel.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPixelMapuiv(
         GLenum  map,
         GLsizei mapsize,
   const GLuint  *values
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*map* 
</dt> <dd>

Um nome simbólico do mapa. Os dez mapas são os a seguir.



| Valor                                                                                                                                                                               | Significado                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <dt>**GL \_ PIXEL MAP I PARA \_ \_ \_ \_ I**</dt> </dl> | Mapas índices de cores para índices de cores.<br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <dt>**GL \_ PIXEL MAP S PARA \_ \_ \_ \_ S**</dt> </dl> | Mapas índices de estêncil para índices de estêncil.<br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ I \_ TO \_ R**</dt> </dl> | Mapas índices de cores para componentes vermelhos.<br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ I \_ TO \_ G**</dt> </dl> | Mapas índices de cores para componentes verdes.<br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <dt>**GL \_ PIXEL MAP I PARA \_ \_ \_ \_ B**</dt> </dl> | Mapas índices de cores para componentes azuis.<br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <dt>**GL \_ PIXEL MAP I PARA \_ \_ \_ \_ UM**</dt> </dl> | Mapas índices de cores para componentes alfa.<br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <dt>**GL \_ PIXEL MAP R PARA \_ \_ \_ \_ R**</dt> </dl> | Mapas componentes vermelhos para componentes vermelhos.<br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ G \_ TO \_ G**</dt> </dl> | Mapas componentes verdes para componentes verdes.<br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <dt>**MAPA \_ DE PIXEL GL B PARA \_ \_ \_ \_ B**</dt> </dl> | Mapas componentes azuis para componentes azuis.<br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <dt>**GL \_ PIXEL MAP A PARA \_ \_ \_ \_ A**</dt> </dl> | Mapas componentes alfa para componentes alfa.<br/> |



 

</dd> <dt>

*Mapsize* 
</dt> <dd>

O tamanho do mapa que está sendo definido.

</dd> <dt>

*Valores* 
</dt> <dd>

Uma matriz de *valores mapeados.*

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *map* não era um valor aceito.<br/>                                                                                                                                                                                |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *mapsize era* negativo ou maior que GL \_ PIXEL MAP \_ \_ TABLE. <br/>                                                                                                                                                   |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *map* era GL PIXEL MAP I TO \_ \_ \_ \_ \_ I, GL \_ PIXEL MAP S TO \_ \_ \_ \_ S, GL PIXEL MAP I \_ \_ TO \_ \_ \_ R, GL PIXEL MAP \_ I TO \_ \_ \_ \_ G, GL PIXEL MAP \_ I TO B ou GL PIXEL MAP I \_ TO A e \_ \_ \_ \_ \_ \_ \_ \_ *mapsize* não era uma potência de dois. <br/> |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md) <br/>                                                                                     |



## <a name="remarks"></a>Comentários

A função **glPixelMap** configura tabelas de tradução ou mapeia *,* usado por [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)e [**glTexSubImage2D**](gltexsubimage2d.md). O uso desses mapas é descrito completamente no tópico [**glPixelTransfer**](glpixeltransfer.md) e, em parte, nos tópicos dos comandos de imagem de pixel e textura. Somente a especificação dos mapas é descrita neste tópico.

O *parâmetro* map é um nome de mapa simbólico, indicando um dos dez mapas a ser definido. O *parâmetro mapsize* especifica o número de entradas  no mapa e os valores são um ponteiro para uma matriz de valores de *mapa mapeados.*

As entradas em um mapa podem ser especificadas como números de ponto flutuante de precisão simples, inteiros curtos sem sinal ou inteiros longos sem sinal. Mapas que armazenam valores de componente de cor (todos, menos GL PIXEL MAP I TO I E GL PIXEL MAP S TO S) retêm seus valores no formato de ponto flutuante, com tamanhos não especificados \_ \_ \_ de \_ \_ \_ \_ mantissa e \_ \_ \_ expoentes. Os valores de ponto flutuante especificados por [**glPixelMapfv**](glpixelmap.md) são convertidos diretamente no formato de ponto flutuante interno desses mapas e, em seguida, fixados no intervalo \[ 0,1 \] . Os valores inteiros não assinados especificados por **glPixelMapusv** e **glPixelMapuiv** são convertidos linearmente, de modo que o maior inteiro representável seja mapeado para 1,0 e zero mapeado para 0,0.

Mapas que armazenam índices, GL PIXEL MAP I TO I e GL PIXEL MAP S TO S, retêm seus valores no formato de ponto fixo, com um número não especificado de bits à direita do ponto \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ binário. Os valores de ponto flutuante especificados por [**glPixelMapfv são**](glpixelmap.md) convertidos diretamente no formato de ponto fixo interno desses mapas. Os valores inteiros não assinados especificados por **glPixelMapusv** e **glPixelMapuiv** especificam valores inteiros, com todos os zeros à direita do ponto binário.

A tabela a seguir mostra os tamanhos e valores iniciais para cada um dos mapas. Mapas que são indexados por índices de cor ou estêncil devem ter *mapsize* = 2 ^ *n* para alguns *n* ou os resultados são indefinido. O tamanho máximo permitida para cada mapa depende da implementação e pode ser determinado chamando **glGet** com o argumento GL \_ MAX PIXEL MAP \_ \_ \_ TABLE. O máximo único se aplica a todos os mapas e é pelo menos 32.



| Mapeamento                      | Índice de lookup  | Valor de lookup  | Tamanho Inicial | Valor inicial |
|--------------------------|---------------|---------------|--------------|---------------|
| GL \_ PIXEL MAP I PARA \_ \_ \_ \_ I | índice de cores   | índice de cores   | 1            | 0,0           |
| GL \_ PIXEL MAP S PARA \_ \_ \_ \_ S | índice de estêncil | índice de estêncil | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ I \_ TO \_ R | índice de cores   | R             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ I \_ TO \_ G | índice de cores   | G             | 1            | 0,0           |
| GL \_ PIXEL MAP I PARA \_ \_ \_ \_ B | índice de cores   | B             | 1            | 0,0           |
| GL \_ PIXEL MAP I PARA \_ \_ \_ \_ UM | índice de cores   | Um             | 1            | 0,0           |
| GL \_ PIXEL MAP R PARA \_ \_ \_ \_ R | R             | R             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ G \_ TO \_ G | G             | G             | 1            | 0,0           |
| MAPA \_ DE PIXEL GL B PARA \_ \_ \_ \_ B | B             | B             | 1            | 0,0           |
| GL \_ PIXEL MAP A PARA \_ \_ \_ \_ A | Um             | Um             | 1            | 0,0           |



 

As funções a seguir recuperam informações relacionadas **a glPixelMap**:

[**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o argumento GL \_ PIXEL MAP I TO I \_ \_ \_ \_ \_ SIZE

**glGet** com o argumento GL \_ PIXEL MAP S TO S \_ \_ \_ \_ \_ SIZE

**glGet com** o argumento GL \_ PIXEL MAP I TO R \_ \_ \_ \_ \_ SIZE

**glGet com** o argumento GL \_ PIXEL MAP I TO G \_ \_ \_ \_ \_ SIZE

**glGet com** o argumento GL \_ PIXEL MAP I TO B \_ \_ \_ \_ \_ SIZE

**glGet** com o argumento GL \_ PIXEL MAP I TO A \_ \_ \_ \_ \_ SIZE

**glGet com** o argumento GL \_ PIXEL MAP R TO R \_ \_ \_ \_ \_ SIZE

**glGet com** o argumento GL \_ PIXEL MAP G TO G \_ \_ \_ \_ \_ SIZE

**glGet** com o argumento GL \_ PIXEL MAP B TO B \_ \_ \_ \_ \_ SIZE

**glGet** com o argumento GL \_ PIXEL MAP A TO A \_ \_ \_ \_ \_ SIZE

**glGet com** o argumento GL \_ MAX PIXEL MAP \_ \_ \_ TABLE

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





