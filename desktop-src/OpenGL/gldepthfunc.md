---
title: função glDepthFunc (GL. h)
description: A função glDepthFunc especifica o valor usado para comparações de buffer de profundidade.
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- função glDepthFunc OpenGL
topic_type:
- apiref
api_name:
- glDepthFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dec5130edb0b8ef30af1397be501fa9cd5d5744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454855"
---
# <a name="gldepthfunc-function"></a>função glDepthFunc

A função **glDepthFunc** especifica o valor usado para comparações de buffer de profundidade.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glDepthFunc(
   GLenum func
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*func* 
</dt> <dd>

Especifica a função de comparação de profundidade. As constantes simbólicas a seguir são aceitas.



| Valor                                                                                                                                                   | Significado                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ nunca**</dt> </dl>          | Nunca passa.<br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ menos**</dt> </dl>             | Passa se o valor *z* de entrada for menor que o valor *z* armazenado. Esse é o valor padrão.<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**\_LEQUAL GL**</dt> </dl>       | Passa se o valor z de entrada for menor ou igual ao valor z armazenado.<br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ igual a**</dt> </dl>          | Passa se o valor z de entrada for igual ao valor z armazenado.<br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ maior**</dt> </dl>    | Passa se o valor z de entrada for maior que o valor z armazenado.<br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL não \_ igual**</dt> </dl> | Passa se o valor z de entrada não for igual ao valor z armazenado.<br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**\_GEQUAL GL**</dt> </dl>       | Passa se o valor z de entrada for maior ou igual ao valor z armazenado.<br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ sempre**</dt> </dl>       | Sempre passa.<br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glDepthFunc** especifica a função usada para comparar cada valor de pixel *z* de entrada com o valor *z* presente no buffer de profundidade. A comparação será executada somente se o teste de profundidade estiver habilitado. (Consulte [**glEnable**](glenable.md) com o argumento GL \_ teste de profundidade \_ .)

Inicialmente, o teste de profundidade está desabilitado.

As funções a seguir recuperam informações relacionadas ao **glDepthFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ Depth \_ Func

[**glIsEnabled**](glisenabled.md) com teste de profundidade do argumento GL \_ \_

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

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





