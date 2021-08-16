---
title: Cancel-Session
description: Use o Cancel-Session para encerrar a sessão de upload com o servidor BITS.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Cancel-Session BITS
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d570a49d1a5ba632fbbb453b6397338af70d29b0dc837db12193d2889c867eaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835105"
---
# <a name="cancel-session"></a>Cancel-Session

Use o **pacote Cancelar Sessão** para encerrar a sessão de upload com o servidor BITS.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
BITS-Session-Id: {guid}
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

Identifica esse pacote de solicitação como um Cancel-Session de solicitação.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

GUID de cadeia de caracteres que identifica a sessão para o servidor. Substitua {guid} pelo identificador de sessão que o servidor retorna no pacote de resposta [**Ack for Create-Session.**](ack-for-create-session.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse pacote cancelará um trabalho de upload se ele for enviado antes do último fragmento ser enviado. Cancel-Session tem nenhum efeito em um arquivo cujo último fragmento já foi enviado. Quando o servidor BITS recebe o último fragmento, ele grava o arquivo em seu destino final e, no caso de uma resposta de upload, posta o arquivo no aplicativo do servidor. No caso de upload-resposta, Cancel-Session pacote cancela a parte de resposta de um trabalho de upload-resposta.

O servidor BITS libera todos os recursos e exclui todos os arquivos temporários quando recebe esse pacote.

O cliente BITS envia esse pacote quando o usuário cancela o trabalho.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Ack para Create-Session**](ack-for-create-session.md)
</dt> <dt>

[**Fechar sessão**](close-session.md)
</dt> </dl>

 

 




