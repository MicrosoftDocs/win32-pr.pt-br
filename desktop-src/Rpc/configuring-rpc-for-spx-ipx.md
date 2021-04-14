---
title: Configurando o RPC para SPX/IPX
description: Ao usar os \_ transportes IPX ncacn SPX e ncadg \_ , o nome do servidor é exatamente o mesmo que o nome do servidor no Windows.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90fa82c216413f1ea745b90ae03749ede4331310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453662"
---
# <a name="configuring-rpc-for-spxipx"></a><span data-ttu-id="c078b-103">Configurando o RPC para SPX/IPX</span><span class="sxs-lookup"><span data-stu-id="c078b-103">Configuring RPC for SPX/IPX</span></span>

<span data-ttu-id="c078b-104">Ao usar os transportes **\_ IPX** **ncacn \_ SPX** e ncadg, o nome do servidor é exatamente o mesmo que o nome do servidor no Windows.</span><span class="sxs-lookup"><span data-stu-id="c078b-104">When using the **ncacn\_spx** and **ncadg\_ipx** transports, the server name is exactly the same as the server name on Windows.</span></span> <span data-ttu-id="c078b-105">No entanto, como os nomes são distribuídos usando protocolos Novell, eles devem estar em conformidade com as convenções de nomenclatura da Novell.</span><span class="sxs-lookup"><span data-stu-id="c078b-105">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="c078b-106">Se um nome de servidor não for um nome de Novell válido, os servidores não poderão criar pontos de extremidade com os transportes **\_ IPX** **ncacn \_ SPX** ou ncadg.</span><span class="sxs-lookup"><span data-stu-id="c078b-106">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncacn\_spx** or **ncadg\_ipx** transports.</span></span>

<span data-ttu-id="c078b-107">Um nome de servidor Novell válido contém apenas os caracteres entre 0x20 e 0x7f.</span><span class="sxs-lookup"><span data-stu-id="c078b-107">A valid Novell server name contains only the characters between 0x20 and 0x7f.</span></span> <span data-ttu-id="c078b-108">Caracteres minúsculos são alterados para letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="c078b-108">Lowercase characters are changed to uppercase.</span></span> <span data-ttu-id="c078b-109">Os seguintes caracteres não podem ser usados:</span><span class="sxs-lookup"><span data-stu-id="c078b-109">The following characters cannot be used:</span></span>

<span data-ttu-id="c078b-110">" \* ,./:; <=>?\[\]\\\|\]</span><span class="sxs-lookup"><span data-stu-id="c078b-110">"\*,./:;<=>?\[\]\\\|\]</span></span>

<span data-ttu-id="c078b-111">Para manter a compatibilidade com a primeira versão do Windows NT, o **ncacn \_ SPX** e o **ncadg \_ IPX** também permitem que você use um formato especial do nome do servidor conhecido como o nome do til.</span><span class="sxs-lookup"><span data-stu-id="c078b-111">To maintain compatibility with the first version of Windows NT, **ncacn\_spx** and **ncadg\_ipx** also enable you to use a special format of the server name known as the tilde name.</span></span> <span data-ttu-id="c078b-112">O nome de til consiste em um til (~), seguido pelo número de rede de oito dígitos do servidor e seguido por seu endereço Ethernet de 12 dígitos.</span><span class="sxs-lookup"><span data-stu-id="c078b-112">The tilde name consists of a tilde (~), followed by the server's eight-digit network number, and then followed by its 12-digit Ethernet address.</span></span> <span data-ttu-id="c078b-113">Os nomes de til têm uma vantagem em que eles não exigem nenhum recurso de serviço de nome.</span><span class="sxs-lookup"><span data-stu-id="c078b-113">Tilde names have an advantage in that they do not require any name service capabilities.</span></span> <span data-ttu-id="c078b-114">Portanto, se você estiver conectado a um servidor, o nome de til funcionará.</span><span class="sxs-lookup"><span data-stu-id="c078b-114">Thus, if you are connected to a server, the tilde name will work.</span></span>

<span data-ttu-id="c078b-115">As tabelas a seguir contêm duas configurações de exemplo que ilustram os pontos descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c078b-115">The following tables contain two sample configurations that illustrate the points previously described.</span></span>



| <span data-ttu-id="c078b-116">Componente</span><span class="sxs-lookup"><span data-stu-id="c078b-116">Component</span></span>                            | <span data-ttu-id="c078b-117">Configurado como</span><span class="sxs-lookup"><span data-stu-id="c078b-117">Configured as</span></span>      |
|--------------------------------------|--------------------|
| <span data-ttu-id="c078b-118">Windows Server</span><span class="sxs-lookup"><span data-stu-id="c078b-118">Windows server</span></span>                       | <span data-ttu-id="c078b-119">NWCS</span><span class="sxs-lookup"><span data-stu-id="c078b-119">NWCS</span></span>               |
| <span data-ttu-id="c078b-120">Windows Client</span><span class="sxs-lookup"><span data-stu-id="c078b-120">Windows client</span></span>                       | <span data-ttu-id="c078b-121">NWCS</span><span class="sxs-lookup"><span data-stu-id="c078b-121">NWCS</span></span>               |
| <span data-ttu-id="c078b-122">cliente Windows de 16 bits, cliente MS-DOS</span><span class="sxs-lookup"><span data-stu-id="c078b-122">16-bit Windows client, MS-DOS client</span></span> | <span data-ttu-id="c078b-123">Redirecionador do NetWare</span><span class="sxs-lookup"><span data-stu-id="c078b-123">NetWare Redirector</span></span> |



 

