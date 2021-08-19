---
title: função glCopyPixels (GL. h)
description: A função glCopyPixels copia pixels no framebuffer.
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- função glCopyPixels OpenGL
topic_type:
- apiref
api_name:
- glCopyPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff31d347e0ab6bedce29898c40451976e3a38990adebc7ae2396878bf726ce1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061815"
---
# <a name="glcopypixels-function"></a>função glCopyPixels

A função **glCopyPixels** copia pixels no framebuffer.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glCopyPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  type
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*x* 
</dt> <dd>

A coordenada de plano x do canto inferior esquerdo da região retangular de pixels a ser copiada.

</dd> <dt>

*y* 
</dt> <dd>

A coordenada de plano y da janela do canto inferior esquerdo da região retangular de pixels a serem copiados.

</dd> <dt>

*width* 
</dt> <dd>

A dimensão de largura da região retangular de pixels a serem copiadas. Deve ser não negativo.

</dd> <dt>

*altura* 
</dt> <dd>

A dimensão de altura da região retangular de pixels a serem copiadas. Deve ser não negativo.

</dd> <dt>

*tipo* 
</dt> <dd>

Especifica se **glCopyPixels** é para copiar valores de cor, valores de profundidade ou valores de estêncil. As constantes simbólicas aceitáveis são.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR"></span><span id="gl_color"></span><dl> <dt><strong>GL_COLOR</strong></dt> </dl></td>
<td>A função <strong>glCopyPixels</strong> lê índices ou cores RGBA do buffer especificado no momento como o buffer de origem de leitura (consulte <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>). <br/> Se OpenGL estiver no modo de índice de cor:<br/>
<ol>
<li>Cada índice lido desse buffer é convertido em um formato de ponto fixo com um número não especificado de bits à direita do ponto binário.</li>
<li>Cada índice é deslocado para a esquerda por GL_INDEX_SHIFT bits e adicionado a GL_INDEX_OFFSET. Se GL_INDEX_SHIFT for negativo, a mudança será à direita. Em ambos os casos, zero bits ocupam locais de bits não especificados no resultado.<br/></li>
<li>Se GL_MAP_COLOR for true, o índice será substituído pelo valor que ele faz referência na tabela de pesquisa GL_PIXEL_MAP_I_TO_I.</li>
<li>Se a substituição da pesquisa do índice for concluída ou não, a parte inteira do índice será, então, Ed com 2<em><sup>b</sup></em> 1 <strong>, em que</strong> <em>b</em> é o número de bits em um buffer de índice de cor.</li>
</ol>
Se OpenGL estiver no modo RGBA:<br/>
<ol>
<li>Os componentes vermelho, verde, azul e alfa de cada pixel lido são convertidos em um formato de ponto flutuante interno com precisão não especificada.</li>
<li>A conversão mapeia o maior valor de componente representável para 1,0 e o valor de componente de zero a 0,0.</li>
<li>Os valores de cor de ponto flutuante resultantes são então multiplicados por GL_c_SCALE e adicionados a GL_c_BIAS, em que <em>c</em> é vermelho, verde, azul e alfa para os respectivos componentes de cor.</li>
<li>Os resultados são clamped para o intervalo [0, 1].</li>
<li>Se GL_MAP_COLOR for true, cada componente de cor será dimensionado pelo tamanho da tabela de pesquisa GL_PIXEL_MAP_c_TO_c e, em seguida, substituído pelo valor referenciado nessa tabela; <em>c</em> é R, G, B ou A, respectivamente. Os índices resultantes ou as cores RGBA são então convertidas em fragmentos anexando as coordenadas de coordenadas <em>z</em>e de textura atuais a cada pixel e, em seguida, atribuindo coordenadas de janela (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), em que (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) é a posição atual da varredura e o pixel era o pixel na posição <em>i</em> na linha <em>j</em> . Esses fragmentos de pixel são tratados exatamente como os fragmentos gerados pela rasterização de pontos, linhas ou polígonos. O mapeamento de textura, a neblina e todas as operações de fragmento são aplicadas antes que os fragmentos sejam gravados no framebuffer.<br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_DEPTH"></span><span id="gl_depth"></span><dl> <dt><strong>GL_DEPTH</strong></dt> </dl></td>
<td>Os valores de profundidade são lidos do buffer de profundidade e convertidos diretamente em um formato de ponto flutuante interno com precisão não especificada. O valor de profundidade de ponto flutuante resultante é então multiplicado por GL_DEPTH_SCALE e adicionado ao GL_DEPTH_BIAS. O resultado é clamped para o intervalo [0, 1]. <br/> Os componentes de profundidade resultantes são então convertidos em fragmentos anexando a cor atual da posição de rasterização ou o índice de cor e as coordenadas de textura a cada pixel e, em seguida, atribuindo coordenadas de janela (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), em que (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) é a posição atual <em></em> da varredura, e o pixel era o pixel na posição <em>i</em> Esses fragmentos de pixel são tratados exatamente como os fragmentos gerados pela rasterização de pontos, linhas ou polígonos. O mapeamento de textura, a neblina e todas as operações de fragmento são aplicadas antes que os fragmentos sejam gravados no framebuffer.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl> <dt><strong>GL_STENCIL</strong></dt> </dl></td>
<td>Os índices de estêncil são lidos do buffer de estêncil e convertidos em um formato de ponto fixo interno com um número não especificado de bits à direita do ponto binário. Cada índice de ponto fixo é então deslocado para a esquerda por GL_INDEX_SHIFT bits e adicionado ao GL_INDEX_OFFSET. Se GL_INDEX_SHIFT for negativo, a mudança será à direita. Em ambos os casos, zero bits ocupam locais de bits não especificados no resultado. Se GL_MAP_STENCIL for true, o índice será substituído pelo valor que ele faz referência na tabela de pesquisa GL_PIXEL_MAP_S_TO_S. Se a substituição da pesquisa do índice for concluída ou não, a parte inteira do índice será <strong>, então,</strong>Ed com 2<sup>b</sup> - 1, em que <em>b</em> é o número de bits no buffer do estêncil. Os índices de estêncil resultantes são gravados no buffer do estêncil, de modo que o índice lido do local <em>i</em> da linha <em>j</em> seja gravado no local (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), em que (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) é a posição atual da varredura. Somente o teste de propriedade de pixel, o teste de tesoura e o estêncil writemask afetam essas gravações.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *tipo* não era um valor aceito.<br/>                                                                                          |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | A *largura* ou a altura era negativa.<br/>                                                                                     |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | o *tipo* era a profundidade GL e não havia \_ buffer de profundidade.<br/>                                                                        |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | o *tipo* foi o estêncil GL e não havia \_ um buffer de estêncil.<br/>                                                                    |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glCopyPixels** copia um retângulo de pixels alinhado por tela do local framebuffer especificado para uma região relativa à posição de rasterização atual. Sua operação será bem definida somente se a região de origem do pixel inteiro estiver dentro da parte exposta da janela. Os resultados de cópias de fora da janela, ou de regiões da janela que não são expostas, são dependentes de hardware e indefinidos.

