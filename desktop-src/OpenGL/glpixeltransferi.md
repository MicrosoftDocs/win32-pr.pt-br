---
title: Função glPixelTransferi (Gl.h)
description: As funções glPixelTransferf e glPixelTransferi configuram modos de transferência de pixel. | Função glPixelTransferi (Gl.h)
ms.assetid: 351a872d-2cce-4fb1-b736-72201baf4157
keywords:
- Função glPixelTransferi OpenGL
topic_type:
- apiref
api_name:
- glPixelTransferi
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a2aa93fdcf0fd86975c433fca88310171986aea9edb6a00d9db8f569db02e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132905"
---
# <a name="glpixeltransferi-function"></a>Função glPixelTransferi

As [**funções glPixelTransferf**](glpixeltransferf.md) e **glPixelTransferi configuram** modos de transferência de pixel.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPixelTransferi(
   GLenum pname,
   GLint  param
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
| Índice de cores | Cada índice de cores é deslocado para a esquerda por bits GL INDEX SHIFT, preenchendo com zeros quaisquer bits além do número de bits fracionados pelo índice \_ \_ de ponto fixo. Se GL \_ INDEX \_ SHIFT for negativo, o deslocamento será para a direita, novamente zero preenchido. GL \_ INDEX OFFSET é adicionado ao \_ índice. GL \_ INDEX SHIFT e GL INDEX OFFSET são \_ \_ \_ especificados com **glPixelTransfer.**<br/> Desse ponto em diante, a operação diverge dependendo do formato necessário dos pixels resultantes. Se os pixels resultantes devem ser gravados em um buffer de índice de cores ou se eles estão sendo lidos novamente na memória do cliente no formato GL COLOR INDEX, os pixels continuam sendo tratados como \_ \_ índices. Se GL MAP COLOR for true, cada índice será mascarado por \_ \_ 2 ^ *n* 1, em que *n* é GL PIXEL MAP I TO I SIZE e, em seguida, substituído pelo conteúdo de GL PIXEL MAP I TO I indexado pelo valor \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ mascarado. GL \_ MAP COLOR é especificado com \_ **glPixelTransfer.** O conteúdo do mapa de índice é especificado com **glPixelMap.**<br/> Se os pixels resultantes devem ser gravados em um buffer de cores RGBA ou se eles estão sendo lidos novamente na memória do cliente em um formato diferente de GL COLOR INDEX, os pixels são convertidos de índices em cores referenciando os quatro mapas \_ GL PIXEL MAP I TO \_ \_ \_ \_ \_ \_ R, GL PIXEL MAP \_ I TO \_ \_ \_ G, GL PIXEL MAP I TO \_ B \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ e GL PIXEL MAP I TO A. Antes de ser desreferenciado, o índice é mascarado por 2 n 1, em que n é GL PIXEL MAP I TO R SIZE para o mapa vermelho, GL PIXEL MAP I TO G SIZE para o mapa \_ \_ \_ \_ \_ \_ \_ \_ \_ verde, GL PIXEL MAP I TO B \_ \_ \_ \_ \_ \_ \_ \_ \_ SIZE \_ \_ \_ \_ \_ \_ para o mapa azul e GL PIXEL MAP I TO A SIZE para o mapa alfa. Todos os componentes retirados dos mapas são então fixados ao intervalo \[ 0,1 \] . O conteúdo dos quatro mapas é especificado com **glPixelMap.**<br/> |
| Profundidade       | Cada valor de profundidade é multiplicado por ESCALA DE PROFUNDIDADE GL, adicionado a GL DEPTH BIAS e, em seguida, fixado ao \_ \_ intervalo \_ \_ \[ 0,1 \] .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Stencil     | Cada índice é deslocado por bits GL INDEX SHIFT, assim como um índice de cores, e, em seguida, adicionado \_ a GL INDEX \_ \_ \_ OFFSET. Se GL MAP STENCIL for true, cada índice será mascarado por \_ \_ 2n  1, em que n é GL PIXEL MAP S TO S SIZE e, em seguida, substituído pelo conteúdo de \_ GL PIXEL MAP S TO S indexado pelo valor \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ mascarado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

A [**função glPixelTransferf**](glpixeltransfer.md) pode ser usada para definir qualquer parâmetro de transferência de pixel. Se o tipo de parâmetro for booliana, 0,0 implica false e qualquer outro valor implica verdadeiro. Se *pname* for um parâmetro inteiro, *param* será arredondado para o inteiro mais próximo.

Da mesma forma, **glPixelTransferi** também pode ser usado para definir qualquer um dos parâmetros de transferência de pixel. Os parâmetros boolianas serão definidos como false *se o parâmetro* for 0 e true caso contrário. O *parâmetro param* é convertido em ponto flutuante antes de ser atribuído a parâmetros com valor real.

Se um comando [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)ou [**glTexImage2D**](glteximage2d.md) for colocado em uma lista de exibição (consulte  [**glNewList**](glnewlist.md) e [**glCallList),**](glcalllist.md)as configurações do modo de transferência de pixel em vigor quando a lista de exibição for executada serão as usadas. Eles podem ser diferentes das configurações quando o comando foi compilado na lista de exibição.

As funções a seguir recuperam informações relacionadas **a glPixelTransfer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MAP \_ COLOR

**glGet** com o argumento GL \_ MAP \_ STENCIL

**glGet** com o argumento GL \_ INDEX \_ SHIFT

**glGet** com o argumento GL \_ INDEX \_ OFFSET

**glGet** com o argumento GL \_ RED \_ SCALE

**glGet** com argumento GL \_ RED \_ BIAS

**glGet** com o argumento GL \_ GREEN \_ SCALE

**glGet com** o argumento GL \_ GREEN \_ BIAS

**glGet** com o argumento GL \_ BLUE \_ SCALE

**glGet com** o argumento GL \_ BLUE \_ BIAS

**glGet** com o argumento GL \_ ALPHA \_ SCALE

**glGet** com o argumento GL \_ ALPHA \_ BIAS

**glGet com** o argumento GL \_ DEPTH \_ SCALE

**glGet com** argumento GL \_ DEPTH \_ BIAS

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

 

 





