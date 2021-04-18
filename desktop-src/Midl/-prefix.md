---
title: comutador/prefix
description: A opção/prefix instrui o compilador MIDL a adicionar cadeias de caracteres de prefixo aos nomes de rotina de stub do cliente e/ou servidor.
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- MIDL do comutador/prefix
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79885a57f257fe2648a27fd67a014421b2c1c13a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104498899"
---
# <a name="prefix-switch"></a>comutador/prefix

A opção **/prefix** instrui o compilador MIDL a adicionar cadeias de caracteres de prefixo aos nomes de rotina de stub do cliente e/ou servidor. Isso pode ser usado para permitir que um único programa seja um cliente e um servidor da mesma interface, sem que os nomes de rotina do cliente e do servidor entrem em conflito entre si.

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span id="client"></span><span id="CLIENT"></span>cliente * * * *


</dt> <dd>

Afeta apenas os nomes de rotina de stub do cliente.

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span id="cstub"></span><span id="CSTUB"></span>cstub****


</dt> <dd>

Igual ao *cliente*. Afeta apenas os nomes de rotina de stub do cliente.

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span id="server"></span><span id="SERVER"></span>servidor * * * *


</dt> <dd>

Afeta apenas os nomes de rotina chamados pela rotina de stub do servidor.

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span id="sstub"></span><span id="SSTUB"></span>sstub****


</dt> <dd>

Igual ao *servidor*. Afeta apenas os nomes de rotina chamados pela rotina de stub do servidor.

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span id="switch"></span><span id="SWITCH"></span>alternar * * * *


</dt> <dd>

Afeta um protótipo extra adicionado ao arquivo de cabeçalho.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>todos * * * *


</dt> <dd>

Afeta os nomes de rotina de stub do cliente e do servidor.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Se o prefixo das rotinas do lado do cliente for diferente do prefixo das rotinas do lado do servidor, o arquivo de cabeçalho gerado terá protótipos de rotina do lado do cliente e protótipos de rotina do lado do servidor.

A opção **/prefix** é útil quando um único arquivo de cabeçalho for usado com stubs de várias execuções do compilador MIDL. Isso força protótipos de rotina adicionais no arquivo de cabeçalho.

Em todos os casos, o cliente, o servidor e os prefixos de comutador substituirão um prefixo ALL.

## <a name="examples"></a>Exemplos

**MIDL/prefix cliente "c \_ " Server "s \_ "**

**MIDL/prefix All "Moo \_ "**

**cliente de MIDL/prefix "latido \_ "**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




