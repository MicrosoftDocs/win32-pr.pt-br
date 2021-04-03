---
title: Funções de autorização (RPC)
description: Cada vez que um programa de servidor recebe uma solicitação de cliente para acesso a um dos procedimentos remotos de gerenciamento, a biblioteca de tempo de execução RPC invoca uma função de autorização padrão.
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490c06ba8e40f132c17986edaef4dc02bbe056d7
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104006852"
---
# <a name="authorization-functions"></a><span data-ttu-id="60963-103">Funções de autorização</span><span class="sxs-lookup"><span data-stu-id="60963-103">Authorization Functions</span></span>

<span data-ttu-id="60963-104">Cada vez que um programa de servidor recebe uma solicitação de cliente para acesso a um dos procedimentos remotos de gerenciamento, a biblioteca de tempo de execução RPC invoca uma função de autorização padrão.</span><span class="sxs-lookup"><span data-stu-id="60963-104">Each time a server program receives a client request for access to one of the management remote procedures, the RPC run-time library invokes a default authorization function.</span></span> <span data-ttu-id="60963-105">Essa função usa o SSP para verificar as credenciais do cliente e autorizar ou rejeitar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="60963-105">This function uses the SSP to check the client's credentials and authorize or reject the request.</span></span>

<span data-ttu-id="60963-106">O programa do servidor pode substituir a função de autorização fornecida pelo SSP.</span><span class="sxs-lookup"><span data-stu-id="60963-106">Your server program can override the authorization function that the SSP provides.</span></span> <span data-ttu-id="60963-107">Invoque a função [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) e passe-a para o endereço da sua função de autorização.</span><span class="sxs-lookup"><span data-stu-id="60963-107">Invoke the function [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) and pass it to the address of your authorization function.</span></span> <span data-ttu-id="60963-108">Depois que o programa do servidor define a função de autorização, a biblioteca de tempo de execução RPC a chama sempre que o programa do servidor recebe uma solicitação do cliente para uma das funções de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="60963-108">Once the server program sets the authorization function, the RPC run-time library calls it every time the server program receives a client request to one of the management functions.</span></span> <span data-ttu-id="60963-109">Para obter mais informações, consulte [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)e [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).</span><span class="sxs-lookup"><span data-stu-id="60963-109">For more information, see [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname), and [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).</span></span>

 

 




