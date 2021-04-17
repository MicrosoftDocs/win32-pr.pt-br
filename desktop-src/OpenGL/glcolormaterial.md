---
title: função glColorMaterial (GL. h)
description: A função glColorMaterial faz com que uma cor de material acompanhe a cor atual.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- função glColorMaterial OpenGL
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
ms.openlocfilehash: d32823eaa82e6a260790dd6fa23747f2b4228649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369698"
---
# <a name="glcolormaterial-function"></a>função glColorMaterial

A função **glColorMaterial** faz com que uma cor de material acompanhe a cor atual.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sorridente* 
</dt> <dd>

Especifica se os parâmetros de material frontal, posterior ou dianteiro devem controlar a cor atual. Os valores aceitos são GL \_ front, GL \_ back e GL \_ front \_ e \_ back. O valor padrão é GL \_ front \_ e \_ back.

</dd> <dt>

*mode* 
</dt> <dd>

Especifica qual dos vários parâmetros de material acompanham a cor atual. Os valores aceitos são \_ emissão GL, ambiente GL, GL difuso, GL \_ \_ \_ especular e \_ ambiente GL \_ e \_ difuso. O valor padrão é GL \_ ambiente \_ e \_ difuso.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | a *face* ou o *modo* não era um valor aceito.<br/>                                                                                |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glColorMaterial** especifica quais parâmetros materiais acompanham a cor atual. Quando você habilita o \_ material de cor GL \_ , para cada material ou material especificado por *face*, o parâmetro de material ou os parâmetros especificados pelo *modo* controlam a cor atual em todos os momentos. Habilite e desabilite o \_ \_ material de cor GL com as funções [**glEnable**](glenable.md) e [**glDisable**](gldisable.md), que você chama com material de \_ cores GL \_ como argumento. Por padrão, o \_ material de cor GL \_ está desabilitado.

Com o **glColorMaterial**, você pode alterar um subconjunto de parâmetros de material para cada vértice usando apenas a função [**glColor**](glcolor-functions.md) , sem chamar [**glMaterial**](glmaterial-functions.md). Se você pretende especificar apenas um subconjunto de parâmetros para cada vértice, é melhor fazê-lo com **glColorMaterial** do que com **glMaterial**.

As funções a seguir recuperam informações relacionadas ao **glColorMaterial**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com parâmetro de \_ material de cor do Argument GL \_ \_

**glGet** com material de cor de argumento GL \_ \_ \_ face

[**glIsEnabled**](glisenabled.md) com material de cor do Argument GL \_ \_

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

 

 





