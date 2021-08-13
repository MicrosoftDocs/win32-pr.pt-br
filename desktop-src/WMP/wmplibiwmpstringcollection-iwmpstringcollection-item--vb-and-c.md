---
title: Método item IWMPStringCollection
description: O método Item retorna a cadeia de caracteres no índice especificado.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Método item Windows Media Player
- Método de Windows Media Player item , interface IWMPStringCollection
- Interface IWMPStringCollection Windows Media Player método , Item
topic_type:
- apiref
api_name:
- IWMPStringCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47928502dce9ed4deb12461763a499de5d962aa1303b4c9cc5eacb02c7619da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568416"
---
# <a name="iwmpstringcollectionitem-method"></a>Método IWMPStringCollection::Item

O **método Item** retorna a cadeia de caracteres no índice especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPStringCollection.Item
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lIndex* \[ Em\]
</dt> <dd>

Um **System.Int32** que é o índice.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um **System.String** que é a cadeia de caracteres no índice especificado.

## <a name="remarks"></a>Comentários

A interface **IWMPStringCollection** é usada para recuperar o conjunto de valores disponíveis para um atributo. Por exemplo, o método **IWMPMediaCollection.getAttributeStringCollection** pode ser usado para recuperar uma interface **IWMPStringCollection** que representa todos os valores para o atributo Genre no tipo de mídia Audio. O **método Item** pode ser usado para iterar por todos os valores possíveis para o atributo Gênero.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMPMediaCollection.getAttributeStringCollection (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[**Interface IWMPStringCollection (VB e C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





