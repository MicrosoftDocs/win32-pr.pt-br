---
title: Função glColorSubTableEXT (Gl.h)
description: A função glColorSubTableEXT especifica uma parte da paleta da textura de alvo a ser substituída.
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- Função glColorSubTableEXT OpenGL
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
ms.openlocfilehash: ff6f4b88a355c25df40a847912d4e3352bd87962
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475392"
---
# <a name="glcolorsubtableext-function"></a>Função glColorSubTableEXT

A **função glColorSubTableEXT** especifica uma parte da paleta da textura de alvo a ser substituída.

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

A textura paleta de destino que deve ter sua paleta alterada. Deve ser TEXTURE \_ 1D ou TEXTURE \_ 2D.

</dd> <dt>

*start* 
</dt> <dd>

A entrada de índice da paleta inicial da paleta a ser alterada.

</dd> <dt>

*contagem* 
</dt> <dd>

O número de entradas de índice de paleta da paleta a ser alterada a partir do *início .* O *parâmetro count* determina o intervalo de entradas de índice de paleta que são alteradas.

</dd> <dt>

*format* 
</dt> <dd>

O formato dos dados de pixel. As constantes simbólicas a seguir são aceitas.




| Valor | Significado | 
|-------|---------|
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl><dt><strong>GL_RGBA</strong></dt></dl> | Cada pixel é um grupo de quatro componentes na seguinte ordem: vermelho, verde, azul, alfa. O formato RGBA é determinado dessa maneira: <br /><ol><li>A <strong>função glColorSubTableEXT</strong> converte valores de ponto flutuante diretamente em um formato interno com precisão não especificada. Os valores inteiros com sinal são mapeados linearmente para o formato interno, de modo que o valor inteiro representável mais positivo mapeia para 1,0 e o valor representável mais negativo é mapeado para -1,0. Dados inteiros sem sinal são mapeados da mesma forma: o maior valor inteiro é mapeado para 1,0 e zero é mapeado para 0,0.</li><li>A <strong>função glColorSubTableEXT</strong> multiplica os valores de cor resultantes por GL_c_SCALE e os adiciona ao GL_c_BIAS, em que <em>c</em> é RED, GREEN, BLUE e ALPHA para os respectivos componentes de cor. Os resultados são fixados no intervalo [0,1].</li><li>Se GL_MAP_COLOR for <strong>TRUE,</strong> <strong>glColorSubTableEXT</strong> dimensiona cada componente de cor pelo tamanho da tabela de GL_PIXEL_MAP_c_TO_c e, em seguida, substitui o componente pelo valor referenciado nessa tabela; <em>c</em> é R, G, B ou A, respectivamente.</li><li>A <strong>função glColorSubTableEXT</strong> converte as cores RGBA resultantes em fragmentos <em></em>anexando as coordenadas de textura e coordenadas de textura e coordenadas da posição raster atual a cada pixel e atribuindo <em>coordenadas de janela x</em> e <em>y</em> ao <em>fragmento n,</em>de forma<em>que x ?</em> = <em>x</em><sub>r</sub>  +  <em>n</em> largura <em>mod</em><br /><em>y</em>? = <em>y</em><sub>r</sub>  + <em>n /width</em><br /> em que (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) é a posição de raster atual.<br /></li><li>Esses fragmentos de pixel são tratados da mesma forma que os fragmentos gerados por pontos de rasterização, linhas ou polígonos. A <strong>função glColorSubTableEXT</strong> aplica o mapeamento de textura, a base e todas as operações de fragmento antes de escrever os fragmentos no framebuffer.</li></ol> | 
| <span id="GL_RED"></span><span id="gl_red"></span><dl><dt><strong>GL_RED</strong></dt></dl> | Cada pixel é um único componente vermelho.<br /> A <strong>função glColorSubTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente vermelho de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com verde e azul definido como 0,0 e alfa definido como 1,0. Após essa conversão, o pixel é tratado como se tivesse sido lido como um pixel RGBA.<br /> | 
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl><dt><strong>GL_GREEN</strong></dt></dl> | Cada pixel é um único componente verde.<br /> A <strong>função glColorSubTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente verde de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho e azul definido como 0,0 e alfa definido como 1,0. Após essa conversão, o pixel é tratado como se tivesse sido lido como um pixel RGBA.<br /> | 
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl><dt><strong>GL_BLUE</strong></dt></dl> | Cada pixel é um único componente azul.<br /> A <strong>função glColorSubTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente azul de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho e verde definido como 0,0 e alfa definido como 1.0. Após essa conversão, o pixel é tratado como se tivesse sido lido como um pixel RGBA.<br /> | 
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl><dt><strong>GL_ALPHA</strong></dt></dl> | Cada pixel é um único componente alfa.<br /> A <strong>função glColorSubTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente alfa de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho, verde e azul definido como 0,0. Após essa conversão, o pixel é tratado como se tivesse sido lido como um pixel RGBA.<br /> | 
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl><dt><strong>GL_RGB</strong></dt></dl> | Cada pixel é um grupo de três componentes nesta ordem: vermelho, verde, azul.<br /> A <strong>função glColorSubTableEXT</strong> converte cada componente no formato interno da mesma forma que os componentes vermelho, verde e azul de um pixel RGBA. A cor tripla é convertida em um pixel RGBA com alfa definido como 1,0. Após essa conversão, o pixel é tratado como se tivesse sido lido como um pixel RGBA.<br /> | 
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl><dt><strong>GL_BGR_EXT</strong></dt></dl> | Cada pixel é um grupo de três componentes nesta ordem: azul, verde, vermelho.<br /> GL_BGR_EXT fornece um formato que corresponde ao layout de memória Windows DIBs (bitmaps independentes de dispositivo). Portanto, seus aplicativos podem usar os mesmos dados com chamadas Windows função e chamadas de função de pixel OpenGL.<br /> | 
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl><dt><strong>GL_BGRA_EXT</strong></dt></dl> | Cada pixel é um grupo de quatro componentes nessa ordem: azul, verde, vermelho, alfa.<br /> GL_BGRA_EXT fornece um formato que corresponde ao layout de memória Windows DIBs (bitmaps independentes de dispositivo). Portanto, seus aplicativos podem usar os mesmos dados com chamadas Windows função e chamadas de função de pixel OpenGL.<br /> | 




 

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de dados para *dados*. As seguintes constantes simbólicas são aceitas: GL \_ UNSIGNED \_ \_ BYTE, GL BYTE, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT e GL \_ FLOAT.

