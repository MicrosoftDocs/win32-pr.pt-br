---
title: Atributo LibraryName
description: O atributo LibraryName é o nome da biblioteca à qual o item pertence.
ms.assetid: 70ce2de1-6c7b-427a-ba48-a9f69bacd015
keywords:
- Atributo LibraryName do Windows Media Player
topic_type:
- apiref
api_name:
- LibraryName
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 263023c9881e109efe77ec30c1e37091200c051b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781221"
---
# <a name="libraryname-attribute"></a>Atributo LibraryName

O atributo LibraryName é o nome da biblioteca à qual o item pertence.

## <a name="applies-to"></a>Aplica-se A

-   [**Itens de áudio**](audio-item-attributes.md)
-   [**Itens de foto**](photo-item-attributes.md)
-   [**Itens da lista de reprodução**](playlist-attributes-ref.md)
-   [**Itens de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Um item de mídia pode pertencer à biblioteca local do usuário atual ou pode pertencer a uma biblioteca que foi disponibilizada por outro usuário em uma rede doméstica.

O valor desse atributo é o mesmo que o valor retornado pelo método [**IWMPLibrary:: get \_ Name**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





