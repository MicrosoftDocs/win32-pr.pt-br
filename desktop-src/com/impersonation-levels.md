---
title: Níveis de representação (COM)
description: Se a representação for bem-sucedida, isso significa que o cliente aceitou permitir que o servidor seja o cliente até certo ponto.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca691c89e7ff4a12e279ae0ecd0fd04cb31a951c8ac3f2671201fe99dd5900a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756386"
---
# <a name="impersonation-levels"></a>Níveis de representação

Se a representação for bem-sucedida, isso significa que o cliente aceitou permitir que o servidor seja o cliente até certo ponto. Os diferentes graus de representação são chamados de níveis de representação *e* indicam a autoridade que é dada ao servidor quando ele está representando o cliente.

Atualmente, há quatro níveis de representação: *anônimo,* *identificar*, *representar* e *delegar*. A lista a seguir descreve brevemente cada nível de representação:

<dl> <dt>

<span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anonymous (RPC \_ C \_ IMP LEVEL \_ \_ ANONYMOUS)
</dt> <dd>

O cliente é anônimo ao servidor. O processo do servidor pode representar o cliente, mas o token de representação não contém nenhuma informação sobre o cliente. Esse nível só tem suporte no transporte de comunicação entre processos local. Todos os outros transportes promovem silenciosamente esse nível para identificar.

</dd> <dt>

<span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identify (RPC \_ C \_ IMP LEVEL \_ \_ IDENTIFY)
</dt> <dd>

O nível padrão do sistema. O servidor pode obter a identidade do cliente e o servidor pode representar o cliente para executar verificações de ACL.

</dd> <dt>

<span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>impersonate (RPC \_ C \_ IMP LEVEL \_ \_ IMPERSONATE)
</dt> <dd>

O servidor pode representar o contexto de segurança do cliente ao atuar em nome do cliente. O servidor pode acessar recursos locais como o cliente. Se o servidor for local, ele poderá acessar recursos de rede como o cliente. Se o servidor for remoto, ele poderá acessar somente os recursos que estão no mesmo computador que o servidor.

</dd> <dt>

<span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>delegate (DELEGADO DE NÍVEL DE IMP do RPC \_ \_ \_ \_ C)
</dt> <dd>

O nível de representação mais avançado. Quando esse nível é selecionado, o servidor (local ou remoto) pode representar contexto de segurança do cliente ao atuar em nome do cliente. Durante a representação, as credenciais do cliente (local e rede) podem ser passadas para qualquer número de computadores.

Para que a representação funcione no nível do delegado, os seguintes requisitos devem ser atendidos:

-   O cliente deve definir o nível de representação como RPC \_ C \_ IMP LEVEL \_ \_ DELEGATE.
-   A conta do cliente não deve ser marcada como "A conta é sensível e não pode ser delegada" no Serviço do Active Directory.
-   A conta do servidor deve ser marcada com o atributo "Confiável para delegação" no Serviço do Active Directory.
-   Os computadores que hospedam o cliente, o servidor e todos os servidores "downstream" devem estar todos em execução em um domínio.

</dd> </dl>

Ao escolher o nível de representação, o cliente informa ao servidor até onde ele pode ir representando o cliente. O cliente define o nível de representação no proxy que ele usa para se comunicar com o servidor.

## <a name="setting-the-impersonation-level"></a>Definindo o nível de representação

Há duas maneiras de definir o nível de representação:

-   O cliente pode defini-lo em todo o processo, por meio de uma chamada para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).
-   Um cliente pode definir a segurança em nível de proxy em uma interface de um objeto remoto por meio de uma chamada para [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (ou a função auxiliar [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).

Você pode definir o nível de representação passando um valor xxx de NÍVEL DE IMP do RPC C apropriado para \_ \_ \_ \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) por meio do *parâmetro dwImpLevel.*

Diferentes serviços de autenticação suportam representação de nível delegado em diferentes extensão. Por exemplo, o NTLMSSP dá suporte à representação de nível delegado entre threads e entre processos, mas não entre computadores. Por outro lado, o protocolo Kerberos dá suporte à representação em nível delegado entre limites do computador, enquanto o Schannel não dá suporte a nenhuma representação no nível delegado. Se você tiver um proxy no nível de representação e quiser definir o nível de representação como delegado, chame [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) usando as constantes padrão para cada parâmetro, exceto o nível de representação. O COM escolherá o NTLM localmente e o protocolo Kerberos remotamente (quando o protocolo Kerberos funcionará).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Delegação e representação](delegation-and-impersonation.md)
</dt> </dl>

 

 