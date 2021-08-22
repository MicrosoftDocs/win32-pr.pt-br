---
description: Remove todos os recursos do dispositivo definindo seus ponteiros como NULL. Isso deve ser chamado durante o desligamento do seu aplicativo. Ele ajuda a garantir que, quando um estiver liberando todos os seus recursos, nenhum deles esteja associado ao dispositivo.
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: Função D3DX10UnsetAllDeviceObjects (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10UnsetAllDeviceObjects
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 079c5f1b437c2755bf7125dee6be10baed1a91b4a37276997e70543c72904036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128338"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a>Função D3DX10UnsetAllDeviceObjects

Remove todos os recursos do dispositivo definindo seus ponteiros como **NULL**. Isso deve ser chamado durante o desligamento do seu aplicativo. Ele ajuda a garantir que, quando um estiver liberando todos os seus recursos, nenhum deles esteja associado ao dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Ponteiro para o dispositivo. Consulte a [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Uso Geral](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




