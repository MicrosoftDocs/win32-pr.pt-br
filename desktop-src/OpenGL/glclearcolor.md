---
title: Função glClearColor (Gl.h)
description: A função glClearColor especifica valores claros para os buffers de cores.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- Função glClearColor OpenGL
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
ms.openlocfilehash: 1bd68590ab9221dd094265a54f3c69ca396f810fb1f716c194b627a675196edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061904"
---
# <a name="glclearcolor-function"></a>Função glClearColor

A **função glClearColor** especifica valores claros para os buffers de cores.

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

*Vermelho* 
</dt> <dd>

O valor vermelho que [**glClear**](glclear.md) usa para limpar os buffers de cores. O valor padrão é zero.

</dd> <dt>

*Verde* 
</dt> <dd>

O valor verde que [**glClear**](glclear.md) usa para limpar os buffers de cores. O valor padrão é zero.

</dd> <dt>

*Azul* 
</dt> <dd>

O valor azul que [**glClear**](glclear.md) usa para limpar os buffers de cores. O valor padrão é zero.

</dd> <dt>

*alfa* 
</dt> <dd>

O valor alfa que [**glClear**](glclear.md) usa para limpar os buffers de cores. O valor padrão é zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glClearColor** especifica os valores vermelho, verde, azul e alfa usados por [**glClear**](glclear.md) para limpar os buffers de cores. Os valores especificados por **glClearColor** são fixados ao intervalo \[ 0,1 \] .

As seguintes funções recuperam informações relacionadas à **função glClearColor:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ ACCUM \_ CLEAR \_ VALUE

**glGet** com o argumento GL \_ COLOR \_ CLEAR \_ VALUE

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

[**glClear**](glclear.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





