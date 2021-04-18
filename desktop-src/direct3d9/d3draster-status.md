---
description: Descreve o status de rasterização.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: Estrutura de D3DRASTER_STATUS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRASTER_STATUS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e77ab0e6ee164eadae862ed03df5652c21ba7040
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105796143"
---
# <a name="d3draster_status-structure"></a>Estrutura de status do D3DRASTER \_

Descreve o status de rasterização.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a>Membros

<dl> <dt>

**InVBlank**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

**True** se a rasterização estiver no período vertical em branco. **False** se a rasterização não estiver no período vertical em branco.

</dd> <dt>

**Verificação**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Se InVBlank for **false**, esse valor será um inteiro aproximadamente correspondente à linha de exame atual pintada pela rasterização. As linhas de verificação são numeradas da mesma maneira que as coordenadas da superfície do Direct3D: 0 é a parte superior da superfície primária, estendendo para o valor (altura da superfície-1) na parte inferior da exibição.

Se InVBlank for **true**, esse valor será definido como zero e poderá ser ignorado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
