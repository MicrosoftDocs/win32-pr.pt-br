---
title: função glOrtho (GL. h)
description: A função glOrtho multiplica a matriz atual por uma matriz ortográfica.
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- função glOrtho OpenGL
topic_type:
- apiref
api_name:
- glOrtho
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1e06c1740e908c34652a6d39bc7a2334763199d222ff9d1dc00ae733803ada0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795211"
---
# <a name="glortho-function"></a>função glOrtho

A função **glOrtho** multiplica a matriz atual por uma matriz ortográfica.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glOrtho(
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

As coordenadas do plano de recorte vertical esquerdo.

</dd> <dt>

*direita* 
</dt> <dd>

As coordenadas para o plano de recorte vertical direito.

</dd> <dt>

*parte inferior* 
</dt> <dd>

As coordenadas do plano de recorte horizontal inferior.

</dd> <dt>

*início* 
</dt> <dd>

As coordenadas dos principais planos de recorte horizontal.

</dd> <dt>

*zNear* 
</dt> <dd>

As distâncias para o plano de recorte de profundidade mais próxima. Essa distância será negativa se o plano estiver por trás do visualizador.

</dd> <dt>

*zFar* 
</dt> <dd>

As distâncias para o plano de recorte de profundidade mais distante. Essa distância será negativa se o plano estiver por trás do visualizador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glOrtho** descreve uma matriz de perspectiva que produz uma projeção paralela. Os parâmetros (*esquerda*, *inferior*, *Near*) e (*direita*, *superior*, *Near*) especificam os pontos no plano de recorte próximo que são mapeados para os cantos inferior esquerdo e superior direito da janela, respectivamente, supondo que o olho está localizado em (0, 0, 0). O parâmetro *far* especifica o local do plano de recorte distante. Tanto *zNear* como *zFar* podem ser positivos ou negativos. A matriz correspondente é mostrada na imagem a seguir.

![Diagrama mostrando a matriz de perspectiva que a função glOrtho descreve.](images/ortho1.png)

onde

![Equações que descrevem a matriz de perspectiva.](images/ortho2.png)

A matriz atual é multiplicada por essa matriz com o resultado que substitui a matriz atual. Ou seja, se M for a matriz atual e O for a matriz Ortho, M será substituído por M O.

Use [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** para salvar e restaurar a pilha de matriz atual. Use [**glMatrixMode**](glmatrixmode.md) para definir a matriz atual.

As funções a seguir recuperam informações relacionadas ao **glOrtho**:

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





