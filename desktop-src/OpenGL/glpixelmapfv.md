---
title: função glPixelMapfv (GL. h)
description: A função glPixelMapfv configura mapas de transferência de pixel.
ms.assetid: 13403243-1ec4-4b1d-a9da-9a6693b6f9b8
keywords:
- função glPixelMapfv OpenGL
topic_type:
- apiref
api_name:
- glPixelMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e447e471f1a37f4d0c8c6bd8fb3ce548bb5657e49afafa01e785b0870ebdd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938351"
---
# <a name="glpixelmapfv-function"></a>função glPixelMapfv

A função **glPixelMapfv** configura mapas de transferência de pixel.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPixelMapfv(
         GLenum  map,
         GLsizei mapsize,
   const GLfloat *values
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*map* 
</dt> <dd>

Um nome de mapa simbólico. Os dez mapas são os seguintes.



| Valor                                                                                                                                                                               | Significado                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <dt>**\_ \_ mapa de pixel GL \_ i \_ para \_**</dt> </dl> | Mapas índices de cores para índices de cores.<br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <dt>**\_ \_ mapas de pixel GL \_ s \_ para \_ s**</dt> </dl> | Mapas índices de estêncil a índices de estêncil.<br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <dt>**\_ \_ mapa de pixel GL \_ I \_ para \_ R**</dt> </dl> | Mapas índices de cores para componentes vermelhos.<br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <dt>**\_ \_ mapa de pixel GL \_ I \_ para \_ G**</dt> </dl> | Mapas índices de cores a componentes verdes.<br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <dt>**\_ \_ mapa de pixel GL \_ I \_ para \_ B**</dt> </dl> | Mapas índices de cores a componentes azuis.<br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <dt>**\_ \_ mapa de pixel GL \_ I \_ para \_ a**</dt> </dl> | Mapas índices de cores para componentes alfa.<br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <dt>**\_ \_ mapa de pixel GL \_ r \_ para \_ r**</dt> </dl> | Mapas componentes vermelhos para componentes vermelhos.<br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <dt>**\_ \_ mapa de pixel GL \_ g \_ a \_ G**</dt> </dl> | Mapas componentes verdes a componentes verdes.<br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <dt>**\_ \_ mapa de pixel GL \_ b \_ para \_ b**</dt> </dl> | Mapas componentes azuis a componentes azuis.<br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <dt>**\_mapa de pixel GL a \_ \_ \_ para \_ um**</dt> </dl> | Mapas componentes alfa para componentes alfa.<br/> |



 

</dd> <dt>

*mapear* 
</dt> <dd>

O tamanho do mapa que está sendo definido.

</dd> <dt>

*os* 
</dt> <dd>

Uma matriz de valores de *mapas* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *mapa* não era um valor aceito.<br/>                                                                                                                                                                                |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | o *Maps* foi negativo ou maior que a \_ tabela de mapa de pixel GL \_ \_ . <br/>                                                                                                                                                   |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | o *MAP* foi \_ o \_ mapa de pixel GL \_ i \_ para \_ i, GL o \_ \_ mapa \_ de pixels s \_ para \_ s, o GL do \_ \_ mapa de pixels \_ i \_ para \_ R, GL \_ pixel \_ map \_ i \_ para \_ G, GL \_ pixel \_ map \_ i \_ para \_ B ou GL \_ \_ o MAP pixel \_ i \_ para \_ a, e *Maps* não era uma potência de dois. <br/> |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md). <br/>                                                                                     |



## <a name="remarks"></a>Comentários

A função **glPixelMap** configura tabelas de conversão ou *mapas*, usados por [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)e [**glTexSubImage2D**](gltexsubimage2d.md). O uso desses mapas é descrito completamente no tópico [**glPixelTransfer**](glpixeltransfer.md) e, em parte, nos tópicos dos comandos de imagem de pixel e textura. Somente a especificação dos mapas é descrita neste tópico.

O parâmetro *MAP* é um nome de mapa simbólico, indicando que um dos dez mapas deve ser definido. O parâmetro *Maps* especifica o número de entradas no mapa, e os *valores* são um ponteiro para uma matriz de *mapas* de valores de mapa.

As entradas em um mapa podem ser especificadas como números de ponto flutuante de precisão simples, inteiros curtos não assinados ou inteiros longos não assinados. Mapas que armazenam valores de componentes de cores (todos, mas o \_ mapa de pixel gl i e o mapa de \_ \_ \_ \_ \_ pixel gl \_ \_ s \_ para \_ s) retêm seus valores no formato de ponto flutuante, com tamanhos mantissa e expoente não especificados. Valores de ponto flutuante especificados por [**glPixelMapfv**](glpixelmap.md) são convertidos diretamente no formato de ponto flutuante interno desses mapas e, em seguida, clamped para o intervalo de \[ 0, 1 \] . Valores inteiros sem sinal especificados por **glPixelMapusv** e **glPixelMapuiv** são convertidos linearmente de forma que o maior inteiro representável seja mapeado para 1,0 e que seja mapeado para 0,0.

Mapas que armazenam índices, \_ o GL pixel \_ map \_ i \_ para \_ i e GL \_ pixel \_ map \_ S \_ para \_ s, retêm seus valores em formato de ponto fixo, com um número não especificado de bits à direita do ponto binário. Os valores de ponto flutuante especificados por [**glPixelMapfv**](glpixelmap.md) são convertidos diretamente no formato de ponto fixo interno desses mapas. Valores inteiros sem sinal especificados por **glPixelMapusv** e **glPixelMapuiv** especificam valores inteiros, com todos os zeros à direita do ponto binário.

A tabela a seguir mostra os tamanhos e valores iniciais para cada um dos mapas. Mapas que são indexados por índices de cor ou de estêncil devem ter *Maps* = 2 ^ *n* para alguns *n* ou os resultados são indefinidos. O tamanho máximo permitido para cada mapa depende da implementação e pode ser determinado com a chamada de **glGet** com a \_ tabela de mapa de pixels máxima do Argument GL \_ \_ \_ . O máximo único se aplica a todos os mapas e é pelo menos 32.



| Mapeamento                      | Índice de pesquisa  | Valor de pesquisa  | Tamanho Inicial | Valor inicial |
|--------------------------|---------------|---------------|--------------|---------------|
| \_ \_ mapa de pixel GL \_ i \_ para \_ | índice de cores   | índice de cores   | 1            | 0,0           |
| \_ \_ mapas de pixel GL \_ s \_ para \_ s | índice de estêncil | índice de estêncil | 1            | 0,0           |
| \_ \_ mapa de pixel GL \_ I \_ para \_ R | índice de cores   | R             | 1            | 0,0           |
| \_ \_ mapa de pixel GL \_ I \_ para \_ G | índice de cores   | G             | 1            | 0,0           |
| \_ \_ mapa de pixel GL \_ I \_ para \_ B | índice de cores   | B             | 1            | 0,0           |
| \_ \_ mapa de pixel GL \_ I \_ para \_ a | índice de cores   | Um             | 1            | 0,0           |
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

 

 





