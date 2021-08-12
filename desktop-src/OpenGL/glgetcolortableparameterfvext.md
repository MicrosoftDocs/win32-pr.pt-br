---
title: função glGetColorTableParameterfvEXT (GL. h)
description: As funções glGetColorTableParameterfvEXT e glGetColorTableParameterivEXT obtêm parâmetros de paleta de tabelas de cores. | função glGetColorTableParameterfvEXT (GL. h)
ms.assetid: e78051aa-4233-413c-8838-0741b54eab0e
keywords:
- função glGetColorTableParameterfvEXT OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterfvEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e7cd93c45c602b35e88fe28c467943829669d329f75007607783ece06f1b51b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118615766"
---
# <a name="glgetcolortableparameterfvext-function"></a>função glGetColorTableParameterfvEXT

As funções **glGetColorTableParameterfvEXT** e [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) obtêm parâmetros de paleta de tabelas de cores.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetColorTableParameterfvEXT(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

A textura de destino da paleta para a qual você deseja dados de parâmetro. Deve ser a textura \_ 1D, a textura \_ 2D, a \_ textura \_ de proxy 1D ou a textura de proxy \_ \_ 2D.

</dd> <dt>

*pname* 
</dt> <dd>

Uma constante simbólica para o tipo de dados de parâmetro de paleta apontados por *params*.

A seguir estão as constantes simbólicas aceitas e seus significados.



| Valor                                                                                                                                                                                                             | Significado                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <dt>**\_formato de tabela de cores GL \_ \_ \_ ext**</dt> </dl>              | Retornar o formato interno especificado pela chamada mais recente para [**glColorTableEXT**](glcolortableext.md) ou o valor padrão.<br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <dt>**\_extensão da \_ largura da tabela de cores GL \_ \_**</dt> </dl>                 | Retorna a largura da paleta atual.<br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <dt>**\_extensão de cor GL \_ \_ Red \_ Size \_ ext**</dt> </dl>       | Retorne o tamanho real usado internamente para armazenar o componente vermelho dos dados da paleta.<br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <dt>**\_ext. \_ de \_ Tamanho verde da tabela de cores \_ GL \_**</dt> </dl> | Retorne o tamanho real usado internamente para armazenar o componente verde dos dados da paleta.<br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <dt>**\_ext. \_ de \_ tamanho azul da tabela de cores \_ GL \_**</dt> </dl>    | Retorne o tamanho real usado internamente para armazenar o componente azul dos dados da paleta.<br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <dt>**\_ext. \_ de \_ tamanho alfa da tabela de cores \_ GL \_**</dt> </dl> | Retornar o tamanho real usado internamente para armazenar o componente alfa dos dados da paleta.<br/>                                         |



 

</dd> <dt>

*params* 
</dt> <dd>

Aponta para os dados de parâmetro da tabela de cores especificados pelo parâmetro *pname* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use as funções **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT** para recuperar dados de parâmetro específicos de tabelas de cores definidas com [**glColorTableEXT**](glcolortableext.md) para paletas de textura direcionadas. Além disso, você pode usar essas funções para determinar o número de entradas da tabela de cores que o **glGetColorTableEXT** retorna.

Quando o parâmetro de *destino* for GL proxy ou textura \_ de proxy ingl \_ \_ \_ 2D ou \_ \_ insupport e a implementação não oferecer suporte aos valores especificados para o *formato* ou a *largura*, **glColorTableEXT** poderá falhar ao criar a tabela de cores solicitada. Nesse caso, a tabela de cores está vazia e todos os parâmetros recuperados serão zero. Você pode determinar se o OpenGL dá suporte a um formato e tamanho de tabela de cores específico chamando **glColorTableEXT** com um destino de proxy e, em seguida, chamando **glGetColorTableParameterivEXT** ou **glGetColorTableParameterfvEXT** para determinar se o parâmetro de largura corresponde ao definido por **glColorTableEXT**. Se a largura recuperada for zero, a solicitação da tabela de cores por **glColorTable** falhou. Se a largura recuperada não for zero, você poderá chamar **glColorTable** com o destino real com textura \_ 1D ou \_ a textura 2D para definir a tabela de cores.

As funções **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT** são funções de extensão que não fazem parte da biblioteca OpenGL padrão, mas fazem parte da extensão de textura da paleta do GL \_ ext \_ \_ . Para verificar se a implementação do OpenGL dá suporte a **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT**, chame [**glGetString**](glgetstring.md)**(** \_ extensões GL **)**. Se ele retornar a \_ textura da paleta do GL ext \_ \_ , **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT** têm suporte. Para obter o endereço da função de uma função de extensão, chame [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





