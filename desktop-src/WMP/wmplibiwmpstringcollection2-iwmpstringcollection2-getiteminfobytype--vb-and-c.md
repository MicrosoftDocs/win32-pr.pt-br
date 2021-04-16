---
title: Método IWMPStringCollection2 getItemInfobyType
description: O método getItemInfoByType retorna o valor correspondente ao índice, nome, idioma e índice de atributo do item de coleção de cadeia de caracteres especificado.
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- método getItemInfobyType Windows Media Player
- método getItemInfobyType Windows Media Player, interface IWMPStringCollection2
- Interface IWMPStringCollection2 Windows Media Player, método getItemInfobyType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfobyType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e227d6471ecf41c8f48420ded61c6f4e7eaac8cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765276"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a>Método IWMPStringCollection2:: getItemInfobyType

O método **getItemInfoByType** retorna o valor correspondente ao índice, nome, idioma e índice de atributo do item de coleção de cadeia de caracteres especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Object getItemInfobyType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lAttributeIndex
);
```


```VB

Public Function getItemInfobyType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lAttributeIndex As System.Int32 _
) As System.Object
Implements IWMPStringCollection2.getItemInfobyType
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lCollectionIndex* \[ no\]
</dt> <dd>

O **System. Int32** que é o índice de base zero do item de coleção de cadeia de caracteres a partir do qual obter o atributo.

</dd> <dt>

*bstrtype* \[ no\]
</dt> <dd>

O **System. String** que é o nome do atributo.

</dd> <dt>

*bstrLanguage* \[ no\]
</dt> <dd>

O **System. String** que indica o idioma. Se o valor for definido como NULL ou para uma cadeia de caracteres de comprimento zero (""), a cadeia de caracteres de localidade atual será usada. Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".

</dd> <dt>

*lAttributeIndex* \[ no\]
</dt> <dd>

Um **System. Int32** que é o índice de base zero do atributo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. Object** que é o item de coleção de cadeia de caracteres.

## <a name="remarks"></a>Comentários

Esse método dá suporte a atributos com vários valores e atributos com valores complexos. O método **getItemInfo** não oferece suporte a atributos com vários valores ou atributos com valores complexos.

Ao passar o valor "childList" no parâmetro *bstrtype* , você pode recuperar uma nova coleção de cadeias de caracteres que contém os filhos de um dos itens na coleção de cadeias de caracteres pai. Por exemplo, se a coleção pai contiver uma lista de AlbumIDs, você poderá usar esse método para obter uma coleção de cadeia de caracteres filho que contém todas as faixas de um dos álbuns. Essa abordagem é mais rápida e mais eficiente do que chamar o método **IWMPMediaCollection2. getStringCollectionByQuery** duas vezes; uma vez para obter uma coleção de AlbumIDs e uma segunda vez para obter uma coleção de faixas para um albumid específico. Para usar filha na maneira descrita anteriormente, a coleção de cadeias de caracteres pai deve ser Obtida de uma coleção de mídia por meio de **IWMPLibraryServices**, e não usando a propriedade **AxWindowsMediaPlayer. mediacollection** .

Ao usar Filhalist, passe o valor "childList" no parâmetro *bstrtype* e o valor 0 no parâmetro *lAttributeIndex* . Em seguida, você pode converter o objeto que é retornado para uma interface **IWMPStringCollection2** para acessar a lista filho.

Para usar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributo albumid**](albumid-attribute.md)
</dt> <dt>

[**Interface IWMPLibraryServices (VB e C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getStringCollectionByQuery (VB e C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**Interface IWMPStringCollection2**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getItemInfo (VB e C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





