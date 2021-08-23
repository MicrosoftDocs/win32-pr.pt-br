---
title: Função gluDisk (Glu.h)
description: A função gluDisk desenha um disco.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- Função gluDisk OpenGL
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
ms.openlocfilehash: 83abb24f665cbcbf978a6423868751794371606cf412f609876a8f17d42c115a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489526"
---
# <a name="gludisk-function"></a>Função gluDisk

A **função gluDisk** desenha um disco.

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

O objeto quadc (criado com [**gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*innerRadius* 
</dt> <dd>

O raio interno do disco (pode ser zero).

</dd> <dt>

*outerRadius* 
</dt> <dd>

O raio externo do disco.

</dd> <dt>

*Fatias* 
</dt> <dd>

O número de subdivisões ao redor do eixo z.

</dd> <dt>

*Loops* 
</dt> <dd>

O número de anéis concêntricos sobre a origem na qual o disco é subdividido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A **função gluDisk** renderiza um disco no *plano z* = 0. O disco tem um raio *de outerRadius* e contém um orifício circular concêntrico com um raio *de innerRadius*. Se *innerRadius* for 0, nenhum orifício será gerado. O disco é subdividido em torno do eixo z em fatias (como fatias de pizza) e também sobre o eixo z em anéis (conforme especificado por *fatias* e *loops,* respectivamente).

Em relação à orientação, o *lado positivo z* do disco é considerado externo (consulte [**gluQuadricOrientation**](gluquadricorientation.md)).  Isso significa que, se a orientação estiver definida como GLU OUTSIDE, qualquer \_ ponto gerado normal ao longo do eixo z positivo.

Se a texturização estiver ativas [**(com gluQuadricTexture),**](gluquadrictexture.md)as coordenadas de textura serão geradas linearmente, de modo que, em que *r* outerRadius , o valor em  =  (*r*, 0, 0) é (1, 0,5); em (0, *r*, 0) é (0,5, 1); em (-*r*, 0, 0) é (0, 0,5); e em (0, -*r*, 0) é (0,5, 0).

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

 

 





