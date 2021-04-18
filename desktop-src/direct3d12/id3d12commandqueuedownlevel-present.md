---
title: 'ID3D12CommandQueueDownlevel: método reenviado:P'
description: 'Copia o conteúdo de um recurso do Direct3D 12 Texture2D para uma janela. | ID3D12CommandQueueDownlevel: método reenviado:P'
keywords:
- Método presente
- Método presente, interface ID3D12CommandQueueDownlevel
- Interface ID3D12CommandQueueDownlevel, método presente
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel.Present
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: a6c74685911e52a671eaeb02645754a45b8d647e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802159"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a>ID3D12CommandQueueDownlevel: método reenviado:P

Copia o conteúdo de um recurso do Direct3D 12 Texture2D para uma janela.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT Present
    ID3D12GraphicsCommandList *pOpenCommandList,
    ID3D12Resource *pSourceTex2D,
    HWND hWindow,
    D3D12_DOWNLEVEL_PRESENT_FLAGS Flags
);
```

## <a name="parameters"></a>Parâmetros

`pOpenCommandList`

Tipo: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Uma lista de comandos aberta, que o Direct3D 12 enfileira um comando presente em e, em seguida, fecha e envia para você.

`pSourceTex2D`

Tipo: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***

Um recurso que contém o conteúdo desejado a ser exibido, com Dimension [**D3D12 \_ Resource \_ Dimension \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)e um formato que seja um dos seguintes.

* DXGI_FORMAT_R16G16B16A16_FLOAT
* DXGI_FORMAT_R10G10B10A2_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM_SRGB
* DXGI_FORMAT_B8G8R8X8_UNORM
* DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM_SRGB

`hWindow`

Tipo: **[HWND](/windows/desktop/WinProg/windows-data-types)**

O identificador para a janela em que o conteúdo deve ser exibido.

`Flags`

Tipo: **[ \_ \_ \_ sinalizadores presentes de D3D12 de nível inferior](d3d12_downlevel_present_flags.md)**

Sinalizadores para modificar a operação **atual** .

## <a name="return-value"></a>Retornar valor

Retorna **S_OK** em caso de êxito ou um HRESULT com falha.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------|------------------|
| parâmetro | d3d12downlevel. h |
| DLL    | D3D12.dll (somente Windows 7) |

## <a name="see-also"></a>Confira também
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [O Direct3D 12 em interfaces do Windows 7](direct3d-12on7-interfaces.md)
* [Referência do Direct3D 12 no Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [O Direct3D 12 no Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
