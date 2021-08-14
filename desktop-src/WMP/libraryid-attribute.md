---
title: Atributo LibraryID
description: O atributo LibraryID é o identificador da biblioteca à qual o item pertence.
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- Atributo LibraryID Windows Media Player
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a011db4e18509761c232bcf5439e33445128ef77c50945f84662a7b7956f607f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468216"
---
# <a name="libraryid-attribute"></a>Atributo LibraryID

O atributo **LibraryID** é o identificador da biblioteca à qual o item pertence.

## <a name="applies-to"></a>Aplica-se A

-   [**Itens de áudio**](audio-item-attributes.md)
-   [**Itens de foto**](photo-item-attributes.md)
-   [**Itens da lista de reprodução**](playlist-attributes-ref.md)
-   [**Itens de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Um item de mídia pode pertencer à biblioteca local do usuário atual ou pode pertencer a uma biblioteca que foi disponibilizada por outro usuário na rede doméstica ou na Internet.

O valor desse atributo é o mesmo que o valor retornado pelo método [**IWMPLibrary2:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





