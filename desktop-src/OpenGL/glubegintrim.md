---
title: Função gluBeginTrim (Glu.h)
description: As funções gluBeginTrim e gluEndTrim delimitam uma definição de loop de corte N GLUS (Racional B-Spline) não uniforme. | Função gluBeginTrim (Glu.h)
ms.assetid: 636402d0-8f6d-4ad8-84c6-66364025d788
keywords:
- Função gluBeginTrim OpenGL
topic_type:
- apiref
api_name:
- gluBeginTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebf103a2476aa856b55319e0eca42b8708da169fcedb34e48362062689727ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937879"
---
# <a name="glubegintrim-function"></a>Função gluBeginTrim

As **funções gluBeginTrim** e [**gluEndTrim**](gluendtrim.md) delimitam uma definição de loop de corte [N GLUS](using-nurbs-curves-and-surfaces.md)(Rational B-Spline ) não uniforme.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluBeginTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nobj* 
</dt> <dd>

O objeto N LTDA (criado com [**gluNewNheisRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use **gluBeginTrim** para marcar o início de um loop de corte e **gluEndTrim** para marcar o final de um loop de corte. Um loop de corte é um conjunto de segmentos de curva orientada (formando uma curva fechada) que definem limites de uma superfície N LTDA. Você inclui esses loops de corte na definição de uma superfície NFACES, entre chamadas para [**gluBeginSurface**](glubeginsurface.md) e [**gluEndSurface**](gluendsurface.md).

A definição de uma superfície N LTDA pode conter muitos loops de corte. Por exemplo, se você escrever uma definição para uma superfície NALTERS semelhante a um retângulo com um orifício cortado, a definição conterá dois loops de corte. Um loop definiria a borda externa do retângulo; o outro definiria o orifício de saída. As definições de cada um desses loops de corte seriam entre colchetes por um **par gluBeginTrim**  /  **gluEndTrim.**

A definição de um único loop de corte fechado pode consistir em vários segmentos de curva, cada um descrito como uma série de segmentos de linha que formam uma curva linear (consulte [**gluPwlCurve**](glupwlcurve.md)), como uma única curva NALTERS (consulte [**gluNrecsCurve)**](glunurbscurve.md)ou como uma combinação de ambos em qualquer ordem. As únicas chamadas de biblioteca que podem aparecer em uma definição de trimming-loop (entre as chamadas para **gluBeginTrim** e **gluEndTrim**) são **gluPwlCurve** e **gluNrecesCurve**.

A área exibida da superfície N EXCELS é a região no domínio à esquerda da curva de corte à medida que o parâmetro de curva aumenta. Portanto, a região retida da superfície N LTDA está dentro de um loop de corte no sentido anti-horário e fora de um loop de corte no sentido horário. Para o retângulo mencionado anteriormente, o loop de corte para a borda externa do retângulo é executado no sentido anti-horário, enquanto o loop de corte para o orifício cortado é executado no sentido horário.

Se você usar mais de uma curva para definir um único loop de corte, os segmentos de curva deverão formar um loop fechado (ou seja, o ponto de extremidade de cada curva deve ser o ponto inicial da próxima curva e o ponto de extremidade da curva final deve ser o ponto inicial da primeira curva). Se os pontos de extremidade da curva estão suficientemente próximos, mas não exatamente coincidentes, eles serão forçados a corresponder. Se os pontos de extremidade não são suficientemente próximos, um erro resulta (consulte [*gluN gluN gluNcallback*](glunurbs.md)).

Se uma definição de loop de corte contiver várias curvas, a direção das curvas deverá ser consistente (ou seja, o interior deve estar à esquerda de todas as curvas). Você pode usar loops de corte aninhados, desde que as orientações de curva alternem corretamente. As curvas de corte não podem ser auto interseção, nem intersecção entre si (ou resultados de erro).

Se nenhuma informação de corte for dada para uma superfície N LTDA, toda a superfície será desenhada.

## <a name="examples"></a>Exemplos

Esse fragmento de código define um loop de corte que consiste em uma curva linear lado a lado e duas curvas NALTERS:

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
| Cabeçalho<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluEndSurface**](gluendsurface.md)
</dt> <dt>

[**gluNewNagisRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[*gluNagisCallback*](glunurbs.md)
</dt> <dt>

[**gluNagisCurve**](glunurbscurve.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





