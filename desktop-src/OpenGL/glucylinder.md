---
title: função gluCylinder (Glu. h)
description: A função gluCylinder desenha um cilindro.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- função gluCylinder OpenGL
topic_type:
- apiref
api_name:
- gluCylinder
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fd201d1ddd720501715d1ead08d94bab72f7b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755976"
---
# <a name="glucylinder-function"></a>função gluCylinder

A função **gluCylinder** desenha um cilindro.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluCylinder(
   GLUquadric *qobj,
   GLdouble   baseRadius,
   GLdouble   topRadius,
   GLdouble   height,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*qobj* 
</dt> <dd>

O objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*baseRadius* 
</dt> <dd>

O raio do cilindro em *z* = 0.

</dd> <dt>

*topRadius* 
</dt> <dd>

O raio do cilindro em altura *z*  =  .

</dd> <dt>

*altura* 
</dt> <dd>

A altura do cilindro.

</dd> <dt>

*fatia* 
</dt> <dd>

O número de subdivisãos em volta do eixo z.

</dd> <dt>

*pilhas* 
</dt> <dd>

O número de subdivisãos ao longo do eixo z.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluCylinder** desenha um cilindro orientado ao longo do eixo z. A base do cilindro é colocada em *z* = 0, e a altura da parte superior em *z*  =  . Como uma esfera, um cilindro é subdividido em torno do eixo z em fatias e, ao longo do eixo z, em pilhas.

Observe que, se *topRadius* for definido como zero, essa rotina irá gerar um cone.

Se a orientação for definida como GLU \_ externamente (com [**gluQuadricOrientation**](gluquadricorientation.md)), então todos os Normals gerados apontarão do eixo z. Caso contrário, eles apontam para o eixo z.

Se texturing estiver ativado (com [**gluQuadricTexture**](gluquadrictexture.md)): coordenadas de textura são geradas para que *t* se torne linearmente de 0,0 a *z* = 0 a 1,0 a *z*  =  *Height*; e *s* varia de 0,0 no eixo y positivo, até 0,25 no eixo x positivo, para 0,5 no eixo y negativo, para 0,75 no eixo x negativo e de volta para 1,0 no eixo y positivo.

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

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





