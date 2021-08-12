---
description: De definir itens de trabalho para o dispositivo depois que eles terminarem de carregar e processar.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: Método ID3DX10ThreadPump::P rocessDeviceWorkItems (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.ProcessDeviceWorkItems
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e7179cf285c056601d00df5126ba98aaa34f827cbcac15400166d8301dc143a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118301772"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a>Método ID3DX10ThreadPump::P rocessDeviceWorkItems

De definir itens de trabalho para o dispositivo depois que eles terminarem de carregar e processar. Quando a bomba de thread terminar de carregar e processar um recurso ou sombreador, ela o manterá em uma fila até que essa API seja chamada, momento em que os itens processados serão definidos para o dispositivo. Isso é útil para controlar a quantidade de processamento gasto na associação de recursos ao dispositivo para cada quadro. Consulte Observações.

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

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O número de itens de trabalho a definir para o dispositivo. ProcessDeviceObjectCreation criará no máximo objetos iWorkItemCount. Se não houver itens de trabalho suficientes na fila para processar objetos iWorkItemCount, ProcessDeviceObjectCreation criará tantos objetos de dispositivo quanto itens na fila.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Como exemplo de como alguém pode usar essa API, digamos que você está se aproximando do final de um nível em seu jogo e deseja começar a pré-carregar as texturas, sombreadores e outros recursos para o próximo nível. A bomba de thread começará a carregar, descompactar e processar os recursos e sombreadores em um thread separado até que eles estão prontos para serem definidos para o dispositivo, momento em que ele os deixará em uma fila. Talvez não seja melhor definir todos os recursos e sombreadores para o dispositivo de uma só vez, pois isso pode causar uma lentidão temporária notável no desempenho do jogo. Portanto, essa API pode ser chamada uma vez por quadro para que apenas um número pequeno de itens de trabalho seja definido para o dispositivo em cada quadro, spreading da carga de trabalho de recursos de associação para o dispositivo em vários quadros e minimizando a possibilidade de uma lentidão notável no desempenho do jogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
