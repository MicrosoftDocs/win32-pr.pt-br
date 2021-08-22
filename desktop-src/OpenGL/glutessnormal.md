---
title: Função gluTessNormal (Glu.h)
description: A função gluTessNormal especifica um normal para um polígono.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- Função gluTessNormal OpenGL
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
ms.openlocfilehash: 2db848c6971fe2893f2bc2cd4ca33e96811dda0d44e81e8a852cd441a6478d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488466"
---
# <a name="glutessnormal-function"></a>Função gluTessNormal

A **função gluTessNormal** especifica um normal para um polígono.

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

*Tess* 
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

*Z* 
</dt> <dd>

O componente de coordenada z de um normal.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A **função gluTessNormal** descreve um normal para um polígono que você define. Todos os dados de entrada são projetados em um plano em um dos três eixos de coordenadas antes do mosaico, e todos os triângulos de saída são orientados no sentido anti-horário em relação ao normal. (Para obter a orientação no sentido horário, reverte o sinal do normal fornecido). Por exemplo, se você sabe que todos os polígonos estão no plano x-y, chame **gluTessNormal**(tess, 0.0, 0.0, 1.0) antes de renderizar os polígonos.

Se o normal fornecido for (0,0, 0,0, 0,0) (o valor padrão), o normal será determinado da seguinte forma:

1.  A direção do normal, até seu sinal, é encontrada ajustando um plano aos vértices, sem considerar como os vértices estão conectados. Espera-se que os dados de entrada estão aproximadamente no plano; caso contrário, a projeção de um dos três eixos de coordenadas pode alterar substancialmente a geometria.
2.  O sinal do normal é escolhido para que a soma das áreas assinadas de todos os contornos de entrada seja não negativo (em que um acento anti-horário tem área positiva).

O normal fornecido persiste até que outra chamada para **gluTessNormal** o mude.

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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> </dl>

 

 





