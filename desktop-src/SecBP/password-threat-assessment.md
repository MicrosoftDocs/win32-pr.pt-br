---
description: Antes de implementar o código que protege as senhas, é melhor analisar seu ambiente específico de maneiras que um invasor possa tentar penetrar nas defesas de software.
ms.assetid: 4ebf7185-0179-4754-80da-63b0002c883f
title: Avaliação de ameaças de senha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48a79d44bda9714083c5dd1085e9d09497e7341
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756691"
---
# <a name="password-threat-assessment"></a><span data-ttu-id="a4af2-103">Avaliação de ameaças de senha</span><span class="sxs-lookup"><span data-stu-id="a4af2-103">Password Threat Assessment</span></span>

<span data-ttu-id="a4af2-104">Antes de implementar o código que protege as senhas, é melhor analisar seu ambiente específico de maneiras que um invasor possa tentar penetrar nas defesas de software.</span><span class="sxs-lookup"><span data-stu-id="a4af2-104">Before implementing code that protects passwords, it is best to analyze your particular environment for ways that an attacker might try to penetrate software defenses.</span></span>

<span data-ttu-id="a4af2-105">Comece analisando sua arquitetura de rede ou de sistema.</span><span class="sxs-lookup"><span data-stu-id="a4af2-105">Start by analyzing your network or system architecture.</span></span> <span data-ttu-id="a4af2-106">Estes são alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="a4af2-106">Here are some examples:</span></span>

-   <span data-ttu-id="a4af2-107">O número de senhas que devem ser protegidas.</span><span class="sxs-lookup"><span data-stu-id="a4af2-107">The number of passwords that must be protected.</span></span> <span data-ttu-id="a4af2-108">É necessária uma senha para fazer logon no computador local?</span><span class="sxs-lookup"><span data-stu-id="a4af2-108">Is a password required to log on to the local computer?</span></span> <span data-ttu-id="a4af2-109">A mesma senha é usada para fazer logon na rede?</span><span class="sxs-lookup"><span data-stu-id="a4af2-109">Is the same password used to log on to the network?</span></span> <span data-ttu-id="a4af2-110">As senhas são propagadas para mais de um servidor na rede?</span><span class="sxs-lookup"><span data-stu-id="a4af2-110">Are passwords propagated to more than one server on the network?</span></span> <span data-ttu-id="a4af2-111">Quantas senhas devem ser acomodadas?</span><span class="sxs-lookup"><span data-stu-id="a4af2-111">How many passwords must be accommodated?</span></span>
-   <span data-ttu-id="a4af2-112">O tipo de rede (se houver) que será usado.</span><span class="sxs-lookup"><span data-stu-id="a4af2-112">The kind of network (if any) that will be used.</span></span> <span data-ttu-id="a4af2-113">A rede é implementada usando um sistema de diretório corporativo (como LDAP) e sua arquitetura de senha é usada?</span><span class="sxs-lookup"><span data-stu-id="a4af2-113">Is the network implemented using a corporate directory system (such as LDAP), and is its password architecture used?</span></span> <span data-ttu-id="a4af2-114">Os objetos estão armazenando senhas não criptografadas?</span><span class="sxs-lookup"><span data-stu-id="a4af2-114">Are any objects storing unencrypted passwords?</span></span>
-   <span data-ttu-id="a4af2-115">Abrir rede versus fechada.</span><span class="sxs-lookup"><span data-stu-id="a4af2-115">Open versus closed network.</span></span> <span data-ttu-id="a4af2-116">A rede é independente ou está aberta para o exterior?</span><span class="sxs-lookup"><span data-stu-id="a4af2-116">Is the network self-contained or is it open to the outside?</span></span> <span data-ttu-id="a4af2-117">Nesse caso, ele é protegido por um firewall?</span><span class="sxs-lookup"><span data-stu-id="a4af2-117">If so, is it protected by a firewall?</span></span>
-   <span data-ttu-id="a4af2-118">Acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="a4af2-118">Remote access.</span></span> <span data-ttu-id="a4af2-119">Os usuários precisarão acessar a rede de um local remoto?</span><span class="sxs-lookup"><span data-stu-id="a4af2-119">Will users need to access the network from a remote location?</span></span>

