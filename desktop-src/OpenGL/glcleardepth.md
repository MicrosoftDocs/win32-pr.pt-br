---
title: função glClearDepth (GL. h)
description: A função glClearDepth especifica o valor claro para o buffer de profundidade.
ms.assetid: 8e26ae78-edc1-4201-a0db-d5bc8ae6dc82
keywords:
- função glClearDepth OpenGL
topic_type:
- apiref
api_name:
- glClearDepth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cf968c7ae172bf4ce354c84b2071d62304327ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295804"
---
# <a name="glcleardepth-function"></a>função glClearDepth

A função **glClearDepth** especifica o valor claro para o buffer de profundidade.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glClearDepth(
   GLclampd depth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Detalhado* 
</dt> <dd>

O valor de profundidade usado quando o buffer de profundidade é limpo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glClearDepth** especifica o valor de profundidade usado pelo [**glClear**](glclear.md) para limpar o buffer de profundidade. Os valores especificados por **glClearDepth** são clamped para o intervalo de \[ 0, 1 \] .

A função a seguir recupera informações relacionadas à função **glClearDepth** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com \_ \_ valor claro de profundidade do argumento GL \_

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

 

 





