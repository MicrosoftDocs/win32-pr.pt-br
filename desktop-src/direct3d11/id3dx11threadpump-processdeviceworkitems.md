---
title: Método ID3DX11ThreadPump ProcessDeviceWorkItems (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Define itens de trabalho para o dispositivo depois que eles terminarem de carregar e processar.
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- Método ProcessDeviceWorkItems Direct3D 11
- Método ProcessDeviceWorkItems Direct3D 11, interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11, método ProcessDeviceWorkItems
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.ProcessDeviceWorkItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad570785ac7dc36fb5dd9d464e97ef46f52ca93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968590"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a>ID3DX11ThreadPump: método rocessDeviceWorkItems de:P

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Define itens de trabalho para o dispositivo depois que eles terminarem de carregar e processar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iWorkItemCount* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de itens de trabalho a serem definidos para o dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Quando a bomba do thread terminar de carregar e processar um recurso ou sombreador, ele a manterá em uma fila até que essa API seja chamada, ponto em que os itens processados serão definidos para o dispositivo. Isso é útil para controlar a quantidade de processamento que é gasto na associação de recursos ao dispositivo para cada quadro.

Como um exemplo de como é possível usar essa API, digamos que você esteja se aproximando do final de um nível em seu jogo e queira começar a carregar as texturas, os sombreadores e outros recursos para o próximo nível. A bomba de thread começará a carregar, descompactar e processar os recursos e os sombreadores em um thread separado até que eles estejam prontos para serem definidos para o dispositivo; nesse ponto, eles serão deixados em uma fila. Talvez você não queira definir todos os recursos e sombreadores para o dispositivo de uma vez, pois isso pode causar uma lentidão temporária perceptível no desempenho do jogo. Portanto, essa API pode ser chamada uma vez por quadro para que apenas um pequeno número de itens de trabalho fosse definido para o dispositivo em cada quadro, distribuindo assim a carga de trabalho dos recursos de ligação para o dispositivo em vários quadros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

