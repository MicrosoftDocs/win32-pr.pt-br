---
title: E (RPC)
description: Palavras que começam com E no Glossário de RPC (chamada de procedimento remoto).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 76e35c3c-91dd-42e3-9699-6767e37b2699
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab198e0908ce27a1776b7f2655527140dea7af2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454501"
---
# <a name="e-rpc"></a>E (RPC)

[A](a-glos.md) [B](b-glos.md) [C](c-glos.md) [D](d-glos.md) E [F](f-glos.md) G H [i](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z

<dl> <dt>

<span id="_rpc_embedded_pointer_glos"></span><span id="_RPC_EMBEDDED_POINTER_GLOS"></span>**ponteiro inserido**
</dt> <dd>

Ponteiro inserido em um parâmetro que é uma estrutura de dados como uma matriz, estrutura ou União. Consulte também o [*ponteiro de nível superior*](t-glos.md).

</dd> <dt>

<span id="_rpc_encoding_services_glos"></span><span id="_RPC_ENCODING_SERVICES_GLOS"></span>**serviços de codificação**
</dt> <dd>

Rotinas de stub geradas por MIDL que fornecem suporte para codificação e decodificação de dados (também conhecido como *seleção* ou *serialização*). Permitir que os programadores controlem buffers contendo dados a serem empacotados e desempacotados. Consulte também [*serialização de tipo*](t-glos.md), [*serialização de procedimento*](p-glos.md).

</dd> <dt>

<span id="_rpc_endpoint_glos"></span><span id="_RPC_ENDPOINT_GLOS"></span>**extremidade**
</dt> <dd>

Endereço específico da rede de um processo do servidor para chamadas de procedimento remoto. O nome real do ponto de extremidade depende da sequência de protocolo que está sendo usada. Confira também [*ponto de extremidade dinâmico*](d-glos.md) e [*ponto de extremidade bem conhecido*](w-glos.md).

</dd> <dt>

<span id="_rpc_endpoint_mapper_glos"></span><span id="_RPC_ENDPOINT_MAPPER_GLOS"></span>**mapeador de ponto de extremidade**
</dt> <dd>

Parte do subsistema RPC (RPCSs) que permite que a biblioteca de tempo de execução atribua e resolva pontos de extremidade dinamicamente. Consulte também [ponto de extremidade](/windows).

</dd> <dt>

<span id="_rpc_encapsulated_union_glos"></span><span id="_RPC_ENCAPSULATED_UNION_GLOS"></span>**União encapsulada**
</dt> <dd>

A construção MIDL que permite que as uniões sejam passadas como parte de uma chamada de procedimento remoto, inserindo a União em uma estrutura na qual discriminante é o primeiro campo da estrutura e a União é o segundo campo (e final) da estrutura. A **opção** de palavra-chave [*IDL*](i-glos.md) especifica que uma União é encapsulada. Consulte também [*União não encapsulada*](n-glos.md).

</dd> <dt>

<span id="_rpc_epv_glos"></span><span id="_RPC_EPV_GLOS"></span>**vetor de ponto de entrada (EPV)**
</dt> <dd>

Matriz de ponteiros para funções que implementam as operações especificadas na interface. Cada elemento na matriz corresponde a uma função definida no arquivo IDL. Os vetores de ponto de entrada permitem que aplicativos distribuídos ofereçam suporte a mais de uma implementação das funções definidas no arquivo IDL.

</dd> </dl>

 

 
