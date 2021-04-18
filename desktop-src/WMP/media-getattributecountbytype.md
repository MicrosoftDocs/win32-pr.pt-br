---
title: Método Media. getAttributeCountByType
description: O método getAttributeCountByType recupera o número de atributos associados ao nome de atributo e idioma especificados.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- método getAttributeCountByType Windows Media Player
- método getAttributeCountByType Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método getAttributeCountByType
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613dca43c32322cd5e7de2b2b04605789009cbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763207"
---
# <a name="mediagetattributecountbytype-method"></a>Método Media. getAttributeCountByType

O método **getAttributeCountByType** recupera o número de atributos associados ao nome de atributo e idioma especificados.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome do atributo. Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.

</dd> <dt>

*idioma* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que representa o idioma. Se o valor for definido como nulo ou "" (cadeia de caracteres vazia), a cadeia de caracteres de localidade atual será usada. Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um **número** (**longo**) que contém a contagem de atributos.

## <a name="remarks"></a>Comentários

Esse método é usado para determinar o número de atributos que correspondem a um determinado nome de atributo para um determinado objeto de **mídia** . Os números de índice podem então ser passados para o método **getItemInfoByType** . Isso é útil, por exemplo, quando um item de mídia é categorizado em vários gêneros.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Mediaobject**](media-object.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





