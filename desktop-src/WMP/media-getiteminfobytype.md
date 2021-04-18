---
title: Método Media. getItemInfoByType
description: O método getItemInfoByType recupera o valor do atributo correspondente ao nome do atributo, idioma e índice especificados.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- método getItemInfoByType Windows Media Player
- método getItemInfoByType Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método getItemInfoByType
topic_type:
- apiref
api_name:
- Media.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2aff2bee7641075bbac1dd04526ee751ea077a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813477"
---
# <a name="mediagetiteminfobytype-method"></a>Método Media. getItemInfoByType

O método **getItemInfoByType** recupera o valor do atributo correspondente ao nome do atributo, idioma e índice especificados.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Media.getItemInfoByType(
  name,
  language,
  index
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

</dd> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) que contém o índice de base zero do valor a ser recuperado do atributo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um **número**, uma **cadeia de caracteres**, um objeto **MetadataPicture** ou um objeto **MetadataText** , conforme indicado na tabela a seguir.



| Atributo                   | Retornar valor                   |
|-----------------------------|--------------------------------|
| **Sincronizarstate**               | **Número** (**longo sem sinal**) |
| **WM/letras de música \_ sincronizadas** | Objeto **MetadataText**        |
| **WM/imagem**              | Objeto **MetadataPicture**     |
| **WM/UserWebURL**           | Objeto **MetadataText**        |
| Todos os outros atributos        | **Cadeia de caracteres**                     |



 

Para atributos cujo valor subjacente é **booliano**, esse método retorna a cadeia de caracteres "true" ou "false".

## <a name="remarks"></a>Comentários

Esse método recupera os metadados de um item de mídia digital individual ou um item de mídia que faz parte de uma lista de reprodução.

Esse método dá suporte a atributos com vários valores e atributos com valores complexos. O método **getItemInfo** não oferece suporte a atributos com vários valores e atributos com valores complexos.

A propriedade **attributeCount** contém o número de nomes de atributo disponíveis para um determinado objeto de **mídia** . Os números de índice podem ser usados com o método **GetAttributeName** para determinar o nome de cada atributo disponível. Nomes de atributo individuais podem ser passados para o parâmetro *Name* de **getItemInfoByType**.

O método **getAttributeCountByType** retorna o número de atributos que correspondem a um determinado nome de atributo para um determinado objeto de **mídia** . Os números de índice podem então ser passados para o parâmetro de *índice* de **getItemInfoByType**. Isso é útil quando um item de mídia digital é categorizado em vários gêneros, por exemplo.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

Esse método pode causar erros. Você deve incluir o código de tratamento de erros ao chamar esse método. Por exemplo, no JScript, você pode implementar o tratamento de erros usando a **tentativa... capturar... Por fim,** estrutura.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getAttributeCountByType**](media-getattributecountbytype.md)
</dt> <dt>

[**Media. GetAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Objeto MetadataPicture**](metadatapicture-object.md)
</dt> <dt>

[**Objeto MetadataText**](metadatatext-object.md)
</dt> <dt>

[**Lendo valores de atributo**](reading-attribute-values.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





