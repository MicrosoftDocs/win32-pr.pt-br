---
title: função glDrawBuffer (GL. h)
description: A função glDrawBuffer especifica em quais buffers de cores devem ser desenhados.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- função glDrawBuffer OpenGL
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
ms.openlocfilehash: 3a99bd2b184766f1621d89b2c8d642902d300e14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754522"
---
# <a name="gldrawbuffer-function"></a>função glDrawBuffer

A função **glDrawBuffer** especifica em quais buffers de cores devem ser desenhados.

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

Especifica até quatro buffers de cores a serem desenhados com as constantes simbólicas aceitáveis a seguir.



| Valor                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <dt>**\_nenhum GL**</dt> </dl>                                 | Nenhum buffer de cores é gravado.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <dt>**GL \_ frontal \_ esquerdo**</dt> </dl>              | Somente o buffer de cores do lado esquerdo é gravado.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <dt>**\_frontal \_ do GL**</dt> </dl>           | Somente o buffer de cores do lado direito é gravado.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <dt>**\_voltar \_ à esquerda do GL**</dt> </dl>                 | Somente o buffer de cores de trás para a esquerda é gravado.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <dt>**\_direito de voltar \_ do GL**</dt> </dl>              | Somente o buffer de cores de fundo à direita é gravado.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <dt>**frente do GL \_**</dt> </dl>                              | Somente os buffers de cores front-Left e front-Right são gravados. Se não houver buffer de cor de front-Right, somente o buffer de cor frontal à esquerda será gravado.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <dt>**GL \_ regressivo**</dt> </dl>                                 | Somente os buffers de cor back-Left e back-Right são gravados. Se não houver buffer de cor do lado direito, somente o buffer de cores do lado esquerdo será gravado.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <dt>**GL \_ restante**</dt> </dl>                                 | Somente os buffers de cores front-Left e back-Left são gravados. Se não houver nenhum buffer de cor de back-Left, somente o buffer de cores do lado esquerdo será gravado.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <dt>**GL \_ à direita**</dt> </dl>                              | Somente os buffers de cores front-Right e back-Right são gravados. Se não houver buffer de cor do lado direito, somente o buffer de cores do lado direito será gravado.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <dt>**GL \_ frontal \_ e \_ posterior**</dt> </dl> | Todos os buffers de cor frontal e traseira (front-Left, frontal direita, back-Left, back-right) são gravados. Se não houver buffers de cor de fundo, somente os buffers de cores front-Left e front-Right serão gravados. Se não houver buffers de cor corretos, somente os buffers de cores front-Left e back-Left serão gravados. Se não houver buffers de cor direita ou voltar, somente o buffer de cores do lado esquerdo será gravado.<br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <dt>**\_AUXI GL**</dt> </dl>       | Somente o buffer de cores auxiliares *i* é gravado; *estou* entre \_ buffers auxiliares 0 e GL \_ -1. (GL \_ \_Os buffers de aux não são o limite superior; use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para consultar o número de buffers auxiliares disponíveis.)<br/>                                                                                                                            |



 

O valor padrão é GL \_ frontal para contextos de buffer único e GL \_ volta para contextos de buffer duplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *modo* não era um valor aceito.<br/>                                                                                          |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | Nenhum dos buffers indicados pelo *modo* existia.<br/>                                                                           |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |


## <a name="remarks"></a>Comentários

Quando as cores são gravadas no framebuffer, elas são gravadas nos buffers de cores especificados por **glDrawBuffer**.

Se mais de um buffer de cores for selecionado para desenho, as operações de mesclagem ou lógicas serão computadas e aplicadas de forma independente para cada buffer de cor e poderão produzir resultados diferentes em cada buffer.

Contextos de Monoscopic incluem somente buffers à esquerda e contextos estereoscópico incluem buffers esquerdo e direito. Da mesma forma, contextos de buffer único incluem somente buffers frontais e contextos com buffer duplo incluem buffers de frente e de trás. O contexto é selecionado na inicialização do OpenGL.

É sempre o caso que GL \_ aux *i* = GL \_ AUX0 + *i*.

As funções a seguir recuperam informações relacionadas à função **glDrawBuffer** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento de desenho do Argument GL \_ \_

**glGet** com \_ buffers auxiliares do Argument GL \_

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

 

 





