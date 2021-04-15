---
title: Atributo DTCPIPPort
description: O atributo DTCPIPPort é o número da porta TCP (protocolo de controle de transmissão) do computador ou dispositivo que deve ser contatado para Proteção de Conteúdo o RIAR (intercâmbio de chaves autenticado) do DTCP (protocolo de Internet) para o item de mídia.
ms.assetid: 63767ec1-dd01-40c2-bf9a-6e9b8a7db7f8
keywords:
- Atributo DTCPIPPort Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPPort Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c1c6117425211c0015d218412c8a9ac0971d7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761464"
---
# <a name="dtcpipport-attribute"></a>Atributo DTCPIPPort

O atributo **DTCPIPPort** é o número da porta TCP (protocolo de controle de transmissão) do computador ou dispositivo que deve ser contatado para proteção de conteúdo o RIAR (intercâmbio de chaves autenticado) do DTCP (protocolo de Internet) para o item de mídia.

## <a name="applies-to"></a>Aplica-se A

-   [**Itens de áudio**](audio-item-attributes.md)
-   [**Itens de foto**](photo-item-attributes.md)
-   [**Itens da lista de reprodução**](playlist-attributes-ref.md)
-   [**Itens de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Se esse atributo estiver disponível, o item de mídia será protegido usando DTCP-IP.

Este atributo não está disponível para itens de mídia na biblioteca local do usuário atual. Ele está disponível somente para itens de mídia que pertencem a uma biblioteca remota; ou seja, uma biblioteca que foi disponibilizada por outro usuário na rede doméstica. Para determinar se uma biblioteca de mídia é remota, chame o [**\_ tipo IWMPLibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





