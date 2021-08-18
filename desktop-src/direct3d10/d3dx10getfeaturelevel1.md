---
description: Obter um ponteiro de interface do dispositivo Direct3D 10.1 de um ponteiro de interface Direct3D 10.0.
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: Função D3DX10GetFeatureLevel1 (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetFeatureLevel1
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: c6511e0d3963e21f8950529b32cf8c3b414cc00b0625b97b2a9d569d1523c326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753166"
---
# <a name="d3dx10getfeaturelevel1-function"></a>Função D3DX10GetFeatureLevel1

Obter um ponteiro de interface do dispositivo Direct3D 10.1 de um ponteiro de interface Direct3D 10.0.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Ponteiro para o dispositivo Direct3D 10.0 (consulte a interface [**ID3D10Device).**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)

</dd> <dt>

*ppDevice* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***

Ponteiro para o dispositivo Direct3D 10.1 (consulte a interface [**ID3D10Device1).**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Essa função retorna um dos códigos [de retorno do Direct3D 10 a seguir.](d3d10-graphics-reference-returnvalues.md) Se uma interface do dispositivo Direct3D 10.1 puder ser adquirida, essa função terá êxito e passará um ponteiro para a interface 10.1 usando o *parâmetro ppDevice.* Se uma interface do dispositivo Direct3D 10.1 não puder ser adquirida, essa função retornará E FAIL e não retornará nada para o \_ *parâmetro ppDevice.*

## <a name="remarks"></a>Comentários

Para que essa função tenha êxito, você deve ter adquirido o ponteiro [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) fornecido usando uma chamada para a função [**D3DX10CreateDevice,**](d3dx10createdevice.md) a função [**D3DX10CreateDeviceAndSwapChain,**](d3dx10createdeviceandswapchain.md) a função [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) ou a [**função D3D10CreateDeviceAndSwapChain1.**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)

Você só pode criar um dispositivo Direct3D 10.1 em computadores que executam o Windows Vista Service Pack 1 ou posterior e com hardware compatível com Direct3D 10.1 instalado. Essa função retornará E \_ FAIL em qualquer computador que não atender a esses requisitos. No entanto, você pode chamar essa função em qualquer versão do Windows que tenha a DLL D3DX10 instalada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso Geral funções](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




