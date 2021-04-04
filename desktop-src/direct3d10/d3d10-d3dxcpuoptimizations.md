---
description: Habilita ou desabilita otimizações de CPU.
ms.assetid: 6f73df12-f2fc-4651-b0f7-f7a55e534d3d
title: Função D3DXCpuOptimizations (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCpuOptimizations
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0ef276e6d3303acd77c9580b55a9aa49dbe2087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664056"
---
# <a name="d3dxcpuoptimizations-function"></a>Função D3DXCpuOptimizations

Habilita ou desabilita otimizações de CPU.

## <a name="syntax"></a>Sintaxe


```C++
D3DX_CPU_OPTIMIZATION D3DXCpuOptimizations(
  _In_ BOOL Enable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Habilitar* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

**True** para habilitar otimizações de CPU; caso contrário, **false**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **\_ \_ otimização da CPU D3DX**](d3dx-cpu-optimization.md)**

Retorna o tipo de CPU detectada e para quais otimizações existem (consulte [**D3DX \_ CPU \_ Optimization**](d3dx-cpu-optimization.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
