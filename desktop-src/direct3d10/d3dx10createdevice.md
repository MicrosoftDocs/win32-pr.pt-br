---
description: Crie o melhor dispositivo Direct3D 10 que representa o adaptador de exibição. Se um dispositivo compatível com Direct3D 10.1 puder ser criado, será possível adquirir um ponteiro de interface ID3D10Device1 do ponteiro de interface do dispositivo retornado.
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: Função D3DX10CreateDevice (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDevice
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 9300eb74027d25562dabb9a596face10105110d1750b359bcaae9ab6b2b83084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634696"
---
# <a name="d3dx10createdevice-function"></a>Função D3DX10CreateDevice

Crie o melhor dispositivo Direct3D 10 que representa o adaptador de exibição. Se um dispositivo compatível com Direct3D 10.1 puder ser criado, será possível adquirir um ponteiro de [**interface ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) do ponteiro de interface do dispositivo retornado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateDevice(
  _In_  IDXGIAdapter      *pAdapter,
  _In_  D3D10_DRIVER_TYPE DriverType,
  _In_  HMODULE           Software,
  _In_  UINT              Flags,
  _Out_ ID3D10Device      **ppDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAdapter* \[ Em\]
</dt> <dd>

Tipo: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Ponteiro para o adaptador de exibição (consulte a interface [**IDXGIAdapter)**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) ao criar um dispositivo de hardware; caso contrário, de definir esse parâmetro como **NULL.** Se **NULL** for especificado ao criar um dispositivo de hardware, o Direct3D usará o primeiro adaptador enumerado pela interface [**IDXGIFactory.**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory)

</dd> <dt>

*DriverType* \[ Em\]
</dt> <dd>

Tipo: **[ **D3D10 \_ TIPO DE \_ DRIVER**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

O tipo de driver de dispositivo (consulte a [**enumeração D3D10 \_ DRIVER \_ TYPE).**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) O tipo de driver determina o tipo de dispositivo que você criará.

</dd> <dt>

*Software* \[ Em\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Um handle para um módulo carregado que implementa um driver de software (como D3D10Ref.dll). Para obter um handle, chame a [função GetModuleHandle.](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)

</dd> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Sinalizadores de criação de dispositivo (consulte a [**enumeração D3D10 \_ CREATE DEVICE \_ \_ FLAG)**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) que habilitam camadas [de API](d3d10-graphics-programming-guide-api-features-layers.md). Esses sinalizadores podem ser OR'd bit a bit juntos.

</dd> <dt>

*ppDevice* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Endereço de um ponteiro para o dispositivo criado (consulte a interface [**ID3D10Device).**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Essa função retorna um dos códigos [de retorno do Direct3D 10 a seguir.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Essa função tenta criar o melhor dispositivo para o hardware. Primeiro, a função tenta criar um dispositivo 10.1. Se um dispositivo 10.1 não puder ser criado, a função tentará criar um dispositivo 10.0. Se nenhum dos dispositivos for criado com êxito, a função retornará E \_ FAIL.

Se seu aplicativo precisar criar apenas um dispositivo 10.1 ou apenas um dispositivo 10.0, use as seguintes funções:

-   Use a [**função D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) para criar apenas um dispositivo Direct3D 10.0.
-   Use a [**função D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) para criar apenas um dispositivo Direct3D 10.1.
-   Use a [**função D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) para obter um ponteiro de interface [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) de um ponteiro de interface [**ID3D10Device.**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)

Um dispositivo Direct3D 10.1 só pode ser criado em computadores que executam o Windows Vista Service Pack 1 ou posterior e com hardware compatível com Direct3D 10.1 instalado. No entanto, é legal chamar essa função em computadores que executam qualquer versão do Windows que tenha a DLL D3DX10 instalada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso Geral funções](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
