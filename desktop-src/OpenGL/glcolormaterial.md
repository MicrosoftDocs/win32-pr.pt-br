---
title: Função glColorMaterial (Gl.h)
description: A função glColorMaterial faz com que uma cor do material acompanhe a cor atual.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- Função glColorMaterial OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55cc846cfbc400d2372186f9af4a09db08e5ad769d1e8fec5f5f6f757e1ff447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360467"
---
# <a name="glcolormaterial-function"></a>Função glColorMaterial

A **função glColorMaterial** faz com que uma cor do material acompanhe a cor atual.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cara* 
</dt> <dd>

Especifica se os parâmetros de material front, back ou front e back devem acompanhar a cor atual. Os valores aceitos são GL \_ FRONT, GL \_ BACK e GL FRONT AND \_ \_ \_ BACK. O valor padrão é GL \_ FRONT \_ AND \_ BACK.

</dd> <dt>

*mode* 
</dt> <dd>

Especifica qual dos vários parâmetros de material acompanha a cor atual. Os valores aceitos são GL \_ EMISSION, GL \_ AMBIENT, GL \_ DIFUSO, GL \_ SPECULAR e GL \_ AMBIENT AND \_ \_ DIFFUSE. O valor padrão é GL \_ AMBIENT \_ AND \_ DIFFUSE.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *face* ou *mode* não era um valor aceito.<br/>                                                                                |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glColorMaterial** especifica quais parâmetros de material acompanham a cor atual. Quando você habilita GL COLOR MATERIAL, para cada um dos materiais ou materiais especificados pelo rosto , o parâmetro de material ou os parâmetros especificados pelo modo acompanham a cor \_ atual em todos os \_ momentos.   Habilita e desabilita GL COLOR MATERIAL com as funções \_ \_ [**glEnable**](glenable.md) e [**glDisable,**](gldisable.md)que você chama com GL \_ COLOR MATERIAL como seu \_ argumento. Por padrão, GL \_ COLOR \_ MATERIAL está desabilitado.

Com **glColorMaterial**, você pode alterar um subconjunto de parâmetros de material para cada vértice usando apenas a [**função glColor,**](glcolor-functions.md) sem chamar [**glMaterial**](glmaterial-functions.md). Se você for especificar apenas esse subconjunto de parâmetros para cada vértice, é melhor fazer isso com **glColorMaterial** do que com **glMaterial**.

As funções a seguir recuperam informações relacionadas **a glColorMaterial:**

[**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o argumento GL \_ COLOR MATERIAL \_ \_ PARAMETER

**glGet com** o argumento GL \_ COLOR MATERIAL \_ \_ FACE

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ COLOR \_ MATERIAL

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





