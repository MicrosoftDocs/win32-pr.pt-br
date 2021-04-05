---
title: função glDrawPixels (GL. h)
description: A função glDrawPixels grava um bloco de pixels no framebuffer.
ms.assetid: c4eda64f-a75e-4e6d-984d-af49414b94d8
keywords:
- função glDrawPixels OpenGL
topic_type:
- apiref
api_name:
- glDrawPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25adc8ad28791086020a37d3a30651e169bfd07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085323"
---
# <a name="gldrawpixels-function"></a>função glDrawPixels

A função **glDrawPixels** grava um bloco de pixels no framebuffer.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glDrawPixels(
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*width* 
</dt> <dd>

A dimensão de largura do retângulo de pixel que será gravada no framebuffer.

</dd> <dt>

*altura* 
</dt> <dd>

A dimensão de altura do retângulo de pixel que será gravada no framebuffer.

</dd> <dt>

*format* 
</dt> <dd>

O formato dos dados de pixel. As constantes simbólicas aceitáveis são as seguintes.



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
<td><span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt><strong>GL_COLOR_INDEX</strong></dt> </dl></td>
<td>Cada pixel é um único valor, um índice de cores. <br/>
<ol>
<li>A função <strong>glDrawPixels</strong> converte cada pixel em formato de ponto fixo, com um número não especificado de bits à direita do ponto binário, independentemente do tipo de dados de memória. Os valores de ponto flutuante são convertidos em valores de ponto fixo verdadeiros. A função <strong>glDrawPixels</strong> converte dados inteiros assinados e não assinados com todos os bits de fração definidos como zero. A função converte dados de bitmap para 0,0 ou 1,0.</li>
<li>A função <strong>glDrawPixels</strong> desloca cada índice de ponto fixo à esquerda por GL_INDEX_SHIFT bits e o adiciona ao GL_INDEX_OFFSET. Se GL_INDEX_SHIFT for negativo, a mudança será à direita. Em ambos os casos, zero bits ocupam locais de bits não especificados no resultado.</li>
<li>No modo RGBA, <strong>glDrawPixels</strong> converte o índice resultante em um pixel RGBA usando as tabelas GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_B e GL_PIXEL_MAP_I_TO_A. Quando estiver no modo de índice de cor e GL_MAP_COLOR for true, o índice será substituído pelo valor que <strong>glDrawPixels</strong> referencia na tabela de pesquisa GL_PIXEL_MAP_I_TO_I.</li>
<li>Se a substituição da pesquisa do índice for concluída ou não, a parte inteira do índice será <strong>e</strong>Ed com 2<sup>b</sup> - 1, em que <em>b</em> é o número de bits em um buffer de índice de cor.</li>
<li>Os índices resultantes ou as cores RGBA são então convertidas em fragmentos anexando as coordenadas de coordenadas <em>z</em>e de textura atuais a cada pixel e, em seguida, atribuindo coordenadas de janela <em>x</em> e <em>y</em> ao <em>n</em>º de fragmento como <em>x</em>? = <em>largura</em> <em>x</em><sub>r</sub> + <em>n</em> mod<br/> <em>y</em>? = <em>y</em><sub>r</sub> + <em>n/largura</em><br/> onde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) é a posição atual da varredura.<br/></li>
<li>A função <strong>glDrawPixels</strong> trata esses fragmentos de pixel, assim como os fragmentos gerados pela rasterização de pontos, linhas ou polígonos. Ele aplica o mapeamento de textura, sombra e todas as operações de fragmento antes de gravar os fragmentos no framebuffer.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt><strong>GL_STENCIL_INDEX</strong></dt> </dl></td>
<td>Cada pixel é um único valor, um índice de estêncil. <br/>
<ol>
<li>A função <strong>glDrawPixels</strong> converte-o em formato de ponto fixo, com um número não especificado de bits à direita do ponto binário, independentemente do tipo de dados de memória. Os valores de ponto flutuante são convertidos em valores de ponto fixo verdadeiros. A função <strong>glDrawPixels</strong> converte dados inteiros assinados e não assinados com todos os bits de fração definidos como zero. Os dados de bitmap são convertidos em 0,0 ou 1,0.</li>
<li>A função <strong>glDrawPixels</strong> desloca cada índice de ponto fixo à esquerda por GL_INDEX_SHIFT bits e o adiciona ao GL_INDEX_OFFSET. Se GL_INDEX_SHIFT for negativo, a mudança será à direita. Em ambos os casos, zero bits ocupam locais de bits não especificados no resultado.</li>
<li>Se GL_MAP_STENCIL for true, o índice será substituído pelo valor que <strong>glDrawPixels</strong> faz referência na tabela de pesquisa GL_PIXEL_MAP_S_TO_S.</li>
<li>Se a substituição da pesquisa do índice for concluída ou não, a parte inteira do índice será <strong>, então,</strong>Ed com 2<sup>b</sup> - 1, em que <em>b</em> é o número de bits no buffer do estêncil. Os índices de estêncil resultantes são gravados no buffer de estêncil, de modo que o <em>n</em>º de índice é gravado no local <em>x</em>? = <em>largura</em> <em>x</em><sub>r</sub> + <em>n</em> mod<br/> <em>y</em>? = <em>y</em><sub>r</sub> + <em>n/largura</em><br/> onde (<em>x</em><sub>r</sub> , <em></em> y<sub>r</sub> ) é a posição atual da varredura. Somente o teste de propriedade de pixel, o teste de tesoura e o estêncil writemask afetam essas gravações.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt><strong>GL_DEPTH_COMPONENT</strong></dt> </dl></td>
<td>Cada pixel é um componente de profundidade única. <br/>
<ol>
<li>A função <strong>glDrawPixels</strong> converte dados de ponto flutuante diretamente em um formato de ponto flutuante interno com precisão não especificada. Os dados inteiros assinados são mapeados linearmente para o formato de ponto flutuante interno, de modo que o valor inteiro representável mais positivo seja mapeado para 1,0 e o valor reapresentável mais negativo seja mapeado para-1,0. Os dados inteiros não assinados são mapeados da mesma forma: o maior valor inteiro é mapeado para 1,0 e zero é mapeado para 0,0.</li>
<li>A função <strong>glDrawPixels</strong> multiplica o valor de profundidade de ponto flutuante resultante por GL_DEPTH_SCALE e o adiciona ao GL_DEPTH_BIAS. O resultado é clamped para o intervalo [0, 1].</li>
<li>A função <strong>glDrawPixels</strong> converte os componentes de profundidade resultantes em fragmentos anexando a cor atual da posição de varredura ou as coordenadas de textura e índice de cor a cada pixel e, em seguida, atribuindo coordenadas de janela <em>x</em> e <em>y</em> ao <em>n</em> º de fragmento como <em>x</em>? = <em></em><em>largura</em> x<sub>r</sub> + <em>n</em> mod<br/> <em>y</em>? = <em>y</em><sub>r</sub> + <em>n/largura</em><br/> onde ( <em></em> x<sub>r</sub> ,<em>y</em><sub>r</sub> ) é a posição atual da varredura.<br/></li>
<li>Esses fragmentos de pixel são tratados exatamente como os fragmentos gerados pela rasterização de pontos, linhas ou polígonos. A função <strong>glDrawPixels</strong> aplica o mapeamento de textura, sombra e todas as operações de fragmento antes de gravar os fragmentos no framebuffer.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt><strong>GL_RGBA</strong></dt> </dl></td>
<td>Cada pixel é um grupo de quatro componentes nesta ordem: vermelho, verde, azul, alfa. <br/>
<ol>
<li>A função <strong>glDrawPixels</strong> converte valores de ponto flutuante diretamente em um formato de ponto flutuante interno com precisão não especificada. Valores inteiros assinados são mapeados linearmente para o formato de ponto flutuante interno, de modo que o valor inteiro representável mais positivo seja mapeado para 1,0 e o valor reapresentável mais negativo seja mapeado para-1,0. Os dados inteiros não assinados são mapeados da mesma forma: o maior valor inteiro é mapeado para 1,0 e zero é mapeado para 0,0.</li>
<li>A função <strong>glDrawPixels</strong> multiplica os valores de cor de ponto flutuante resultantes por GL_c_SCALE e os adiciona ao GL_c_BIAS, em que <em>c</em> é vermelho, verde, azul e alfa para os respectivos componentes de cor. Os resultados são clamped para o intervalo [0, 1].</li>
<li>Se GL_MAP_COLOR for true, <strong>glDrawPixels</strong> dimensionará cada componente de cor pelo tamanho da tabela de pesquisa GL_PIXEL_MAP_c_TO_c e, em seguida, substituirá o componente pelo valor que ele faz referência a essa tabela; <em>c</em> é R, G, B ou A, respectivamente.</li>
<li>A função <strong>glDrawPixels</strong> converte as cores de RGBA resultantes em fragmentos anexando as coordenadas de coordenadas <em>z</em>e de textura atuais a cada pixel e, em seguida, atribuindo coordenadas de janela <em>x</em> e <em>y</em> ao <em>n</em>º de fragmento como <em>x</em>? = <em>largura</em> <em>x</em><sub>r</sub> + <em>n</em> mod<br/> <em>y</em>? = <em>y</em><sub>r</sub> + <em>n/Width</em><br/> onde (<em>x</em><sub>r</sub> ,<em>y</em><sub>r</sub> ) é a posição atual da varredura.<br/></li>
<li>Esses fragmentos de pixel são tratados exatamente como os fragmentos gerados pela rasterização de pontos, linhas ou polígonos. A função <strong>glDrawPixels</strong> aplica o mapeamento de textura, sombra e todas as operações de fragmento antes de gravar os fragmentos no framebuffer.</li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Cada pixel é um único componente vermelho.<br/> A função <strong>glDrawPixels</strong> converte esse componente no formato de ponto flutuante interno da mesma forma que o componente vermelho de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com verde e azul definido como 0,0 e alfa definido como 1,0. Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Cada pixel é um único componente verde.<br/> A função <strong>glDrawPixels</strong> converte esse componente no formato de ponto flutuante interno da mesma forma que o componente verde de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho e azul definido como 0,0 e alfa definido como 1,0. Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Cada pixel é um único componente azul.<br/> A função <strong>glDrawPixels</strong> converte esse componente no formato de ponto flutuante interno da mesma forma que o componente azul de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho e verde definido como 0,0 e alfa definido como 1,0. Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Cada pixel é um único componente alfa.<br/> A função <strong>glDrawPixels</strong> converte esse componente no formato de ponto flutuante interno da mesma forma que o componente alfa de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho, verde e azul definido como 0,0. Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Cada pixel é um grupo de três componentes nesta ordem: vermelho, verde, azul. A função <strong>glDrawPixels</strong> converte cada componente no formato de ponto flutuante interno da mesma forma que os componentes vermelho, verde e azul de um pixel RGBA. A cor tripla é convertida em um pixel RGBA com alfa definido como 1,0. Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt><strong>GL_LUMINANCE</strong></dt> </dl></td>
<td>Cada pixel é um único componente de luminância.<br/> A função <strong>glDrawPixels</strong> converte esse componente no formato de ponto flutuante interno da mesma forma que o componente vermelho de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho, verde e azul definido como o valor de luminância convertido e alfa definido como 1,0. Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt><strong>GL_LUMINANCE_ALPHA</strong></dt> </dl></td>
<td>Cada pixel é um grupo de dois componentes nesta ordem: luminância, alfa.<br/> A função <strong>glDrawPixels</strong> converte os dois componentes no formato de ponto flutuante interno da mesma maneira que o componente vermelho de um pixel RGBA e os converte em um pixel RGBA com vermelho, verde e azul definido como o valor de luminância convertido e alfa definido para o valor alfa convertido. Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Cada pixel é um grupo de três componentes nesta ordem: azul, verde e vermelho.<br/> GL_BGR_EXT fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs). Portanto, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>Cada pixel é um grupo de quatro componentes nesta ordem: azul, verde, vermelho, alfa.<br/> GL_BGRA_EXT fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs). Portanto, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de dados para *pixels*. A seguir estão as constantes simbólicas aceitas e seus significados.



