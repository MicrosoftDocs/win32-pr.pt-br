---
description: Defina itens de trabalho para o dispositivo depois que eles terminarem de carregar e processar.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: 'ID3DX10ThreadPump: método rocessDeviceWorkItems de:P (D3DX10. h)'
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
ms.openlocfilehash: 88b98d68e4e0e47b2c8e7f9a2e095565c53e2561
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104092004"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a>ID3DX10ThreadPump: método rocessDeviceWorkItems de:P

Defina itens de trabalho para o dispositivo depois que eles terminarem de carregar e processar. Quando a bomba do thread terminar de carregar e processar um recurso ou sombreador, ele a manterá em uma fila até que essa API seja chamada, ponto em que os itens processados serão definidos para o dispositivo. Isso é útil para controlar a quantidade de processamento que é gasto na associação de recursos ao dispositivo para cada quadro. Consulte Observações.

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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de itens de trabalho a serem definidos para o dispositivo. ProcessDeviceObjectCreation criará no máximo objetos iWorkItemCount. Se não houver itens de trabalho suficientes na fila para processar objetos iWorkItemCount, o ProcessDeviceObjectCreation criará tantos objetos de dispositivo quantos houver itens na fila.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Como um exemplo de como é possível usar essa API, digamos que você esteja se aproximando do final de um nível em seu jogo e queira começar a carregar as texturas, os sombreadores e outros recursos para o próximo nível. A bomba de thread começará a carregar, descompactar e processar os recursos e os sombreadores em um thread separado até que eles estejam prontos para serem definidos para o dispositivo; nesse ponto, eles serão deixados em uma fila. Talvez não seja necessário definir todos os recursos e sombreadores para o dispositivo de uma só vez, pois isso pode causar uma lentidão temporária no desempenho do jogo. Portanto, essa API pode ser chamada uma vez por quadro, de forma que apenas um pequeno número de itens de trabalho seja definido para o dispositivo em cada quadro, distribuindo assim a carga de trabalho dos recursos de associação para o dispositivo em vários quadros e minimizando a possibilidade de um inatividade ser prejudicado no desempenho do jogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
