---
description: A partir do Windows Vista, o SCM (Gerenciador de controle de serviços) dá suporte a chamadas de procedimento remotos em Protocolo RPC/TCP e pipes nomeados (RPC/NP).
ms.assetid: c51732f6-c22f-4726-afaa-13a8948ac44f
title: Serviços e RPC/TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fdb2ef3b21f280ba4e5078d302813de41a5a43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762891"
---
# <a name="services-and-rpctcp"></a><span data-ttu-id="34c81-103">Serviços e RPC/TCP</span><span class="sxs-lookup"><span data-stu-id="34c81-103">Services and RPC/TCP</span></span>

<span data-ttu-id="34c81-104">A partir do Windows Vista, o SCM (Gerenciador de controle de serviços) dá suporte a chamadas de procedimento remotos em Protocolo RPC/TCP e pipes nomeados (RPC/NP).</span><span class="sxs-lookup"><span data-stu-id="34c81-104">Starting with Windows Vista, the service control manager (SCM) supports remote procedure calls over both Transmission Control Protocol (RPC/TCP) and named pipes (RPC/NP).</span></span> <span data-ttu-id="34c81-105">Por padrão, as funções SCM do lado do cliente usam RPC/TCP.</span><span class="sxs-lookup"><span data-stu-id="34c81-105">Client-side SCM functions use RPC/TCP by default.</span></span>

<span data-ttu-id="34c81-106">O RPC/TCP é apropriado para a maioria dos aplicativos que usam funções SCM remotamente, como ferramentas de administração ou monitoramento remoto.</span><span class="sxs-lookup"><span data-stu-id="34c81-106">RPC/TCP is appropriate for most applications that use SCM functions remotely, such as remote administration or monitoring tools.</span></span> <span data-ttu-id="34c81-107">No entanto, para compatibilidade e desempenho, alguns aplicativos podem precisar desabilitar RPC/TCP definindo os valores de registro descritos neste tópico.</span><span class="sxs-lookup"><span data-stu-id="34c81-107">However, for compatibility and performance, some applications might need to disable RPC/TCP by setting the registry values described in this topic.</span></span>

<span data-ttu-id="34c81-108">Quando um serviço chama uma função SCM remota, o SCM do lado do cliente tenta primeiro usar RPC/TCP para se comunicar com o SCM do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="34c81-108">When a service calls a remote SCM function, the client-side SCM first attempts to use RPC/TCP to communicate with the server-side SCM.</span></span> <span data-ttu-id="34c81-109">Se o servidor estiver executando uma versão do Windows que dá suporte a RPC/TCP e permitir o tráfego RPC/TCP, a conexão RPC/TCPP terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="34c81-109">If the server is running a version of Windows that supports RPC/TCP and allows RPC/TCP traffic, the RPC/TCPP connection will succeed.</span></span> <span data-ttu-id="34c81-110">Se o servidor estiver executando uma versão do Windows que não dá suporte a RPC/TCP, ou der suporte a RPC/TCP, mas estiver operando atrás de um firewall que permita apenas o tráfego de pipe nomeado, a conexão RPC/TCP atingirá o tempo limite e o SCM tentará novamente a conexão com RPC/NP.</span><span class="sxs-lookup"><span data-stu-id="34c81-110">If the server is running a version of Windows that does not support RPC/TCP, or supports RPC/TCP but is operating behind a firewall which allows only named pipe traffic, the RPC/TCP connection times out and the SCM retries the connection with RPC/NP.</span></span> <span data-ttu-id="34c81-111">Isso terá sucesso eventualmente, mas pode levar algum tempo (normalmente mais de 20 segundos), fazendo com que a função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) pareça bloqueada.</span><span class="sxs-lookup"><span data-stu-id="34c81-111">This will succeed eventually but can take some time (typically more than 20 seconds), causing the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to appear blocked.</span></span>

<span data-ttu-id="34c81-112">O TCP não carrega as credenciais de usuário especificadas com um comando **net use** .</span><span class="sxs-lookup"><span data-stu-id="34c81-112">TCP does not carry user credentials specified with a **net use** command.</span></span> <span data-ttu-id="34c81-113">Portanto, se RPC/TCP estiver habilitado e **sc.exe** for usado para tentar acessar o serviço especificado, o comando poderá falhar com acesso negado.</span><span class="sxs-lookup"><span data-stu-id="34c81-113">Therefore, if RPC/TCP is enabled and **sc.exe** is used to attempt to access the specified service, the command could fail with access denied.</span></span> <span data-ttu-id="34c81-114">Desabilitar o RPC/TCP no lado do cliente faz com que o comando **sc.exe** use um pipe nomeado que transporta as credenciais do usuário, para que o comando seja bem sucedido.</span><span class="sxs-lookup"><span data-stu-id="34c81-114">Disabling RPC/TCP on the client side causes the **sc.exe** command to use a named pipe that does carry user credentials, so the command will succeed.</span></span> <span data-ttu-id="34c81-115">Para obter informações sobre sc.exe, consulte [controlando um serviço usando SC](controlling-a-service-using-sc.md).</span><span class="sxs-lookup"><span data-stu-id="34c81-115">For information about sc.exe, see [Controlling a Service Using SC](controlling-a-service-using-sc.md).</span></span>

