---
title: função glListBase (GL. h)
description: A função glListBase define a base da lista de exibição para glCallLists.
ms.assetid: df82f699-b2af-471a-83f3-5620857ba45d
keywords:
- função glListBase OpenGL
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
ms.openlocfilehash: c46af03477afc1b656df3a321fd8aa652b034b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918098"
---
# <a name="gllistbase-function"></a>função glListBase

A função **glListBase** define a base da lista de exibição para **glCallLists**.

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

Um deslocamento de inteiro que será adicionado a deslocamentos [**glCallLists**](glcalllists.md) para gerar nomes de lista de exibição. O valor inicial é zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glListBase** especifica uma matriz de deslocamentos. Nomes de lista de exibição são gerados adicionando *base* a cada deslocamento. Os nomes que fazem referência a listas de exibição válidas são executados; outras são ignoradas.

A função a seguir recupera informações relacionadas a **glListBase**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com base de lista de argumentos GL \_ \_

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

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





