---
title: Método IWMPMedia getItemInfoByAtom
description: O método getItemInfoByAtom retorna o valor do atributo com o número de índice especificado.
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- método getItemInfoByAtom Windows Media Player
- método getItemInfoByAtom Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, método getItemInfoByAtom
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfoByAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb37243960360120fbfe508a39db31e37728ac39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750734"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a>Método IWMPMedia:: getItemInfoByAtom

O método **getItemInfoByAtom** retorna o valor do atributo com o número de índice especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String getItemInfoByAtom(
  System.Int32 lAtom
);
```


```VB

Public Function getItemInfoByAtom( _
  ByVal lAtom As System.Int32 _
) As System.String
Implements IWMPMedia.getItemInfoByAtom
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lAtom* \[ no\]
</dt> <dd>

Um **System. Int32** que especifica o índice no qual o atributo solicitado reside no conjunto de atributos disponíveis.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. String** que é o valor do atributo.

## <a name="remarks"></a>Comentários

Esse método pode ser usado para recuperar metadados para um item de mídia específico usando um número de índice de atributo. A propriedade **attributeCount** pode ser usada para determinar o número de atributos disponíveis para o item de mídia.

O método **getMediaAtom** da interface **IWMPMediaCollection** também pode ser usado para recuperar o índice de um atributo específico. Essa técnica geralmente é mais eficiente do que os métodos **getItemInfo** ou **getItemInfoByType** ao trabalhar com listas de reprodução grandes.

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB e C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. setItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection. getMediaAtom (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 





