---
title: função gluEndTrim (Glu. h)
description: As funções gluBeginTrim e gluEndTrim delimitam uma definição de loop de corte de B-spline racional não uniforme (NURBS). | função gluEndTrim (Glu. h)
ms.assetid: e85cc60b-4492-441d-b778-31a3d52b398a
keywords:
- função gluEndTrim OpenGL
topic_type:
- apiref
api_name:
- gluEndTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4105cc911105f0444ba17c6b57a3deb048bc96d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104012014"
---
# <a name="gluendtrim-function"></a>função gluEndTrim

As funções [**gluBeginTrim**](glubegintrim.md) e **gluEndTrim** delimitam uma definição de loop de corte de B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluEndTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nobj* 
</dt> <dd>

O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use [**gluBeginTrim**](glubegintrim.md) para marcar o início de um loop de corte e **gluEndTrim** para marcar o final de um loop de corte. Um loop de corte é um conjunto de segmentos de curva orientados (formando uma curva fechada) que definem limites de uma superfície NURBS. Você inclui esses loops de corte na definição de uma superfície NURBS, entre chamadas para [**gluBeginSurface**](glubeginsurface.md) e [**gluEndSurface**](gluendsurface.md).

A definição de uma superfície NURBS pode conter muitos loops de corte. Por exemplo, se você escrever uma definição para uma superfície NURBS que se assemelha a um retângulo com uma perfuração perfurada, a definição conteria dois loops de corte. Um loop definiria a borda externa do retângulo; o outro definiria o buraco perfurado. As definições de cada um desses loops de corte seriam enmarcadas por um par [**gluBeginTrim**](glubegintrim.md)  /  **gluEndTrim** .

A definição de um único loop de corte fechado pode consistir em vários segmentos de curva, cada um descrito como uma série de segmentos de linha que formam uma curva linear (consulte [**gluPwlCurve**](glupwlcurve.md)), como uma curva NURBS única (consulte [**gluNurbsCurve**](glunurbscurve.md)) ou como uma combinação de ambos em qualquer ordem. As únicas chamadas de biblioteca que podem aparecer em uma definição de loop de corte (entre as chamadas para [**gluBeginTrim**](glubegintrim.md) e **GluEndTrim**) são **gluPwlCurve** e **gluNurbsCurve**.

A área exibida da superfície NURBS é a região no domínio à esquerda da curva de corte conforme o parâmetro de curva aumenta. Assim, a região retida da superfície NURBS está dentro de um loop de corte no sentido anti-horário e fora de um loop de corte no sentido horário. Para o retângulo mencionado anteriormente, o loop de corte para a borda externa do retângulo é executado no sentido anti-horário, enquanto o loop de corte para o buraco perfurado é executado no sentido horário.

Se você usar mais de uma curva para definir um único loop de corte, os segmentos de curva deverão formar um loop fechado (ou seja, o ponto de extremidade de cada curva deverá ser o início da próxima curva e o ponto de extremidade da curva final deverá ser o início da primeira curva). Se os pontos de extremidade da curva estiverem suficientemente próximos juntos, mas não forem exatamente coincidentes, eles serão forçados a coincidir. Se os pontos de extremidade não estiverem suficientemente fechados, ocorrerá um erro (consulte [*gluNurbsCallback*](glunurbs.md)).

Se uma definição de loop de corte contiver várias curvas, a direção das curvas deverá ser consistente (ou seja, o interior deve estar à esquerda de todas as curvas). Você pode usar loops de corte aninhados, desde que as orientações de curva sejam alternadas corretamente. As curvas de corte não podem ser interseccionadas automaticamente nem se interseccionam uma com a outra (ou um resultado de erro).

Se nenhuma informação de corte for fornecida para uma superfície NURBS, toda a superfície será desenhada.

## <a name="examples"></a>Exemplos

Este fragmento de código define um loop de corte que consiste em uma curva linear piecewise e duas curvas NURBS:

``` syntax
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);
```

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

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluEndSurface**](gluendsurface.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





