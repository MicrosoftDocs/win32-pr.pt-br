---
title: Ping
description: Use o pacote ping para estabelecer uma conexão e negociar a segurança com o servidor.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- BITS de ping
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9428a39cfaebbce150583d47a344c4a36ca66
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "105753002"
---
# <a name="ping"></a>Ping

Use o pacote **ping** para estabelecer uma conexão e negociar a segurança com o servidor.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a>Cabeçalhos

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_postagem de bits
</dt> <dd>

Verbo específico do BITS que identifica esse pacote para o servidor BITS.

Substitua a URL remota pelo URI absoluto ou relativo. Normalmente, substitua a URL remota pelo nome do arquivo remoto do trabalho.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote
</dt> <dd>

Identifica esse pacote de solicitação como um pacote de ping.

</dd> </dl>

## <a name="remarks"></a>Comentários

O pacote de **ping** é opcional. Em vez de enviar um pacote **ping** , você pode usar o pacote [**Create-Session**](create-session.md) para estabelecer uma conexão e negociar a segurança. No entanto, é mais eficiente usar o pacote de **ping** para essa finalidade.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ACK para ping**](ack-for-ping.md)
</dt> <dt>

[**Criar sessão**](create-session.md)
</dt> </dl>

 

 




