---
title: Close-Session
description: Use o pacote Close-Session para informar ao servidor BITS que o carregamento do arquivo foi concluído e para encerrar a sessão.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- BITS DE Close-Session
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ae1318a99e690b13f4f0cad03624fb351c359efbcb1be9e105076ce53ceba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021194"
---
# <a name="close-session"></a>Close-Session

Use o pacote de **sessão de fechamento** para informar ao servidor bits que o carregamento do arquivo foi concluído e para encerrar a sessão.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
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

Identifica esse pacote de solicitação como um pacote Close-Session.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-ID da sessão
</dt> <dd>

GUID de cadeia de caracteres que identifica a sessão para o servidor. Substitua {GUID} pelo identificador de sessão que o servidor retorna no pacote [**ACK para a resposta de Create-Session**](ack-for-create-session.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

O servidor BITS libera todos os recursos e exclui todos os arquivos temporários quando recebe esse pacote.

Para trabalhos de resposta de upload, você deve baixar a resposta antes de enviar a **sessão de fechamento**. Caso contrário, a resposta será perdida.

Se você enviar esse pacote antes de carregar todos os fragmentos, o arquivo de carregamento será excluído; Não é possível carregar um arquivo parcial.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ACK para fechamento de sessão**](ack-for-close-session.md)
</dt> <dt>

[**Cancelar sessão**](cancel-session.md)
</dt> <dt>

[**Criar sessão**](create-session.md)
</dt> </dl>

 

 




