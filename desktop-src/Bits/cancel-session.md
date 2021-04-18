---
title: Cancel-Session
description: Use o pacote Cancel-Session para encerrar a sessão de carregamento com o servidor BITS.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- BITS DE Cancel-Session
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017097bea656309aabf3d773f34152805fd6a579
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105755882"
---
# <a name="cancel-session"></a>Cancel-Session

Use o pacote **Cancel-Session** para encerrar a sessão de carregamento com o servidor bits.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a>Cabeçalhos

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_postagem de bits
</dt> <dd>

Verbo específico do BITS que identifica esse pacote para o servidor BITS.

Substitua a URL remota pelo URI absoluto ou relativo. Normalmente, substitua a URL remota pelo nome do arquivo remoto do trabalho. Para obter considerações sobre balanceamento de carga de rede, consulte o cabeçalho BITS-host-ID no pacote de [**criação de sessão**](create-session.md) .

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote
</dt> <dd>

Identifica esse pacote de solicitação como um pacote Cancel-Session.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-ID da sessão
</dt> <dd>

GUID de cadeia de caracteres que identifica a sessão para o servidor. Substitua {GUID} pelo identificador de sessão que o servidor retorna no pacote [**ACK para a resposta de Create-Session**](ack-for-create-session.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse pacote cancelará um trabalho de carregamento se ele for enviado antes que o último fragmento seja enviado. Cancel-Session não tem efeito em um arquivo cujo último fragmento já foi enviado. Quando o servidor BITS recebe o último fragmento, ele grava o arquivo em seu destino final e, no caso de um upload-reply, posta o arquivo no aplicativo do servidor. No caso de resposta de upload, o pacote de Cancel-Session cancela a parte de resposta de um trabalho de resposta de upload.

O servidor BITS libera todos os recursos e exclui todos os arquivos temporários quando recebe esse pacote.

O cliente BITS envia esse pacote quando o usuário cancela o trabalho.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ACK para Create-Session**](ack-for-create-session.md)
</dt> <dt>

[**Fechar sessão**](close-session.md)
</dt> </dl>

 

 




