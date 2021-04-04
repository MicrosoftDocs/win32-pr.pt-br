---
title: função glClearAccum (GL. h)
description: A função glClearAccum especifica os valores claros para o buffer de acumulação.
ms.assetid: 77d8f340-be47-43f4-96fc-31025a4c8b4e
keywords:
- função glClearAccum OpenGL
topic_type:
- apiref
api_name:
- glClearAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3098e87a47509b8c05035171a8f31e57d8618424
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085705"
---
# <a name="glclearaccum-function"></a>função glClearAccum

A função **glClearAccum** especifica os valores claros para o buffer de acumulação.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glClearAccum(
   GLfloat red,
   GLfloat green,
   GLfloat blue,
   GLfloat alpha
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vermelho* 
</dt> <dd>

O valor vermelho usado quando o buffer de acumulação é limpo. O valor padrão é zero.

</dd> <dt>

*amarela* 
</dt> <dd>

O valor verde usado quando o buffer de acumulação é limpo. O valor padrão é zero.

</dd> <dt>

*azul* 
</dt> <dd>

O valor azul usado quando o buffer de acumulação é limpo. O valor padrão é zero.

</dd> <dt>

*Alfa* 
</dt> <dd>

O valor alfa usado quando o buffer de acumulação é limpo. O valor padrão é zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glClearAccum** especifica os valores vermelho, verde, azul e alfa usados pelo [**glClear**](glclear.md) para limpar o buffer de acumulação.

Os valores especificados por **glClearAccum** são clamped para o intervalo \[ 1, 1 \] .

A função a seguir recupera informações relacionadas a **glClearAccum**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com argumento GL \_ Accum \_ valor de limpeza \_

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

 

 





