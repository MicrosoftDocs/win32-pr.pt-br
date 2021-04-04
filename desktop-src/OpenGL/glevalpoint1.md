---
title: função glEvalPoint1 (GL. h)
description: As funções glEvalPoint1 e glEvalPoint2 geram e avaliam um único ponto em uma malha. | função glEvalPoint1 (GL. h)
ms.assetid: 5ef1d2f0-d77b-4bb8-a0d4-45c1a6a91c18
keywords:
- função glEvalPoint1 OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b9c3b8e17f5a0554c1864a401ecf49343806c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837882"
---
# <a name="glevalpoint1-function"></a>função glEvalPoint1

As funções [**glEvalPoint1**](glevalpoint.md) e **glEvalPoint2** geram e avaliam um único ponto em uma malha.

## <a name="syntax"></a>Sintaxe


```C++
void glEvalPoint1(
   GLint i
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*i* 
</dt> <dd>

O valor inteiro para a variável de domínio de grade *i*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

As funções [**glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) são usadas em conjunto para gerar e avaliar com eficiência uma série de valores de domínio de mapa com espaçamento uniforme. Você pode usar **glEvalPoint** para avaliar um único ponto de grade no mesmo gridspace que é percorrido pelo **glEvalMesh**. Chamar [**glEvalPoint1**](glevalpoint.md) é equivalente a chamar

**glEvalCoord1** (*i* ?*u*  + *u* 1);

onde

? *u* = (*u* 2 *u* 1)/*n*

e *n*, *u* 1 e *u* 2 são os argumentos para a função **glMapGrid1** mais recente. O requisito numérico absoluto é que, se *eu*  =  *n*, o valor calculado de (*i* ?*u* + U1) é exatamente *u* 2.

No caso bidimensional, **glEvalPoint2**, Let

? *u* = (*u* 2 *u* 1)/*n*

? *v* = (*v* 2 *v* 1)/*m*

onde *n*, *u* 1, *u* 2, *m*, *v* 1 e *v* 2 são os argumentos para a função **glMapGrid2** mais recente. Em seguida, a função **glEvalPoint2** é equivalente a chamar

**glEvalCoord2** (*i* ?*u*  +  *u* 1, *j* ?*v*  +  *v* 1);

Os únicos requisitos numéricos absolutos são que, se *eu* = *n*, o valor calculado de (*i* ?*u*  +  *u* 1) é exatamente U2 e, se *j*  =  *m*, o valor calculado de (*j* ?*v*  +  *v* 1) é exatamente *v* 2.

As funções a seguir recuperam informações relacionadas a [**glEvalPoint1**](glevalpoint.md) e **glEvalPoint2**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MAP1 \_ grade \_ Domain

**glGet** com o argumento GL \_ map2 \_ grade \_ Domain

**glGet** com os segmentos de grade Argument GL \_ MAP1 \_ \_

**glGet** com os segmentos de grade Argument GL \_ map2 \_ \_

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

 

 





