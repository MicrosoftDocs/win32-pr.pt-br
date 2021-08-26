---
title: Interfaces do servidor de publicidade
description: O lado do servidor de um aplicativo que usa alças automáticas deve chamar a função RpcNsBindingExport para disponibilizar informações de associação sobre o servidor aos clientes.
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f81ec4b494c9ce2abd18031e3bf0ed3dd25d55908238ebc7bba96bce57e88f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073596"
---
# <a name="advertising-server-interfaces"></a>Interfaces do servidor de publicidade

O lado do servidor de um aplicativo que usa alças automáticas deve chamar a função [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) para disponibilizar informações de associação sobre o servidor aos clientes. Os alças de associação automática exigem um serviço de nome em execução em um servidor acessível ao cliente. A implementação da Microsoft do serviço de nome, Microsoft Locator, gerencia os manipuladores automáticos. Aplicativos de servidor que usam alças de associação implícitas e explícitas também podem anunciar sua presença no banco de dados de serviço de nome.

Normalmente, o servidor chama as seguintes funções de tempo de executar:

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

As chamadas para as duas primeiras funções neste fragmento de código são semelhantes ao [exemplo Hello, World](tutorial.md). Essas funções disponibilizam informações sobre a associação para o cliente. As chamadas para [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) e [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) colocam as informações no nome do banco de dados do serviço. A chamada para [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) preenche o vetor de associação com alças de associação válidas antes que os alças sejam exportados para o serviço de nome. Depois que o programa de servidor exporta os alças para o banco de dados, o cliente (ou stubs de cliente) pode chamar [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) e [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) para obter essas informações. Para obter detalhes, consulte [Localizar sistemas de host do servidor](finding-server-host-systems.md).

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

Observe que o [**parâmetro RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) *pBindingVector* é um ponteiro para um ponteiro para [**RPC \_ BINDING \_ VECTOR.**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) Lembre-se também de que cada chamada para [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) deve ser seguida por uma chamada para [**RpcBindingVectorFree.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)

Para remover a interface exportada do banco de dados de serviço name, o servidor chama [**RpcNsBindingUnexport,**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) conforme mostrado:

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

A [**função RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) deve ser usada somente quando o serviço estiver sendo removido permanentemente. Ele não deve ser usado quando o serviço está temporariamente desabilitado, como quando o servidor é desligado para manutenção. Um programa de servidor pode se registrar com o nome do banco de dados de serviço, mas não está disponível porque o servidor está temporariamente offline. O aplicativo cliente deve conter código de tratamento de exceção para essa condição.

Para obter mais informações sobre o conteúdo e o formato do nome do banco de dados de serviço, consulte O Banco de Dados do Serviço [de Nome RPC](the-rpc-name-service-database.md).

Os aplicativos poderão utilizar o serviço do Active Directory se os programas cliente e servidor estão em execução no Windows 2000. Os computadores que executam os programas cliente e servidor devem ser membros de um Windows 2000.

Para anunciar sua presença usando o serviço do Active Directory, o programa de servidor deve ser executado no contexto de segurança de um administrador de domínio. Se estiver em execução no contexto de usuários do domínio, um administrador de domínio deverá modificar a ACL (lista de controle de acesso) no contêiner RPC Services. Para obter mais informações, consulte a documentação do Active Directory.

 

 




