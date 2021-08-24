---
title: Fragmento
description: Use o pacote Fragment para enviar um fragmento do arquivo de upload para o servidor.
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
ms.openlocfilehash: 613acaabc017b9e673d2cba6a64f84db054a4cdc0d73a0639fcf8455edff8298
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528826"
---
# <a name="fragment"></a>Fragmento

Use o **pacote** Fragment para enviar um fragmento do arquivo de upload para o servidor.

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

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

Verbo específico de BITS que identifica esse pacote para o servidor BITS.

Substitua REMOTE-URL pelo URI absoluto ou relativo. Normalmente, substitua REMOTE-URL pelo nome de arquivo remoto do trabalho. Para considerações sobre balanceamento de carga de rede, consulte o header BITS-Host-Id no [**pacote Create-Session.**](create-session.md)

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Packet-Type
</dt> <dd>

Identifica esse pacote de solicitação como um pacote fragmentado.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

GUID de cadeia de caracteres que identifica a sessão para o servidor. Substitua {guid} pelo identificador de sessão que o servidor retorna no pacote de resposta [**Ack for Create-Session.**](ack-for-create-session.md)

</dd> <dt>

<span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Nome do conteúdo
</dt> <dd>

Especifique esse header somente com o fragmento inicial. Substitua filename pelo nome do arquivo local do trabalho. O nome não inclui o caminho.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Comprimento do conteúdo
</dt> <dd>

Substitua length pelo número de bytes enviados no corpo do fragmento.

</dd> <dt>

<span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Intervalo de conteúdo
</dt> <dd>

Informa ao servidor onde aplicar o intervalo no arquivo de destino. Substitua o intervalo pelas deslocamentos inicial e final do intervalo no arquivo de destino. Os deslocamentos são baseados em zero. Se o intervalo determinado se sobrepor a um intervalo existente, o BITS grava apenas a parte não sobreposta do intervalo; BITS não substitui o conteúdo existente. Por exemplo, se o primeiro pacote contiver o intervalo de 0 a 100 e o segundo pacote contiver o intervalo de 50 a 150, o BITS grava apenas bytes de 101 a 150 do segundo pacote. Substitua o comprimento total pelo número total de bytes no arquivo.

</dd> <dt>

<span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Codificação de conteúdo
</dt> <dd>

Substitua a codificação pelo tipo de codificação que o cliente usa no fragmento. O cliente deve usar a codificação que o servidor identifica no Accept-Encoding do pacote de resposta [**Ack for Create-Session.**](ack-for-create-session.md) O servidor usa o tipo de codificação para decodificar o fragmento. Todos os fragmentos devem especificar a mesma codificação.

Não envie esse header se o tipo de codificação for Identity. O servidor BITS dá suporte apenas à codificação identity.

</dd> </dl>

## <a name="remarks"></a>Comentários

O fragmento é um intervalo de bytes enviados no corpo do pacote. O cliente envia os fragmentos em ordem sequencial começando com o deslocamento zero; o servidor não mantém o controle de intervalos não contíguos. Se o cliente enviar intervalos não contíguos, o servidor retornará um código de retorno HTTP 416 (intervalo não satisfizável) na resposta [**Ack for Fragment.**](ack-for-fragment.md)

Os cabeçalhos *Content-xxxx* são cabeçalhos HTTP 1.1 padrão. Para obter mais detalhes sobre os headers *Content-xxxx,* consulte a [especificação RFC 2616.](https://www.ietf.org/rfc/rfc2616.txt)

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Ack for Fragment**](ack-for-fragment.md)
</dt> <dt>

[**Fechar sessão**](close-session.md)
</dt> <dt>

[**Criar sessão**](create-session.md)
</dt> </dl>

 

 




