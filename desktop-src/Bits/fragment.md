---
title: Fragmento
description: Use o pacote de fragmento para enviar um fragmento do arquivo de upload para o servidor.
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- BITS de fragmento
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5103e90ec84a20ff4c04d9036a744919d9b1fd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104084364"
---
# <a name="fragment"></a>Fragmento

Use o pacote de **fragmento** para enviar um fragmento do arquivo de upload para o servidor.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Fragment
BITS-Session-Id: {guid}
Content-Name: filename
Content-Length: length
Content-Range: Bytes range/total-length
Content-Encoding: encoding
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

Identifica esse pacote de solicitação como um pacote de fragmento.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-ID da sessão
</dt> <dd>

GUID de cadeia de caracteres que identifica a sessão para o servidor. Substitua {GUID} pelo identificador de sessão que o servidor retorna no pacote [**ACK para a resposta de Create-Session**](ack-for-create-session.md) .

</dd> <dt>

<span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Nome-do-conteúdo
</dt> <dd>

Especifique este cabeçalho somente com o fragmento inicial. Substitua filename pelo nome do nome do arquivo local do trabalho. O nome não inclui o caminho.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Comprimento do conteúdo
</dt> <dd>

Substitua o comprimento pelo número de bytes enviados no corpo do fragmento.

</dd> <dt>

<span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Intervalo de conteúdo
</dt> <dd>

Informa ao servidor onde aplicar o intervalo no arquivo de destino. Substitua intervalo pelos deslocamentos inicial e final do intervalo no arquivo de destino. Os deslocamentos são baseados em zero. Se o intervalo especificado sobrepor um intervalo existente, o BITS gravará apenas a parte não sobreposta do intervalo; O BITS não substitui o conteúdo existente. Por exemplo, se o primeiro pacote contiver o intervalo de 0 a 100 e o segundo pacote contiver o intervalo de 50 a 150, o BITS gravará somente os bytes de 101 a 150 do segundo pacote. Substitua total-Length pelo número total de bytes no arquivo.

</dd> <dt>

<span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Codificação de conteúdo
</dt> <dd>

Substitua Encoding pelo tipo de codificação que o cliente usa no fragmento. O cliente deve usar a codificação que o servidor identifica no cabeçalho Accept-Encoding do ACK para o pacote de resposta de [**Create-Session**](ack-for-create-session.md) . O servidor usa o tipo de codificação para decodificar o fragmento. Todos os fragmentos devem especificar a mesma codificação.

Não envie esse cabeçalho se o tipo de codificação for Identity. O servidor BITS dá suporte apenas à codificação de identidade.

</dd> </dl>

## <a name="remarks"></a>Comentários

O fragmento é um intervalo de bytes enviados no corpo do pacote. O cliente envia os fragmentos em ordem sequencial começando com deslocamento zero; o servidor não mantém o controle de intervalos não contíguos. Se o cliente enviar intervalos não contíguos, o servidor retornará um código de retorno HTTP 416 (intervalo insatisfatório) no [**ACK para a resposta do fragmento**](ack-for-fragment.md) .

Os cabeçalhos content-*xxxx* são cabeçalhos HTTP 1,1 padrão. Para obter mais detalhes sobre os cabeçalhos content-*xxxx* , consulte a especificação [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Confirmação para fragmento**](ack-for-fragment.md)
</dt> <dt>

[**Fechar sessão**](close-session.md)
</dt> <dt>

[**Criar sessão**](create-session.md)
</dt> </dl>

 

 




