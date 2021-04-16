---
title: Atributo DLNASourceURI
description: O atributo DLNASourceURI é o URI (identificador de recurso universal) do item.
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- Atributo DLNASourceURI Windows Media Player
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ebe21a39a67dec9356c5dd5360efb48f4ef029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789567"
---
# <a name="dlnasourceuri-attribute"></a>Atributo DLNASourceURI

O atributo **DLNASourceURI** é o URI (identificador de recurso universal) do item.

## <a name="applies-to"></a>Aplica-se A

-   [**Itens de áudio**](audio-item-attributes.md)
-   [**Outros itens**](other-item-attributes.md)
-   [**Itens de foto**](photo-item-attributes.md)
-   [**Itens da lista de reprodução**](playlist-attributes-ref.md)
-   [**Itens de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Se o item estiver na biblioteca local do usuário atual, esse atributo, o atributo [**SourceURL**](sourceurl-attribute.md) e o valor retornado por [**IWMPMedia:: get \_ SourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) serão os mesmos.

Se o item não estiver na biblioteca local do usuário atual, mas pertencer a uma biblioteca remota, esse atributo será um identificador do formato DLNA-playsingle://*xxx*.

Você pode passar um URI DLNA-playsingle para o método [**IWMPCore3:: newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) para obter uma interface [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) que permite que você exiba os metadados do item de mídia e, potencialmente, edite a classificação por estrelas do item de mídia. Observe, no entanto, que o URI DLNA-playsingle deve ser para um CDS (serviço de diretório de conteúdo) que o Windows Media Player já descobriu. O método **newMedia** não iniciará a descoberta de UPnP e pesquisará o CDs.

Você poderá editar a classificação por estrelas de um item de mídia em uma biblioteca remota somente se a biblioteca remota oferecer suporte à operação de edição. As bibliotecas remotas hospedadas em um computador que executa o Windows 7 dão suporte à operação de edição. As bibliotecas remotas hospedadas em um computador que executa um sistema operacional Windows anterior ao Windows 7 não oferecem suporte à operação de edição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





