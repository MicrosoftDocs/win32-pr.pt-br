---
title: Create-Session
description: Use o Create-Session para solicitar uma sessão de upload com o servidor BITS.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Session BITS
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639db08c5a29b09f5c32d7b0243de66f2c4dced001a1ff2afa7e74837c8d67e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021184"
---
# <a name="create-session"></a>Create-Session

Use o **pacote Create-Session** para solicitar uma sessão de upload com o servidor BITS.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a>Cabeçalhos

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

Verbo específico de BITS que identifica esse pacote para o servidor BITS.

Substitua REMOTE-URL pelo URI absoluto ou relativo. Normalmente, substitua REMOTE-URL pelo nome de arquivo remoto do trabalho. Para considerações sobre balanceamento de carga de rede, consulte o header BITS-Host-Id.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Packet-Type
</dt> <dd>

Identifica esse pacote de solicitação como um Create-Session de solicitação.

</dd> <dt>

<span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>Protocolos com suporte para BITS
</dt> <dd>

Lista delimitada por espaço dos protocolos compatíveis com o cliente. Use GUIDs de cadeia de caracteres para identificar os protocolos. Especifique a lista em ordem de preferência da maioria para a menos preferencial. A tabela a seguir lista o protocolo compatível com o cliente BITS. Substitua {guid1} ... {guidN} com um ou mais GUIDs de cadeia de caracteres da lista.



| Protocolo                                          | Descrição                         |
|---------------------------------------------------|-------------------------------------|
| {7df0354d-249b-430f-820d-3d2a9bef4931}<br/> | Protocolo de Upload BITS 1.5<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve enviar um [**pacote ping**](ping.md) para estabelecer uma conexão HTTP antes de enviar o Create-Session pacote. O Create-Session pacote também pode estabelecer a conexão; no entanto, o Create-Session pacote é menos eficiente.

O servidor seleciona o protocolo que deseja usar na lista que o cliente fornece no header BITS-Supported-Protocols. O servidor retorna o protocolo selecionado no BITS-Protocol do pacote de resposta [**Ack for Create-Session.**](ack-for-create-session.md)

O cliente espera que o servidor retorne um [**Ack para o pacote de resposta Create-Session.**](ack-for-create-session.md) Se o servidor conseguir estabelecer uma sessão, o cliente usará o pacote de solicitação [**Fragment**](fragment.md) para enviar intervalos do arquivo para o servidor.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Ack para Create-Session**](ack-for-create-session.md)
</dt> <dt>

[**Fragmento**](fragment.md)
</dt> <dt>

[**Ping**](ping.md)
</dt> </dl>

 

 





