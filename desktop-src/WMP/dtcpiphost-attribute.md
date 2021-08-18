---
title: Atributo DTCPIPHost
description: O atributo DTCPIPHost é o nome ou o endereço Proteção de Conteúdo IP do computador ou dispositivo que deve ser contatado para Exchange o protocolo AKE para o item de mídia.
ms.assetid: 61b7d6fb-c216-49ae-811a-8ce42fdb71e4
keywords:
- Atributo DTCPIPHost Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPHost Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88eaa85b756a46b1333db2e5eabda9cbaf86a702f5ae9c8225d6f6d8928e2d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996946"
---
# <a name="dtcpiphost-attribute"></a>Atributo DTCPIPHost

O atributo **DTCPIPHost** é o nome ou o endereço IP do computador ou dispositivo que deve ser contatado para o AKE (Protocolo DTCP-IP Exchange) de Transmissão Proteção de Conteúdo Digital para o item de mídia.

## <a name="applies-to"></a>Aplica-se A

-   [**Itens de áudio**](audio-item-attributes.md)
-   [**Itens de foto**](photo-item-attributes.md)
-   [**Itens de playlist**](playlist-attributes-ref.md)
-   [**Itens de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Se esse atributo estiver disponível, o item de mídia será protegido usando DTCP-IP.

Esse atributo não está disponível para itens de mídia na biblioteca local do usuário atual. Ele está disponível somente para itens de mídia que pertencem a uma biblioteca remota; ou seja, uma biblioteca que foi disponibilizada por outro usuário na rede base. Para determinar se uma biblioteca de mídia é remota, chame [**IWMPLibrary::get \_ type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





