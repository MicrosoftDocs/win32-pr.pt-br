---
title: Interface ID3D12CommandQueueDownlevel
description: Fornece um mecanismo presente do Windows-7 específico.
keywords:
- Interface ID3D12CommandQueueDownlevel
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 6f2aee6fd1b0f58469162c640d92aeb187bd9641
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105769660"
---
# <a name="id3d12commandqueuedownlevel-interface"></a>Interface ID3D12CommandQueueDownlevel

Essa interface pode ser acessada por meio de **QueryInterface** de uma [fila de comando do Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) ao usar o [Direct3D 12 no Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/). Ele fornece um mecanismo presente do Windows-7 específico.

### <a name="methods"></a>Métodos

A interface **ID3D12CommandQueueDownlevel** tem esses métodos.

| Método | Descrição |
|:-------|:------------|
| [**Existi**](id3d12commandqueuedownlevel-present.md) | Copia o conteúdo de um recurso D3D12 Texture2D para uma janela. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------|------------------|
| parâmetro | d3d12downlevel. h |
| DLL    | D3D12.dll (somente Windows 7) |

## <a name="see-also"></a>Confira também
* [O Direct3D 12 em interfaces do Windows 7](direct3d-12on7-interfaces.md)
* [Referência do Direct3D 12 no Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [O Direct3D 12 no Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
