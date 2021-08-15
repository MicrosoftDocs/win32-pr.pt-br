---
title: Função glScaled (Gl.h)
description: As funções glScaled e glScalef multiplicam a matriz atual por uma matriz de dimensionamento geral. | Função glScaled (Gl.h)
ms.assetid: 3846289f-5c7b-4bb6-95a8-90a58dd8b9d9
keywords:
- Função glScaled OpenGL
topic_type:
- apiref
api_name:
- glScaled
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46742831eaa0a014de0f6ae50271b28c922893133588758119cbf5bff7ba628b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491786"
---
# <a name="glscaled-function"></a>Função glScaled

As **funções glScaled** e [**glScalef**](glscalef.md) multiplicam a matriz atual por uma matriz de dimensionamento geral.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glScaled(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*x* 
</dt> <dd>

Fatores de escala ao longo do *eixo x.*

</dd> <dt>

*y* 
</dt> <dd>

Fatores de escala ao longo do *eixo y.*

</dd> <dt>

*Z* 
</dt> <dd>

Fatores de escala ao longo do *eixo z.*

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glScaled** produz um dimensionamento geral ao longo dos *eixos x*, *y* e *z.* Os três argumentos indicam os fatores de escala desejados ao longo de cada um dos três eixos. A matriz resultante é

![Diagrama mostrando a matriz de fatores de escala ao longo dos eixos x, y e z.](images/scale01.png)

A matriz atual (consulte [**glMatrixMode**](glmatrixmode.md)) é multiplicada por essa matriz de escala, com o produto substituindo a matriz atual. Ou seja, se M for a matriz atual e S for a matriz de escala, M será substituído por M S.

Se o modo de matriz for GL MODELVIEW ou GL PROJECTION, todos os objetos desenhados \_ \_ depois que **glScaled** for chamado serão dimensionados. Use [**glPushMatrix e**](glpushmatrix.md) [**glPopMatrix**](glpopmatrix.md) para salvar e restaurar o sistema de coordenadas não escalado.

Se fatores de escala que não sejam 1,0 são aplicados à matriz modelview e a iluminação está habilitada, a normalização automática de normais provavelmente também deve ser habilitada [**(glEnable**](glenable.md) e [**glDisable**](gldisable.md) com o argumento GL \_ NORMALIZE).

As seguintes funções recuperam informações relacionadas **a glScaled**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MATRIX \_ MODE

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MODELVIEW \_ MATRIX

[**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o argumento GL \_ PROJECTION \_ MATRIX

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ TEXTURE \_ MATRIX

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

 

 





