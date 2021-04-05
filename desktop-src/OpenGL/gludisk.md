---
title: função gluDisk (Glu. h)
description: A função gluDisk desenha um disco.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- função gluDisk OpenGL
topic_type:
- apiref
api_name:
- gluDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9a9e8b547790049c93360f060e944aafcea4511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009336"
---
# <a name="gludisk-function"></a>função gluDisk

A função **gluDisk** desenha um disco.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*qobj* 
</dt> <dd>

O objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*innerRadius* 
</dt> <dd>

O raio interno do disco (pode ser zero).

</dd> <dt>

*outerRadius* 
</dt> <dd>

O raio externo do disco.

</dd> <dt>

*fatia* 
</dt> <dd>

O número de subdivisãos em volta do eixo z.

</dd> <dt>

*loops* 
</dt> <dd>

O número de anéis concêntricos sobre a origem na qual o disco é subdividido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluDisk** renderiza um disco no plano *z* = 0. O disco tem um raio de *outerRadius* e contém um buraco circular concêntrico com um raio de *innerRadius*. Se *innerRadius* for 0, nenhum orifício será gerado. O disco é subdividido em torno do eixo z em fatias (como fatias de pizza) e também sobre o eixo z em anéis (conforme especificado por *fatias* e *loops*, respectivamente).

Em relação à orientação, o lado *z* positivo do disco é considerado *fora* (consulte [**gluQuadricOrientation**](gluquadricorientation.md)). Isso significa que, se a orientação for definida como GLU \_ externamente, qualquer normal gerado apontará ao longo do eixo z positivo.

Se texturing estiver ativado (com [**gluQuadricTexture**](gluquadrictexture.md)), as coordenadas de textura serão geradas linearmente, de onde *r*  =  *outerRadius*, o valor em (*r*, 0, 0) é (1, 0,5); at (0, *r*, 0) é (0,5, 1); at (-*r*, 0, 0) é (0, 0,5); e at (0,-*r*, 0) é (0,5, 0).

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

[**gluCylinder**](glucylinder.md)
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

 

 





