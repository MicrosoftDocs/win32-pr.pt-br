---
title: Função glEvalPoint2 (Gl.h)
description: As funções glEvalPoint1 e glEvalPoint2 geram e avaliam um único ponto em uma malha. | Função glEvalPoint2 (Gl.h)
ms.assetid: babae9c7-84a8-4a7e-b6f9-97c4e8bd42fe
keywords:
- Função glEvalPoint2 OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f0c188ec5f3e8171b8035e58b235bc0c5942e221d6d85a6dd4e5a8ff1786c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675556"
---
# <a name="glevalpoint2-function"></a>Função glEvalPoint2

As [**funções glEvalPoint1**](glevalpoint.md) **e glEvalPoint2** geram e avaliam um único ponto em uma malha.

## <a name="syntax"></a>Sintaxe


```C++
void glEvalPoint2(
   GLint i,
   GLint j
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*i* 
</dt> <dd>

O valor inteiro da variável de domínio de grade *i*.

</dd> <dt>

*J* 
</dt> <dd>

O valor inteiro da variável de domínio de *grade j.*

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

As [**funções glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) são usadas em tandem para gerar e avaliar com eficiência uma série de valores de domínio de mapa com espalismo de maneira eficiente. Você pode usar **glEvalPoint para** avaliar um único ponto de grade no mesmo espaço de grade que é percorrido por **glEvalMesh.** Chamar [**glEvalPoint1**](glevalpoint.md) é equivalente a chamar

**glEvalCoord1** (*i* ?*u*  + *u* 1 );

onde

? *u* = (*u* 2 *u* 1 )/*n*

e *n*, *u* 1 e *u* 2 são os argumentos para a função **glMapGrid1 mais** recente. O único requisito numérico absoluto é que, se *i*  =  *n*, o valor calculado de (*i* ?*u* + u1 ) é exatamente *u* 2 .

No caso bidimensional, **glEvalPoint2**, vamos

? *u* = (*u* 2 *u* 1 )/*n*

? *v* = (*v* 2 *v* 1 )/*m*

em *que n*, *u* 1 , *u* 2 , *m*, *v* 1 e *v* 2 são os argumentos para a função **glMapGrid2 mais** recente. Em **seguida, a função glEvalPoint2** é equivalente a chamar

**glEvalCoord2** (*i* ?*u*  +  *u* 1 , *j* ?*v*  +  *v* 1 );

Os únicos requisitos numéricos absolutos são que, se *i* = *n*, o valor calculado de (*i* ?*u*  +  *u* 1 ) é exatamente u2 e, se *j*  =  *m*, o valor computado de (*j* ?*v*  +  *v* 1 ) é exatamente *v* 2.

As funções a seguir recuperam informações relacionadas [**a glEvalPoint1**](glevalpoint.md) e **glEvalPoint2:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MAP1 \_ GRID \_ DOMAIN

**glGet** com o argumento GL \_ MAP2 \_ GRID \_ DOMAIN

**glGet** com o argumento GL \_ MAP1 \_ GRID \_ SEGMENTS

**glGet** com o argumento GL \_ MAP2 \_ GRID \_ SEGMENTS

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> </dl>

 

 





