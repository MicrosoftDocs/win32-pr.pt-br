---
title: Método ID3D12DeviceDownlevel::QueryVideoMemoryInfo
description: Copia o conteúdo de um recurso Texture2D do Direct3D 12 em uma janela. | Método ID3D12DeviceDownlevel::QueryVideoMemoryInfo
keywords:
- Método QueryVideoMemoryInfo
- Método QueryVideoMemoryInfo, interface ID3D12DeviceDownlevel
- Interface ID3D12DeviceDownlevel, método QueryVideoMemoryInfo
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel.QueryVideoMemoryInfo
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 526d25e8331fc949eb470c0813a083774afddc94312ed6751aaab9672e557d3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124104"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a>Método ID3D12DeviceDownlevel::QueryVideoMemoryInfo

Fornece estatísticas de memória Windows 7. Esse método é equivalente a [IDXGIAdapter3::QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), que não está disponível no Windows 7.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT QueryVideoMemoryInfo( 
    UINT NodeIndex,
    DXGI_MEMORY_SEGMENT_GROUP MemorySegmentGroup,
    DXGI_QUERY_VIDEO_MEMORY_INFO *pVideoMemoryInfo
);
```

## <a name="parameters"></a>Parâmetros

`NodeIndex`

Tipo: **UINT**

Especifica o adaptador físico do dispositivo para o qual as informações de memória de vídeo são consultadas. Para a operação de GPU única, de definido como zero. Se houver vários nós de GPU, de definido como o índice do nó (o adaptador físico do dispositivo) para o qual as informações de memória de vídeo são consultadas. Consulte [Sistemas de vários adaptadores.](multi-engine.md)

`MemorySegmentGroup`

Tipo: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**

Especifica um **DXGI_MEMORY_SEGMENT_GROUP** que identifica o grupo como local ou não local.

`pVideoMemoryInfo`

Tipo: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***

Preenche uma estrutura **DXGI_QUERY_VIDEO_MEMORY_INFO** com os valores atuais.

## <a name="return-value"></a>Valor retornado

Retorna **S_OK** em caso de êxito ou então um HRESULT com falha.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------|------------------|
| parâmetro | d3d12downlevel.h e dxgi1_4.h |
| DLL    | D3D12.dll (Windows somente 7) |

## <a name="see-also"></a>Confira também
* [ID3D12DeviceDownlevel](id3d12devicedownlevel.md)
* [O Direct3D 12 em interfaces do Windows 7](direct3d-12on7-interfaces.md)
* [Direct3D 12 na Windows 7 (d3d12downlevel.h)](direct3d-12on7-reference.md)
* [O Direct3D 12 no Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
