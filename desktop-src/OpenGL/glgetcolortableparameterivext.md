---
title: Função glGetColorTableParameterivEXT (Gl.h)
description: As funções glGetColorTableParameterfvEXT e glGetColorTableParameterivEXT obterão parâmetros de paleta de tabelas de cores. | Função glGetColorTableParameterivEXT (Gl.h)
ms.assetid: 39a0b346-d103-4426-8536-95e7e1548f7a
keywords:
- Função GlGetColorTableParameterivEXT OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterivEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc45217d420aab9c5db3b1ceb416c369b5fb948df2911ea20e6e174eeed0649f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742027"
---
# <a name="glgetcolortableparameterivext-function"></a>Função glGetColorTableParameterivEXT

As [**funções glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) e **glGetColorTableParameterivEXT** obterão parâmetros de paleta de tabelas de cores.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetColorTableParameterivEXT(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

A textura de destino da paleta para a qual você deseja dados de parâmetro. Deve ser TEXTURE \_ 1D, TEXTURE \_ 2D, PROXY \_ TEXTURE \_ 1D ou PROXY \_ TEXTURE \_ 2D.

</dd> <dt>

*Pname* 
</dt> <dd>

Uma constante simbólica para o tipo de dados de parâmetro de paleta apontado por *parâmetros*.

A seguir estão as constantes simbólicas aceitas e seus significados.



| Valor                                                                                                                                                                                                             | Significado                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <dt>**FORMATO DE \_ TABELA DE CORES GL \_ \_ \_ EXT**</dt> </dl>              | Retorne o formato interno especificado pela chamada mais recente para [**glColorTableEXT**](glcolortableext.md) ou o valor padrão.<br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ WIDTH \_ EXT**</dt> </dl>                 | Retornar a largura da paleta atual.<br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ RED \_ SIZE \_ EXT**</dt> </dl>       | Retornar o tamanho real usado internamente para armazenar o componente vermelho dos dados da paleta.<br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ GREEN \_ SIZE \_ EXT**</dt> </dl> | Retornar o tamanho real usado internamente para armazenar o componente verde dos dados da paleta.<br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ BLUE \_ SIZE \_ EXT**</dt> </dl>    | Retornar o tamanho real usado internamente para armazenar o componente azul dos dados da paleta.<br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <dt>**TAMANHO \_ ALFA DA TABELA DE CORES GL \_ \_ \_ \_ EXT**</dt> </dl> | Retornar o tamanho real usado internamente para armazenar o componente alfa dos dados da paleta.<br/>                                         |



 

</dd> <dt>

*params* 
</dt> <dd>

Aponta para os dados de parâmetro da tabela de cores especificados pelo *parâmetro pname.*

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use as funções **glGetColorTableParameterivEXT** e [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) para recuperar dados de parâmetro específicos de tabelas de cores definidas com [**glColorTableEXT**](glcolortableext.md) para paletas de textura direcionadas. Além disso, você pode usar essas funções para determinar o número de entradas da tabela de cores **que glGetColorTableEXT** retorna.

Quando  o parâmetro de destino é GL PROXY TEXTURE 1D ou GL PROXY TEXTURE 2D e a implementação não dá suporte aos valores especificados para formato ou largura \_ , \_ \_ \_ \_ \_ **glColorTableEXT**  pode falhar ao criar a tabela de cores solicitada. Nesse caso, a tabela de cores está vazia e todos os parâmetros recuperados serão zero. Você pode determinar se o OpenGL dá suporte a um formato e tamanho de tabela de cores específicos chamando **glColorTableEXT** com um destino de proxy e, em seguida, chamando **glGetColorTableParameterivEXT** ou [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) para determinar se o parâmetro de largura corresponde ao definido por **glColorTableEXT**. Se a largura recuperada for zero, a solicitação da tabela de cores por **glColorTable** falhará. Se a largura recuperada não for zero, você poderá chamar **glColorTable** com o destino real com TEXTURE 1D ou TEXTURE 2D para definir a \_ \_ tabela de cores.

As **funções glGetColorTableParameterivEXT** e [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) são funções de extensão que não fazem parte da biblioteca OpenGL padrão, mas que fazem parte da extensão de textura paleta GL \_ \_ \_ EXT. Para verificar se sua implementação do OpenGL dá suporte **a glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT**, chame [**glGetString**](glgetstring.md)**(** GL \_ EXTENSIONS **)**. Se ele retornar textura paleta GL EXT, há suporte para \_ \_ \_ **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT.** Para obter o endereço de função de uma função de extensão, chame [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

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

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





