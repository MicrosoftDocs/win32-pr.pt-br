---
title: Função glPixelTransferf (Gl.h)
description: As funções glPixelTransferf e glPixelTransferi configuram modos de transferência de pixel. | Função glPixelTransferf (Gl.h)
ms.assetid: c18ecbb9-af2a-4662-8e3f-0ac850b04fc1
keywords:
- Função glPixelTransferf OpenGL
topic_type:
- apiref
api_name:
- glPixelTransferf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc2268147511a40aaf70a928c77b177f76870e65a7f40da4f2c6bf9428f67db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358566"
---
# <a name="glpixeltransferf-function"></a>Função glPixelTransferf

As **funções glPixelTransferf** e [**glPixelTransferi configuram**](glpixeltransferi.md) modos de transferência de pixel.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPixelTransferf(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pname* 
</dt> <dd>

O nome simbólico do parâmetro de transferência de pixel a ser definido. A tabela a seguir fornece o tipo, o valor inicial e o intervalo de valores válidos para cada um dos parâmetros de transferência de pixel definidos com **glPixelTransfer.**



| Pname             | Tipo    | Valor inicial  | Intervalo Válido  |
|-------------------|---------|----------------|--------------|
| COR \_ DO MAPA \_ GL    | Boolean | false          | true/false   |
| GL \_ MAP \_ STENCIL  | Boolean | false          | true/false   |
| GL \_ INDEX \_ SHIFT  | inteiro | 0              | (8,8)        |
| GL \_ INDEX \_ OFFSET | inteiro | 0              | (8,8)        |
| ESCALA VERMELHA GL \_ \_    | Número inteiro | 1.0            | (8,8)        |
| ESCALA VERDE GL \_ \_  | FLOAT   | 1.0            | (8,8)        |
| ESCALA AZUL GL \_ \_   | FLOAT   | 1.0            | (8,8)        |
| ESCALA \_ ALFA \_ GL  | FLOAT   | 1.0            | (8,8)        |
| ESCALA \_ DE PROFUNDIDADE DE GL \_  | FLOAT   | 1.0            | (8,8)        |
| DESVIO \_ VERMELHO \_ GL     | FLOAT   | 0,0            | (8,8)        |
| GL \_ GREEN \_ BIAS   | FLOAT   | 0,0            | (8,8)        |
| GL \_ BLUE \_ BIAS    | FLOAT   | 0,0            | (8,8)        |
| DESVIO ALFA \_ \_ GL   | FLOAT   | 0,0            | (8,8)        |
| DESVIO \_ DE PROFUNDIDADE DE \_ GL   | FLOAT   | 0,0            | (8,8)        |



 

</dd> <dt>

*param* 
</dt> <dd>

O valor para *o que pname* está definido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A **função glPixelTransfer** define modos de transferência de pixel que afetam a operação de [**glCopyPixels subsequentes,**](glcopypixels.md) [**glCopyTexImage1D,**](glcopyteximage1d.md) [**glCopyTexImage2D,**](glcopyteximage2d.md) [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)e [**comandos glTexSubImage2D.**](gltexsubimage2d.md) Os algoritmos especificados pelos modos de transferência de pixel operam em pixels depois que são lidos do framebuffer (**glReadPixels** e **glCopyPixels**) ou desempacodados da memória do cliente **(glDrawPixels,** **glTexImage1D** e **glTexImage2D).** As operações de transferência de pixel ocorrem na mesma ordem e da mesma maneira, independentemente do comando que resultou na operação de pixel. Os modos de armazenamento de pixel ([**glPixelStore**](glpixelstore-functions.md)) controlam a desempacotar os pixels que estão sendo lidos da memória do cliente e o empacotamento de pixels que estão sendo gravados novamente na memória do cliente.

As operações de transferência de pixel lidam com quatro tipos de pixel fundamentais: *cor*, *índice de cores,* *profundidade* e *estêncil*. Pixels de cor são feitos de quatro valores de ponto flutuante com tamanhos de mantissa e expoentes não especificados, dimensionados de forma que 0,0 representa intensidade zero e 1,0 representa intensidade total. Índices de cores compõem um único valor de ponto fixo, com precisão não especificada à direita do ponto binário. Pixels de profundidade compõem um único valor de ponto flutuante, com tamanhos de mantissa e expoentes não especificados, dimensionados de forma que 0,0 representa o valor mínimo do buffer de profundidade e 1,0 representa o valor máximo do buffer de profundidade. Por fim, os pixels de estêncil compõem um único valor de ponto fixo, com precisão não especificada à direita do ponto binário.

As operações de transferência de pixel executadas nos quatro tipos de pixel básicos são as seguinte:



| Tipo de pixel  | Operação de transferência de pixel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Color       | Cada um dos quatro componentes de cor é multiplicado por um fator de escala e, em seguida, adicionado a um fator de desvio. Ou seja, o componente vermelho é multiplicado por GL RED SCALE e, em seguida, adicionado a GL RED BIAS; o componente verde é multiplicado por GL GREEN SCALE e, em seguida, adicionado a GL GREEN BIAS; o componente azul é multiplicado por GL BLUE SCALE e, em seguida, adicionado a GL BLUE BIAS; e o componente alfa é multiplicado por GL ALPHA SCALE e, em seguida, adicionado ao \_ \_ GL \_ \_ \_ ALPHA \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ BIAS. Depois que todos os quatro componentes de cor são dimensionados e parcialmente, cada um é fixado no intervalo \[ 0,1 \] . Todos os valores de escala de cor e desvio são especificados com **glPixelTransfer.** <br/> Se GL MAP COLOR for true, cada componente de cor será dimensionado pelo tamanho do mapa de cor para cor correspondente e, em seguida, substituído pelo conteúdo desse mapa indexado pelo componente \_ \_ dimensionado. Ou seja, o componente vermelho é dimensionado por GL PIXEL MAP R TO R SIZE e, em seguida, substituído pelo conteúdo de \_ GL PIXEL MAP R TO \_ \_ R \_ \_ \_ \_ \_ \_ \_ \_ indexado por si só. O componente verde é dimensionado por GL PIXEL MAP G TO G SIZE e, em seguida, substituído pelo conteúdo de \_ GL PIXEL MAP G TO \_ \_ G \_ \_ \_ \_ \_ \_ \_ \_ indexado por si só. O componente azul é dimensionado por GL PIXEL MAP B TO B SIZE e, em seguida, substituído pelo conteúdo de \_ GL PIXEL MAP B TO \_ \_ B \_ \_ \_ \_ \_ \_ \_ \_ indexado por si só. O componente alfa é dimensionado por GL PIXEL MAP A TO A SIZE e, em seguida, substituído pelo conteúdo de \_ GL PIXEL MAP A TO \_ \_ A \_ \_ \_ \_ \_ \_ \_ \_ indexado por si mesmo. Todos os componentes retirados dos mapas são então fixados ao intervalo \[ 0,1 \] . GL \_ MAP COLOR é especificado com \_ **glPixelTransfer.** O conteúdo dos vários mapas é especificado com **glPixelMap.**<br/>                                                                                                                        |
| Índice de cores | Cada índice de cor é deslocado à esquerda por bits de deslocamento de índice do GL \_ \_ , preenchendo com zeros quaisquer bits além do número de bits de fração transportados pelo índice de ponto fixo. Se \_ \_ o deslocamento do índice GL for negativo, o deslocamento será à direita, novamente preenchido com zero. \_ \_ O deslocamento do índice GL é então adicionado ao índice. O \_ índice do GL \_ Shift e o \_ deslocamento do índice GL \_ são especificados com **glPixelTransfer**.<br/> A partir desse ponto, a operação varia de acordo com o formato necessário dos pixels resultantes. Se os pixels resultantes forem gravados em um buffer de índice de cor ou se estiverem sendo lidos novamente na memória do cliente no \_ formato de índice de cores GL \_ , os pixels continuarão a ser tratados como índices. Se \_ a cor do mapa GL \_ for verdadeira, cada índice será mascarado por 2 ^ *n* 1, em que *n* é o \_ \_ mapa de pixel GL \_ i para o \_ \_ \_ tamanho e, em seguida, substituído pelo conteúdo do \_ mapa de pixel GL \_ \_ i \_ para \_ indexei pelo valor mascarado. \_A cor do mapa GL \_ é especificada com **glPixelTransfer**. O conteúdo do mapa de índice é especificado com **glPixelMap**.<br/> Se os pixels resultantes forem gravados em um buffer de cores RGBA, ou se estiverem sendo lidos de volta para a memória do cliente em um formato diferente de \_ o índice de cores GL \_ , os pixels serão convertidos de índices em cores referenciando o mapa pixel do GL GL i para \_ \_ \_ \_ \_ R, GL \_ pixel MAP i para \_ \_ \_ \_ G, GL \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ Antes de ser desreferenciado, o índice é mascarado por 2 n 1, em que n é o GL \_ do mapa de pixels de \_ tamanho do R para \_ \_ \_ \_ o mapa vermelho, o \_ \_ mapa de pixel GL \_ i para o tamanho do \_ \_ \_ mapa verde, o GL \_ pixel \_ map \_ i para o tamanho do \_ \_ \_ mapa azul e o GL do mapa de \_ pixel \_ \_ \_ para \_ um \_ tamanho para o mapa alfa. Todos os componentes extraídos dos mapas são então clamped para o intervalo de \[ 0, 1 \] . O conteúdo dos quatro mapas é especificado com **glPixelMap**.<br/> |
| Profundidade       | Cada valor de profundidade é multiplicado pela \_ escala de profundidade GL \_ , adicionada à \_ tendência de profundidade GL \_ e, em seguida, clamped ao intervalo de \[ 0, 1 \] .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Stencil     | Cada índice é deslocado com deslocamento do \_ índice GL \_ e os bits de deslocamento de um índice de cor são adicionados ao \_ deslocamento do índice GL \_ . Se o \_ estêncil de mapa GL \_ for verdadeiro, cada índice será mascarado por 2n 1, em que *n* é o \_ \_ \_ tamanho do mapa de pixel GL s \_ para \_ \_ , em seguida, substituído pelo conteúdo do \_ mapa de pixel GL \_ \_ s \_ para \_ s indexado pelo valor mascarado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

A função [**glPixelTransferf**](glpixeltransfer.md) pode ser usada para definir qualquer parâmetro de transferência de pixel. Se o tipo de parâmetro for booliano, 0,0 implica falso e qualquer outro valor implica verdadeiro. Se *pname* for um parâmetro inteiro, *param* será arredondado para o número inteiro mais próximo.

Da mesma forma, **glPixelTransferi** também pode ser usado para definir qualquer um dos parâmetros de transferência de pixel. Os parâmetros boolianos são definidos como false se *param* for 0 e true caso contrário. O parâmetro *param* é convertido em ponto flutuante antes de ser atribuído a parâmetros de valor real.

Se um comando [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)ou [**glTexImage2D**](glteximage2d.md) for colocado em uma lista de exibição (consulte [**glNewList**](glnewlist.md) e [**glCallList**](glcalllist.md)), as configurações do modo de transferência de pixel em vigor quando a lista de exibição for *executada* serão aquelas usadas. Eles podem ser diferentes das configurações quando o comando foi compilado na lista de exibição.

As funções a seguir recuperam informações relacionadas ao **glPixelTransfer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com cor do mapa do argumento GL \_ \_

**glGet** com estêncil de mapa de argumento GL \_ \_

**glGet** com o argumento \_ GL \_ Shift de índice

**glGet** com deslocamento de índice do argumento GL \_ \_

**glGet** com o argumento GL \_ Red \_ Scale

**glGet** com o argumento GL de \_ \_ diferença vermelha

**glGet** com a \_ escala verde do argumento GL \_

**glGet** com \_ diferença verde de argumento GL \_

**glGet** com a \_ escala azul do argumento GL \_

**glGet** com \_ diferença azul de argumento GL \_

**glGet** com escala de alfa do argumento GL \_ \_

**glGet** com \_ diferença alfa do argumento GL \_

**glGet** com escala de profundidade do argumento GL \_ \_

**glGet** com tendência de profundidade de argumento GL \_ \_

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





