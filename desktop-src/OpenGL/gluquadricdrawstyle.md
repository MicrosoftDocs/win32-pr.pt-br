---
title: Função gluQuadricDrawStyle (Glu.h)
description: A função gluQuadricDrawStyle especifica o estilo de desenho desejado para os quadcs.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- Função gluQuadricDrawStyle OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a873ed4f4ceaff4aa3dad678dbb4c1fd7a635b0ce41d7a9480af84278c8360c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061554"
---
# <a name="gluquadricdrawstyle-function"></a>Função gluQuadricDrawStyle

A **função gluQuadricDrawStyle** especifica o estilo de desenho desejado para os quadcs.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*quadObject* 
</dt> <dd>

O objeto quadc (criado com [**gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*Drawstyle* 
</dt> <dd>

O estilo de desenho desejado. Os valores a seguir são válidos.



| Valor                                                                                                                                                            | Significado                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <dt>**PREENCHIMENTO \_ DE GLU**</dt> </dl>                   | Os quadrics são renderizados com primitivos de polígono. Os polígonos são desenhados de maneira anti-horário em relação aos seus normais (conforme definido com [**gluQuadricOrientation**](gluquadricorientation.md)).<br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <dt>**GLU \_ LINE**</dt> </dl>                   | Os quadrics são renderizados como um conjunto de linhas.<br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <dt>**GLU \_ SILHOUETTE**</dt> </dl> | Os quadrics são renderizados como um conjunto de linhas, exceto que as bordas que separam faces coplanares não serão desenhadas.<br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <dt>**GLU \_ POINT**</dt> </dl>                | Os quadrics são renderizados como um conjunto de pontos.<br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A **função gluQuadricDrawStyle** especifica o estilo de desenho para quadrics renderizados com **quadObject**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





