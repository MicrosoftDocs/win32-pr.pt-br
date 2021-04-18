---
title: função gluPartialDisk (Glu. h)
description: A função gluPartialDisk desenha um arco de um disco.
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- função gluPartialDisk OpenGL
topic_type:
- apiref
api_name:
- gluPartialDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e35a6ea905f20e1cb30eddc5b270786614403b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754137"
---
# <a name="glupartialdisk-function"></a>função gluPartialDisk

A função **gluPartialDisk** desenha um arco de um disco.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluPartialDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops,
   GLdouble   startAngle,
   GLdouble   sweepAngle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*qobj* 
</dt> <dd>

Um objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*innerRadius* 
</dt> <dd>

O raio interno do disco parcial (pode ser zero).

</dd> <dt>

*outerRadius* 
</dt> <dd>

O raio externo do disco parcial.

</dd> <dt>

*fatia* 
</dt> <dd>

O número de subdivisãos em volta do eixo z.

</dd> <dt>

*loops* 
</dt> <dd>

O número de anéis concêntricos sobre a origem na qual o disco parcial é subdividido.

</dd> <dt>

*startAngle* 
</dt> <dd>

O ângulo inicial, em graus, da parte do disco.

</dd> <dt>

*sweepAngle* 
</dt> <dd>

O ângulo de flecha, em graus, da parte do disco.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluPartialDisk** renderiza um disco parcial no plano *z* = 0. Um disco parcial é semelhante a um disco cheio, exceto pelo fato de que apenas o subconjunto do disco de *StartAngle* até *StartAngle*  +  *SweepAngle* está incluído (onde 0 graus está ao longo do eixo y positivo, 90 graus é ao longo do eixo x positivo, 180 graus é ao longo do eixo y negativo e 270 graus está ao longo do eixo x negativo).

O disco parcial tem um raio de *outerRadius* e contém um buraco circular concêntrico com um raio de *innerRadius*. Se *innerRadius* for zero, nenhum buraco será gerado. O disco parcial é subdividido em torno do eixo z em fatias (como fatias de pizza) e também sobre o eixo z em anéis (conforme especificado por *fatias* e *loops*, respectivamente).

Em relação à orientação, o lado z positivo do disco parcial é considerado fora (consulte [**gluQuadricOrientation**](gluquadricorientation.md)). Isso significa que, se a orientação for definida como GLU \_ externamente, qualquer normal gerado apontará ao longo do eixo z positivo.

Se você tiver ativado texturing (com [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** gerará coordenadas de textura linearmente, de modo que, em que em *r*  =  *outerRadius*, o valor em (*r*, 0, 0) é (1, 0,5); at (0, *r*, 0) é (0,5, 1); at (*r*, 0, 0) é (0, 0,5); e at (0, *r*, 0) é (0,5, 0).

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

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





