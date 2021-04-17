---
title: Propriedade de erro IWMPMedia2
description: A Propriedade Error obterá uma interface IWMPErrorItem se o item de mídia tiver uma condição de erro.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Propriedade de erro Windows Media Player
- Propriedade de erro Windows Media Player, interface IWMPMedia2
- Interface IWMPMedia2 Windows Media Player, Propriedade Error
topic_type:
- apiref
api_name:
- IWMPMedia2.Error
- IWMPMedia2.get_Error
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2179b4604efd03574c78261575ce02311cd18a0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811778"
---
# <a name="iwmpmedia2error-property"></a>Propriedade IWMPMedia2:: Error

A propriedade **Error** obterá uma interface **IWMPErrorItem** se o item de mídia tiver uma condição de erro.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a>Valor da propriedade

Uma interface **WMPLib. IWMPErrorItem** que fornece acesso a informações sobre a condição de erro.

## <a name="remarks"></a>Comentários

Se o item de mídia não puder ser reproduzido, essa propriedade obterá uma interface **IWMPErrorItem** que contém informações sobre o problema encontrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMPErrorItem (VB e C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia2 (VB e C#)**](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