Os parâmetros *x* e *y* especificam as coordenadas da janela do canto inferior esquerdo da região retangular a ser copiada. Os parâmetros *Width* e *Height* especificam as dimensões da região retangular a ser copiada. A *largura* e a *altura* devem ser não negativas.

Vários parâmetros controlam o processamento dos dados de pixel enquanto eles estão sendo copiados. Esses parâmetros são definidos com três funções: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)e [**glPixelZoom**](glpixelzoom.md). Este tópico descreve os efeitos sobre **glCopyPixels** , mas não todos, dos parâmetros especificados por essas três funções.

A função **glCopyPixels** copia valores de cada pixel com o canto inferior esquerdo em (*x*  +  *i*, *y*  +  *j*) para 0 = *i*  <  *Width* e 0 = *j*  <  *Height*. Esse pixel é considerado o pixel *i* na linha *j* . Os pixels são copiados em ordem de linha do menor para a linha mais alta, da esquerda para a direita em cada linha.

O parâmetro de *tipo* especifica se os dados de cor, profundidade ou estêncil devem ser copiados.

A rasterização descrita até o momento pressupõe fatores de zoom de pixel de 1,0. Se você usar [**glPixelZoom**](glpixelzoom.md) para alterar os fatores de zoom *x* e *y* pixel, os pixels serão convertidos em fragmentos da seguinte maneira. Se (*x*<sub>r</sub> , *y*<sub>r</sub> ) for a posição atual da varredura e um determinado pixel estiver na localização *i* na linha *j* do retângulo do pixel de origem, os fragmentos serão gerados para os pixels cujos centros estão no retângulo com os cantos em

(*x*<sub>r</sub>  +  *aplicar zoom*? i, y <sub>r</sub>  +  *zoom*<sub>y</sub> *j*)

e

(*x*<sub>r</sub>  +  *aplicar zoom*? (*i* + 1), *y*<sub>r</sub>  +  *zoom*<sub>y</sub> (*j* + 1))

onde *aplicar zoom*? é o valor de GL \_ zoom \_ X e *zoom*<sub>y</sub> é o valor de GL \_ zoom \_ y.

Os modos especificados por [**glPixelStore**](glpixelstore-functions.md) não têm efeito sobre a operação de **glCopyPixels**.

As funções a seguir recuperam informações relacionadas ao **glCopyPixels**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ posição de rasterização atual \_

**glGet** com Argument GL \_ \_ posição de rasterização atual \_ \_ válida

Para copiar o pixel de cor no canto inferior esquerdo da janela para a posição de rasterização atual, use

**glCopyPixels**(0, 0, 1, 1, cor do GL \_ );

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





