---
title: função gluSphere (Glu. h)
description: A função gluSphere desenha uma esfera.
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- função gluSphere OpenGL
topic_type:
- apiref
api_name:
- gluSphere
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590c4b7335fe0596c5b5b0f3dc709998fafc21f7be78f493a05f6520ed9fd368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488726"
---
# <a name="glusphere-function"></a>função gluSphere

A função **gluSphere** desenha uma esfera.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluSphere(
   GLUquadric *qobj,
   GLdouble   radius,
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

*radiano* 
</dt> <dd>

O raio da esfera.

</dd> <dt>

*fatia* 
</dt> <dd>

O número de subdivisãos em volta do eixo z (semelhante às linhas de longitude).

</dd> <dt>

*pilhas* 
</dt> <dd>

O número de subdivisãos ao longo do eixo z (semelhante às linhas de latitude).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluSphere** desenha uma esfera do raio determinado centralizado em relação à origem. A esfera é subdividida em torno do eixo z em fatias e ao longo do eixo z em pilhas (semelhante às linhas de longitude e latitude).

Se a orientação for definida como GLU \_ fora (com **gluQuadricOrientation**), qualquer normal gerado apontará para fora do centro da esfera. Caso contrário, eles apontam para o centro da esfera.

Se texturing estiver ativado (com **gluQuadricTexture**): coordenadas de textura são geradas para *que t* varie de 0,0 a *z* =-*RADIUS* para 1,0 a *z*  =  *RADIUS* (*t* aumenta linearmente ao longo das linhas longitudinal); e *s* varia de 0,0 no eixo y positivo, até 0,25, no eixo x positivo, para 0,5 no eixo y negativo, para 0,75 no eixo x negativo, e de volta para 1,0 no eixo y positivo do.

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

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





