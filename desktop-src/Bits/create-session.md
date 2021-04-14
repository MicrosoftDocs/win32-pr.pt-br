---
title: Create-Session
description: Use o pacote Create-Session para solicitar uma sessão de carregamento com o servidor BITS.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- BITS DE Create-Session
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425ad3bd36305f94547cf2cd8b13c1a420491499
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104453750"
---
# <a name="create-session"></a>Create-Session

Use o pacote **Create-Session** para solicitar uma sessão de carregamento com o servidor bits.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a>Cabeçalhos

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_postagem de bits
</dt> <dd>

Verbo específico do BITS que identifica esse pacote para o servidor BITS.

Substitua a URL remota pelo URI absoluto ou relativo. Normalmente, substitua a URL remota pelo nome do arquivo remoto do trabalho. Para obter considerações sobre balanceamento de carga de rede, consulte o cabeçalho BITS-host-ID.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote
</dt> <dd>

Identifica esse pacote de solicitação como um pacote Create-Session.

</dd> <dt>

<span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-com suporte-protocolos
</dt> <dd>

Lista delimitada por espaço dos protocolos aos quais o cliente dá suporte. Use GUIDs de cadeia de caracteres para identificar os protocolos. Especifique a lista em ordem de preferência do mais para o menos preferível. A tabela a seguir lista o protocolo ao qual o cliente BITS dá suporte. Substituir {guid1}... {guidn} com um ou mais GUIDs de cadeia de caracteres da lista.



| Protocolo                                          | Descrição                         |
|---------------------------------------------------|-------------------------------------|
| {7df0354d-249b-430f-820d-3d2a9bef4931}<br/> | Protocolo de upload BITS 1,5<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve enviar um pacote de [**ping**](ping.md) para estabelecer uma conexão http antes de enviar o pacote de Create-Session. O pacote de Create-Session também pode estabelecer a conexão; no entanto, o pacote de Create-Session é menos eficiente.

O servidor seleciona o protocolo que deseja usar na lista que o cliente fornece no cabeçalho BITS-supported-Protocols. O servidor retorna o protocolo selecionado no cabeçalho de BITS-Protocol do [**ACK para o pacote de resposta de Create-Session**](ack-for-create-session.md) .

O cliente espera que o servidor retorne um [**ACK para o pacote de resposta de Create-Session**](ack-for-create-session.md) . Se o servidor foi capaz de estabelecer uma sessão, o cliente usa o pacote de solicitação de [**fragmento**](fragment.md) para enviar intervalos do arquivo para o servidor.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ACK para Create-Session**](ack-for-create-session.md)
</dt> <dt>

[**Fragmento**](fragment.md)
</dt> <dt>

[**Executar**](ping.md)
</dt> </dl>

 

 