> [!Note]  
> <span data-ttu-id="34c81-116">Um serviço não deve fornecer credenciais explícitas para um comando **net use** , pois essas credenciais podem ser compartilhadas inadvertidamente fora dos limites de serviço.</span><span class="sxs-lookup"><span data-stu-id="34c81-116">A service should not provide explicit credentials to a **net use** command, because those credentials might be inadvertently shared outside of the service boundaries.</span></span> <span data-ttu-id="34c81-117">Em vez disso, o serviço deve usar a [representação do cliente](/windows/desktop/SecAuthZ/client-impersonation) para representar o usuário.</span><span class="sxs-lookup"><span data-stu-id="34c81-117">Instead, the service should use [client impersonation](/windows/desktop/SecAuthZ/client-impersonation) to impersonate the user.</span></span>

 

### <a name="rpctcp-registry-values"></a><span data-ttu-id="34c81-118">Valores do registro RPC/TCP</span><span class="sxs-lookup"><span data-stu-id="34c81-118">RPC/TCP Registry Values</span></span>

<span data-ttu-id="34c81-119">O RPC/TCP é controlado pelos valores de registro **SCMApiConnectionParam**, **DisableRPCOverTCP** e **DisableRemoteScmEndpoints** , que estão todos sob a chave de controle **HKEY \_ \_ local** \\ **System** \\ **CurrentControlSet** \\  .</span><span class="sxs-lookup"><span data-stu-id="34c81-119">RPC/TCP is controlled by the **SCMApiConnectionParam**, **DisableRPCOverTCP**, and **DisableRemoteScmEndpoints** registry values, which are all under the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control** key.</span></span> <span data-ttu-id="34c81-120">Todos esses valores têm um tipo de \_ dados reg DWORD.</span><span class="sxs-lookup"><span data-stu-id="34c81-120">All of these values have a REG\_DWORD data type.</span></span> <span data-ttu-id="34c81-121">Os procedimentos a seguir mostram como usar esses valores de registro para controlar RPC/TCP.</span><span class="sxs-lookup"><span data-stu-id="34c81-121">The following procedures show how to use these registry values to control RPC/TCP.</span></span>

<span data-ttu-id="34c81-122">O procedimento a seguir descreve como desabilitar o RPC/TCP no lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="34c81-122">The following procedure describes how to disable RPC/TCP on the client side.</span></span>

<span data-ttu-id="34c81-123">**Para desabilitar RPC/TCP no lado do cliente**</span><span class="sxs-lookup"><span data-stu-id="34c81-123">**To disable RPC/TCP on the client side**</span></span>

1.  <span data-ttu-id="34c81-124">Combine o valor do registro **SCMApiConnectionParam** com o valor de Mask 0x80000000.</span><span class="sxs-lookup"><span data-stu-id="34c81-124">Combine the **SCMApiConnectionParam** registry value with the mask value 0x80000000.</span></span>
2.  <span data-ttu-id="34c81-125">Reinicie o aplicativo que chama a função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) .</span><span class="sxs-lookup"><span data-stu-id="34c81-125">Restart the application that calls the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function.</span></span>

<span data-ttu-id="34c81-126">O procedimento a seguir descreve como desabilitar o TCP no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="34c81-126">The following procedure describes how to disable TCP on the server side.</span></span>

<span data-ttu-id="34c81-127">**Para desabilitar o TCP no lado do servidor**</span><span class="sxs-lookup"><span data-stu-id="34c81-127">**To disable TCP on the server side**</span></span>

1.  <span data-ttu-id="34c81-128">Defina o valor do registro **DisableRPCOverTCP** como 1.</span><span class="sxs-lookup"><span data-stu-id="34c81-128">Set the **DisableRPCOverTCP** registry value to 1.</span></span>
2.  <span data-ttu-id="34c81-129">Reinicie o servidor.</span><span class="sxs-lookup"><span data-stu-id="34c81-129">Restart the server.</span></span>

<span data-ttu-id="34c81-130">O procedimento a seguir descreve como desabilitar RPC/TCP e RPC/NP no servidor (por exemplo, para reduzir a superfície de ataque).</span><span class="sxs-lookup"><span data-stu-id="34c81-130">The following procedure describes how to disable both RPC/TCP and RPC/NP on the server (for example, to reduce the attack surface).</span></span>

<span data-ttu-id="34c81-131">**Para desabilitar RPC/TCP e RPC/NP no servidor**</span><span class="sxs-lookup"><span data-stu-id="34c81-131">**To disable both RPC/TCP and RPC/NP on the server**</span></span>

1.  <span data-ttu-id="34c81-132">Defina o valor do registro **DisableRemoteScmEndpoints** como 1.</span><span class="sxs-lookup"><span data-stu-id="34c81-132">Set the **DisableRemoteScmEndpoints** registry value to 1.</span></span>
2.  <span data-ttu-id="34c81-133">Reinicie o servidor.</span><span class="sxs-lookup"><span data-stu-id="34c81-133">Restart the server.</span></span>

<span data-ttu-id="34c81-134">O valor do registro **SCMApiConnectionParam** também pode ser usado para especificar o intervalo de tempo limite de RPC/TCP, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="34c81-134">The **SCMApiConnectionParam** registry value can also be used to specify the RPC/TCP time-out interval, in milliseconds.</span></span> <span data-ttu-id="34c81-135">Por exemplo, um valor de 30.000 especifica um intervalo de tempo limite de 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="34c81-135">For example, a value of 30,000 specifies a time-out interval of 30 seconds.</span></span> <span data-ttu-id="34c81-136">O padrão é 21.000 (21 segundos).</span><span class="sxs-lookup"><span data-stu-id="34c81-136">The default is 21,000 (21 seconds).</span></span>

 

 