| Valor                                                                                                                                                                      | Significado                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**\_byte não assinado GL \_**</dt> </dl>    | Inteiro de 8 bits sem sinal<br/>                 |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**\_byte GL**</dt> </dl>                                | Inteiro de 8 bits com sinal<br/>                   |
| <span id="GL_BITMAP"></span><span id="gl_bitmap"></span><dl> <dt>**\_bitmap GL**</dt> </dl>                          | Bits únicos em inteiros de 8 bits não assinados<br/> |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ não assinado \_ curto**</dt> </dl> | Inteiro de 16 bits sem sinal<br/>                |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ curto**</dt> </dl>                             | Inteiro de 16 bits com sinal<br/>                  |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ não assinado \_ int**</dt> </dl>       | Inteiro de 32 bits sem sinal<br/>                |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**RAZÃO \_ int**</dt> </dl>                                   | Inteiro de 32 bits<br/>                         |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ float**</dt> </dl>                             | Ponto flutuante de precisão simples<br/>        |



 

</dd> <dt>

*pixels* 
</dt> <dd>

Um ponteiro para os dados de pixel.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | A *largura* ou a *altura* era negativa.<br/>                                                                                                                                          |
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | O *formato* ou o *tipo* não era um valor aceito. <br/>                                                                                                                             |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | *Format* era GL \_ Red, GL \_ verde, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminância ou GL de \_ luminância \_ alfa e OpenGL estava no modo de índice de cor.<br/> |
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *tipo* era \_ o bitmap GL e o *formato* não era um índice de cores GL \_ ou o \_ \_ Index de estêncil GL \_ .<br/>                                                                                         |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | o *formato* era \_ \_ um índice de estêncil GL e não havia um buffer de estêncil.<br/>                                                                                                                  |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/>                                                        |


