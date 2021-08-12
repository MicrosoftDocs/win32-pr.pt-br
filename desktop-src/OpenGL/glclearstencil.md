---
title: função glClearStencil (GL. h)
description: A função glClearStencil especifica o valor de limpeza para o buffer de estêncil.
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
keywords:
- função glClearStencil OpenGL
topic_type:
- apiref
api_name:
- glClearStencil
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4749a8d9c4844bd95181a7353bb0ce4559001fa47164fec3dbab5c188de8d994
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618026"
---
# <a name="glclearstencil-function"></a>função glClearStencil

A função **glClearStencil** especifica o valor de limpeza para o buffer de estêncil.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glClearStencil(
   GLint s
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*s* 
</dt> <dd>

O índice usado quando o buffer do estêncil é limpo. O valor padrão é zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glClearStencil** especifica o índice usado pelo [**glClear**](glclear.md) para limpar o buffer de estêncil. O parâmetro *s* é mascarado com 2 <sup>m</sup>  -1, em que *m* é o número de bits no buffer do estêncil.

As funções a seguir recuperam informações relacionadas à função **glClearStencil** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ valor de \_ limpeza do estêncil GL do argumento \_

**glGet** com bits de estêncil do Argument GL \_ \_

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

[**glClear**](glclear.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





