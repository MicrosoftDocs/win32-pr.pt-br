---
title: Interface ID3D12DeviceDownlevel
description: Fornece uma consulta de estatísticas de memória específica do Windows-7.
keywords:
- Interface ID3D12DeviceDownlevel
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 401cbd0045211ef51e3ef6b06042262964ae2ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764320"
---
# <a name="id3d12devicedownlevel-interface"></a>Interface ID3D12DeviceDownlevel

Essa interface pode ser acessada por meio de **QueryInterface** de um [dispositivo Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) ao usar o [Direct3D 12 no Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/). Ele fornece uma consulta de estatísticas de memória específica do Windows-7.

### <a name="methods"></a>Métodos

A interface **ID3D12DeviceDownlevel** tem esses métodos.

| Método | Descrição |
|:-------|:------------|
| [**QueryVideoMemoryInfo**](id3d12devicedownlevel-queryvideomemoryinfo.md) | Fornece estatísticas de memória no Windows 7. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------|------------------|
| parâmetro | d3d12downlevel. h |
| DLL    | D3D12.dll (somente Windows 7) |

## <a name="see-also"></a>Confira também
* [O Direct3D 12 em interfaces do Windows 7](direct3d-12on7-interfaces.md)
* [Referência do Direct3D 12 no Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [O Direct3D 12 no Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
