---
title: função gluErrorString (Glu. h)
description: A função gluErrorString produz uma cadeia de caracteres de erro de um código de erro OpenGL ou GLU. A cadeia de caracteres de erro é somente ANSI.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- função gluErrorString OpenGL
topic_type:
- apiref
api_name:
- gluErrorString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cdcfad0e2a943bf3a475317f32d37921878a8f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644554"
---
# <a name="gluerrorstring-function"></a>função gluErrorString

A função **gluErrorString** produz uma cadeia de caracteres de erro de um código de erro OpenGL ou Glu. A cadeia de caracteres de erro é somente ANSI.

## <a name="syntax"></a>Sintaxe


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*errCode* 
</dt> <dd>

Um código de erro OpenGL ou GLU.

</dd> </dl>

## <a name="remarks"></a>Comentários

A função **gluErrorString** produz uma cadeia de caracteres de erro de um código de erro OpenGL ou Glu. A cadeia de caracteres está em um formato ISO Latin 1. Por exemplo, **gluErrorString**(GL \_ sem \_ \_ memória) retorna a cadeia de caracteres "memória insuficiente".

Os códigos de erro padrão do GLU são GLU \_ Enumeração inválida \_ , glu \_ \_ valor inválido e Glu \_ memória insuficiente \_ \_ . Algumas outras funções GLU podem retornar códigos de erro especializados por meio de retornos de chamada. Para obter a lista de códigos de erro OpenGL, consulte [**glGetError**](glgeterror.md).

A função **gluErrorString** produz cadeias de caracteres de erro somente em ANSI. Sempre que possível, use **gluErrorStringWIN**, que permite cadeias de caracteres de erro ANSI ou Unicode. Isso facilita a localização do seu programa para uso com outro idioma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>GLU. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[*gluQuadricCallback*](gluquadric.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> </dl>

 

 





