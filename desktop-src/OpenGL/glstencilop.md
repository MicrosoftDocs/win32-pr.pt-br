---
title: função glStencilOp (GL. h)
description: A função glStencilOp define as ações de teste de estêncil.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- função glStencilOp OpenGL
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
ms.openlocfilehash: 8b23162f8606ed68dc90a0cb6debdcc903e0ccd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789741"
---
# <a name="glstencilop-function"></a>função glStencilOp

A função **glStencilOp** define as ações de teste de estêncil.

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

*recuperação* 
</dt> <dd>

A ação a ser tomada quando o teste de estêncil falhar. As seis constantes simbólicas a seguir são aceitas.



| Valor                                                                                                                                                | Significado                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <dt>**\_Keep GL**</dt> </dl>          | Mantém o valor atual.<br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <dt>**GL \_ zero**</dt> </dl>          | Define o valor do buffer de estêncil como zero.<br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <dt>**\_substituição GL**</dt> </dl> | Define o valor do buffer de estêncil como *ref*, conforme especificado por **glStencilFunc**.<br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <dt>**\_incr GL**</dt> </dl>          | Incrementa o valor do buffer do estêncil atual. Coloca o valor não assinado máximo reapresentável.<br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <dt>**\_DECR GL**</dt> </dl>          | Decrementa o valor do buffer do estêncil atual. Coloca para zero.<br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**\_inverter GL**</dt> </dl>    | A bit invertido inverte o valor do buffer do estêncil atual.<br/>                                                |



 

</dd> <dt>

*zfail* 
</dt> <dd>

Ação de estêncil quando o teste de estêncil passa, mas o teste de profundidade falha. Aceita as mesmas constantes simbólicas como *falha.*

</dd> <dt>

*zpass* 
</dt> <dd>

Ação de estêncil quando o teste de estêncil e o teste de profundidade são aprovados, ou quando o teste de estêncil passa e não há um buffer de profundidade ou o teste de profundidade não está habilitado. Aceita as mesmas constantes simbólicas como *falha*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *Fail*, *zfail* ou *ZPass* era qualquer valor diferente dos seis valores constantes definidos.<br/>                                      |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

O estêncil, como o armazenamento em buffer *z*, habilita e desabilita o desenho em uma base por pixel. Você desenha nos planos de estêncil usando primitivas de desenho OpenGL e, em seguida, renderiza a geometria e as imagens, usando os planos de estêncil para mascarar partes da tela. A criação de estêncil normalmente é usada em algoritmos de renderização de passagem multipassadas para obter efeitos especiais, como decals, estrutura de tópicos e renderização de geometria sólida construtivas.

O teste de estêncil elimina condicionalmente um pixel com base no resultado de uma comparação entre o valor no buffer do estêncil e um valor de referência. O teste é habilitado com chamadas [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com teste de estêncil GL do argumento \_ \_ e controlado com [**glStencilFunc**](glstencilfunc.md).

A função **glStencilOp** usa três argumentos que indicam o que acontece com o valor de estêncil armazenado enquanto o estêncil está habilitado. Se o teste de estêncil falhar, nenhuma alteração será feita na cor ou nos buffers de profundidade do pixel e a *falha* especificará o que acontece com o conteúdo do buffer do estêncil.

Os valores de buffer de estêncil são tratados como inteiros não assinados. Quando incrementado e diminuído, os valores são clamped para 0 e 2 *n* 1, em que *n* é o valor retornado pela consulta de bits de \_ estêncil GL \_ .

Os outros dois argumentos para **glStencilOp** especificar ações de buffer de estêncil devem ter os testes de buffer de profundidade subsequentes com êxito (*ZPass*) ou Fail (*zfail*). (Consulte [**glDepthFunc**](gldepthfunc.md).) Eles são especificados usando as mesmas seis constantes simbólicas que *falham*. Observe que *zfail* é ignorado quando não há um buffer de profundidade ou quando o buffer de profundidade não está habilitado. Nesses casos, *falha* e *ZPass* especificam a ação de estêncil quando o teste de estêncil falha e passa, respectivamente.

Inicialmente, o teste de estêncil está desabilitado. Se não houver nenhum buffer de estêncil, nenhuma modificação de estêncil poderá ocorrer e será como se os testes de estêncil sempre passarem, independentemente de qualquer chamada para **glStencilOp**.

As funções a seguir recuperam informações relacionadas ao **glStencilOp**:

falha de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o estêncil Argument GL \_ \_

**glGet** com a \_ passagem de \_ profundidade de passagem do estêncil GL \_ do argumento \_

**glGet** com falha de \_ \_ profundidade de aprovação do estêncil do \_ argumento GL \_

**glGet** com bits de estêncil do Argument GL \_ \_

teste de estêncil [**glIsEnabled**](glisenabled.md) com Argument GL \_ \_

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

 

 





