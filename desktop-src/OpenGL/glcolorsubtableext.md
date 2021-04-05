---
title: função glColorSubTableEXT (GL. h)
description: A função glColorSubTableEXT especifica uma parte da paleta da textura de destino a ser substituída.
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- função glColorSubTableEXT OpenGL
topic_type:
- apiref
api_name:
- glColorSubTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0386bda82bf08ae778d20b1be69858698ac7bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824495"
---
# <a name="glcolorsubtableext-function"></a>função glColorSubTableEXT

A função **glColorSubTableEXT** especifica uma parte da paleta da textura de destino a ser substituída.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glColorSubTableEXT(
         GLenum  target,
         GLsizei start,
         GLsizei count,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

A textura da paleta de destino que deve ter sua paleta alterada. Deve ser textura \_ 1D ou 2D de textura \_ .

</dd> <dt>

*start* 
</dt> <dd>

A entrada de índice da paleta inicial da paleta a ser alterada.

</dd> <dt>

*contagem* 
</dt> <dd>

O número de entradas de índice de paleta da paleta a ser alterada começando no *início*. O parâmetro *Count* determina o intervalo de entradas de índice de paleta que são alteradas.

</dd> <dt>

*format* 
</dt> <dd>

O formato dos dados de pixel. As constantes simbólicas a seguir são aceitas.



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
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt><strong>GL_RGBA</strong></dt> </dl></td>
<td>Cada pixel é um grupo de quatro componentes na seguinte ordem: vermelho, verde, azul, alfa. O formato RGBA é determinado dessa maneira: <br/>
<ol>
<li>A função <strong>glColorSubTableEXT</strong> converte valores de ponto flutuante diretamente em um formato interno com precisão não especificada. Valores inteiros assinados são mapeados linearmente para o formato interno, de modo que o valor inteiro representável mais positivo seja mapeado para 1,0 e o valor reapresentável mais negativo seja mapeado para-1,0. Os dados inteiros não assinados são mapeados da mesma forma: o maior valor inteiro é mapeado para 1,0 e zero é mapeado para 0,0.</li>
<li>A função <strong>glColorSubTableEXT</strong> multiplica os valores de cor resultantes por GL_c_SCALE e os adiciona ao GL_c_BIAS, em que <em>c</em> é vermelho, verde, azul e alfa para os respectivos componentes de cor. Os resultados são clamped para o intervalo [0, 1].</li>
<li>Se GL_MAP_COLOR for <strong>true</strong>, <strong>glColorSubTableEXT</strong> dimensionará cada componente de cor pelo tamanho da tabela de pesquisa GL_PIXEL_MAP_c_TO_c e, em seguida, substituirá o componente pelo valor que ele faz referência a essa tabela; <em>c</em> é R, G, B ou A, respectivamente.</li>
<li>A função <strong>glColorSubTableEXT</strong> converte as cores de RGBA resultantes em fragmentos anexando as coordenadas de coordenadas <em>z</em>e de textura atuais a cada pixel e, em seguida, atribuindo coordenadas de janela <em>x</em> e <em>y</em> ao <em>n</em>º de fragmento como<em>x</em>? = <em>largura</em> <em>x</em><sub>r</sub> + <em>n</em> mod<br/> <em>y</em>? = <em>y</em><sub>r</sub> +<em>n/largura</em><br/> onde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) é a posição atual da varredura.<br/></li>
<li>Esses fragmentos de pixel são tratados exatamente como os fragmentos gerados pela rasterização de pontos, linhas ou polígonos. A função <strong>glColorSubTableEXT</strong> aplica o mapeamento de textura, sombra e todas as operações de fragmento antes de gravar os fragmentos no framebuffer.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Cada pixel é um único componente vermelho.<br/> A função <strong>glColorSubTableEXT</strong> converte esse componente no formato interno da mesma maneira que o componente vermelho de um pixel RGBA, em seguida, converte-o em um pixel RGBA com verde e azul definido como 0,0 e alfa definido como 1,0. Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Cada pixel é um único componente verde.<br/> A função <strong>glColorSubTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente verde de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho e azul definido como 0,0 e alfa definido como 1,0. Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Cada pixel é um único componente azul.<br/> A função <strong>glColorSubTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente azul de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho e verde definido como 0,0 e alfa definido como 1,0. Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Cada pixel é um único componente alfa.<br/> A função <strong>glColorSubTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente alfa de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho, verde e azul definido como 0,0. Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Cada pixel é um grupo de três componentes nesta ordem: vermelho, verde, azul.<br/> A função <strong>glColorSubTableEXT</strong> converte cada componente no formato interno da mesma maneira que os componentes vermelho, verde e azul de um pixel RGBA. A cor tripla é convertida em um pixel RGBA com alfa definido como 1,0. Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Cada pixel é um grupo de três componentes nesta ordem: azul, verde e vermelho.<br/> GL_BGR_EXT fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs). Assim, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>Cada pixel é um grupo de quatro componentes nesta ordem: azul, verde, vermelho, alfa.<br/> GL_BGRA_EXT fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs). Assim, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de dados para *dados*. As constantes simbólicas a seguir são aceitas: GL \_ não assinado \_ byte, GL \_ byte, GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int e GL \_ float.

A tabela a seguir resume o significado das constantes válidas para o parâmetro de *tipo* .



| Valor                                                                                                                                                                      | Significado                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**\_byte não assinado GL \_**</dt> </dl>    | Inteiro de 8 bits sem sinal<br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**\_byte GL**</dt> </dl>                                | Inteiro de 8 bits com sinal<br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ não assinado \_ curto**</dt> </dl> | Inteiro de 16 bits sem sinal<br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ curto**</dt> </dl>                             | Inteiro de 16 bits com sinal<br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ não assinado \_ int**</dt> </dl>       | Inteiro de 32 bits sem sinal<br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**RAZÃO \_ int**</dt> </dl>                                   | Inteiro de 32 bits<br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ float**</dt> </dl>                             | Valor do ponto flutuante de precisão simples<br/> |



 

</dd> <dt>

*data* 
</dt> <dd>

Um ponteiro para os dados de textura da paleta. Os dados são tratados como pixels únicos de uma entrada de paleta de textura 1D para uma entrada de paleta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                              | Significado                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl> | *Start* ou *Count* foi um número inteiro inválido.<br/>                                                                                 |
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>  | o *destino*, o *formato* ou o *tipo* não era um valor aceito.<br/>                                                                    |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glColorSubTableEXT** especifica partes da paleta da textura de destino atual a serem substituídas. Ao contrário de [**glColorTableEXT**](glcolortableext.md), você não pode especificar o parâmetro de *destino* como uma paleta de textura de proxy.

> [!Note]  
> A função **glColorSubTableEXT** é uma função de extensão que não faz parte da biblioteca OpenGL padrão, mas faz parte da extensão de textura da paleta do GL \_ ext \_ \_ . Para verificar se a implementação do OpenGL dá suporte a **glColorSubTableEXT**, chame [**glGetString**](glgetstring.md)( \_ extensões GL). Se ele retornar a \_ textura da paleta do GL ext \_ \_ , haverá suporte para **glColorSubTableEXT** . Para obter o endereço da função de uma função de extensão, chame [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





