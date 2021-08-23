---
title: Método ID3DX11ThreadPump ProcessDeviceWorkItems (D3DX11core.h)
description: Observação A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Define itens de trabalho para o dispositivo depois que eles terminam de carregar e processar.
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- Método ProcessDeviceWorkItems Direct3D 11
- Método ProcessDeviceWorkItems Direct3D 11 , interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11 , método ProcessDeviceWorkItems
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
ms.openlocfilehash: 07a6918e9ecea9d66c3ebca034628387ea471e9173b4b14f24e9b7f866897325
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608666"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a>Método ID3DX11ThreadPump::P rocessDeviceWorkItems

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Define itens de trabalho para o dispositivo depois que eles terminam de carregar e processar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iWorkItemCount* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O número de itens de trabalho a definir para o dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Quando a bomba de thread terminar de carregar e processar um recurso ou sombreador, ela o manterá em uma fila até que essa API seja chamada, momento em que os itens processados serão definidos para o dispositivo. Isso é útil para controlar a quantidade de processamento gasto na associação de recursos ao dispositivo para cada quadro.

Como exemplo de como alguém pode usar essa API, digamos que você está se aproximando do final de um nível em seu jogo e deseja começar a pré-carregar as texturas, sombreadores e outros recursos para o próximo nível. A bomba de thread começará a carregar, descompactar e processar os recursos e sombreadores em um thread separado até que eles estão prontos para serem definidos para o dispositivo, momento em que ele os deixará em uma fila. Talvez não seja melhor definir todos os recursos e sombreadores para o dispositivo de uma só vez, pois isso pode causar uma lentidão temporária perceptível no desempenho do jogo. Portanto, essa API pode ser chamada uma vez por quadro para que apenas um número pequeno de itens de trabalho seja definido para o dispositivo em cada quadro, spreading da carga de trabalho de recursos de associação para o dispositivo em vários quadros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