## <a name="remarks"></a>Comentários

A função **glDrawPixels** lê dados de pixel da memória e grava-os em framebuffer em relação à posição de rasterização atual. Use [**glRasterPos**](glrasterpos-functions.md) para definir a posição atual da varredura e use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ posição de varredura atual \_ para consultar a posição da rasterização.

Vários parâmetros definem a codificação dos dados de pixel na memória e controlam o processamento dos dados de pixel antes de serem colocados no framebuffer. Esses parâmetros são definidos com quatro funções: [**glPixelStore**](glpixelstore-functions.md), [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)e [**glPixelZoom**](glpixelzoom.md). Este tópico descreve os efeitos sobre **glDrawPixels** de muitos, mas não todos, dos parâmetros especificados por essas quatro funções.

Os dados são lidos a partir de *pixels* como uma sequência de bytes assinados ou sem sinal, inteiros assinados ou sem sinal, inteiro assinado ou não assinado ou valores de ponto flutuante de precisão única, dependendo do *tipo*. Cada um desses bytes, shorts, inteiros ou valores de ponto flutuante é interpretado como um componente de cor ou profundidade, ou um índice, dependendo do *formato*. Os índices são sempre tratados individualmente. Os componentes de cor são tratados como grupos de um, dois, três ou quatro valores, novamente com base no *formato*. Os índices individuais e os grupos de componentes são chamados de pixels. Se o *tipo* for um \_ bitmap GL, os dados deverão ser bytes não assinados e o *formato* deverá ser um índice de \_ cores GL \_ ou \_ Index de estêncil GL \_ . Cada byte não assinado é tratado como pixels de 8 1 bits, com ordenação de bits determinada por GL \_ Unpack \_ LSB \_ First (consulte [**glPixelStore**](glpixelstore-functions.md)).

