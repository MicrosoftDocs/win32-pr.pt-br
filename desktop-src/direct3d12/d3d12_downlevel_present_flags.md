---
title: Enumeração de D3D12_DOWNLEVEL_PRESENT_FLAGS
description: Sinalizadores passados para o método ID3D12CommandQueueDownlevel::P reenviado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
topic_type:
- APIRef
api_name:
- D3D12_DOWNLEVEL_PRESENT_FLAGS
api_type:
- HeaderDef
ms.openlocfilehash: 1ce1536945748bae09fc7a0981c14c076fc6394e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790645"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a>\_Enumeração de \_ \_ sinalizadores presentes de D3D12 de nível inferior

Sinalizadores passados para a função [**ID3D12CommandQueueDownlevel::P reenviada**](id3d12commandqueuedownlevel-present.md) para modificar o comportamento.

## <a name="syntax"></a>Syntax

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a>Constantes

**\_Sinalizador de apresentação de nível inferior D3D12 \_ \_ \_ None**

Nenhuma opção selecionada.

**D3D12 \_ \_ \_ de sinalizador presente \_ de nível inferior \_ de \_ VBLANK**

A operação **atual** não será feita até que um vsync tenha ocorrido desde a última vez que você **apresentar** o Ed.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------|------------------|
| parâmetro | d3d12downlevel. h |
| DLL    | D3D12.dll (somente Windows 7) |

## <a name="see-also"></a>Confira também
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Enumerações do Direct3D 12 no Windows 7](direct3d-12on7-enumerations.md)
* [Referência do Direct3D 12 no Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [O Direct3D 12 no Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
