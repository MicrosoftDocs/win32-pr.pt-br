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
ms.openlocfilehash: 07e5383de75fef1a0e1957f270a8a5238951bce4ede1418dbf79ba2038777372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997166"
---
# <a name="dlnasourceuri-attribute"></a>Atributo DLNASourceURI

O **atributo DLNASourceURI** é o URI (identificador de recurso universal) do item.

## <a name="applies-to"></a>Aplica-se A

-   [**Itens de áudio**](audio-item-attributes.md)
-   [**Outros itens**](other-item-attributes.md)
-   [**Itens de foto**](photo-item-attributes.md)
-   [**Itens de playlist**](playlist-attributes-ref.md)
-   [**Itens de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Se o item estiver na biblioteca local do usuário atual, esse atributo, o atributo [**SourceURL**](sourceurl-attribute.md) e o valor retornado por [**IWMPMedia::get \_ sourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) serão os mesmos.

Se o item não estiver na biblioteca local do usuário atual, mas pertencer a uma biblioteca remota, esse atributo será um identificador do formato dlna-playsingle://*xxx*.

Você pode passar um URI dlna-playsingle para o método [**IWMPCore3::newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) para obter uma interface [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) que permite exibir os metadados do item de mídia e, potencialmente, editar a classificação em estrela do item de mídia. Observe, no entanto, que o URI dlna-playsingle deve ser para um CDS (serviço de diretório de conteúdo) que Windows Media Player já tenha descoberto. O **novo métodoMedia** não iniciará a descoberta de UPnP e pesquisa o CDS.

Você só poderá editar a classificação em estrela de um item de mídia em uma biblioteca remota se a biblioteca remota for compatível com a operação de edição. As bibliotecas remotas hospedadas em um computador que executa Windows 7 são suportadas pela operação de edição. As bibliotecas remotas hospedadas em um computador que executa um Windows operacional anterior ao Windows 7 não são suportadas pela operação de edição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





