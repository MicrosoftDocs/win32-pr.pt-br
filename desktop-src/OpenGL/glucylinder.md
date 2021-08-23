---
title: Função gluCylinder (Glu.h)
description: A função gluCylinder desenha um cilindro.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- Função gluCylinder OpenGL
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
ms.openlocfilehash: 1a09ff92aec17a13f03ecb1cbaaf118398b2b88dea76936454d527bb9c37032f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061604"
---
# <a name="glucylinder-function"></a>Função gluCylinder

A **função gluCylinder** desenha um cilindro.

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

O objeto quadc (criado com [**gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*baseRadius* 
</dt> <dd>

O raio do cilindro em *z* = 0.

</dd> <dt>

*topRadius* 
</dt> <dd>

O raio do cilindro na *altura z.*  =  

</dd> <dt>

*altura* 
</dt> <dd>

A altura do cilindro.

</dd> <dt>

*Fatias* 
</dt> <dd>

O número de subdivisões ao redor do eixo z.

</dd> <dt>

*Pilhas* 
</dt> <dd>

O número de subdivisões ao longo do eixo z.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A **função gluCylinder** desenha um cilindro orientado ao longo do eixo z. A base do cilindro é colocada *em z* = 0 e a parte superior na *altura z*  =  . Como uma esfera, um cilindro é subdividido em torno do eixo z em fatias e ao longo do eixo z em pilhas.

Observe que, *se topRadius* estiver definido como zero, essa rotina gerará um cone.

Se a orientação for definida como GLU \_ OUTSIDE [**(com gluQuadricOrientation),**](gluquadricorientation.md)quaisquer normais gerados apontarão para fora do eixo z. Caso contrário, eles apontam para o eixo z.

Se a texturização estiver ligado [**(com gluQuadricTexture):**](gluquadrictexture.md)as coordenadas de textura serão geradas de modo que *t* seja linear de 0,0 em *z* = 0 a 1,0 na *altura z*; e s intervalos de  =  0,0 no eixo y positivo, para 0,25 no eixo x positivo, para 0,5 no eixo y negativo, para 0,75 no eixo x negativo e de volta para 1,0 no eixo y positivo. 

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

 

 





