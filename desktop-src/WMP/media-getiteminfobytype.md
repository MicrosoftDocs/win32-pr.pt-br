---
title: Método Media.getItemInfoByType
description: O método getItemInfoByType recupera o valor do atributo correspondente ao nome do atributo, idioma e índice especificados.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- Método getItemInfoByType Windows Media Player
- Método getItemInfoByType Windows Media Player classe , Media
- Classe de Windows Media Player de mídia , getItemInfoByType
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
ms.openlocfilehash: aa180834d70c8dd078beafc360400c931e7058994f1cc46d4e9abb011987d158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135119"
---
# <a name="mediagetiteminfobytype-method"></a>Método Media.getItemInfoByType

O **método getItemInfoByType** recupera o valor do atributo correspondente ao nome do atributo, idioma e índice especificados.

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

*name* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que contém o nome do atributo. Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a Referência Windows Media Player [atributo de referência.](attribute-reference.md)

</dd> <dt>

*idioma* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que representa o idioma. Se o valor for definido como nulo ou "" (cadeia de caracteres vazia), a cadeia de caracteres de localidade atual será usada. Caso contrário, o valor deverá ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-us".

</dd> <dt>

*índice* \[ Em\]
</dt> <dd>

**Number** (**long**) que contém o índice baseado em zero do valor a ser recuperado do atributo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **objeto Number**, **String**, **MetadataPicture** ou **objeto MetadataText,** conforme indicado na tabela a seguir.



| Atributo                   | Valor retornado                   |
|-----------------------------|--------------------------------|
| **SyncState**               | **Number** (**unsigned long**) |
| **\_WM/Synchronizado** | **Objeto MetadataText**        |
| **WM/Picture**              | **Objeto MetadataPicture**     |
| **WM/UserWebURL**           | **Objeto MetadataText**        |
| Todos os outros atributos        | **Cadeia de caracteres**                     |



 

Para atributos cujo valor subjacente é **booliana,** esse método retorna a cadeia de caracteres "true" ou "false".

## <a name="remarks"></a>Comentários

Esse método recupera os metadados para um item de mídia digital individual ou um item de mídia que faz parte de uma playlist.

Esse método dá suporte a atributos com vários valores e atributos com valores complexos. O **método getItemInfo** não dá suporte a atributos com vários valores e atributos com valores complexos.

A **propriedade attributeCount** contém o número de nomes de atributo disponíveis para um determinado **objeto Media.** Os números de índice podem ser usados com o **método getAttributeName** para determinar o nome de cada atributo disponível. Nomes de atributo individuais podem ser passados para *o parâmetro name* de **getItemInfoByType**.

O **método getAttributeCountByType** retorna o número de atributos que correspondem a um nome de atributo específico para um determinado **objeto Media.** Os números de índice podem ser passados para o *parâmetro de* índice **de getItemInfoByType**. Isso é útil quando um item de mídia digital foi categorizado em vários gêneros, por exemplo.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

Esse método pode causar erros. Você deve incluir o código de tratamento de erros ao chamar esse método. Por exemplo, no JScript você pode implementar o tratamento de erro usando **o try... Pegar... finalmente** estrutura.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player Série 9 ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Media.attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media.getAttributeCountByType**](media-getattributecountbytype.md)
</dt> <dt>

[**Media.getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Objeto MetadataPicture**](metadatapicture-object.md)
</dt> <dt>

[**Objeto MetadataText**](metadatatext-object.md)
</dt> <dt>

[**Lendo valores de atributo**](reading-attribute-values.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





