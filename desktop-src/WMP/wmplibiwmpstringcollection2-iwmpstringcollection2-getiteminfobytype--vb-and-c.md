---
title: Método IWMPStringCollection2 getItemInfobyType
description: O método getItemInfoByType retorna o valor correspondente ao índice, o nome, o idioma e o índice de atributo da coleção de cadeias de caracteres especificados.
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- Método getItemInfobyType Windows Media Player
- Método getItemInfobyType Windows Media Player interface , IWMPStringCollection2
- Interface IWMPStringCollection2 Windows Media Player , método getItemInfobyType
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
ms.openlocfilehash: cc2894faedc8e2573fad5beaa7744216fbb53fbd1b090e4be2122a3194827f43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899756"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a>Método IWMPStringCollection2::getItemInfobyType

O **método getItemInfoByType** retorna o valor correspondente ao índice, o nome, o idioma e o índice de atributo da coleção de cadeias de caracteres especificados.

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

*lCollectionIndex* \[ Em\]
</dt> <dd>

O **System.Int32 que** é o índice baseado em zero do item de coleção de cadeias de caracteres do qual obter o atributo.

</dd> <dt>

*bstrType* \[ Em\]
</dt> <dd>

O **System.String** que é o nome do atributo.

</dd> <dt>

*bstrLanguage* \[ Em\]
</dt> <dd>

O **System.String** que indica o idioma. Se o valor for definido como nulo ou como uma cadeia de caracteres de comprimento zero (""), a cadeia de caracteres de localidade atual será usada. Caso contrário, o valor deverá ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-us".

</dd> <dt>

*lAttributeIndex* \[ Em\]
</dt> <dd>

Um **System.Int32** que é o índice baseado em zero do atributo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um **System.Object que é** o item de coleção de cadeias de caracteres.

## <a name="remarks"></a>Comentários

Esse método dá suporte a atributos com vários valores e atributos com valores complexos. O **método getItemInfo** não dá suporte a atributos com vários valores ou atributos com valores complexos.

Ao passar o valor "ChildList" no parâmetro *bstrType,* você pode recuperar uma nova coleção de cadeias de caracteres que contém os filhos de um dos itens na coleção de cadeias de caracteres pai. Por exemplo, se a coleção pai contiver uma lista de AlbumIDs, você poderá usar esse método para obter uma coleção de cadeias de caracteres filho que contém todas as faixas de um dos álbums. Essa abordagem é mais rápida e eficiente do que chamar o método **IWMPMediaCollection2.getStringCollectionByQuery** duas vezes; uma vez para obter uma coleção de AlbumIDs e uma segunda vez para obter uma coleção de faixas para um Determinado AlbumID. Para usar ChildList da maneira descrita, a coleção de cadeias de caracteres pai deve ser obtida de uma coleção de mídias por meio de **IWMPLibraryServices** e não usando a propriedade **AxWindowsMediaPlayer.mediaCollection.**

Ao usar ChildList, passe o valor "ChildList" no parâmetro *bstrType* e o valor 0 no *parâmetro lAttributeIndex.* Em seguida, você pode castar o objeto que é retornado para uma interface **IWMPStringCollection2** para acessar a lista filho.

Para usar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributo AlbumID**](albumid-attribute.md)
</dt> <dt>

[**Interface IWMPLibraryServices (VB e C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2.getStringCollectionByQuery (VB e C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2 Interface**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2.getItemInfo (VB e C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





