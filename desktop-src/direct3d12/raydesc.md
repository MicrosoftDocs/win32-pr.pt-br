---
description: Passado para a função TraceRay para definir a origem, a direção e as extensões do raio.
ms.assetid: ''
title: Estrutura RayDesc
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: a5fd6e041fc476c24ff926c9c8f99f05699f5e41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814049"
---
# <a name="raydesc-structure"></a>Estrutura RayDesc

Passado para a função [**TraceRay**](traceray-function.md) para definir a origem, a direção e as extensões do raio.

## <a name="syntax"></a>Sintaxe


```
struct RayDesc
{
    float3 Origin;
    float  TMin;
    float3 Direction;
    float  TMax;
};

```



## <a name="fields"></a>Campos

<dl> <dt>

<span id="Origin"></span><span id="origin"></span>**Ter**
</dt> <dd>

A origem do raio.

</dd> <dt>

<span id="TMin"></span><span id="tmin"></span>**TMin**
</dt> <dd>

A extensão mínima do raio.


</dd> <dt>

<span id="Direction"></span><span id="direction"></span>**Direção**
</dt> <dd>

A direção do raio.


</dd> <dt>

<span id="TMax"></span><span id="tmax"></span>**TMax**
</dt> <dd>

A extensão máxima do raio.


</dd>

## <a name="requirements"></a>Requisitos



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




