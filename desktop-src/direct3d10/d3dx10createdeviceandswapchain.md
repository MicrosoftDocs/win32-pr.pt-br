---
description: Crie o melhor dispositivo Direct3D e uma cadeia de permuta.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: Função D3DX10CreateDeviceAndSwapChain (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDeviceAndSwapChain
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: fe71aeae91f8c43966e0fda2d2f430c7908f2855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298759"
---
# <a name="d3dx10createdeviceandswapchain-function"></a>Função D3DX10CreateDeviceAndSwapChain

Crie o melhor dispositivo Direct3D e uma cadeia de permuta.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateDeviceAndSwapChain(
  _In_  IDXGIAdapter         *pAdapter,
  _In_  D3D10_DRIVER_TYPE    DriverType,
  _In_  HMODULE              Software,
  _In_  UINT                 Flags,
  _In_  DXGI_SWAP_CHAIN_DESC *pSwapChainDesc,
  _Out_ IDXGISwapChain       **ppSwapChain,
  _Out_ ID3D10Device         **ppDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAdapter* \[ no\]
</dt> <dd>

Tipo: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Ponteiro para um [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).

</dd> <dt>

*DriverType* \[ no\]
</dt> <dd>

Tipo: **[ **\_ \_ tipo de driver d3d10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

O tipo de driver para o dispositivo. Consulte [**\_ \_ tipo de driver d3d10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

</dd> <dt>

*Software* \[ no\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Um identificador para a DLL que implementa um rasterizador de software. Deve ser **NULL** se o driverType for não software. O HMODULE de uma DLL pode ser obtido com [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)ou [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Opcional. Sinalizadores de criação de dispositivo (consulte [**d3d10 \_ criar \_ \_ sinalizador de dispositivo**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) que habilitam [camadas de API](d3d10-graphics-programming-guide-api-features-layers.md). Esses sinalizadores podem ser unificados ou juntos.

</dd> <dt>

*pSwapChainDesc* \[ no\]
</dt> <dd>

Tipo: a **[ **cadeia de permuta do dxgi \_ \_ \_ desc**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***

Descrição da cadeia de permuta. Consulte [**\_ desc de \_ cadeia \_ de permuta dxgi**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).

</dd> <dt>

*ppSwapChain* \[ fora\]
</dt> <dd>

Tipo: **[ **IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***

Endereço de um ponteiro para um [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).

</dd> <dt>

*ppDevice* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Endereço de um ponteiro para uma [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) que receberá o dispositivo recém-criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Esse método retorna um dos seguintes [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Para criar o melhor dispositivo, esse método implementa mais de uma opção de criação de dispositivo. Primeiro, o método tenta criar um dispositivo 10,1 (e uma cadeia de permuta). Se isso falhar, o método tentará criar um dispositivo 10,0. Se isso falhar, o método falhará. Se seu aplicativo precisar criar apenas um dispositivo 10,1 ou um dispositivo 10,0, use essas APIs em vez disso:

-   Use [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) para criar um dispositivo Direct3D 10,0 (somente) e uma cadeia de permuta.
-   Use [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) para criar um dispositivo Direct3D 10,1 (somente) e uma cadeia de permuta.

Esse método requer o Windows Vista Service Pack 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Uso Geral](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
