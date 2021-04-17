---
title: Método IWMPMediaCollection getMediaAtom
description: O método getMediaAtom retorna o índice de um atributo especificado dentro do conjunto de atributos disponíveis.
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- método getMediaAtom Windows Media Player
- método getMediaAtom Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método getMediaAtom
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08487cf60c351ff4f8e0741209655cb78c30c3f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783803"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a>Método IWMPMediaCollection:: getMediaAtom

O `getMediaAtom` método retorna o índice de um atributo especificado dentro do conjunto de atributos disponíveis.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrItemName* \[ no\]
</dt> <dd>

O **System. String** que é o nome do item para o qual o índice deve ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O **System. Int32** que é o índice.

## <a name="remarks"></a>Comentários

O número de índice recuperado com esse método pode ser passado para o **IWMPMedia. getItemInfoByAtom** para acessar valores de atributo. Essa técnica é geralmente mais eficiente ao trabalhar com listas de reprodução grandes do que acessar um valor de atributo pelo nome por meio de **IWMPMedia. getItemInfo**.

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMPMedia. getItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfoByAtom (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





