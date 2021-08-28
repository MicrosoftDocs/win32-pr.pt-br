---
title: função glLoadIdentity (GL. h)
description: A função glLoadIdentity substitui a matriz atual pela matriz de identidade.
ms.assetid: 59273aa9-4db3-4c8c-8364-f54c03d2f97a
keywords:
- função glLoadIdentity OpenGL
topic_type:
- apiref
api_name:
- glLoadIdentity
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38c0917dae2ae21acd61b6931bcb683a4f3f85f88af45c20fe6137e464254f8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492996"
---
# <a name="glloadidentity-function"></a>função glLoadIdentity

A função **glLoadIdentity** substitui a matriz atual pela matriz de identidade.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glLoadIdentity(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glLoadIdentity** substitui a matriz atual pela matriz de identidade. É semanticamente equivalente a chamar [**glLoadMatrix**](glloadmatrix.md) com a seguinte matriz de identidade.

![Diagrama que mostra a matriz de identidade que o glLoadIdentity chama.](images/load01.png)

No entanto, em alguns casos, é mais eficiente.

As funções a seguir recuperam informações relacionadas ao **glLoadIdentity**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_

**glGet** com o argumento GL \_ MODELVIEW \_ Matrix

 \_ matriz de projeção GLGET com Argument GL \_

**glGet** com matriz de \_ textura Argument GL \_

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

[**glEnd**](glend.md)
</dt> <dt>

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





