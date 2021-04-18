---
title: função glMapGrid1f (GL. h)
description: Define uma malha unidimensional. | função glMapGrid1f (GL. h)
ms.assetid: 242c0197-2fa6-4356-b536-627660ebd3a7
keywords:
- função glMapGrid1f OpenGL
topic_type:
- apiref
api_name:
- glMapGrid1f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75479e8e25098fbfc5b906ba1785913cba9f2e30
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105779970"
---
# <a name="glmapgrid1f-function"></a>função glMapGrid1f

Define uma malha unidimensional.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glMapGrid1f(
   GLint   un,
   GLfloat u1,
   GLfloat u2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*anula* 
</dt> <dd>

O número de partições no intervalo de intervalo de grade \[ U1, U2 \] . Esse valor deve ser positivo.

</dd> <dt>

*U1* 
</dt> <dd>

Um valor usado como o mapeamento para o valor de domínio da grade de inteiros i = 0.

</dd> <dt>

*U2* 
</dt> <dd>

Um valor usado como o mapeamento para o valor de domínio da grade de inteiros i = un.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | O  *vn* não era positivo.<br/>                                                                                      |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

As funções **glMapGrid** e [glEvalMesh](glevalmesh-functions.md) são usadas em conjunto para gerar e avaliar com eficiência uma série de valores de domínio de mapa com espaçamento uniforme. A função glEvalMesh percorre o domínio inteiro de uma grade de uma ou duas dimensões, cujo intervalo é o domínio dos mapas de avaliação especificados por [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).

As funções [**glMapGrid1**](glmapgrid1d.md) e [**glMapGrid2**](glmapgrid2d.md) especificam os mapeamentos de grade linear entre as coordenadas de grade de inteiros i (ou i e j) para as coordenadas de mapa de avaliação de ponto flutuante u (ou você e v). Consulte [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md) para obter detalhes de como você e as coordenadas v são avaliados.

A função [**glMapGrid1**](glmapgrid1d.md) especifica um mapeamento linear único, de modo que *a coordenada* de grade de inteiros 0 é mapeada exatamente para U1, e a coordenada de grade de inteiros remapeia exatamente para *U2*. Todas as outras coordenadas de grade de *inteiros que são* mapeadas de modo que:

*u = i (U2 U1)/un + U1*

A função [**glMapGrid2**](glmapgrid2d.md) especifica dois mapeamentos lineares. Um mapeia a coordenada de grade de inteiros *i = 0* exatamente para *U1* e a coordenada de grade de inteiros *i =* não exatamente como *U2*. A outra coordenada de grade de inteiros de mapas *j = 0* exatamente para *v1* e a coordenada de grade de inteiros *j = vn* exatamente para *v2*. Outras coordenadas de grade de inteiros i e j são mapeadas de modo que

*u = i (U2 U1)/un + U1*

*v = j (v2 v1)/VN + v1*

Os mapeamentos especificados por [**glMapGrid**](glmapgrid1d.md) são usados de forma idêntica por [glEvalMesh](glevalmesh-functions.md) e [**glEvalPoint**](glevalpoint.md).

As funções a seguir recuperam informações relacionadas ao [**glMapGrid**](glmapgrid1d.md):

<dl>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MAP1 \_ grade \_ Domain  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ map2 \_ grade \_ Domain  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com os segmentos de grade Argument GL \_ MAP1 \_ \_  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com os segmentos de grade Argument GL \_ map2 \_ \_  
</dl>

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

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[glEvalMesh](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





