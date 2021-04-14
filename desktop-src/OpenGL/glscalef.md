---
title: função glScalef (GL. h)
description: As funções glScaled e glScalef multiplicam a matriz atual por uma matriz de dimensionamento geral. | função glScalef (GL. h)
ms.assetid: bf039bbc-7669-4282-b629-71440b798cb1
keywords:
- função glScalef OpenGL
topic_type:
- apiref
api_name:
- glScalef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eda183b763f22736370dd5c9ea13ca8793243e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104564516"
---
# <a name="glscalef-function"></a>função glScalef

As funções [**glScaled**](glscaled.md) e **glScalef** multiplicam a matriz atual por uma matriz de dimensionamento geral.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glScalef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*x* 
</dt> <dd>

Fatores de escala ao longo do eixo *x* .

</dd> <dt>

*y* 
</dt> <dd>

Fatores de escala ao longo do eixo *y* .

</dd> <dt>

*z* 
</dt> <dd>

Fatores de escala ao longo do eixo *z* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glScalef** produz um dimensionamento geral ao longo dos eixos *x*, *y* e *z* . Os três argumentos indicam os fatores de escala desejados ao longo de cada um dos três eixos. A matriz resultante aparece na imagem a seguir.

![Diagrama mostrando a matriz de fatores de escala ao longo dos eixos x, y e z.](images/scale01.png)

A matriz atual (consulte [**glMatrixMode**](glmatrixmode.md)) é multiplicada por essa matriz de escala, com o produto que substitui a matriz atual. Ou seja, se M for a matriz atual e S for a matriz de escala, M será substituído por M S.

Se o modo de matriz for uma \_ projeção GL MODELVIEW ou GL \_ , todos os objetos desenhados após o **glScalef** são chamados são dimensionados. Use [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) para salvar e restaurar o sistema de coordenadas não dimensionada.

Se fatores de escala diferentes de 1,0 forem aplicados à matriz modelview e a iluminação estiver habilitada, a normalização automática de Normals provavelmente também deverá ser habilitada ([**glEnable**](glenable.md) e [**GLDISABLE**](gldisable.md) com Argument GL \_ NORMALIZE).

As funções a seguir recuperam informações relacionadas ao **glScalef**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MODELVIEW \_ Matrix

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ matriz de projeção GLGET com Argument GL \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com matriz de \_ textura Argument GL \_

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

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotated**](glrotated.md)
</dt> <dt>

[**glRotatef**](glrotatef.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





