---
title: Função glDrawBuffer (Gl.h)
description: A função glDrawBuffer especifica em quais buffers de cores devem ser desenhados.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- Função glDrawBuffer OpenGL
topic_type:
- apiref
api_name:
- glDrawBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5bc715aad24198031ed096d53f1a468b6672532e4df4ae1ef66b416002a65b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081606"
---
# <a name="gldrawbuffer-function"></a>Função glDrawBuffer

A **função glDrawBuffer** especifica em quais buffers de cores devem ser desenhados.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glDrawBuffer(
   GLenum mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mode* 
</dt> <dd>

Especifica até quatro buffers de cores a serem desenhados com as seguintes constantes simbólicas aceitáveis.



| Valor                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <dt>**GL \_ NONE**</dt> </dl>                                 | Nenhum buffer de cores é gravado.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <dt>**GL \_ FRONT \_ LEFT**</dt> </dl>              | Somente o buffer de cores da frente esquerda é gravado.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <dt>**GL \_ FRONT \_ RIGHT**</dt> </dl>           | Somente o buffer de cores da frente direita é gravado.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <dt>**GL \_ BACK \_ LEFT**</dt> </dl>                 | Somente o buffer de cores da parte traseira esquerda é gravado.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <dt>**GL \_ BACK \_ RIGHT**</dt> </dl>              | Somente o buffer de cores do back-right é gravado.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <dt>**GL \_ FRONT**</dt> </dl>                              | Somente os buffers de cores da frente esquerda e da direita são gravados. Se não houver nenhum buffer de cores à frente direita, somente o buffer de cor esquerda frontal será gravado.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <dt>**GL \_ BACK**</dt> </dl>                                 | Somente os buffers de cores de voltar para a esquerda e para a direita são gravados. Se não houver nenhum buffer de cores à direita, somente o buffer de cores da parte traseira esquerda será gravado.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <dt>**GL \_ LEFT**</dt> </dl>                                 | Somente os buffers de cores à esquerda esquerda e esquerda esquerda são gravados. Se não houver nenhum buffer de cores à esquerda, somente o buffer de cores da parte frontal esquerda será gravado.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <dt>**GL \_ RIGHT**</dt> </dl>                              | Somente os buffers de cores à direita e à direita frontal são gravados. Se não houver nenhum buffer de cores à direita, somente o buffer de cores da frente direita será gravado.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <dt>**GL \_ FRONT \_ E \_ BACK**</dt> </dl> | Todos os buffers de cores frontal e voltar (front-left, front-right, back-left, back-right) são gravados. Se não houver buffers de cor de fundo, somente os buffers de cores da frente esquerda e da frente direita serão gravados. Se não houver buffers de cores à direita, somente os buffers de cores à esquerda esquerda e esquerda esquerda serão gravados. Se não houver buffers de cores à direita ou voltar, somente o buffer de cores da parte frontal esquerda será gravado.<br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <dt>**GL \_ AUXi**</dt> </dl>       | Somente o buffer de cor auxiliar *i* é gravado; *i* está entre 0 e GL \_ AUX \_ BUFFERS - 1. (GL \_ BUFFERS \_ de AUX não é o limite superior; use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para consultar o número de buffers auxiliares disponíveis.)<br/>                                                                                                                            |



 

O valor padrão é GL FRONT para contextos em \_ buffer único e GL BACK para \_ contextos com buffer duplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *mode* não era um valor aceito.<br/>                                                                                          |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | Nenhum dos buffers indicados pelo *modo* existia.<br/>                                                                           |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |


## <a name="remarks"></a>Comentários

Quando as cores são escritas no framebuffer, elas são escritas nos buffers de cores especificados por **glDrawBuffer.**

Se mais de um buffer de cores for selecionado para desenho, as operações lógicas ou de mesclagem serão computadas e aplicadas independentemente para cada buffer de cores e poderão produzir resultados diferentes em cada buffer.

Os contextos monogramas incluem apenas buffers esquerdos e contextos estereotipagem incluem buffers esquerdo e direito. Da mesma forma, os contextos com buffer único incluem apenas buffers front e os contextos com buffer duplo incluem buffers front e back. O contexto é selecionado na inicialização do OpenGL.

É sempre o caso de GL \_ AUX *i* = GL \_ AUX0 + *i*.

As funções a seguir recuperam informações relacionadas à **função glDrawBuffer:**

[**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o argumento GL \_ DRAW \_ BUFFER

**glGet** com o argumento GL \_ AUX \_ BUFFERS

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> </dl>

 

 





