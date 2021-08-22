---
title: Função glListBase (Gl.h)
description: A função glListBase define a base da lista de exibição para glCallLists.
ms.assetid: df82f699-b2af-471a-83f3-5620857ba45d
keywords:
- Função glListBase OpenGL
topic_type:
- apiref
api_name:
- glListBase
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ba7cbe7b179184efa739ac3492f4e74b36f56abe0f02498a0e1a688b85183a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938513"
---
# <a name="gllistbase-function"></a>Função glListBase

A **função glListBase** define a base da lista de exibição **para glCallLists.**

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glListBase(
   GLuint base
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*base* 
</dt> <dd>

Um deslocamento inteiro que será adicionado a [**deslocamentos glCallLists**](glcalllists.md) para gerar nomes de lista de exibição. O valor inicial é zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glListBase** especifica uma matriz de deslocamentos. Os nomes de lista de exibição são gerados *adicionando base* a cada deslocamento. Os nomes que referenciam listas de exibição válidas são executados; outros são ignorados.

A função a seguir recupera informações relacionadas a **glListBase:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ LIST \_ BASE

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

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





