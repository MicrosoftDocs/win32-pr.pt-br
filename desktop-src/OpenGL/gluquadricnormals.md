---
title: função gluQuadricNormals (Glu. h)
description: A função gluQuadricNormals especifica que tipo de Normals deve ser usado para quadrics.
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- função gluQuadricNormals OpenGL
topic_type:
- apiref
api_name:
- gluQuadricNormals
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11f9d8cd1884d7a5d1bc4cd03797517ba484126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455580"
---
# <a name="gluquadricnormals-function"></a>função gluQuadricNormals

A função **gluQuadricNormals** especifica que tipo de Normals deve ser usado para quadrics.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*quádruplo* 
</dt> <dd>

O objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*Normals* 
</dt> <dd>

O tipo desejado de Normals. Os valores a seguir são válidos.



| Valor                                                                                                                                                | Significado                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <dt>**GLU \_ nenhum**</dt> </dl>       | Nenhum normal é gerado.<br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <dt>**GLU \_ simples**</dt> </dl>       | Um normal é gerado para cada faceta de um Quadric.<br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <dt>**\_Smooth Glu**</dt> </dl> | Um normal é gerado para cada vértice de um Quadric. Esse é o valor padrão.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluQuadricNormals** especifica que tipo de Normals deve ser usado para quadrics renderizado com o **quadobject**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>GLU. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





