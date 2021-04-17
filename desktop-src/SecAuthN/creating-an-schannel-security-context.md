---
description: Explica como estabelecer um contexto de segurança que protege as comunicações entre um cliente e um servidor.
ms.assetid: eb1eadb2-14b2-4265-994a-dcea4208e650
title: Criando um contexto de segurança Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e364e6319fbaddb50bffaf59541af9e8f43bfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748467"
---
# <a name="creating-an-schannel-security-context"></a><span data-ttu-id="acd94-103">Criando um contexto de segurança Schannel</span><span class="sxs-lookup"><span data-stu-id="acd94-103">Creating an Schannel Security Context</span></span>

<span data-ttu-id="acd94-104">Para estabelecer um [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) que protegerá as comunicações entre um cliente e um servidor, ambos devem participar do seguinte processo de troca de informações:</span><span class="sxs-lookup"><span data-stu-id="acd94-104">To establish a [*security context*](/windows/desktop/SecGloss/s-gly) that will protect communications between a client and server, both must participate in the following information exchange process:</span></span>

## <a name="client"></a><span data-ttu-id="acd94-105">Cliente</span><span class="sxs-lookup"><span data-stu-id="acd94-105">Client</span></span>

1.  <span data-ttu-id="acd94-106">O cliente chama a função [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .</span><span class="sxs-lookup"><span data-stu-id="acd94-106">The client calls the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span>
2.  <span data-ttu-id="acd94-107">O Schannel começa a criar um contexto de segurança de acordo com as regras do protocolo de segurança selecionado.</span><span class="sxs-lookup"><span data-stu-id="acd94-107">Schannel begins creating a security context according to the rules of the selected security protocol.</span></span> <span data-ttu-id="acd94-108">O código de retorno da função indica se o cliente deve chamar a função novamente.</span><span class="sxs-lookup"><span data-stu-id="acd94-108">The function's return code indicates whether the client must call the function again.</span></span> <span data-ttu-id="acd94-109">[**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) pode retornar um token que representa o contexto.</span><span class="sxs-lookup"><span data-stu-id="acd94-109">[**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) may return a token that represents the context.</span></span>
3.  <span data-ttu-id="acd94-110">Se um token for retornado, o cliente o enviará ao servidor.</span><span class="sxs-lookup"><span data-stu-id="acd94-110">If a token was returned, the client sends it to the server.</span></span>
4.  <span data-ttu-id="acd94-111">Quando [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) retorna s \_ E \_ OK, o cliente é concluído.</span><span class="sxs-lookup"><span data-stu-id="acd94-111">When [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) returns SEC\_E\_OK, the client is done.</span></span> <span data-ttu-id="acd94-112">Se a função retornar s \_ \_ , continuaria \_ necessário, o cliente deverá aguardar até que o servidor envie um token para ele.</span><span class="sxs-lookup"><span data-stu-id="acd94-112">If the function returns SEC\_I\_CONTINUE\_NEEDED, the client must wait for the server to send it a token.</span></span> <span data-ttu-id="acd94-113">Quando o cliente tem o token do servidor, ele deve chamar a função **InitializeSecurityContext (geral)** [](/windows/desktop/SecGloss/c-gly) novamente.</span><span class="sxs-lookup"><span data-stu-id="acd94-113">When the client has the token from the server, it must call the **InitializeSecurityContext (General)** [*function*](/windows/desktop/SecGloss/c-gly) again.</span></span> <span data-ttu-id="acd94-114">(Volte para a etapa 2.)</span><span class="sxs-lookup"><span data-stu-id="acd94-114">(Return to step 2.)</span></span>

## <a name="server"></a><span data-ttu-id="acd94-115">Servidor</span><span class="sxs-lookup"><span data-stu-id="acd94-115">Server</span></span>

1.  <span data-ttu-id="acd94-116">O servidor aguarda que um cliente envie uma mensagem que contém um token de segurança.</span><span class="sxs-lookup"><span data-stu-id="acd94-116">The server waits for a client to send a message that contains a security token.</span></span> <span data-ttu-id="acd94-117">O servidor passa o token recebido do cliente para a função [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .</span><span class="sxs-lookup"><span data-stu-id="acd94-117">The server passes the token received from the client into the [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span>
2.  <span data-ttu-id="acd94-118">O Schannel se baseia no contexto de segurança parcial representado pelo token.</span><span class="sxs-lookup"><span data-stu-id="acd94-118">Schannel builds on the partial security context represented by the token.</span></span> <span data-ttu-id="acd94-119">O Schannel retorna um token para o servidor e um código de retorno que indica se o servidor deve chamar a função novamente.</span><span class="sxs-lookup"><span data-stu-id="acd94-119">Schannel returns a token to the server, and a return code indicating whether the server must call the function again.</span></span>
3.  <span data-ttu-id="acd94-120">Se um token foi retornado, o servidor o envia para o cliente.</span><span class="sxs-lookup"><span data-stu-id="acd94-120">If a token was returned, the server sends it to the client.</span></span>
4.  <span data-ttu-id="acd94-121">Quando [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) retorna s \_ E \_ OK, o servidor é concluído.</span><span class="sxs-lookup"><span data-stu-id="acd94-121">When [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) returns SEC\_E\_OK, the server is done.</span></span> <span data-ttu-id="acd94-122">Se a função retornar s \_ \_ , continuaria \_ necessário, o servidor deverá aguardar até que o cliente envie um token.</span><span class="sxs-lookup"><span data-stu-id="acd94-122">If the function returns SEC\_I\_CONTINUE\_NEEDED, then the server must wait for the client to send it a token.</span></span> <span data-ttu-id="acd94-123">Quando o servidor tem o token do cliente, ele deve chamar a função **AcceptSecurityContext (geral)** novamente.</span><span class="sxs-lookup"><span data-stu-id="acd94-123">When the server has the token from the client, it must call the **AcceptSecurityContext (General)** function again.</span></span> <span data-ttu-id="acd94-124">(Volte para a etapa 2.)</span><span class="sxs-lookup"><span data-stu-id="acd94-124">(Return to step 2.)</span></span>

<span data-ttu-id="acd94-125">Se uma das funções retornar um valor diferente de s \_ e \_ OK, a opção s \_ \_ continuaria \_ necessária \_ ou \_ a mensagem s E incompleta \_ (consulte o parágrafo a seguir) ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="acd94-125">If either function returns a value other than SEC\_E\_OK, SEC\_I\_CONTINUE\_NEEDED, or SEC\_E\_INCOMPLETE\_MESSAGE (see the following paragraph) an error has occurred.</span></span> <span data-ttu-id="acd94-126">O cliente e o servidor devem chamar a função [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) para excluir o contexto de segurança parcialmente estabelecido.</span><span class="sxs-lookup"><span data-stu-id="acd94-126">The client and server should call the [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) function to delete the partially established security context.</span></span>

<span data-ttu-id="acd94-127">Um caso especial que pode alterar o processamento de cliente e servidor é quando muitas informações são enviadas para o cliente ou para o servidor da outra parte.</span><span class="sxs-lookup"><span data-stu-id="acd94-127">A special case that can alter client and server processing is when too little or too much information is sent to the client or server from the other party.</span></span> <span data-ttu-id="acd94-128">No caso de poucas informações, ambas as funções retornam a \_ mensagem s E \_ incompletas \_ .</span><span class="sxs-lookup"><span data-stu-id="acd94-128">In the case of too little information, both functions return SEC\_E\_INCOMPLETE\_MESSAGE.</span></span> <span data-ttu-id="acd94-129">Para obter informações sobre como reconhecer e manipular informações insuficientes ou em excesso, consulte [buffers extras retornados pelo Schannel](extra-buffers-returned-by-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="acd94-129">For information about recognizing and handling insufficient or excess information, see [Extra buffers Returned by Schannel](extra-buffers-returned-by-schannel.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="acd94-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="acd94-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acd94-131">Executando a autenticação usando Schannel</span><span class="sxs-lookup"><span data-stu-id="acd94-131">Performing Authentication Using Schannel</span></span>](performing-authentication-using-schannel.md)
</dt> <dt>

[<span data-ttu-id="acd94-132">Mapeando certificados</span><span class="sxs-lookup"><span data-stu-id="acd94-132">Mapping Certificates</span></span>](mapping-certificates.md)
</dt> <dt>

[<span data-ttu-id="acd94-133">Validando manualmente as credenciais do Schannel</span><span class="sxs-lookup"><span data-stu-id="acd94-133">Manually Validating Schannel Credentials</span></span>](manually-validating-schannel-credentials.md)
</dt> </dl>

 

 
