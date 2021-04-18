---
title: Método de item IWMPStringCollection
description: O método Item retorna a cadeia de caracteres no índice especificado.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Método de item Windows Media Player
- Método de item Windows Media Player, interface IWMPStringCollection
- Interface IWMPStringCollection do Windows Media Player, método de item
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
ms.openlocfilehash: f69bdc63448699a595238b9907f4b1253209ad06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784675"
---
# <a name="iwmpstringcollectionitem-method"></a>Método IWMPStringCollection:: item

O método **Item** retorna a cadeia de caracteres no índice especificado.

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

*Lindex* \[ no\]
</dt> <dd>

Um **System. Int32** que é o índice.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. String** que é a cadeia de caracteres no índice especificado.

## <a name="remarks"></a>Comentários

A interface **IWMPStringCollection** é usada para recuperar o conjunto de valores disponíveis para um atributo. Por exemplo, o método **IWMPMediaCollection. getAttributeStringCollection** pode ser usado para recuperar uma interface **IWMPStringCollection** representando todos os valores para o atributo gênero dentro do tipo de mídia de áudio. O método **Item** pode então ser usado para iterar por todos os valores possíveis para o atributo gênero.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMPMediaCollection. getAttributeStringCollection (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[**Interface IWMPStringCollection (VB e C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





