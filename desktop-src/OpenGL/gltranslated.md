---
title: função glTranslated (GL. h)
description: A função glTranslated multiplica a matriz atual por uma matriz de conversão.
ms.assetid: 9f066a92-ee78-44d1-b8f8-0eacde0e1a47
keywords:
- função glTranslated OpenGL
topic_type:
- apiref
api_name:
- glTranslated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705c8dd0635294b066897db99c0770b5f6622c75
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105796389"
---
# <a name="gltranslated-function"></a>função glTranslated

A função **glTranslated** multiplica a matriz atual por uma matriz de conversão.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTranslated(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*x* 
</dt> <dd>

A coordenada *x* de um vetor de tradução.

</dd> <dt>

*y* 
</dt> <dd>

A coordenada *y* de um vetor de tradução.

</dd> <dt>

*z* 
</dt> <dd>

A coordenada *z* de um vetor de tradução.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **glTranslated** produz a tradução especificada por (*x*, *y*, *z*). O vetor de conversão é usado para calcular uma matriz de conversão 4x4:

![Diagrama mostrando a matriz de tradução 4x4 especificada por x, y, z.](images/trans01.png)

A matriz atual (consulte [**glMatrixMode**](glmatrixmode.md)) é multiplicada por essa matriz de tradução, com o produto que substitui a matriz atual. Ou seja, se M for a matriz atual e T for a matriz de conversão, M será substituído por M T.

Se o modo de matriz for uma \_ projeção GL MODELVIEW ou GL \_ , todos os objetos desenhados depois de **glTranslated** serão convertidos. Use [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** para salvar e restaurar o sistema de coordenadas não traduzido.

As funções a seguir recuperam informações relacionadas ao [**glTranslated**](gltranslate.md):

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_

**glGet** com o argumento GL \_ MODELVIEW \_ Matrix

 \_ matriz de projeção GLGET com Argument GL \_

**glGet** com matriz de \_ textura Argument GL \_

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

[**glEnd**](glend.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> </dl>

 

 





