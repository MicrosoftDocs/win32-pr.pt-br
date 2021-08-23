---
title: função glFrustum (GL. h)
description: A função glFrustum multiplica a matriz atual por uma matriz de perspectiva.
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- função glFrustum OpenGL
topic_type:
- apiref
api_name:
- glFrustum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1ca2375206165576405c96528d0590596f4d4d870121f0a30884c8e448ca93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625239"
---
# <a name="glfrustum-function"></a>função glFrustum

A função **glFrustum** multiplica a matriz atual por uma matriz de perspectiva.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glFrustum(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*esquerda* 
</dt> <dd>

A coordenada para o plano de recorte vertical esquerdo.

</dd> <dt>

*direita* 
</dt> <dd>

A coordenada do plano de recorte vertical à direita.

</dd> <dt>

*parte inferior* 
</dt> <dd>

A coordenada do plano de recorte inferior horizontal.

</dd> <dt>

*início* 
</dt> <dd>

A coordenada do plano de recorte inferior horizontal.

</dd> <dt>

*zNear* 
</dt> <dd>

As distâncias para o plano de recorte quase aprofundado. Deve ser positivo.

</dd> <dt>

*zFar* 
</dt> <dd>

As distâncias para os planos de recorte muito detalhados. Deve ser positivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *zNear* ou *zFar* não era postitive.<br/>                                                                                       |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glFrustum** descreve uma matriz de perspectiva que produz uma projeção de perspectiva. Os parâmetros (*esquerda*, *inferior*, *zNear*) e (*direita*, *superior*, *zNear*) especificam os pontos no plano de recorte próximo que são mapeados para os cantos inferior esquerdo e superior direito da janela, respectivamente, supondo que o olho está localizado em (0, 0, 0). O parâmetro *zFar* especifica o local do plano de recorte distante. *ZNear* e *zFar* devem ser positivos. A matriz correspondente é mostrada na imagem a seguir.

![Diagrama que mostra a matriz de perspectiva que produz uma projeção em perspectiva.](images/frust01.png)![Equações mostrando a função glFrustum que descreve uma matriz de perspectiva.](images/frust02.png)

A função **glFrustum** multiplica a matriz atual por esta matriz, com o resultado que substitui a matriz atual. Ou seja, se M for a matriz atual e F for a matriz de perspectiva frustum, **glFrustum** substituirá M por m F.

Use [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) para salvar e restaurar a pilha de matriz atual.

A precisão do buffer de profundidade é afetada pelos valores especificados para *zNear* e *zFar*. Quanto maior a proporção de *zFar* para *zNear* , menor será o buffer de profundidade em relação à distinção entre as superfícies que estão próximas umas das outras. If

![Equação mostrando a proporção de até o próximo.](images/frust03.png)

aproximadamente *log* 2 (*r*) partes de precisão do buffer de profundidade são perdidas. Como o *r* se aproxima do infinito, uma vez que o *zNear* se aproxima de zero, você nunca deve definir *zNear* como zero.

As seguintes funções recuperam informações sobre **glFrustum**:

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

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





