---
title: Método de item IWMPPlaylistArray
description: O método Item retorna uma interface IWMPPlaylist que representa a playlist no índice especificado.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Método de item Windows Media Player
- método de Item Windows Media Player, interface IWMPPlaylistArray
- Windows Media Player de interface IWMPPlaylistArray, método Item
topic_type:
- apiref
api_name:
- IWMPPlaylistArray.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e73614e1ef00f29d6b09d3d49e2c7e514bae807245f00f30f4d3382d8f1a2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331155"
---
# <a name="iwmpplaylistarrayitem-method"></a>Método IWMPPlaylistArray:: item

O método **Item** retorna uma interface **IWMPPlaylist** que representa a playlist no índice especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPPlaylist Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPPlaylist
Implements IWMPPlaylistArray.Item
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Lindex* \[ no\]
</dt> <dd>

Um **System. Int32** que contém o índice que identifica a lista de reprodução que o método deve recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução recuperada.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistArray (VB e C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





