---
title: Método IWMPMediaCollection2 getByAttributeAndMediaType
description: O método getByAttributeAndMediaType retorna uma interface IWMPPlaylist que fornece acesso a itens de mídia que têm um tipo de mídia e um atributo especificado.
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- método getByAttributeAndMediaType Windows Media Player
- método getByAttributeAndMediaType Windows Media Player, interface IWMPMediaCollection2
- Interface IWMPMediaCollection2 Windows Media Player, método getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getByAttributeAndMediaType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1ee4e9421b4546cdc8ace6173dacab5034b905
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764104"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a>Método IWMPMediaCollection2:: getByAttributeAndMediaType

O `getByAttributeAndMediaType` método retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia que têm um tipo de mídia e um atributo especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPPlaylist getByAttributeAndMediaType(
  System.String bstrAttribute,
  System.String bstrValue,
  System.String bstrMediaType
);
```


```VB

Public Function getByAttributeAndMediaType( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getByAttributeAndMediaType
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrattribute* \[ no\]
</dt> <dd>

O **System. String** que é o atributo especificado.

</dd> <dt>

*bstrvalue* \[ no\]
</dt> <dd>

O **System. String** que é o valor especificado para o atributo que é especificado em *bstrattribute*.

</dd> <dt>

*bstrMediaType* \[ no\]
</dt> <dd>

O **System. String** que é o tipo de mídia especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução recuperada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMediaCollection2 (VB e C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





