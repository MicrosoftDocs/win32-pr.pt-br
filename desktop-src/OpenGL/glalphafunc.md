---
title: função glAlphaFunc (GL. h)
description: A função glAlphaFunc permite que seu aplicativo defina a função de teste alfa.
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
keywords:
- função glAlphaFunc OpenGL
topic_type:
- apiref
api_name:
- glAlphaFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf96cfe2be0224c9c2e2409fc68805b530ae1f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784169"
---
# <a name="glalphafunc-function"></a>função glAlphaFunc

A função **glAlphaFunc** permite que seu aplicativo defina a função de teste alfa.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glAlphaFunc(
   GLenum   func,
   GLclampf ref
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*func* 
</dt> <dd>

A função de comparação alfa. A seguir estão as constantes simbólicas aceitas e seus significados.



| Valor                                                                                                                                                   | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ nunca**</dt> </dl>          | Nunca passa.<br/>                                                                       |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ menos**</dt> </dl>             | Passa se o valor alfa de entrada for menor que o valor de referência.<br/>                |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ igual a**</dt> </dl>          | Passa se o valor alfa de entrada for igual ao valor de referência.<br/>                 |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**\_LEQUAL GL**</dt> </dl>       | Passa se o valor alfa de entrada for menor ou igual ao valor de referência.<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ maior**</dt> </dl>    | Passa se o valor alfa de entrada for maior que o valor de referência.<br/>             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL não \_ igual**</dt> </dl> | Passa se o valor alfa de entrada não for igual ao valor de referência.<br/>             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**\_GEQUAL GL**</dt> </dl>       | Passa se o valor alfa de entrada for maior ou igual ao valor de referência.<br/> |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ sempre**</dt> </dl>       | Sempre passa. Esse é o padrão.<br/>                                                 |



 

</dd> <dt>

*ref* 
</dt> <dd>

O valor de referência para o qual os valores Alfa de entrada são comparados. Esse valor é clamped para o intervalo de 0 a 1, em que 0 representa o menor valor alfa possível e 1 o maior valor possível. A referência padrão é 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *Func* não era um valor aceito.<br/>                                                                                          |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

O teste alfa descarta fragmentos dependendo do resultado de uma comparação entre os valores Alfa dos fragmentos de entrada e um valor de referência constante. A função **glAlphaFunc** especifica a função de referência e comparação. A comparação será executada somente se o teste alfa estiver habilitado. (Para obter mais informações sobre o GL \_ \_Teste alfa, consulte [**glEnable**](glenable.md).)

Os parâmetros *Func* e *ref* especificam as condições sob as quais o pixel é desenhado. O valor alfa de entrada é comparado com *ref* usando a função especificada por *Func*. Se a comparação passar, o fragmento de entrada será desenhado, condicional nos testes subseqüentes de estêncil e buffer de profundidade. Se a comparação falhar, nenhuma alteração será feita no framebuffer naquele local de pixel.

A função **glAlphaFunc** opera em todas as gravações de pixel, incluindo aquelas resultantes da conversão de verificação de pontos, linhas, polígonos e bitmaps e de operações de desenho e de cópia de pixel. A função **glAlphaFunc** não afeta as operações de limpeza de tela.

O teste alfa é feito somente no modo RGBA.

As funções a seguir recuperam informações relacionadas à função **glAlphaFunc** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ alfa \_ test \_ Func

**glGet** com Argument GL \_ Alpha \_ test \_ ref

teste de [**glIsEnabled**](glisenabled.md) com Argument GL \_ Alpha \_

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

[**glClear**](glclear.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





