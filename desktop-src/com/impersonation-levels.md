---
title: Níveis de representação (COM)
description: Se a representação for realizada com sucesso, significa que o cliente concordou em permitir que o servidor seja o cliente para algum grau.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85286e5fa880ea7620d6f6ccb6107bf139ec2005
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103823996"
---
# <a name="impersonation-levels"></a>Níveis de representação

Se a representação for realizada com sucesso, significa que o cliente concordou em permitir que o servidor seja o cliente para algum grau. Os graus variados de representação são chamados de *níveis de representação* e indicam a quantidade de autoridade atribuída ao servidor quando ele está representando o cliente.

Atualmente, há quatro níveis de representação: *anônimo*, *identificar*, *representar* e *delegar*. A lista a seguir descreve brevemente cada nível de representação:

<dl> <dt>

<span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anônimo (RPC \_ C \_ IMP \_ nível \_ anônimo)
</dt> <dd>

O cliente é anônimo ao servidor. O processo do servidor pode representar o cliente, mas o token de representação não contém nenhuma informação sobre o cliente. Esse nível só tem suporte no transporte de comunicação entre processos local. Todos os outros transportes promovem silenciosamente esse nível para identificar.

</dd> <dt>

<span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identificar (identificação de nível de imp do RPC \_ C \_ \_ \_ )
</dt> <dd>

O nível padrão do sistema. O servidor pode obter a identidade do cliente e o servidor pode representar o cliente para executar verificações de ACL.

</dd> <dt>

<span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>Impersonate (representação de nível de imp do RPC \_ C \_ \_ \_ )
</dt> <dd>

O servidor pode representar o contexto de segurança do cliente ao atuar em nome do cliente. O servidor pode acessar recursos locais como o cliente. Se o servidor for local, ele poderá acessar os recursos de rede como o cliente. Se o servidor for remoto, ele poderá acessar apenas os recursos que estão no mesmo computador que o servidor.

</dd> <dt>

<span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>delegate (delegado de nível de imp do RPC \_ C \_ \_ \_ )
</dt> <dd>

O nível de representação mais avançado. Quando esse nível é selecionado, o servidor (local ou remoto) pode representar contexto de segurança do cliente ao atuar em nome do cliente. Durante a representação, as credenciais do cliente (local e de rede) podem ser passadas para qualquer número de computadores.

Para que a representação funcione no nível de representante, os seguintes requisitos devem ser atendidos:

-   O cliente deve definir o nível de representação para o delegado de nível de imp do RPC \_ C \_ \_ \_ .
-   A conta do cliente não deve ser marcada como "a conta é confidencial e não pode ser delegada" no serviço de Active Directory.
-   A conta do servidor deve ser marcada com o atributo "confiável para delegação" no serviço de Active Directory.
-   Os computadores que hospedam o cliente, o servidor e todos os servidores "downstream" devem estar em execução em um domínio.

</dd> </dl>

Ao escolher o nível de representação, o cliente informa ao servidor como ele pode ir para representar o cliente. O cliente define o nível de representação no proxy que ele usa para se comunicar com o servidor.

## <a name="setting-the-impersonation-level"></a>Definindo o nível de representação

Há duas maneiras de definir o nível de representação:

-   O cliente pode defini-lo processwide, por meio de uma chamada para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).
-   Um cliente pode definir a segurança em nível de proxy em uma interface de um objeto remoto por meio de uma chamada para [**IClientSecurity:: setampla**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (ou a função auxiliar [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).

Você define o nível de representação passando um valor xxx apropriado de nível de imp do RPC \_ C \_ \_ \_ para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) por meio do parâmetro *dwImpLevel* .

Serviços de autenticação diferentes dão suporte à representação em nível de delegado para diferentes extensões. Por exemplo, o NTLMSSP dá suporte à representação de nível delegado entre threads e entre processos, mas não entre computadores. Por outro lado, o protocolo Kerberos dá suporte à representação em nível de delegado entre limites de computador, enquanto Schannel não oferece suporte a qualquer representação no nível de delegado. Se você tiver um proxy no nível de Impersonate e desejar definir o nível de representação como delegado, [**deverá chamar**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) SetConstant usando as constantes padrão para cada parâmetro, exceto o nível de representação. O COM escolherá o NTLM localmente e o protocolo Kerberos remotamente (quando o protocolo Kerberos funcionará).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Delegação e representação](delegation-and-impersonation.md)
</dt> </dl>

 

 