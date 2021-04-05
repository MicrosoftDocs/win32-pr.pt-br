---
title: Terminologia de ligação de RPC essencial
description: Para obter melhor ajuda em uma discussão sobre o processo de conexão do cliente/servidor, é útil conhecer os termos a seguir.
ms.assetid: 05aca325-87ee-4581-9152-a8a2ff7fb490
keywords:
- Chamada de procedimento remoto RPC, descrita, associação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18b8d3872c830d90079ad740505fead14c1b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007998"
---
# <a name="essential-rpc-binding-terminology"></a>Terminologia de ligação de RPC essencial

Para obter melhor ajuda em uma discussão sobre o processo de conexão do cliente/servidor, é útil conhecer os termos a seguir.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Sequência de protocolos
</dt> <dd>

Quando os sistemas operacionais de rede se comunicam entre si, eles devem escutar e falar da mesma linguagem. Esses idiomas são chamados de *sequências de protocolo*. Os programas cliente e servidor devem usar sequências de protocolo às quais a rede que os conectam oferece suporte. O Microsoft RPC dá suporte a uma variedade de sequências de protocolo. Para obter detalhes, consulte [selecionando uma sequência de protocolo](selecting-a-protocol-sequence.md), [especificando sequências de protocolo](specifying-protocol-sequences.md)e ponto de [**extremidade**](/windows/desktop/Midl/endpoint).

</dd> <dt>

<span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Computador host do servidor ou sistema host do servidor
</dt> <dd>

O programa do servidor é executado no computador host do servidor. No entanto, muitos literatura sobre a computação cliente/servidor refere-se ao programa do servidor e ao computador host do servidor como o "servidor". O resultado é que nem sempre é claro que está sendo discutido.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade
</dt> <dd>

Os programas de servidor escutam uma porta ou um grupo de portas no computador host do servidor para solicitações de cliente. Os sistemas de host de servidor mantêm um banco de dados dessas portas, que são chamadas de pontos de extremidade no RPC. O banco de dados é chamado de mapa de ponto de extremidade.

</dd> <dt>

<span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Vinculação
</dt> <dd>

Os programas cliente criam uma associação ao servidor para estabelecer uma sessão de comunicação. Uma associação contém todas as informações de que os aplicativos cliente precisam para criar a sessão.

</dd> </dl>

 

 