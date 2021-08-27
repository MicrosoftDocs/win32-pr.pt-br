---
title: Função glGetColorTableEXT (Gl.h)
description: A função glGetColorTableEXT obtém os dados da tabela de cores da paleta de textura de alvo atual.
ms.assetid: 9169c4e1-a22e-48fe-bd45-4549c1a10ff0
keywords:
- Função glGetColorTableEXT OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46593ac7b03781288d7d0d3932ced799dbbdfcff
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469623"
---
# <a name="glgetcolortableext-function"></a>Função glGetColorTableEXT

A **função glGetColorTableEXT** obtém os dados da tabela de cores da paleta de textura de alvo atual.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetColorTableEXT(
         GLenum target,
         GLenum format,
         GLenum type,
   const GLvoid *data
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

A textura de destino que deve ter sua paleta alterada. Deve ser TEXTURE \_ 1D ou TEXTURE \_ 2D.

</dd> <dt>

*format* 
</dt> <dd>

O formato dos dados de pixel. As constantes simbólicas a seguir são aceitas.




| Valor | Significado | 
|-------|---------|
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl><dt><strong>GL_RGBA</strong></dt></dl> | Cada pixel é um grupo de quatro componentes na seguinte ordem: vermelho, verde, azul, alfa. O formato RGBA é determinado dessa maneira: <br /><ol><li>A <strong>função glGetColorTableEXT</strong> converte valores de ponto flutuante diretamente em um formato interno com precisão não especificada. Os valores inteiros com sinal são mapeados linearmente para o formato interno, de modo que o valor inteiro representável mais positivo mapeia para 1,0 e o valor inteiro representável mais negativo é mapeado para -1,0. Dados inteiros sem sinal são mapeados da mesma forma: o maior valor inteiro é mapeado para 1,0 e zero é mapeado para 0,0.</li><li>A <strong>função glGetColorTableEXT</strong> multiplica os valores de cor resultantes por GL_c_SCALE e os adiciona ao GL_c_BIAS, em que <em>c</em> é RED, GREEN, BLUE e ALPHA para os respectivos componentes de cor. Os resultados são fixados no intervalo [0,1].</li><li>Se GL_MAP_COLOR for <strong>TRUE,</strong> <strong>glGetColorTableEXT</strong> dimensiona cada componente de cor pelo tamanho da tabela de GL_PIXEL_MAP_c_TO_c e, em seguida, substitui o componente pelo valor referenciado nessa tabela; <em>c</em> é R, G, B ou A, respectivamente.</li><li>A <strong>função glGetColorTableEXT</strong> converte as cores RGBA resultantes em fragmentos anexando as coordenadas de textura e a coordenada de textura da posição de raster atual a cada pixel e atribuindo <em>coordenadas de</em> janela x e <em>y</em> ao <em>fragmento n,</em>de forma <em>que x ?</em> = <em>x</em><sub>r</sub>  +  <em>n</em> largura <em>mod</em><br /><em>y</em>? = <em>y</em><sub>r</sub>  +  <em>n/width</em><br /> em que (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) é a posição de raster atual.<br /></li><li>Esses fragmentos de pixel são tratados da mesma forma que os fragmentos gerados por pontos de rasterização, linhas ou polígonos. A <strong>função glGetColorTableEXT</strong> aplica o mapeamento de textura, a base e todas as operações de fragmento antes de escrever os fragmentos no framebuffer.</li></ol> | 
| <span id="GL_RED"></span><span id="gl_red"></span><dl><dt><strong>GL_RED</strong></dt></dl> | Cada pixel é um único componente vermelho.<br /> A <strong>função glGetColorTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente vermelho de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com verde e azul definido como 0,0 e alfa definido como 1.0. Após essa conversão, o pixel é tratado como se tivesse sido lido como um pixel RGBA.<br /> | 
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl><dt><strong>GL_GREEN</strong></dt></dl> | Cada pixel é um único componente verde.<br /> A <strong>função glGetColorTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente verde de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho e azul definido como 0,0 e alfa definido como 1.0. Após essa conversão, o pixel é tratado como se tivesse sido lido como um pixel RGBA.<br /> | 
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl><dt><strong>GL_BLUE</strong></dt></dl> | Cada pixel é um único componente azul.<br /> A <strong>função glGetColorTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente azul de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho e verde definido como 0,0 e alfa definido como 1,0. Após essa conversão, o pixel é tratado como se tivesse sido lido como um pixel RGBA.<br /> | 
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl><dt><strong>GL_ALPHA</strong></dt></dl> | Cada pixel é um único componente alfa.<br /> A <strong>função glGetColorTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente alfa de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho, verde e azul definido como 0,0. Após essa conversão, o pixel é tratado como se tivesse sido lido como um pixel RGBA.<br /> | 
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl><dt><strong>GL_RGB</strong></dt></dl> | Cada pixel é um grupo de três componentes nesta ordem: vermelho, verde, azul.<br /> A <strong>função glGetColorTableEXT</strong> converte cada componente no formato interno da mesma forma que os componentes vermelho, verde e azul de um pixel RGBA. A cor tripla é convertida em um pixel RGBA com alfa definido como 1,0. Após essa conversão, o pixel é tratado como se tivesse sido lido como um pixel RGBA.<br /> | 
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl><dt><strong>GL_BGR_EXT</strong></dt></dl> | Cada pixel é um grupo de três componentes nesta ordem: azul, verde, vermelho.<br /> GL_BGR_EXT fornece um formato que corresponde ao layout de memória do Microsoft Windows DIBs (bitmaps independentes de dispositivo). Portanto, seus aplicativos podem usar os mesmos dados com chamadas Windows função e chamadas de função de pixel OpenGL.<br /> | 
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl><dt><strong>GL_BGRA_EXT</strong></dt></dl> | Cada pixel é um grupo de quatro componentes nessa ordem: azul, verde, vermelho, alfa.<br /> GL_BGRA_EXT fornece um formato que corresponde ao layout de memória Windows DIBs (bitmaps independentes de dispositivo). Portanto, seus aplicativos podem usar os mesmos dados com chamadas Windows função e chamadas de função de pixel OpenGL.<br /> | 




 

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de dados para *dados*. A seguir estão as constantes simbólicas aceitas e seus significados.



| Valor                                                                                                                                                                      | Significado                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL \_ UNSIGNED \_ BYTE**</dt> </dl>    | Inteiro de 8 bits sem sinal<br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ BYTE**</dt> </dl>                                | Inteiro de 8 bits com sinal<br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ UNSIGNED \_ SHORT**</dt> </dl> | Inteiro de 16 bits sem sinal<br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ SHORT**</dt> </dl>                             | Inteiro de 16 bits com sinal<br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ UNSIGNED \_ INT**</dt> </dl>       | Inteiro de 32 bits sem sinal<br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ INT**</dt> </dl>                                   | Inteiro de 32 bits<br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ FLOAT**</dt> </dl>                             | Valor do ponto flutuante de precisão simples<br/> |



 

</dd> <dt>

*data* 
</dt> <dd>

Aponta para o local em que as informações da tabela de cores retornadas devem ser armazenadas. Cada entrada da tabela de cores é armazenada como se fosse um único pixel de uma textura 1D. Como todas as texturas têm uma paleta padrão, **glGetColorTableEXT** sempre retorna informações de paleta, mesmo se os dados de textura não estão em um formato paletado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target*, *format* ou *type* não era um valor aceito.<br/>                                                                   |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glGetColorTableEXT** obtém os dados reais da tabela de cores especificados por [**glColorTableEXT**](glcolortableext.md) e [**glColorSubTableEXT.**](glcolorsubtableext.md)

A **função glGetColorTableEXT** é uma função de extensão que não faz parte da biblioteca OpenGL padrão, mas faz parte da extensão de textura paletada GL \_ \_ \_ EXT. Para verificar se a implementação do OpenGL dá **suporte a glGetColorTableEXT,** [**chame glGetString**](glgetstring.md)(GL \_ EXTENSIONS). Se retornar textura paletada GL \_ \_ \_ EXT, **há suporte para glGetColorTableEXT.** Para obter o endereço de função de uma função de extensão, chame [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Gl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