<span data-ttu-id="a4af2-120">Depois de analisar o sistema ou a arquitetura de rede, você pode começar a analisar como um invasor pode tentar atacar.</span><span class="sxs-lookup"><span data-stu-id="a4af2-120">After you have analyzed your system or network architecture, then you can start to analyze how an attacker might try to attack it.</span></span> <span data-ttu-id="a4af2-121">Aqui estão algumas possibilidades:</span><span class="sxs-lookup"><span data-stu-id="a4af2-121">Here are some possibilities:</span></span>

-   <span data-ttu-id="a4af2-122">Ler uma senha não criptografada do registro de um computador.</span><span class="sxs-lookup"><span data-stu-id="a4af2-122">Read an unencrypted password from a computer's registry.</span></span>
-   <span data-ttu-id="a4af2-123">Ler uma senha não criptografada que é embutida no software.</span><span class="sxs-lookup"><span data-stu-id="a4af2-123">Read an unencrypted password that is hard-coded in the software.</span></span>
-   <span data-ttu-id="a4af2-124">Ler uma senha não criptografada na página de código trocado de um computador.</span><span class="sxs-lookup"><span data-stu-id="a4af2-124">Read an unencrypted password from a computer's swapped-out code page.</span></span>
-   <span data-ttu-id="a4af2-125">Ler uma senha do log de eventos de um programa.</span><span class="sxs-lookup"><span data-stu-id="a4af2-125">Read a password from a program's event log.</span></span>
-   <span data-ttu-id="a4af2-126">Leia uma senha de um esquema de serviço de diretório do Microsoft Active Directory estendido que tenha objetos que contenham uma senha de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="a4af2-126">Read a password from an extended Microsoft Active Directory directory service schema that has objects that contain a plaintext password.</span></span>
-   <span data-ttu-id="a4af2-127">Execute um depurador em um programa que exija uma senha.</span><span class="sxs-lookup"><span data-stu-id="a4af2-127">Run a debugger on a program that requires a password.</span></span>
-   <span data-ttu-id="a4af2-128">Adivinhe uma senha.</span><span class="sxs-lookup"><span data-stu-id="a4af2-128">Guess a password.</span></span> <span data-ttu-id="a4af2-129">Qualquer uma das várias técnicas pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="a4af2-129">Any of several techniques might be used.</span></span> <span data-ttu-id="a4af2-130">Por exemplo, o invasor pode saber algumas informações pessoais sobre um usuário e tentar adivinhar uma senha dessas informações (por exemplo, o nome de um cônjuge ou parceiro ou filho).</span><span class="sxs-lookup"><span data-stu-id="a4af2-130">For example, the attacker might know some personal information about a user and try to guess a password from that information (for example, the name of a spouse/partner or child).</span></span> <span data-ttu-id="a4af2-131">Ou, um método de força bruta pode ser tentado, onde todas as combinações de letras, números e pontuações são tentadas (somente viáveis onde são usadas senhas curtas).</span><span class="sxs-lookup"><span data-stu-id="a4af2-131">Or, a brute-force method might be tried, where all combinations of letters, numbers, and punctuation are tried (only feasible where short passwords are used).</span></span>

<span data-ttu-id="a4af2-132">Comparar as possíveis metodologias de ataque com a arquitetura de rede ou sistema provavelmente revelará os riscos de segurança.</span><span class="sxs-lookup"><span data-stu-id="a4af2-132">Comparing the possible attack methodologies with system or network architecture will likely reveal security risks.</span></span> <span data-ttu-id="a4af2-133">Nesse ponto, um fator de risco pode ser estabelecido para cada risco, e os fatores de risco podem ser usados para fazer a triagem de correções.</span><span class="sxs-lookup"><span data-stu-id="a4af2-133">At that point, a risk factor can be established for each risk, and the risk factors can be used to triage fixes.</span></span>

 

 



