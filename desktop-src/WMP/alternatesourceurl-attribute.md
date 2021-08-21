---
title: Atributo AlternateSourceURL
description: O atributo AlternateSourceURL é um localizador de recursos uniforme para o item de mídia que serve como uma alternativa aos atributos DLNASourceURI e SourceURL.
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- Atributo AlternateSourceURL Windows Media Player
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765c7a3945224e82a0112c0f4dd7249e4340ec13e0d78adbd59039d25f234aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055234"
---
# <a name="alternatesourceurl-attribute"></a>Atributo AlternateSourceURL

O **atributo AlternateSourceURL** é um localizador de recursos uniforme para o item de mídia que serve como uma alternativa aos atributos [**DLNASourceURI**](dlnasourceuri-attribute.md) e [**SourceURL.**](sourceurl-attribute.md)

## <a name="applies-to"></a>Aplica-se A

-   [**Itens de áudio**](audio-item-attributes.md)
-   [**Itens de foto**](photo-item-attributes.md)
-   [**Itens de playlist**](playlist-attributes-ref.md)
-   [**Itens de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo não está disponível para itens de mídia na biblioteca local do usuário atual. Ele está disponível somente para itens de mídia que pertencem a uma biblioteca remota; ou seja, uma biblioteca que foi disponibilizada por outro usuário na rede base. Para determinar se uma biblioteca de mídia é remota, chame [**IWMPLibrary::get \_ type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





