---
title: Método Media.getAttributeCountByType
description: O método getAttributeCountByType recupera o número de atributos associados ao nome e ao idioma do atributo especificados.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- Método getAttributeCountByType Windows Media Player
- Método getAttributeCountByType Windows Media Player classe , Media
- Classe de Windows Media Player de mídia , método getAttributeCountByType
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
ms.openlocfilehash: 222f92a57ba9fbcd9971a5536be5f31078e2e09373fb1d168a7074911b027d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123441"
---
# <a name="mediagetattributecountbytype-method"></a>Método Media.getAttributeCountByType

O **método getAttributeCountByType** recupera o número de atributos associados ao nome e ao idioma do atributo especificados.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*name* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que contém o nome do atributo. Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a Referência Windows Media Player [atributo de referência.](attribute-reference.md)

</dd> <dt>

*idioma* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que representa o idioma. Se o valor for definido como nulo ou "" (cadeia de caracteres vazia), a cadeia de caracteres de localidade atual será usada. Caso contrário, o valor deverá ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-us".

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **Número** (**longo**) que contém a contagem de atributos.

## <a name="remarks"></a>Comentários

Esse método é usado para determinar o número de atributos correspondentes a um nome de atributo específico para um determinado **objeto Media.** Os números de índice podem ser passados para o **método getItemInfoByType.** Isso é útil, por exemplo, quando um item de mídia foi categorizado em vários gêneros.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player Série 9 ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MediaObject**](media-object.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





