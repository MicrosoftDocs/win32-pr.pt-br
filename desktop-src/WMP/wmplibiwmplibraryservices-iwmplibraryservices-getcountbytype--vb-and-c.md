---
title: Método IWMPLibraryServices getCountByType
description: O método getCountByType retorna a contagem de bibliotecas disponíveis de um tipo especificado.
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- método getCountByType Windows Media Player
- método getCountByType Windows Media Player, interface IWMPLibraryServices
- Interface IWMPLibraryServices Windows Media Player, método getCountByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbd874c06c2557102011c63ee1abb895d092656
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754585"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a>Método IWMPLibraryServices:: getCountByType

O método **getCountByType** retorna a contagem de bibliotecas disponíveis de um tipo especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Int32 getCountByType(
  WMPLibraryType wmplt
);
```


```VB

Public Function getCountByType( _
  ByVal wmplt As WMPLibraryType _
) As System.Int32
Implements IWMPLibraryServices.getCountByType
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wmplt* \[ no\]
</dt> <dd>

Um valor da enumeração **WMPLib. WMPLibraryType** que especifica o tipo de biblioteca a ser contabilizada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. Int32** que é a contagem de bibliotecas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPLibraryServices (VB e C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





