---
title: Método Media.getItemInfoByAtom
description: O método getItemInfoByAtom recupera o valor do atributo com o número de índice especificado.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- Método getItemInfoByAtom Windows Media Player
- Método getItemInfoByAtom Windows Media Player classe , Media
- Classe de mídia Windows Media Player método , getItemInfoByAtom
topic_type:
- apiref
api_name:
- Media.getItemInfoByAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26db8e87a52c0d8c8236b5e4b8b5e7325fb3bb0a995dcbd81da668ea760df660
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135129"
---
# <a name="mediagetiteminfobyatom-method"></a>Método Media.getItemInfoByAtom

O **método getItemInfoByAtom** recupera o valor do atributo com o número de índice especificado.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ Em\]
</dt> <dd>

**Number** (**long**) especificando o índice no qual um determinado atributo reside dentro do conjunto de atributos disponíveis.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna uma **Cadeia de** Caracteres que representa o valor do atributo especificado. Para atributos cujo valor subjacente é **booliana,** ele retorna a cadeia de caracteres "true" ou "false".

## <a name="remarks"></a>Comentários

Esse método pode ser usado para recuperar metadados para um item de mídia digital específico usando um número de índice de atributo. A **propriedade attributeCount** pode ser usada para determinar o número de atributos disponíveis para o item de mídia.

O **método getMediaAtom** do **objeto MediaCollection** também pode ser usado para recuperar o índice de um atributo específico. Essa técnica geralmente é mais eficiente do que os **métodos getItemInfo** ou **getItemInfoByType** ao trabalhar com playlists grandes.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a referência Windows Media Player [atributo](attribute-reference.md)..

**Windows Media Player 10 Mobile:** Os atributos de um item de mídia estão disponíveis somente durante a reprodução, a menos que sejam recuperados do item por meio da coleção de mídias.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Media.attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**MediaCollection.getMediaAtom**](mediacollection-getmediaatom.md)
</dt> <dt>

[**Lendo valores de atributo**](reading-attribute-values.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





