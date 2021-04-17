---
title: Método IWMPMedia3 getItemInfoByType
description: O método getItemInfoByType retorna o valor do atributo correspondente ao tipo de atributo e ao índice especificados.
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- método getItemInfoByType Windows Media Player
- método getItemInfoByType Windows Media Player, interface IWMPMedia3
- Interface IWMPMedia3 Windows Media Player, método getItemInfoByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getItemInfoByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f37992201d5d19397724071f8c2a4b8e851aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768422"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a>Método IWMPMedia3:: getItemInfoByType

O método **getItemInfoByType** retorna o valor do atributo correspondente ao tipo de atributo e ao índice especificados.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Object getItemInfoByType(
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lIndex
);
```


```VB

Public Function getItemInfoByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lIndex As System.Int32 _
) As System.Object
Implements IWMPMedia3.getItemInfoByType
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrtype* \[ no\]
</dt> <dd>

Um **System. String** que é o tipo de atributo.

</dd> <dt>

*bstrLanguage* \[ no\]
</dt> <dd>

Um **System. String** que é o idioma. Se o valor for definido como NULL ou uma cadeia de caracteres de comprimento zero (""), a cadeia de caracteres de localidade atual será usada. Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".

</dd> <dt>

*Lindex* \[ no\]
</dt> <dd>

Um **System. Int32** que é o índice de atributo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. Object** que é o valor do atributo. O tipo para o qual converter este objeto depende do tipo do atributo.

## <a name="remarks"></a>Comentários

Esse método retorna os metadados de um item de mídia digital individual ou um item de mídia que faz parte de uma lista de reprodução.

Esse método dá suporte a atributos com vários valores e atributos com valores complexos. O método **getItemInfo** não oferece suporte a atributos com vários valores e atributos com valores complexos.

A propriedade **attributeCount** Obtém o número de nomes de atributo disponíveis para um determinado item de mídia. Os números de índice podem ser usados com o método **GetAttributeName** para determinar o nome de cada atributo disponível. Nomes de atributo individuais podem ser passados para o parâmetro *Name* de **getItemInfoByType**.

O método **getAttributeCountByType** retorna o número de atributos que correspondem a um determinado nome de atributo para um determinado item de mídia. Os números de índice podem então ser passados para o parâmetro de *índice* de **getItemInfoByType**. Isso é útil quando um item de mídia é categorizado em vários gêneros, por exemplo.

Se o item de mídia vier de uma biblioteca que foi recuperada chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o conjunto de atributos disponíveis será diferente daqueles que podem ser consultados a partir da biblioteca local recuperada chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md). Por exemplo, os atributos disponíveis da biblioteca local recuperados usando **IWMPLibrary** serão um subconjunto dos atributos disponíveis na biblioteca local recuperada usando **AxWindowsMediaPlayer**. O conjunto de atributos disponíveis de outras fontes (bibliotecas remotas, dispositivos portáteis ou CDs é definido pelas outras fontes.

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMedia3 (VB e C#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB e C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. GetAttributeName (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getAttributeCountByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 





