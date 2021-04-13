---
title: função glLogicOp (GL. h)
description: A função glLogicOp especifica uma operação de pixel lógica para renderização de índice de cor.
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- função glLogicOp OpenGL
topic_type:
- apiref
api_name:
- glLogicOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb29e8f845e99f6d3c988dfd0c0201de129bee69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499824"
---
# <a name="gllogicop-function"></a>função glLogicOp

A função **glLogicOp** especifica uma operação de pixel lógica para renderização de índice de cor.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*opcode* 
</dt> <dd>

Uma constante simbólica que seleciona uma operação lógica. Os símbolos a seguir são aceitos em que s é igual ao valor do bit de origem e d é o valor do bit de destino.



| Valor                                                                                                                                                                   | Significado              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <dt>**GL \_ desmarcado**</dt> </dl>                          | 0<br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <dt>**\_set GL**</dt> </dl>                                | 1<br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <dt>**\_cópia GL**</dt> </dl>                             | s<br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <dt>**a \_ cópia GL é \_ invertida**</dt> </dl> | ! s<br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <dt>**o \_ NOOP GL**</dt> </dl>                             | d<br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**\_inverter GL**</dt> </dl>                       | ! d<br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <dt>**GL \_ e**</dt> </dl>                                | s & d<br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <dt>**GL \_ NAND**</dt> </dl>                             | ! (s & d)<br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <dt>**GL \_ ou**</dt> </dl>                                   | s \| d<br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <dt>**GL \_ e**</dt> </dl>                                | ! (s \| )<br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <dt>**\_XOR GL**</dt> </dl>                                | s ^ d<br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <dt>**GL \_ equiv**</dt> </dl>                          | ! (s ^ d)<br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <dt>**GL \_ e \_ reverso**</dt> </dl>       | s &! d<br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <dt>**GL \_ e \_ invertido**</dt> </dl>    | ! s & d<br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <dt>**GL \_ ou \_ reverso**</dt> </dl>          | s \| ! d<br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <dt>**GL \_ ou \_ invertido**</dt> </dl>       | ! s \| d<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *opcode* não era um valor aceito.<br/>                                                                                        |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glLogicOp** especifica uma operação lógica que, quando habilitada, é aplicada entre o índice de cores de entrada e o índice de cores no local correspondente no framebuffer. A operação lógica está habilitada ou desabilitada com [**glEnable**](glenable.md) e **glDisable** usando a lógica simbólica de Operational do GL de constante \_ \_ .

O parâmetro *opcode* é uma constante simbólica escolhida na lista abaixo. Na explicação das operações lógicas, *s* representa o índice de cores de entrada e *d* representa o índice no framebuffer. Os operadores padrão de linguagem C são usados. À medida que esses operadores bit a pouco sugerem, a operação lógica é aplicada de forma independente a cada par de bits dos índices de origem e de destino.

As operações de pixel lógico não são aplicadas a buffers de cores RGBA.

Quando mais de um buffer de índice de cor está habilitado para o desenho, as operações lógicas são feitas separadamente para cada buffer habilitado, usando o conteúdo desse buffer para o índice de destino (consulte [**glDrawBuffer**](gldrawbuffer.md)).

O parâmetro *opcode* deve ser um dos 16 valores aceitos. Outros valores resultam em um erro.

As funções a seguir recuperam informações relacionadas ao **glLogicOp**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com modo de \_ op lógico de Argument GL \_ \_

[**glIsEnabled**](glisenabled.md) com o argumento GL \_ lógico \_ op

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

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





