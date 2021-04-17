---
title: função glPixelTransferf (GL. h)
description: As funções glPixelTransferf e glPixelTransferi definem os modos de transferência de pixel. | função glPixelTransferf (GL. h)
ms.assetid: c18ecbb9-af2a-4662-8e3f-0ac850b04fc1
keywords:
- função glPixelTransferf OpenGL
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
ms.openlocfilehash: f6d6404c9b219b8a27dd3d422bfb85cd45ac8cac
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105761880"
---
# <a name="glpixeltransferf-function"></a>função glPixelTransferf

As funções **glPixelTransferf** e [**glPixelTransferi**](glpixeltransferi.md) definem os modos de transferência de pixel.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPixelTransferf(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* 
</dt> <dd>

O nome simbólico do parâmetro de transferência de pixel a ser definido. A tabela a seguir fornece o tipo, o valor inicial e o intervalo de valores válidos para cada um dos parâmetros de transferência de pixel que são definidos com **glPixelTransfer**.



| Pname             | Tipo    | Valor inicial  | Intervalo Válido  |
|-------------------|---------|----------------|--------------|
| \_cor do mapa GL \_    | Boolean | false          | true/false   |
| \_estêncil do mapa GL \_  | Boolean | false          | true/false   |
| \_deslocamento de índice GL \_  | integer | 0              | (8, 8)        |
| \_deslocamento do índice GL \_ | integer | 0              | (8, 8)        |
| escala do GL \_ vermelho \_    | Número inteiro | 1,0            | (8, 8)        |
| \_escala de verde do GL \_  | FLOAT   | 1,0            | (8, 8)        |
| \_escala azul do GL \_   | FLOAT   | 1,0            | (8, 8)        |
| \_escala de alfa do GL \_  | FLOAT   | 1,0            | (8, 8)        |
| \_escala de profundidade do GL \_  | FLOAT   | 1,0            | (8, 8)        |
| \_diferença vermelha do GL \_     | FLOAT   | 0.0            | (8, 8)        |
| \_diferença verde do GL \_   | FLOAT   | 0.0            | (8, 8)        |
| \_diferença azul \_ GL    | FLOAT   | 0.0            | (8, 8)        |
| \_diferença alfa do GL \_   | FLOAT   | 0.0            | (8, 8)        |
| \_diferença de profundidade do GL \_   | FLOAT   | 0.0            | (8, 8)        |



 

</dd> <dt>

*param* 
</dt> <dd>

O valor para o qual *pname* é definido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **glPixelTransfer** define os modos de transferência de pixel que afetam a operação dos comandos subseqüentes [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)e [**glTexSubImage2D**](gltexsubimage2d.md) . Os algoritmos especificados pelos modos de transferência de pixel operam em pixels depois que são lidos do framebuffer (**glReadPixels** e **glCopyPixels**) ou desempacotados da memória do cliente (**glDrawPixels**, **glTexImage1D** e **glTexImage2D**). As operações de transferência de pixel acontecem na mesma ordem, e da mesma maneira, independentemente do comando que resultou na operação de pixel. Os modos de armazenamento de pixel ([**glPixelStore**](glpixelstore-functions.md)) controlam o desempacotamento de pixels que estão sendo lidos da memória do cliente e a embalagem dos pixels que estão sendo gravados novamente na memória do cliente.

Operações de transferência de pixel lidam com quatro tipos de pixel fundamentais: *cor*, *índice de cores*, *profundidade* e *estêncil*. Os pixels de cor são compostos de quatro valores de ponto flutuante com tamanhos mantissa e expoente não especificados, dimensionados de forma que 0,0 represente zero intensidade e 1,0 represente a intensidade total. Os índices de cores compõem um único valor de ponto fixo, com precisão não especificada à direita do ponto binário. Os pixels de profundidade compõem um único valor de ponto flutuante, com tamanhos mantissa e expoente não especificados, dimensionados de modo que 0,0 representa o valor mínimo de buffer de profundidade e 1,0 representa o valor máximo de buffer de profundidade. Por fim, os pixels do estêncil incluem um único valor de ponto fixo, com precisão não especificada à direita do ponto binário.

As operações de transferência de pixel executadas nos quatro tipos de pixel básicos são as seguintes:



| Tipo de pixel  | Operação de transferência de pixel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cor       | Cada um dos quatro componentes de cor é multiplicado por um fator de escala e, em seguida, adicionado a um fator de tendência. Ou seja, o componente vermelho é multiplicado pela escala do GL \_ vermelho \_ e, em seguida, adicionado à \_ \_ diferença vermelha do GL; o componente verde é multiplicado pela \_ escala verde do GL \_ e, em seguida, adicionado à diferença verde do GL; \_ \_ o componente azul é \_ \_ \_ \_ \_ \_ \_ \_ multiplicado pela escala azul do GL e, em seguida, adicionado à diferença alfa do GL. Depois que todos os quatro componentes de cores são dimensionados e inclinados, cada um é clamped ao intervalo de \[ 0, 1 \] . Todos os valores de escala de cores e tendência são especificados com **glPixelTransfer**. <br/> Se \_ \_ a cor do mapa GL for verdadeira, cada componente de cor será dimensionado pelo tamanho do mapa de cor a cor correspondente e, em seguida, substituído pelo conteúdo desse mapa indexado pelo componente dimensionado. Ou seja, o componente vermelho é dimensionado por um mapa de pixel do GL \_ \_ para o tamanho do \_ \_ \_ r \_ e, em seguida, substituído pelo conteúdo do \_ mapa de pixel GL \_ \_ r \_ para \_ r indexado por si só. O componente verde é dimensionado pelo \_ \_ tamanho do mapa de pixel do GL \_ \_ de g a \_ g \_ e, em seguida, substituído pelo conteúdo do \_ mapa de pixel GL \_ \_ g \_ para \_ g indexado por si só. O componente azul é dimensionado pelo \_ \_ \_ tamanho do mapa de pixel GL b \_ para \_ b \_ e, em seguida, substituído pelo conteúdo do \_ mapa de pixel GL \_ \_ b \_ para \_ b indexado por si só. O componente alfa é dimensionado por um \_ mapa de pixel GL \_ \_ \_ para \_ um \_ tamanho e, em seguida, substituído pelo conteúdo do \_ mapa de pixel GL a \_ \_ \_ para \_ um indexado por si só. Todos os componentes extraídos dos mapas são então clamped para o intervalo de \[ 0, 1 \] . \_A cor do mapa GL \_ é especificada com **glPixelTransfer**. O conteúdo dos vários mapas é especificado com **glPixelMap**.<br/>                                                                                                                        |
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

 

 





