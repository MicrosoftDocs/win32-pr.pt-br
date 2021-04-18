---
description: Negociação de nível de autenticação
ms.assetid: 31353d02-bfe2-48ac-81a1-0e38895a8a75
title: Negociação de nível de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b9983bd2a2df1d85cc6df4bfc0ba2a757b200f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784504"
---
# <a name="negotiation-of-authentication-level"></a><span data-ttu-id="2656a-103">Negociação de nível de autenticação</span><span class="sxs-lookup"><span data-stu-id="2656a-103">Negotiation of Authentication Level</span></span>

<span data-ttu-id="2656a-104">Tanto o cliente quanto o servidor devem participar da autenticação, e cada parte indica que ele deseja executar um determinado nível de autenticação.</span><span class="sxs-lookup"><span data-stu-id="2656a-104">Both client and server must participate in authentication, and each party indicates that it wants to perform a certain level of authentication.</span></span> <span data-ttu-id="2656a-105">No início de uma chamada, o nível de autenticação é negociado entre as duas partes, um serviço apropriado é escolhido e a chamada é autenticada e prossegue (com possível criptografia, dependendo do nível de autenticação escolhido).</span><span class="sxs-lookup"><span data-stu-id="2656a-105">At the beginning of a call, the authentication level is negotiated between the two parties, an appropriate service is chosen, and the call is authenticated and proceeds (with possible encryption, depending on the authentication level chosen).</span></span> <span data-ttu-id="2656a-106">O nível de autenticação negociado entre o cliente e o servidor é determinado como máximo (*preferência do cliente*, *preferência do servidor*).</span><span class="sxs-lookup"><span data-stu-id="2656a-106">The authentication level negotiated between client and server is determined as Maximum(*Client preference*, *Server preference*).</span></span> <span data-ttu-id="2656a-107">O efeito disso significa que o servidor sempre pode determinar um nível mínimo de autenticação com o qual ele se sente confortável; ou seja, a autenticação pode ser ditada administrativamente do servidor.</span><span class="sxs-lookup"><span data-stu-id="2656a-107">The effect of this means that the server can always dictate a minimum level of authentication that it is comfortable with; that is, authentication can be administratively dictated from the server.</span></span>

<span data-ttu-id="2656a-108">O cliente especifica que deseja executar a autenticação em um determinado nível como com qualquer aplicativo COM.</span><span class="sxs-lookup"><span data-stu-id="2656a-108">The client specifies that it wants to perform authentication at a certain level as with any COM application.</span></span> <span data-ttu-id="2656a-109">O nível de autenticação do cliente pode ser indicado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2656a-109">The client authentication level can be indicated as follows:</span></span>

-   <span data-ttu-id="2656a-110">Por computador cliente, com o nível de autenticação COM de todo o computador definido usando [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) ou a ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="2656a-110">Per client machine, with the machine-wide COM authentication level set by using either [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) or the Component Services administrative tool.</span></span>
-   <span data-ttu-id="2656a-111">Por aplicativo cliente administrativamente, usando [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) ou usando a ferramenta administrativa serviços de componentes se o cliente deve ser um aplicativo com+.</span><span class="sxs-lookup"><span data-stu-id="2656a-111">Per client application administratively, using [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) or using the Component Services administrative tool if the client should be a COM+ application.</span></span>
-   <span data-ttu-id="2656a-112">Por processo de cliente de forma programática, com [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="2656a-112">Per client process programmatically, with [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>
-   <span data-ttu-id="2656a-113">A qualquer momento programaticamente, usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="2656a-113">At any point programmatically, using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="2656a-114">O aplicativo do servidor COM+ especifica um nível de autenticação administrativamente usando a ferramenta administrativa serviços de componentes (ou por meio de um script administrativo).</span><span class="sxs-lookup"><span data-stu-id="2656a-114">The COM+ server application specifies an authentication level administratively by using the Component Services administrative tool (or through an administrative script).</span></span>

<span data-ttu-id="2656a-115">A negociação de autenticação para uma chamada continua na seguinte sequência:</span><span class="sxs-lookup"><span data-stu-id="2656a-115">Negotiating authentication for a call proceeds in the following sequence:</span></span>

1.  <span data-ttu-id="2656a-116">O nível de autenticação é escolhido como máximo (*cliente*, *servidor*).</span><span class="sxs-lookup"><span data-stu-id="2656a-116">Authentication level is chosen as MAX(*client*, *server*).</span></span>
2.  <span data-ttu-id="2656a-117">Negociação do protocolo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="2656a-117">Negotiation of authentication protocol.</span></span>
3.  <span data-ttu-id="2656a-118">O servidor autentica a identidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="2656a-118">Server authenticates client identity.</span></span>
4.  <span data-ttu-id="2656a-119">Opcionalmente, o cliente autentica a identidade do servidor, dependendo do protocolo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="2656a-119">Optionally, client authenticates server identity, depending on the authentication protocol.</span></span>
5.  <span data-ttu-id="2656a-120">As chamadas de método são comunicadas com o nível escolhido de autenticação.</span><span class="sxs-lookup"><span data-stu-id="2656a-120">Method calls are communicated with the chosen level of authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2656a-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2656a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2656a-122">Autenticação de cliente</span><span class="sxs-lookup"><span data-stu-id="2656a-122">Client Authentication</span></span>](client-authentication.md)
</dt> </dl>

 

 
