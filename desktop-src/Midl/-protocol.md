---
title: comutador/Protocol
description: A opção/Protocol especifica qual protocolo de conexão tem suporte no stub gerado.
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- MIDL do comutador/Protocol
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555482677afff83d9f52e06c7b8e445504d222c8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887380"
---
# <a name="protocol-switch"></a>comutador/Protocol

A opção **/Protocol** especifica qual protocolo de conexão tem suporte no stub gerado.

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span id="dce"></span><span id="DCE"></span>DCE * * * *


</dt> <dd>

O stub gerado dá suporte apenas ao protocolo DCE.

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span id="ndr64"></span><span id="NDR64"></span>ndr64****


</dt> <dd>

O stub gerado dá suporte apenas ao protocolo Microsoft NDR64.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>todos * * * *


</dt> <dd>

O stub gerado dá suporte a todos os protocolos disponíveis para um determinado ambiente.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

O RPC realiza marshaling e desempacota os dados de acordo com um protocolo de fio estrito, também chamado de sintaxe de transferência, que define a representação de transmissão de dados, como a ordem na qual os membros de dados são empacotados, o alinhamento dos dados na transmissão, informações adicionais incluídas nos dados, entre outros. O Microsoft RPC é compatível com o protocolo NDR do uso DCE (representação de dados de rede). na versão de 64 bits do Windows XP, a Microsoft apresenta um NDR64 de protocolo experimental que é otimizado para transferir dados de 64 bits. NDR64 não é compatível com versões anteriores com o protocolo DCE.

O protocolo **DCE** é compatível com a sintaxe de transferência NDR do uso DCE. Esse protocolo é otimizado para transferir dados de 32 bits.

No momento, o protocolo **ndr64** tem suporte apenas quando usado em conjunto com a opção [**/Win64**](-win64.md) . Se um cliente somente ndr64 tentar se conectar a um servidor somente DCE, ou vice-versa, a chamada será rejeitada com o RPC \_ S \_ unsupported \_ Trans \_ SYN.

A opção **All** cria um stub que pode usar qualquer protocolo disponível. Para stubs de 32 bits, o único protocolo disponível atualmente é a DCE. Para stubs de 64 bits, criados usando a opção [**/Win64**](-win64.md) , tanto o DCE quanto o NDR64 estão disponíveis.

## <a name="examples"></a>Exemplos

**MIDL/Protocol All/Win64 filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/&lt;sistema&gt;**](-system-.md)
</dt> </dl>

 

 