A tabela a seguir resume o significado das constantes válidas para o *parâmetro de* tipo.



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

Um ponteiro para os dados de textura paletada. Os dados são tratados como pixels individuais de uma entrada de paleta de textura 1D para uma entrada de paleta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                              | Significado                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl> | *start* ou *count* era um inteiro inválido.<br/>                                                                                 |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>  | *target*, *format* ou *type* não era um valor aceito.<br/>                                                                    |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glColorSubTableEXT** especifica partes da paleta da textura de alvo atual a serem substituídas. Ao [**contrário de glColorTableEXT,**](glcolortableext.md)não é possível especificar o *parâmetro de* destino como uma paleta de textura de proxy.

> [!Note]  
> A **função glColorSubTableEXT** é uma função de extensão que não faz parte da biblioteca OpenGL padrão, mas faz parte da extensão de textura paleta GL \_ \_ \_ EXT. Para verificar se a implementação do OpenGL dá suporte **a glColorSubTableEXT,** [**chame glGetString**](glgetstring.md)(GL \_ EXTENSIONS). Se ele retornar textura paletada GL \_ \_ \_ EXT, **glColorSubTableEXT** terá suporte. Para obter o endereço de função de uma função de extensão, chame [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Gl.h</dt> </dl> |



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

 

 





