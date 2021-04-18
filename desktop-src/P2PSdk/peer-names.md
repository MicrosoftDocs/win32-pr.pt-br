---
description: Os nomes de pares são usados pelo PNRP (Peer Name Resolution Protocol), pelo Gerenciador de identidades de mesmo nível e pela infraestrutura de agrupamento de pares.
ms.assetid: b0d78b17-6f48-4294-b8a2-8fcc1a7f8ef1
title: Nomes de par
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18774939d5e0e9bad208999fbc6ca1e5f624300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756706"
---
# <a name="peer-names"></a><span data-ttu-id="87877-103">Nomes de par</span><span class="sxs-lookup"><span data-stu-id="87877-103">Peer Names</span></span>

<span data-ttu-id="87877-104">Os nomes de pares são usados pelo PNRP (Peer Name Resolution Protocol), pelo Gerenciador de identidades de mesmo nível e pela infraestrutura de agrupamento de pares.</span><span class="sxs-lookup"><span data-stu-id="87877-104">Peer names are used by Peer Name Resolution Protocol (PNRP), the Peer Identity Manager, and the Peer Grouping Infrastructure.</span></span> <span data-ttu-id="87877-105">Os nomes de pares são nomes estáveis para recursos como computadores, usuários, grupos ou serviços.</span><span class="sxs-lookup"><span data-stu-id="87877-105">Peer names are stable names for resources such as computers, users, groups, or services.</span></span> <span data-ttu-id="87877-106">O PNRP usa nomes de pares para identificar nós em uma rede de mesmo nível.</span><span class="sxs-lookup"><span data-stu-id="87877-106">PNRP uses peer names to identify nodes in a peer network.</span></span>

> [!Note]  
> <span data-ttu-id="87877-107">Um ponto de extremidade usado pela infraestrutura de pares é, na verdade, uma tupla que consiste em um endereço IPv4 ou IPv6, porta e protocolo (TCP ou UDP).</span><span class="sxs-lookup"><span data-stu-id="87877-107">An endpoint that the Peer Infrastructure uses is actually a tuple that consists of an IPv4 or IPv6 address, port, and protocol (either TCP or UDP).</span></span> <span data-ttu-id="87877-108">Um nome de par pode ter mais de uma tupla.</span><span class="sxs-lookup"><span data-stu-id="87877-108">One peer name can have more than one tuple.</span></span>

 

<span data-ttu-id="87877-109">Um nome de par é uma cadeia de caracteres de texto que tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="87877-109">A peer name is a text string that has the following format:</span></span>

-   <span data-ttu-id="87877-110">"Authority. classificador"</span><span class="sxs-lookup"><span data-stu-id="87877-110">"Authority.Classifier"</span></span>

<span data-ttu-id="87877-111">O valor de uma autoridade depende de se o nome é seguro ou não.</span><span class="sxs-lookup"><span data-stu-id="87877-111">The value of an Authority depends on whether the name is secure or unsecured.</span></span> <span data-ttu-id="87877-112">O classificador de um nome de par é uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="87877-112">The Classifier of a peer name is a string.</span></span> <span data-ttu-id="87877-113">Um classificador pode ser qualquer nome que contenha 150 ou menos caracteres UNICODE.</span><span class="sxs-lookup"><span data-stu-id="87877-113">A Classifier can be any name that contains 150 or less UNICODE characters.</span></span> <span data-ttu-id="87877-114">Os nomes de pares diferenciam maiúsculas de minúsculas e podem ser registrados como protegidos ou não seguros.</span><span class="sxs-lookup"><span data-stu-id="87877-114">Peer names are case-sensitive and can be registered as secured or unsecured.</span></span> <span data-ttu-id="87877-115">A lista a seguir identifica alguns exemplos de nomes de pares:</span><span class="sxs-lookup"><span data-stu-id="87877-115">The following list identifies some examples of peer names:</span></span>

-   <span data-ttu-id="87877-116">"0. MyUnsecuredPeerName"</span><span class="sxs-lookup"><span data-stu-id="87877-116">"0.MyUnsecuredPeerName"</span></span>
-   <span data-ttu-id="87877-117">"0. davibarros. Games"</span><span class="sxs-lookup"><span data-stu-id="87877-117">"0.JohnDoe.Games"</span></span>
-   <span data-ttu-id="87877-118">"6520c005f63fc1864b7d8f3cabebd4916ae7f33d. Davibarros</span><span class="sxs-lookup"><span data-stu-id="87877-118">"6520c005f63fc1864b7d8f3cabebd4916ae7f33d.JohnDoe"</span></span>

