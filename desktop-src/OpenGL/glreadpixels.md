---
title: Função glReadPixels (Gl.h)
description: A função glReadPixels lê um bloco de pixels do framebuffer.
ms.assetid: 41fbad5c-b8ca-456d-bbfc-b48c176e15b0
keywords:
- Função glReadPixels OpenGL
topic_type:
- apiref
api_name:
- glReadPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b03a90fcd6ee5179a900739c40e78f796c6340d9609f4cfbeb21e6a70156afe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937936"
---
# <a name="glreadpixels-function"></a>Função glReadPixels

A **função glReadPixels** lê um bloco de pixels do framebuffer.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glReadPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  format,
   GLenum  type,
   GLvoid  *pixels
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*x* 
</dt> <dd>

A coordenada *x* da janela do primeiro pixel que é lido do framebuffer. Junto com a *coordenada y,* especifica o local do canto inferior esquerdo de um bloco retangular de pixels.

</dd> <dt>

*y* 
</dt> <dd>

As coordenadas *y* da janela do primeiro pixel que é lido do framebuffer. Junto com a *coordenada x,* especifica o local do canto inferior esquerdo de um bloco retangular de pixels.

</dd> <dt>

*width* 
</dt> <dd>

A largura do retângulo de pixel.

</dd> <dt>

*altura* 
</dt> <dd>

A altura do retângulo de pixel. *Os* *parâmetros* de largura e altura do valor "1" correspondem a um único pixel.

</dd> <dt>

*format* 
</dt> <dd>

O formato dos dados de pixel. Os seguintes valores simbólicos são aceitos:



| Valor                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**GL \_ COLOR \_ INDEX**</dt> </dl>                                                                                                                                                                                                                                                                                                               | Os índices de cores são lidos do buffer de cores selecionado por [**glReadBuffer.**](glreadbuffer.md) Cada índice é convertido em ponto fixo, deslocado para a esquerda ou para a direita, dependendo do valor e do sinal de GL INDEX SHIFT e adicionado \_ \_ ao GL INDEX \_ \_ OFFSET. Se GL \_ MAP COLOR for GL \_ \_ TRUE, os índices serão substituídos por seus mapeamentos na tabela GL \_ PIXEL MAP I TO \_ \_ \_ \_ I.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt>**GL \_ STENCIL \_ INDEX**</dt> </dl>                                                                                                                                                                                                                                                                                                         | Os valores de estêncil são lidos do buffer de estêncil. Cada índice é convertido em ponto fixo, deslocado para a esquerda ou para a direita, dependendo do valor e do sinal de GL INDEX SHIFT e adicionado \_ \_ ao GL INDEX \_ \_ OFFSET. Se GL \_ MAP STENCIL for GL TRUE, os índices serão substituídos por seus mapeamentos na tabela \_ GL PIXEL MAP S TO \_ \_ \_ \_ \_ \_ S.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt>**COMPONENTE \_ GL DEPTH \_**</dt> </dl>                                                                                                                                                                                                                                                                                                   | Os valores de profundidade são lidos do buffer de profundidade. Cada componente é convertido em ponto flutuante, de forma que o valor mínimo de profundidade mapeia para 0,0 e o valor máximo é mapeado para 1,0. Em seguida, cada componente é multiplicado por ESCALA DE PROFUNDIDADE GL, adicionado ao DESVIO DE PROFUNDIDADE GL e, por fim, fixado ao \_ \_ intervalo \_ \_ \[ 0,1 \] .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_RED__GL_GREEN__GL_BLUE__GL_ALPHA__GL_RGB__GL_RGBA__GL_BGR_EXT__GL_BGRA_EXT__GL_LUMINANCE__GL_LUMINANCE_ALPHA"></span><span id="gl_red__gl_green__gl_blue__gl_alpha__gl_rgb__gl_rgba__gl_bgr_ext__gl_bgra_ext__gl_luminance__gl_luminance_alpha"></span><dl> <dt>**GL \_ RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE, GL \_ LUMINANCE \_ ALPHA**</dt> </dl> | O processamento difere dependendo se os buffers de cores armazenam índices de cores ou componentes de cor RGBA. Se os índices de cores forem armazenados, eles serão lidos do buffer de cores selecionado por [**glReadBuffer.**](glreadbuffer.md) Cada índice é convertido em ponto fixo, deslocado para a esquerda ou para a direita, dependendo do valor e do sinal de GL INDEX SHIFT e adicionado \_ \_ ao GL INDEX \_ \_ OFFSET. Os índices são substituídos pelos valores vermelho, verde, azul e alfa obtidos pela indexação das tabelas GL \_ PIXEL MAP I TO \_ \_ \_ \_ R, GL PIXEL MAP \_ I TO G, GL PIXEL MAP I TO B e \_ GL PIXEL MAP I \_ \_ \_ TO \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ A. Se os componentes de cor RGBA forem armazenados nos buffers de cores, eles serão lidos do buffer de cores selecionado por **glReadBuffer**. Cada componente de cor é convertido em ponto flutuante, de forma que a intensidade zero é mapeada para 0,0 e a intensidade total é mapeada para 1,0. Cada componente é multiplicado por GL c SCALE e adicionado a GL c BIAS, em que c é \_ \_ GL \_ \_ \_ RED, GL \_ GREEN, GL BLUE e GL \_ \_ ALPHA. Cada componente é fixado ao intervalo \[ 0,1 \] . Por fim, se GL MAP COLOR for GL TRUE, cada componente de cor c será substituído por seu mapeamento na tabela GL PIXEL MAP c TO c, em que c novamente é \_ \_ GL \_ \_ \_ \_ \_ \_ \_ RED, GL GREEN, GL \_ BLUE \_ \_ e GL ALPHA. Cada componente é dimensionado para o tamanho de sua tabela correspondente antes que a análise seja executada. Por fim, os dados não sãonenedos são descartados. Por exemplo, GL \_ RED descarta os componentes verde, azul e alfa, enquanto GL \_ RGB descarta apenas o componente alfa. O GL LUMINANCE calcula um único valor de componente como a soma dos componentes vermelho, verde e azul e GL LUMINANCE ALPHA faz o mesmo, mantendo alfa como um \_ \_ segundo \_ valor.<br/> |



 

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de dados dos dados de pixel. Deve ser um dos valores a seguir.



