---
title: Método ID3D12CommandQueueDownlevel::P resent
description: Copia o conteúdo de um recurso Texture2D do Direct3D 12 em uma janela. | Método ID3D12CommandQueueDownlevel::P resent
keywords:
- Método presente
- Método present, interface ID3D12CommandQueueDownlevel
- Interface ID3D12CommandQueueDownlevel, método Present
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
ms.openlocfilehash: b21a97d15d2666dcfe0a304f2393d6d14c5dbcc4142d8b42f43f295d8751614b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118529126"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a>Método ID3D12CommandQueueDownlevel::P resent

Copia o conteúdo de um recurso Texture2D do Direct3D 12 em uma janela.

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

Uma lista de comandos aberta, na qual o Direct3D 12 enquete um comando Present e, em seguida, fecha e envia para você.

`pSourceTex2D`

Tipo: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***

Um recurso que contém o conteúdo desejado a ser exibido, com a dimensão [**D3D12 \_ RESOURCE \_ DIMENSION \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)e um formato que é um dos seguintes.

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

O alça para a janela em que o conteúdo deve ser exibido.

`Flags`

Tipo: **[SINALIZADORES D3D12 \_ DOWNLEVEL \_ PRESENT \_](d3d12_downlevel_present_flags.md)**

Sinalizadores para modificar a **operação** Present.

## <a name="return-value"></a>Valor retornado

Retorna **S_OK** em caso de êxito ou então um HRESULT com falha.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------|------------------|
| parâmetro | d3d12downlevel.h |
| DLL    | D3D12.dll (Windows somente 7) |

## <a name="see-also"></a>Confira também
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [O Direct3D 12 em interfaces do Windows 7](direct3d-12on7-interfaces.md)
* [Direct3D 12 na Windows 7 (d3d12downlevel.h)](direct3d-12on7-reference.md)
* [O Direct3D 12 no Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
