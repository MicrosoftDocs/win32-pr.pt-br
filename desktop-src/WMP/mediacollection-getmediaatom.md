---
title: Método mediacollection. getMediaAtom
description: O método getMediaAtom recupera o índice no qual um atributo especificado reside dentro do conjunto de atributos disponíveis.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- Windows Media Player do método getMediaAtom
- método getMediaAtom Windows Media Player, classe mediacollection
- classe mediacollection Windows Media Player, método getMediaAtom
topic_type:
- apiref
api_name:
- MediaCollection.getMediaAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f537b759516d5fa0f382d0c72aabbc0edb836ad8e4ae6d7f210d012fa19ea60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837199"
---
# <a name="mediacollectiongetmediaatom-method"></a>Método mediacollection. getMediaAtom

O método **getMediaAtom** recupera o índice no qual um atributo especificado reside dentro do conjunto de atributos disponíveis.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*atributo* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome do atributo. para obter informações sobre os atributos com suporte pelo Windows Media Player, consulte a [referência de atributo](attribute-reference.md)Windows Media Player.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **número** (**longo**).

## <a name="remarks"></a>Comentários

O número de índice recuperado com esse método pode ser passado para a *mídia*. método **getItemInfoByAtom** para acessar valores de atributo. Essa técnica é geralmente mais eficiente ao trabalhar com listas de reprodução grandes do que acessar um valor de atributo por nome por meio de *mídia*. **getItemInfo** ou *mídia*. **getItemInfoByType**.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. getItemInfoByAtom**](media-getiteminfobyatom.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





