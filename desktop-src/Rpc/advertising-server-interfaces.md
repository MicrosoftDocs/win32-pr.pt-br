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
# <a name="advertising-server-interfaces"></a><span data-ttu-id="a3ddd-103">Interfaces de servidor de anúncios</span><span class="sxs-lookup"><span data-stu-id="a3ddd-103">Advertising Server Interfaces</span></span>

<span data-ttu-id="a3ddd-104">O lado do servidor de um aplicativo que usa identificadores automáticos deve chamar a função [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) para tornar as informações de associação sobre o servidor disponíveis para os clientes.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-104">The server side of an application that uses automatic handles must call the function [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) to make binding information about the server available to clients.</span></span> <span data-ttu-id="a3ddd-105">Os identificadores de ligação automática exigem um serviço de nome em execução em um servidor que possa ser acessado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-105">Automatic binding handles require a name service running on a server that is accessible to the client.</span></span> <span data-ttu-id="a3ddd-106">A implementação da Microsoft do serviço de nome, Microsoft Locator, gerencia identificadores automáticos.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-106">The Microsoft implementation of the name service, Microsoft Locator, manages automatic handles.</span></span> <span data-ttu-id="a3ddd-107">Os aplicativos de servidor que usam identificadores de associação implícitos e explícitos também podem anunciar sua presença no banco de dados do serviço de nome.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-107">Server applications that use implicit and explicit binding handles can also advertise their presence in the name service database.</span></span>

<span data-ttu-id="a3ddd-108">Normalmente, o servidor chama as seguintes funções de tempo de execução:</span><span class="sxs-lookup"><span data-stu-id="a3ddd-108">Typically, the server calls the following run-time functions:</span></span>

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

<span data-ttu-id="a3ddd-109">As chamadas para as duas primeiras funções neste fragmento de código são semelhantes ao [exemplo Hello, World](tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="a3ddd-109">The calls to the first two functions in this code fragment are similar to the [Hello, World example](tutorial.md).</span></span> <span data-ttu-id="a3ddd-110">Essas funções tornam informações sobre a associação disponível para o cliente.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-110">These functions make information about the binding available to the client.</span></span> <span data-ttu-id="a3ddd-111">As chamadas para [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) e [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) colocam as informações no banco de dados do serviço de nome.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-111">The calls to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) and [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) put the information in the name service database.</span></span> <span data-ttu-id="a3ddd-112">A chamada para [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) preenche o vetor de associação com identificadores de associação válidos antes que os identificadores sejam exportados para o serviço de nome.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-112">The call to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) fills the binding vector with valid binding handles before the handles are exported to the name service.</span></span> <span data-ttu-id="a3ddd-113">Depois que o programa do servidor exporta os identificadores para o banco de dados, o cliente (ou stubs de cliente) pode chamar [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) e [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) para obter essas informações.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-113">After the server program exports the handles to the database, the client (or client stubs) can call [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) and [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) to obtain this information.</span></span> <span data-ttu-id="a3ddd-114">Para obter detalhes, consulte [localizando sistemas de host de servidor](finding-server-host-systems.md).</span><span class="sxs-lookup"><span data-stu-id="a3ddd-114">For details, see [Finding Server Host Systems](finding-server-host-systems.md).</span></span>

<span data-ttu-id="a3ddd-115">As chamadas para [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) e [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) e suas estruturas de dados associadas são semelhantes às seguintes:</span><span class="sxs-lookup"><span data-stu-id="a3ddd-115">The calls to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) and [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) and their associated data structures look similar to the following:</span></span>

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

<span data-ttu-id="a3ddd-116">Observe que o [](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) parâmetro RpcServerInqBindings *pBindingVector* é um ponteiro para um ponteiro para [**o \_ \_ vetor de associação RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector).</span><span class="sxs-lookup"><span data-stu-id="a3ddd-116">Note that the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) parameter *pBindingVector* is a pointer to a pointer to [**RPC\_BINDING\_VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector).</span></span> <span data-ttu-id="a3ddd-117">Lembre-se também de que cada chamada para [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) deve ser seguida por uma chamada para [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).</span><span class="sxs-lookup"><span data-stu-id="a3ddd-117">Also remember that each call to [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) must be followed by a call to [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).</span></span>

<span data-ttu-id="a3ddd-118">Para remover a interface exportada do banco de dados do serviço de nome, o servidor chama [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) , conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="a3ddd-118">To remove the exported interface from the name service database, the server calls [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) as shown:</span></span>

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

<span data-ttu-id="a3ddd-119">A função [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) deve ser usada somente quando o serviço está sendo removido permanentemente.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-119">The [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) function should be used only when the service is being permanently removed.</span></span> <span data-ttu-id="a3ddd-120">Ele não deve ser usado quando o serviço está temporariamente desabilitado, como quando o servidor é desligado para manutenção.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-120">It should not be used when the service is temporarily disabled, such as when the server is shut down for maintenance.</span></span> <span data-ttu-id="a3ddd-121">Um programa de servidor pode se registrar com o banco de dados do serviço de nome, mas não está disponível porque o servidor está temporariamente offline.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-121">A server program can register itself with the name service database, yet be unavailable because the server is temporarily offline.</span></span> <span data-ttu-id="a3ddd-122">O aplicativo cliente deve conter código de tratamento de exceções para tal condição.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-122">The client application should contain exception-handling code for such a condition.</span></span>

<span data-ttu-id="a3ddd-123">Para obter mais informações sobre o conteúdo e o formato do banco de dados do serviço de nome, consulte [o banco de dados do serviço de nome RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="a3ddd-123">For more information on the content and format of the name service database, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

<span data-ttu-id="a3ddd-124">Os aplicativos podem utilizar o serviço Active Directory se os programas cliente e servidor estiverem em execução no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-124">Applications can utilize the Active Directory service if both the client and server programs are running under Windows 2000.</span></span> <span data-ttu-id="a3ddd-125">Os computadores que executam os programas cliente e servidor devem ser membros de um domínio do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-125">The computers running the client and server programs must both be members of a Windows 2000 domain.</span></span>

<span data-ttu-id="a3ddd-126">Para anunciar sua presença usando o serviço de Active Directory, o programa do servidor deve ser executado no contexto de segurança de um administrador de domínio.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-126">To advertise its presence using the Active Directory service, the server program should run in the security context of a domain administrator.</span></span> <span data-ttu-id="a3ddd-127">Se ele estiver em execução no contexto de usuários de domínio, um administrador de domínio deverá modificar a ACL (lista de controle de acesso) no contêiner de serviços RPC.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-127">If it is running in the context of domain users, a domain administrator must modify the access control list (ACL) on the RPC Services container.</span></span> <span data-ttu-id="a3ddd-128">Para obter mais informações, consulte a documentação do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-128">For more information, see the Active Directory documentation.</span></span>

 

 




