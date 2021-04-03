---
title: função glClearColor (GL. h)
description: A função glClearColor especifica valores claros para os buffers de cor.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- função glClearColor OpenGL
topic_type:
- apiref
api_name:
- glClearColor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34005ce34900f5fee8a4c9b2f1b963b7fe4bb6d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644759"
---
# <a name="glclearcolor-function"></a>função glClearColor

A função **glClearColor** especifica valores claros para os buffers de cor.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glClearColor(
   GLclampf red,
   GLclampf green,
   GLclampf blue,
   GLclampf alpha
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vermelho* 
</dt> <dd>

O valor vermelho que o [**glClear**](glclear.md) usa para limpar os buffers de cor. O valor padrão é zero.

</dd> <dt>

*amarela* 
</dt> <dd>

O valor verde que o [**glClear**](glclear.md) usa para limpar os buffers de cor. O valor padrão é zero.

</dd> <dt>

*azul* 
</dt> <dd>

O valor azul que o [**glClear**](glclear.md) usa para limpar os buffers de cor. O valor padrão é zero.

</dd> <dt>

*Alfa* 
</dt> <dd>

O valor alfa que o [**glClear**](glclear.md) usa para limpar os buffers de cor. O valor padrão é zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glClearColor** especifica os valores vermelho, verde, azul e alfa usados pelo [**glClear**](glclear.md) para limpar os buffers de cor. Os valores especificados por **glClearColor** são clamped para o intervalo de \[ 0, 1 \] .

As funções a seguir recuperam informações relacionadas à função **glClearColor** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com argumento GL \_ Accum \_ valor de limpeza \_

**glGet** com o \_ valor de \_ limpeza de cor do argumento GL \_

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

 

 





