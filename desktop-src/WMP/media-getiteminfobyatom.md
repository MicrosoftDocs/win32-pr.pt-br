---
title: Método Media. getItemInfoByAtom
description: O método getItemInfoByAtom recupera o valor do atributo com o número de índice especificado.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- método getItemInfoByAtom Windows Media Player
- método getItemInfoByAtom Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método getItemInfoByAtom
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
ms.openlocfilehash: cf54d2ae177a65e1a71b5726090bba90f4ee4e5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794618"
---
# <a name="mediagetiteminfobyatom-method"></a>Método Media. getItemInfoByAtom

O método **getItemInfoByAtom** recupera o valor do atributo com o número de índice especificado.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) que especifica o índice no qual um determinado atributo reside no conjunto de atributos disponíveis.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna uma **cadeia de caracteres** que representa o valor do atributo especificado. Para atributos cujo valor subjacente é **booliano**, ele retorna a cadeia de caracteres "true" ou "false".

## <a name="remarks"></a>Comentários

Esse método pode ser usado para recuperar metadados para um item de mídia digital específico usando um número de índice de atributo. A propriedade **attributeCount** pode ser usada para determinar o número de atributos disponíveis para o item de mídia.

O método **getMediaAtom** do objeto **mediacollection** também pode ser usado para recuperar o índice de um atributo específico. Essa técnica geralmente é mais eficiente do que os métodos **getItemInfo** ou **getItemInfoByType** ao trabalhar com listas de reprodução grandes.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player..

**Windows Media Player 10 Mobile:** Os atributos de um item de mídia estão disponíveis somente durante a reprodução, a menos que sejam recuperados do item por meio da coleção de mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Mediacollection. getMediaAtom**](mediacollection-getmediaatom.md)
</dt> <dt>

[**Lendo valores de atributo**](reading-attribute-values.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