| Tipo                | Máscara de índice | Conversão de componente |
|---------------------|------------|----------------------|
| GL \_ UNSIGNED \_ BYTE  | 281        | (281) *c*             |
| GL \_ BYTE            | 271        | \[(271) *c*-1 \] /2     |
| GL \_ BITMAP          | 1          | 1                    |
| GL \_ UNSIGNED \_ SHORT | 2 61       | (2 61) *c*            |
| GL \_ SHORT           | 2 51       | \[(2 51) *c* 1 \] /2     |
| GL \_ UNSIGNED \_ INT\_ | 2 1       | (2 1) *c*            |
| GL \_ INT             | 2 1      | \[(2 1) *c* 1 \] /2     |
| GL \_ FLOAT           | nenhum       | *c*                  |



 

</dd> <dt>

*pixels* 
</dt> <dd>

Retorna os dados de pixel.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *format* ou *type* não era um valor aceito.<br/>                                                                              |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | A *largura ou* a *altura* era negativa.<br/>                                                                                   |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | *O formato* era GL COLOR INDEX e os buffers de cores \_ \_ armazenavam componentes RGBA ou de cor BGRA.<br/>                                 |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | *O formato* era GL \_ STENCIL \_ INDEX e não havia nenhum buffer de estêncil.<br/>                                                          |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | *O formato* era GL \_ DEPTH COMPONENT e não havia buffer de \_ profundidade.<br/>                                                          |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |

## <a name="remarks"></a>Comentários

A função **glReadPixels** retorna dados de pixel do framebuffer, começando com o pixel cujo canto inferior esquerdo está no local (*x*, *y*), na memória do cliente, começando nos *pixels* do local. Vários parâmetros controlam o processamento dos dados de pixel antes de serem colocados na memória do cliente. Esses parâmetros são definidos com três comandos: [**glPixelStore**](glpixelstore-functions.md), [**glPixelTransfer**](glpixeltransfer.md)e [**glPixelMap**](glpixelmap.md). Este tópico descreve os efeitos sobre **glReadPixels** , mas não todos os parâmetros especificados por esses três comandos.

A função **glReadPixels** retorna valores de cada pixel com canto inferior esquerdo em (*x* + i, *y* + j) para 0 = i < *Width* e 0 = j < *Height*. Esse pixel é considerado como o *i*-ésimo na linha *j* th. Os pixels são retornados em ordem de linha do menor para a linha mais alta, da esquerda para a direita em cada linha.

Os fatores de deslocamento, escala, tendência e pesquisa descritos acima são todos especificados por [**glPixelTransfer**](glpixeltransfer.md). O conteúdo da tabela de pesquisa é especificado por [**glPixelMap**](glpixelmap.md).

A etapa final envolve converter os índices ou componentes para o formato adequado, conforme especificado por *tipo*. Se *Format* for GL \_ Color \_ index ou GL \_ stencil \_ Index e *Type* não for GL \_ float, cada índice será mascarado com o valor de Mask fornecido na tabela a seguir. Se *Type* for GL \_ float, cada índice de inteiro será convertido em formato de ponto flutuante de precisão simples.

Se o *formato* for GL \_ vermelho, GL \_ verde, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminescência ou GL de \_ luminância \_ alfa e o *tipo* não for GL \_ float, cada componente será multiplicado pelo multiplicador mostrado na tabela anterior. Se Type for GL \_ float, cada componente será passado como está (ou convertido no formato de ponto flutuante de precisão única do cliente se ele for diferente daquele usado pelo OpenGL).

Os valores de retorno são colocados na memória da seguinte maneira. Se o *formato* for \_ o \_ índice de cores GL, o índice do \_ estêncil GL \_ , o componente de profundidade do GL \_ \_ , \_ o GL vermelho, \_ o GL verde, o GL \_ em azul, \_ o GL alfa ou o GL \_ , um único valor será retornado e os dados do *i*-pixel na linha *j* serão colocados na *largura* de local (*j* )  +  *i*. GL \_ RGB e GL \_ BGR \_ ext retornam três valores, GL \_ RGBA e GL \_ BGRA \_ ext retornam quatro valores e \_ a luminância do GL \_ alfa retorna dois valores para cada pixel, com todos os valores correspondentes a um único pixel ocupando espaço contíguo em *pixels*. Armazenamento parâmetros definidos por [**glPixelStore**](glpixelstore-functions.md), como o gl \_ pack \_ SWAP \_ BYTES e o gl \_ pack \_ LSB \_ primeiro, afetam a forma como os dados são gravados na memória. Consulte [**glPixelStore**](glpixelstore-functions.md) para obter uma descrição.

Valores de pixels que ficam fora da janela conectada ao contexto OpenGL atual são indefinidos.

Se um erro for gerado, nenhuma alteração será feita no conteúdo de *pixels*.

A função a seguir recupera informações relacionadas a **glReadPixels**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de índice do Argument GL \_

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> </dl>

 

 





