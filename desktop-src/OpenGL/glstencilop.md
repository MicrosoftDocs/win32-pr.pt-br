---
title: Função glStencilOp (Gl.h)
description: A função glStencilOp define as ações de teste de estêncil.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- Função glStencilOp OpenGL
topic_type:
- apiref
api_name:
- glStencilOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da899207456cece58216874c7540a032326e4180e9484590e2effd619eea72f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614330"
---
# <a name="glstencilop-function"></a>Função glStencilOp

A **função glStencilOp** define as ações de teste de estêncil.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glStencilOp(
   GLenum fail,
   GLenum zfail,
   GLenum zpass
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Falhar* 
</dt> <dd>

A ação a ser tomada quando o teste de estêncil falhar. As seis constantes simbólicas a seguir são aceitas.



| Valor                                                                                                                                                | Significado                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <dt>**GL \_ KEEP**</dt> </dl>          | Mantém o valor atual.<br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <dt>**GL \_ ZERO**</dt> </dl>          | Define o valor do buffer de estêncil como zero.<br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <dt>**GL \_ REPLACE**</dt> </dl> | Define o valor do buffer de estêncil *como ref*, conforme especificado por **glStencilFunc.**<br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <dt>**GL \_ INCR**</dt> </dl>          | Incrementa o valor atual do buffer de estêncil. Fixa para o valor máximo não assinado representável.<br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <dt>**GL \_ DECR**</dt> </dl>          | Diminui o valor atual do buffer de estêncil. Fixa a zero.<br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**GL \_ INVERT**</dt> </dl>    | Inverte bit a bit o valor atual do buffer de estêncil.<br/>                                                |



 

</dd> <dt>

*zfail* 
</dt> <dd>

Ação de estêncil quando o teste de estêncil é aprovado, mas o teste de profundidade falha. Aceita as mesmas constantes simbólicas que *falham.*

</dd> <dt>

*zpass* 
</dt> <dd>

Ação de estêncil quando o teste de estêncil e a profundidade de teste são aprovados ou quando o teste de estêncil é aprovado e não há nenhum buffer de profundidade ou teste de profundidade não está habilitado. Aceita as mesmas constantes simbólicas que *falham.*

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *fail*, *zfail* ou *zpass* era qualquer valor diferente dos seis valores constantes definidos.<br/>                                      |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A cerca, como *z*-buffering, habilita e desabilita o desenho por pixel. Você desenha nos planos de estêncil usando primitivos de desenho OpenGL e, em seguida, renderiza geometria e imagens, usando os planos de estêncil para mascarar partes da tela. Normalmente, a estrutura é usada em algoritmos de renderização multipasso para obter efeitos especiais, como decalques, estrutura de estrutura de estrutura e renderização construtiva de geometria sólida.

O teste de estêncil elimina condicionalmente um pixel com base no resultado de uma comparação entre o valor no buffer de estêncil e um valor de referência. O teste é habilitado com [**chamadas glEnable**](glenable.md) e [**glDisable**](gldisable.md) com o argumento GL \_ STENCIL TEST e controlado com \_ [**glStencilFunc**](glstencilfunc.md).

A **função glStencilOp** aceita três argumentos que indicam o que acontece com o valor de estêncil armazenado enquanto a cerca está habilitada. Se o teste de estêncil falhar, nenhuma alteração será feita nos  buffers de cor ou profundidade do pixel e falhará especificando o que acontece com o conteúdo do buffer de estêncil.

Os valores de buffer de estêncil são tratados como inteiros sem sinal. Quando incrementados e decrementados, os valores são fixados em 0 e 2 *n* 1, em que *n* é o valor retornado consultando GL \_ STENCIL \_ BITS.

Os outros dois argumentos para **glStencilOp especificam** ações de buffer de estêncil caso os testes de buffer de profundidade subsequentes deem êxito (*zpass*) ou falham (*zfail*). (Consulte [**glDepthFunc**](gldepthfunc.md).) Eles são especificados usando as mesmas seis constantes simbólicas que *falham.* Observe que *zfail* é ignorado quando não há buffer de profundidade ou quando o buffer de profundidade não está habilitado. Nesses casos, *fail e* *zpass* especificam a ação de estêncil quando o teste de estêncil falha e é aprovado, respectivamente.

Inicialmente, o teste de estêncil está desabilitado. Se não houver nenhum buffer de estêncil, nenhuma modificação de estêncil poderá ocorrer e será como se os testes de estêncil sempre passem, independentemente de qualquer chamada para **glStencilOp**.

As funções a seguir recuperam informações **relacionadas a glStencilOp**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ STENCIL \_ FAIL

**glGet** com o argumento GL \_ STENCIL \_ PASS DEPTH \_ \_ PASS

**glGet** com o argumento GL \_ STENCIL \_ PASS DEPTH \_ \_ FAIL

**glGet** com o argumento GL \_ STENCIL \_ BITS

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ STENCIL \_ TEST

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