<span data-ttu-id="c078b-124">A configuração na tabela anterior requer que você tenha servidores de arquivos ou roteadores do NetWare em sua rede.</span><span class="sxs-lookup"><span data-stu-id="c078b-124">The configuration in the previous table requires that you have NetWare file servers or routers on your network.</span></span> <span data-ttu-id="c078b-125">Ele produzirá o melhor desempenho, pois os nomes de servidor são armazenados na ligação do NetWare.</span><span class="sxs-lookup"><span data-stu-id="c078b-125">It will produce the best performance because the server names are stored in the NetWare Bindery.</span></span>



| <span data-ttu-id="c078b-126">Componente</span><span class="sxs-lookup"><span data-stu-id="c078b-126">Component</span></span>                            | <span data-ttu-id="c078b-127">Configurado como</span><span class="sxs-lookup"><span data-stu-id="c078b-127">Configured as</span></span> |
|--------------------------------------|---------------|
| <span data-ttu-id="c078b-128">Windows Server</span><span class="sxs-lookup"><span data-stu-id="c078b-128">Windows server</span></span>                       | <span data-ttu-id="c078b-129">Agente SAP</span><span class="sxs-lookup"><span data-stu-id="c078b-129">SAP Agent</span></span>     |
| <span data-ttu-id="c078b-130">Windows Client</span><span class="sxs-lookup"><span data-stu-id="c078b-130">Windows client</span></span>                       | <span data-ttu-id="c078b-131">IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="c078b-131">IPX/SPX</span></span>       |
| <span data-ttu-id="c078b-132">cliente Windows de 16 bits, cliente MS-DOS</span><span class="sxs-lookup"><span data-stu-id="c078b-132">16-bit Windows client, MS-DOS client</span></span> | <span data-ttu-id="c078b-133">IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="c078b-133">IPX/SPX</span></span>       |



 

<span data-ttu-id="c078b-134">A segunda configuração funciona em um ambiente que não contém servidores de arquivos ou roteadores do NetWare (por exemplo, uma rede de dois computadores: um Windows Server e um cliente MS-DOS).</span><span class="sxs-lookup"><span data-stu-id="c078b-134">The second configuration works in an environment that does not contain NetWare file servers or routers (for example, a network of two computers: a Windows server and an MS-DOS client).</span></span> <span data-ttu-id="c078b-135">A resolução de nomes, que é realizada durante a primeira chamada em um identificador de ligação, será um pouco mais lenta do que na primeira configuração.</span><span class="sxs-lookup"><span data-stu-id="c078b-135">Name resolution, which is accomplished during the first call over a binding handle, will be slightly slower than in the first configuration.</span></span> <span data-ttu-id="c078b-136">Além disso, a segunda configuração resulta em mais tráfego gerado pela rede.</span><span class="sxs-lookup"><span data-stu-id="c078b-136">In addition, the second configuration results in more traffic generated over the network.</span></span>

<span data-ttu-id="c078b-137">Para implementar a resolução de nomes, quando um servidor RPC usa um ponto de extremidade SPX ou IPX, o nome do servidor e o ponto de extremidade são registrados como um servidor SAP (Service Advertising Protocol) do tipo 640 (hexadecimal).</span><span class="sxs-lookup"><span data-stu-id="c078b-137">To implement name resolution, when an RPC server uses an SPX or IPX endpoint, the server name and endpoint are registered as a Service Advertising Protocol (SAP) server of type 640 (hexadecimal).</span></span> <span data-ttu-id="c078b-138">Para resolver um nome de servidor, o cliente RPC envia uma solicitação SAP para todos os serviços do mesmo tipo e, em seguida, verifica a lista de respostas para o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c078b-138">To resolve a server name, the RPC client sends a SAP request for all services of the same type, and then scans the list of responses for the name of the server.</span></span> <span data-ttu-id="c078b-139">Esse processo ocorre durante a primeira chamada RPC em cada identificador de ligação.</span><span class="sxs-lookup"><span data-stu-id="c078b-139">This process occurs during the first RPC call over each binding handle.</span></span> <span data-ttu-id="c078b-140">Para obter informações adicionais sobre o protocolo SAP para Novell, consulte a documentação do NetWare.</span><span class="sxs-lookup"><span data-stu-id="c078b-140">For additional information on the SAP protocol for Novell, see your NetWare documentation.</span></span>

> [!Note]  
> <span data-ttu-id="c078b-141">Os aplicativos cliente do Windows de 16 bits que usam os transportes **\_ IPX** **ncacn \_ SPX** ou ncadg exigem que o arquivo Nwipxspx.dll ser instalado para ser executado no subsistema WOW.</span><span class="sxs-lookup"><span data-stu-id="c078b-141">The 16-bit Windows client applications that use the **ncacn\_spx** or **ncadg\_ipx** transports require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="c078b-142">Contate a Novell para obter esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="c078b-142">Contact Novell to obtain this file.</span></span>

 

 

 




