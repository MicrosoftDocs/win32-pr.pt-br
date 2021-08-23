---
description: Passado para a função TraceRay para definir a origem, a direção e as extensão do raio.
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
ms.openlocfilehash: a4fa44e68e8747a0a8366ca2d949290f585d4b70d9e75b4ed2d3b6fdda0d05c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123681"
---
# <a name="raydesc-structure"></a>Estrutura RayDesc

Passado para a [**função TraceRay**](traceray-function.md) para definir a origem, a direção e as extensão do raio.

## <a name="syntax"></a>Syntax


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

<span id="Origin"></span><span id="origin"></span>**Origem**
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

<span id="TMax"></span><span id="tmax"></span>**Tmax**
</dt> <dd>

A extensão máxima do raio.


</dd>

## <a name="requirements"></a>Requisitos



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




