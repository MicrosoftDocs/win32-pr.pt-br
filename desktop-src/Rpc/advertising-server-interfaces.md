---
title: Interfaces de servidor de anúncios
description: O lado do servidor de um aplicativo que usa identificadores automáticos deve chamar a função RpcNsBindingExport para tornar as informações de associação sobre o servidor disponíveis para os clientes.
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45955ac7228018d8ddebbc7c156031648091b6f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005565"
---
# <a name="advertising-server-interfaces"></a>Interfaces de servidor de anúncios

O lado do servidor de um aplicativo que usa identificadores automáticos deve chamar a função [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) para tornar as informações de associação sobre o servidor disponíveis para os clientes. Os identificadores de ligação automática exigem um serviço de nome em execução em um servidor que possa ser acessado pelo cliente. A implementação da Microsoft do serviço de nome, Microsoft Locator, gerencia identificadores automáticos. Os aplicativos de servidor que usam identificadores de associação implícitos e explícitos também podem anunciar sua presença no banco de dados do serviço de nome.

Normalmente, o servidor chama as seguintes funções de tempo de execução:

``` syntax
/* auto handle server application (fragment) */
 
//interface header file that the MIDL compiler generates
#include "auto.h" 
 
void main(void)
{
    RpcUseProtseqEp(...);
    RpcServerRegisterIf(...);
    RpcServerInqBindings(...);
    RpcNsBindingExport(...);
    ...
}
```

As chamadas para as duas primeiras funções neste fragmento de código são semelhantes ao [exemplo Hello, World](tutorial.md). Essas funções tornam informações sobre a associação disponível para o cliente. As chamadas para [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) e [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) colocam as informações no banco de dados do serviço de nome. A chamada para [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) preenche o vetor de associação com identificadores de associação válidos antes que os identificadores sejam exportados para o serviço de nome. Depois que o programa do servidor exporta os identificadores para o banco de dados, o cliente (ou stubs de cliente) pode chamar [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) e [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) para obter essas informações. Para obter detalhes, consulte [localizando sistemas de host de servidor](finding-server-host-systems.md).

As chamadas para [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) e [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) e suas estruturas de dados associadas são semelhantes às seguintes:

``` syntax
RPC_BINDING_VECTOR * pBindingVector;
RPCSTATUS status;
 
status = RpcServerInqBindings(&pBindingVector);
 
status = RpcNsBindingExport(
                fNameSyntaxType,      // name syntax type 
                pszAutoEntryName,     // nsi entry name 
                autoh_ServerIfHandle, // if server handle
                pBindingVector,       // set in previous call 
                NULL);                // UUID vector
```

Observe que o [](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) parâmetro RpcServerInqBindings *pBindingVector* é um ponteiro para um ponteiro para [**o \_ \_ vetor de associação RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector). Lembre-se também de que cada chamada para [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) deve ser seguida por uma chamada para [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).

Para remover a interface exportada do banco de dados do serviço de nome, o servidor chama [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) , conforme mostrado:

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

A função [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) deve ser usada somente quando o serviço está sendo removido permanentemente. Ele não deve ser usado quando o serviço está temporariamente desabilitado, como quando o servidor é desligado para manutenção. Um programa de servidor pode se registrar com o banco de dados do serviço de nome, mas não está disponível porque o servidor está temporariamente offline. O aplicativo cliente deve conter código de tratamento de exceções para tal condição.

Para obter mais informações sobre o conteúdo e o formato do banco de dados do serviço de nome, consulte [o banco de dados do serviço de nome RPC](the-rpc-name-service-database.md).

Os aplicativos podem utilizar o serviço Active Directory se os programas cliente e servidor estiverem em execução no Windows 2000. Os computadores que executam os programas cliente e servidor devem ser membros de um domínio do Windows 2000.

Para anunciar sua presença usando o serviço de Active Directory, o programa do servidor deve ser executado no contexto de segurança de um administrador de domínio. Se ele estiver em execução no contexto de usuários de domínio, um administrador de domínio deverá modificar a ACL (lista de controle de acesso) no contêiner de serviços RPC. Para obter mais informações, consulte a documentação do Active Directory.

 

 




