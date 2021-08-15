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
ms.openlocfilehash: 479e03e6e18c0ec7421bd225744c5181029fc2b2e220f35c7bae7a3b02d42b07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004886"
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

 

 




