---
title: função gluTessNormal (Glu. h)
description: A função gluTessNormal especifica um normal para um polígono.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- função gluTessNormal OpenGL
topic_type:
- apiref
api_name:
- gluTessNormal
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af04ab2364fafcea709ca36cab2f10a8bea1a96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919056"
---
# <a name="glutessnormal-function"></a>função gluTessNormal

A função **gluTessNormal** especifica um normal para um polígono.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluTessNormal(
   GLUtesselator *tess,
   GLdouble      x,
   GLdouble      y,
   GLdouble      z
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tess* 
</dt> <dd>

O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*x* 
</dt> <dd>

O componente de coordenada x de um normal.

</dd> <dt>

*y* 
</dt> <dd>

O componente de coordenada y de um normal.

</dd> <dt>

*z* 
</dt> <dd>

O componente de coordenada z de um normal.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluTessNormal** descreve um normal para um polígono que você define. Todos os dados de entrada são projetados em um plano perpendicular a um dos três eixos de coordenadas antes do mosaico, e todos os triângulos de saída são orientados no sentido anti-horário com relação ao normal. (Para obter a orientação no sentido horário, inverta o sinal do normal fornecido). Por exemplo, se você souber que todos os polígonos estão no plano x-y, chame **gluTessNormal**(tess, 0,0, 0,0, 1,0) antes de renderizar quaisquer polígonos.

Se o normal fornecido for (0,0, 0,0, 0,0) (o valor padrão), o normal será determinado da seguinte maneira:

1.  A direção do normal, até o sinal, é encontrada ao ajustar um plano aos vértices, sem considerar como os vértices estão conectados. Espera-se que os dados de entrada estejam aproximadamente no plano; caso contrário, a projeção perpendicular a um dos três eixos de coordenadas pode alterar a geometria substancialmente.
2.  O sinal do normal é escolhido para que a soma das áreas assinadas de todos os contornos de entrada seja não negativa (onde uma delimitação no sentido anti-horário tem uma área positiva).

O normal é mantido até que outra chamada para **gluTessNormal** o altere.

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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> </dl>

 

 