A *largura* por pixels de *altura* é lida da memória, começando em *pixels* de localização. Por padrão, esses pixels são retirados de locais de memória adjacentes, exceto que depois que todos os pixels de *largura* são lidos, o ponteiro de leitura é avançado para o próximo limite de 4 bytes. A função **glPixelStore** especifica o alinhamento de linha de 4 bytes com o \_ alinhamento de descompactação do argumento GL \_ , e você pode defini-lo como 1, 2, 4 ou 8 bytes. Outros parâmetros de armazenamento de pixel especificam avanços de ponteiro de leitura diferentes, antes de o primeiro pixel ser lido e depois que todos os pixels de *largura* são lidos. A função **glPixelStore** opera em cada um dos pixels de *largura por altura* que ele lê da memória da mesma maneira, com base nos valores de vários parâmetros especificados por [**glPixelTransfer**](glpixeltransfer.md) e [**glPixelMap**](glpixelmap.md). Os detalhes dessas operações, bem como o buffer de destino no qual os pixels são desenhados, são específicos ao formato dos pixels, conforme especificado por *formato*.

A rasterização descrita até o momento pressupõe fatores de zoom de pixel de 1,0. Se você usar [**glPixelZoom**](glpixelzoom.md) para alterar os fatores de zoom *x* e *y* pixel, os pixels serão convertidos em fragmentos da seguinte maneira. Se (*XR, ano*) for a posição atual da varredura e um determinado pixel estiver na coluna *n*-th e *m* th do retângulo de pixel, os fragmentos serão gerados para os pixels cujos centros estão no retângulo com os cantos em

(*x*<sub>r</sub>  +  *aplicar zoom*? *n*, *y*<sub>r</sub>  +  *zoom*<sub>y</sub> *m*)

(*x*<sub>r</sub>  +  *aplicar zoom*? (*n* + 1), *y*<sub>r</sub>  +  *zoom*<sub>y</sub> (*m* + 1))

onde *aplicar zoom*? é o valor de GL \_ zoom \_ X e *zoom*<sub>y</sub> é o valor de GL \_ zoom \_ y.

As funções a seguir recuperam informações relacionadas ao **glDrawPixels**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ posição de rasterização atual \_

**glGet** com Argument GL \_ \_ posição de rasterização atual \_ \_ válida

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
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

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