## <a name="secure-peer-names"></a><span data-ttu-id="87877-119">Nomes de pares seguros</span><span class="sxs-lookup"><span data-stu-id="87877-119">Secure Peer Names</span></span>

<span data-ttu-id="87877-120">Para um nome seguro, a autoridade é o hash do SHA (algoritmo de hash seguro) da chave pública do nome do par e resulta em uma cadeia de caracteres hexadecimal de 40 caracteres.</span><span class="sxs-lookup"><span data-stu-id="87877-120">For a secure name, the Authority is the Secure Hash Algorithm (SHA) hash of the public key of the peer name, and results in a 40 character hexadecimal string.</span></span> <span data-ttu-id="87877-121">Um nome de par seguro só pode ser registrado com PNRP pelo proprietário ou pelo delegado do proprietário do nome de par.</span><span class="sxs-lookup"><span data-stu-id="87877-121">A secure peer name can only be registered with PNRP by the owner or delegate of the peer name owner.</span></span> <span data-ttu-id="87877-122">Um nome de par protegido deve ser criado chamando [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).</span><span class="sxs-lookup"><span data-stu-id="87877-122">A secured peer name must be created by calling [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).</span></span>

## <a name="unsecured-peer-names"></a><span data-ttu-id="87877-123">Nomes de pares não seguros</span><span class="sxs-lookup"><span data-stu-id="87877-123">Unsecured Peer Names</span></span>

<span data-ttu-id="87877-124">Para um nome não seguro, a autoridade é zero (0) e o classificador é a única parte significativa do nome de par, que cria um nome de par não seguro sem uma [identidade](identity-manager-api.md)associada.</span><span class="sxs-lookup"><span data-stu-id="87877-124">For an unsecured name, the Authority is zero (0), and the Classifier is the only significant part of the peer name, which creates an unsecured peer name without an associated [identity](identity-manager-api.md).</span></span> <span data-ttu-id="87877-125">Os nomes de pares não seguros são usados na resolução e no registro de nome PNRP.</span><span class="sxs-lookup"><span data-stu-id="87877-125">Unsecured peer names are used in PNRP name registration and resolution.</span></span> <span data-ttu-id="87877-126">Os nomes de pares não seguros fornecem uma maneira útil de registrar e resolver recursos que não exigem resolução de nomes segura.</span><span class="sxs-lookup"><span data-stu-id="87877-126">Unsecured peer names provide a useful way to register and resolve resources that do not require secure name resolution.</span></span> <span data-ttu-id="87877-127">No entanto, qualquer nó pode publicar qualquer nome não seguro.</span><span class="sxs-lookup"><span data-stu-id="87877-127">However, any node can publish any unsecured name.</span></span> <span data-ttu-id="87877-128">Os aplicativos preocupados com a segurança devem garantir que eles sejam robustos e protegidos em seu consumo de nomes de pares não seguros.</span><span class="sxs-lookup"><span data-stu-id="87877-128">Applications concerned with security must ensure that they are robust and secure in their consumption of unsecured peer names.</span></span>

> [!Note]  
> <span data-ttu-id="87877-129">Qualquer pessoa pode registrar um nome de par não seguro com o PNRP.</span><span class="sxs-lookup"><span data-stu-id="87877-129">Anyone can register an unsecured peer name with PNRP.</span></span>

 

## <a name="pnrp-and-the-nearest-peer-name-instance"></a><span data-ttu-id="87877-130">PNRP e a instância de nome de par mais próxima</span><span class="sxs-lookup"><span data-stu-id="87877-130">PNRP and the Nearest Peer Name Instance</span></span>

<span data-ttu-id="87877-131">Pode haver mais de uma instância de um nome de par.</span><span class="sxs-lookup"><span data-stu-id="87877-131">There can be more than one instance of a peer name.</span></span> <span data-ttu-id="87877-132">Ao usar o [PNRP](pnrp-namespace-provider-api.md) para resolver um nome de par, há um conceito de uma instância de nome de par **mais próximo** , o que significa que o nome tem um local de serviço mais próximo do membro **saHint** especificado em [**PNRPINFO \_ v1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) ou [**PNRPINFO \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="87877-132">When using [PNRP](pnrp-namespace-provider-api.md) to resolve a peer name, there is a concept of a **nearest** peer name instance, which means that the name has a service location closest to the **saHint** member specified in [**PNRPINFO\_V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) or [**PNRPINFO\_V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)).</span></span> <span data-ttu-id="87877-133">Se nenhuma dica for fornecida, mais próximo de um dos endereços IP locais.</span><span class="sxs-lookup"><span data-stu-id="87877-133">If no hint is supplied, closest to one of the local IP addresses.</span></span>

 

 
