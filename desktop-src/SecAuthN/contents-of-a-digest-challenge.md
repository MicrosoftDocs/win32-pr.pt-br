---
description: O tamanho de um desafio de acesso de resumo deve ser inferior a 2048 bytes.
ms.assetid: 16c6728a-966b-436f-902d-3e12368986b6
title: Conteúdo de um desafio de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f90dd78ae28536f6e2d07882f69335975df14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089954"
---
# <a name="contents-of-a-digest-challenge"></a><span data-ttu-id="56041-103">Conteúdo de um desafio de resumo</span><span class="sxs-lookup"><span data-stu-id="56041-103">Contents of a Digest Challenge</span></span>

<span data-ttu-id="56041-104">O tamanho de um desafio de acesso de resumo deve ser inferior a 2048 bytes.</span><span class="sxs-lookup"><span data-stu-id="56041-104">The size of a Digest Access challenge must be less than 2048 bytes.</span></span> <span data-ttu-id="56041-105">O exemplo a seguir mostra um desafio atribuído à cadeia de caracteres szChallenge.</span><span class="sxs-lookup"><span data-stu-id="56041-105">The following example shows a challenge assigned to the character string szChallenge.</span></span>


```C++
szChallenge = "realm=\"Microsoft_Example_Forest\",";
algorithm = "MD5-sess\", qop=\"auth\", nonce=\"0123456789abcdef\"";
```



> [!Note]  
> <span data-ttu-id="56041-106">A cadeia de caracteres de desafio é colocada entre aspas duplas e contém aspas duplas inseridas.</span><span class="sxs-lookup"><span data-stu-id="56041-106">The challenge string is enclosed in double quotes and contains embedded double quotes.</span></span> <span data-ttu-id="56041-107">Aspas duplas inseridas devem ser precedidas (escape) com uma barra invertida ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="56041-107">Embedded double quotes must be preceded (escaped) with a backslash (\\).</span></span>

 

<span data-ttu-id="56041-108">Um desafio de resumo pode conter as seguintes diretivas.</span><span class="sxs-lookup"><span data-stu-id="56041-108">A Digest challenge can contain the following directives.</span></span>



| <span data-ttu-id="56041-109">Diretiva</span><span class="sxs-lookup"><span data-stu-id="56041-109">Directive</span></span>         | <span data-ttu-id="56041-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="56041-110">Description</span></span>                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56041-111">territórios</span><span class="sxs-lookup"><span data-stu-id="56041-111">realm</span></span>             | <span data-ttu-id="56041-112">Uma dica definida pela implementação para o cliente sobre quais [*credenciais*](/windows/desktop/SecGloss/c-gly) são necessárias.</span><span class="sxs-lookup"><span data-stu-id="56041-112">An implementation-defined hint to the client about which [*credentials*](/windows/desktop/SecGloss/c-gly) are required.</span></span> <span data-ttu-id="56041-113">O cliente deve exibir essas informações para o usuário se ele estiver solicitando credenciais.</span><span class="sxs-lookup"><span data-stu-id="56041-113">The client should display this information to the user if it is prompting for credentials.</span></span>                                                  |
| <span data-ttu-id="56041-114">algoritmo</span><span class="sxs-lookup"><span data-stu-id="56041-114">algorithm</span></span>         | <span data-ttu-id="56041-115">Microsoft Digest dá suporte a MD5 e MD5-sess.</span><span class="sxs-lookup"><span data-stu-id="56041-115">Microsoft Digest supports MD5 and MD5-Sess.</span></span> <span data-ttu-id="56041-116">Para obter um desempenho ideal, use MD5-sess.</span><span class="sxs-lookup"><span data-stu-id="56041-116">For optimal performance, use MD5-Sess.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="56041-117">qop</span><span class="sxs-lookup"><span data-stu-id="56041-117">qop</span></span>               | <span data-ttu-id="56041-118">Essa diretiva pode ser definida como auth, auth-int ou auth-conf.</span><span class="sxs-lookup"><span data-stu-id="56041-118">This directive can be set to auth, auth-int, or auth-conf.</span></span> <span data-ttu-id="56041-119">Para obter mais informações, consulte [qualidade de proteção e codificações](quality-of-protection-and-ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="56041-119">For more information, see [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).</span></span>                                                                                                                                       |
| <span data-ttu-id="56041-120">nonce</span><span class="sxs-lookup"><span data-stu-id="56041-120">nonce</span></span>             | <span data-ttu-id="56041-121">Um valor codificado exclusivo gerado pelo servidor para cada desafio.</span><span class="sxs-lookup"><span data-stu-id="56041-121">A unique encoded value generated by the server for each challenge.</span></span> <span data-ttu-id="56041-122">Esse valor não deve ser alterado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="56041-122">This value must not be altered by the client.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="56041-123">opaco</span><span class="sxs-lookup"><span data-stu-id="56041-123">opaque</span></span>            | <span data-ttu-id="56041-124">Contém uma referência para o [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) que está sendo estabelecido.</span><span class="sxs-lookup"><span data-stu-id="56041-124">Contains a reference for the [*security context*](/windows/desktop/SecGloss/s-gly) that is being established.</span></span> <span data-ttu-id="56041-125">Para obter mais informações, consulte [mantendo o contexto de segurança entre conexões](maintaining-the-security-context-between-connections.md).</span><span class="sxs-lookup"><span data-stu-id="56041-125">For more information, see [Maintaining the Security Context Between Connections](maintaining-the-security-context-between-connections.md).</span></span> |
| <span data-ttu-id="56041-126">cipher (somente SASL)</span><span class="sxs-lookup"><span data-stu-id="56041-126">cipher(SASL only)</span></span> | <span data-ttu-id="56041-127">A lista de codificações às quais o servidor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="56041-127">The list of ciphers that the server supports.</span></span> <span data-ttu-id="56041-128">Esse elemento pode estar presente em um desafio de Digest SASL somente se a diretiva QoP especifica auth-conf.</span><span class="sxs-lookup"><span data-stu-id="56041-128">This element can be present in a Digest SASL challenge only if the qop directive specifies auth-conf.</span></span> <span data-ttu-id="56041-129">Para obter mais informações, consulte [qualidade de proteção e codificações](quality-of-protection-and-ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="56041-129">For more information, see [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).</span></span>                                              |
| <span data-ttu-id="56041-130">charset</span><span class="sxs-lookup"><span data-stu-id="56041-130">charset</span></span>           | <span data-ttu-id="56041-131">Essa diretiva pode ser definida como UTF-8 se o servidor puder processar nomes de usuário e territórios codificados em UTF-8.</span><span class="sxs-lookup"><span data-stu-id="56041-131">This directive can be set to utf-8 if the server can process UTF-8–encoded user names and realms.</span></span> <span data-ttu-id="56041-132">Se o cliente compreender a diretiva charset, ele poderá responder usando valores codificados em UTF-8.</span><span class="sxs-lookup"><span data-stu-id="56041-132">If the client understands the charset directive, it can respond by using UTF-8–encoded values.</span></span>                                                                                                       |



 

<span data-ttu-id="56041-133">Microsoft Digest gera a cadeia de caracteres de desafio Digest para aplicativos de servidor.</span><span class="sxs-lookup"><span data-stu-id="56041-133">Microsoft Digest generates the Digest challenge string for server applications.</span></span> <span data-ttu-id="56041-134">Para obter detalhes, consulte [gerando o desafio Digest](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="56041-134">For details, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

 

 
