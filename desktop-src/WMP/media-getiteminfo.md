---
title: Método Media. getItemInfo
description: O método getItemInfo recupera o valor do atributo especificado para o item de mídia atual.
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- Windows Media Player do método getItemInfo
- método getItemInfo Windows Media Player, classe Media
- classe de mídia Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- Media.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab885a8505f3637d21f4a406e5a7c324ee6b9ec90e5ad0434a385e321072ccaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135149"
---
# <a name="mediagetiteminfo-method"></a>Método Media. getItemInfo

O método **getItemInfo** recupera o valor do atributo especificado para o item de mídia atual.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome do atributo. para obter informações sobre os atributos com suporte pelo Windows Media Player, consulte a [referência de atributo](attribute-reference.md)Windows Media Player.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna uma **cadeia de caracteres** que representa o valor do atributo especificado. Para atributos cujo valor subjacente é **booliano**, ele retorna a cadeia de caracteres "true" ou "false".

## <a name="remarks"></a>Comentários

Esse método recupera os metadados de um item de mídia digital individual ou um item de mídia que faz parte de uma lista de reprodução.

A propriedade **attributeCount** contém o número de nomes de atributo disponíveis para um determinado objeto de **mídia** . Os números de índice podem ser usados com o método **GetAttributeName** para determinar o nome de cada atributo disponível. Nomes de atributo individuais podem ser passados para **getItemInfo**.

Para recuperar atributos com vários valores e atributos com valores complexos, use o método **getItemInfoByType** .

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

para compartilhar as bibliotecas de mídia Windows sobre UPnP, Windows Media Player cria um serviço de diretório de conteúdo (CDS) que é exposto por upnp. Outros dispositivos podem, então, navegar e navegar pelas bibliotecas.

no Windows 7, um aplicativo pode usar os atributos Windows Media Player [**trackingid**](trackingid-attribute.md) e [**MediaType**](mediatype-attribute.md) para construir a ID de objeto de cada item no CDS. Observe que essa construção pode ser alterada em versões futuras do Windows. O aplicativo passa cada uma dessas cadeias de caracteres de atributo no parâmetro *Name* em uma chamada para **getItemInfo**. **getItemInfo** retorna o valor para cada atributo no valor de retorno. O aplicativo usa a seguinte sintaxe para construir cada ID de objeto:

*TrackingID*. 0. *Mediatypeid*

Essa sintaxe tem o seguinte significado:

-   *trackingid* é a cadeia de caracteres que é armazenada no atributo Windows Media Player [**trackingid**](trackingid-attribute.md) do item de mídia.
-   *Mediatypeid* depende do valor do atributo [**MediaType**](mediatype-attribute.md) , conforme mostrado na tabela a seguir:

    | Atributo MediaType                      | MediaTypeid |
    |------------------------------------------|-------------|
    | [Itens de áudio](audio-item-attributes.md) | 4           |
    | [Itens de foto](photo-item-attributes.md) | B           |
    | [Itens de vídeo](video-item-attributes.md) | 8           |

    

     

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

[**Media. GetAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Lendo valores de atributo**](reading-attribute-values.md)
</dt> <dt>

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





