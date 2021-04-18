---
title: Método IWMPMedia getItemInfo
description: O método getItemInfo retorna o valor do atributo especificado para o item de mídia.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- método getItemInfo Windows Media Player
- método getItemInfo Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523e57e68d13df55395cd4deca6e09904723bbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757058"
---
# <a name="iwmpmediagetiteminfo-method"></a>Método IWMPMedia:: getItemInfo

O método **getItemInfo** retorna o valor do atributo especificado para o item de mídia.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrItemName* \[ no\]
</dt> <dd>

Um **System. String** que é o nome do atributo. Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. String** que é o valor do atributo especificado.

## <a name="remarks"></a>Comentários

Esse método retorna os metadados para um item de mídia individual ou um item de mídia que faz parte de uma lista de reprodução.

A propriedade **attributeCount** Obtém o número de nomes de atributo disponíveis para um determinado item de mídia. Os números de índice podem ser usados com o método **GetAttributeName** para determinar o nome de cada atributo disponível. Nomes de atributo individuais podem ser passados para **getItemInfo**.

Para recuperar atributos com vários valores e atributos com valores complexos, use o método **getItemInfoByType** .

Se o item de mídia vier de uma biblioteca que foi recuperada chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o conjunto de atributos disponíveis será diferente daqueles que podem ser consultados a partir da biblioteca local recuperada chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md). Por exemplo, os atributos disponíveis da biblioteca local recuperados usando **IWMPLibrary** serão um subconjunto dos atributos disponíveis na biblioteca local recuperada usando **IWMPCore**. O conjunto de atributos disponíveis de outras fontes (bibliotecas remotas, dispositivos portáteis ou CDs) é definido pelas outras fontes.

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB e C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. GetAttributeName (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. setItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





