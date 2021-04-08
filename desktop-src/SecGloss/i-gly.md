---
description: Contém definições de termos de segurança que começam com a letra I.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: af511aed-88f5-4b12-ad44-317925297f70
title: I (Glossário de segurança)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d3e727128c2494f313bdffc879b5c5e47a28ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011360"
---
# <a name="i-security-glossary"></a><span data-ttu-id="92063-103">I (Glossário de segurança)</span><span class="sxs-lookup"><span data-stu-id="92063-103">I (Security Glossary)</span></span>

<span data-ttu-id="92063-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) i J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="92063-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) I J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="92063-105"><span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**IIS**</span><span class="sxs-lookup"><span data-stu-id="92063-105"><span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**IIS**</span></span>
</dt> <dd>

<span data-ttu-id="92063-106">Serviços de software que dão suporte à criação, configuração e gerenciamento de sites, juntamente com outras funções de Internet.</span><span class="sxs-lookup"><span data-stu-id="92063-106">Software services that support website creation, configuration, and management, along with other Internet functions.</span></span> <span data-ttu-id="92063-107">Os Serviços de Informações da Internet incluem o protocolo NNTP (rede de transferência de notícias), o protocolo FTP (FTP) e o protocolo SMTP.</span><span class="sxs-lookup"><span data-stu-id="92063-107">Internet Information Services include Network News Transfer Protocol (NNTP), File Transfer Protocol (FTP), and Simple Mail Transfer Protocol (SMTP).</span></span> <span data-ttu-id="92063-108">O IIS incorpora várias funções de segurança, permite aplicativos CGI e fornece servidores de Gopher e FTP.</span><span class="sxs-lookup"><span data-stu-id="92063-108">IIS incorporates various functions for security, allows for CGI applications, and provides for Gopher and FTP servers.</span></span>

</dd> <dt>

<span data-ttu-id="92063-109"><span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**representação**</span><span class="sxs-lookup"><span data-stu-id="92063-109"><span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**impersonation**</span></span>
</dt> <dd>

<span data-ttu-id="92063-110">Um mecanismo que permite a execução de um processo do servidor usando as credenciais de segurança do cliente ou outro usuário usando as credenciais.</span><span class="sxs-lookup"><span data-stu-id="92063-110">A mechanism that allows a server process to run by using the security credentials of the client or some other user using the credentials.</span></span> <span data-ttu-id="92063-111">Quando o servidor está representando o cliente, todas as operações executadas pelo servidor são executadas usando as credenciais do cliente (representando o usuário).</span><span class="sxs-lookup"><span data-stu-id="92063-111">When the server is impersonating the client, any operations performed by the server are performed by using the client's (impersonating user's) credentials.</span></span> <span data-ttu-id="92063-112">A representação não permite que o servidor acesse recursos remotos em nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="92063-112">Impersonation does not allow the server to access remote resources on behalf of the client.</span></span> <span data-ttu-id="92063-113">Isso requer delegação.</span><span class="sxs-lookup"><span data-stu-id="92063-113">This requires delegation.</span></span>

</dd> <dt>

<span data-ttu-id="92063-114"><span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**token de representação**</span><span class="sxs-lookup"><span data-stu-id="92063-114"><span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**impersonation token**</span></span>
</dt> <dd>

<span data-ttu-id="92063-115">Um token de acesso que foi criado para capturar as informações de segurança de um processo de cliente, permitindo que um servidor "represente" o processo do cliente em operações de segurança.</span><span class="sxs-lookup"><span data-stu-id="92063-115">An access token that has been created to capture the security information of a client process, allowing a server to "impersonate" the client process in security operations.</span></span>

<span data-ttu-id="92063-116">Consulte também [*token de acesso*](a-gly.md) e [*token primário*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="92063-116">See also [*access token*](a-gly.md) and [*primary token*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="92063-117"><span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**vetor de inicialização**</span><span class="sxs-lookup"><span data-stu-id="92063-117"><span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**initialization vector**</span></span>
</dt> <dd>

<span data-ttu-id="92063-118">(IV) uma sequência de bytes aleatórios acrescentados à frente do texto não criptografado antes da criptografia por uma codificação de bloco.</span><span class="sxs-lookup"><span data-stu-id="92063-118">(IV) A sequence of random bytes appended to the front of the plaintext before encryption by a block cipher.</span></span> <span data-ttu-id="92063-119">Adicionar o vetor de inicialização ao início do texto não criptografado elimina a possibilidade de que o texto cifrado inicial seja o mesmo para duas mensagens.</span><span class="sxs-lookup"><span data-stu-id="92063-119">Adding the initialization vector to the beginning of the plaintext eliminates the possibility of having the initial ciphertext block the same for any two messages.</span></span> <span data-ttu-id="92063-120">Por exemplo, se as mensagens são sempre iniciadas com um cabeçalho comum (um timbre ou uma linha "de"), seu texto cifrado inicial sempre será o mesmo, supondo que o mesmo algoritmo criptográfico e a chave simétrica foram usados.</span><span class="sxs-lookup"><span data-stu-id="92063-120">For example, if messages always start with a common header (a letterhead or "From" line) their initial ciphertext would always be the same, assuming that the same cryptographic algorithm and symmetric key was used.</span></span> <span data-ttu-id="92063-121">A adição de um vetor de inicialização aleatório elimina isso de acontecer.</span><span class="sxs-lookup"><span data-stu-id="92063-121">Adding a random initialization vector eliminates this from happening.</span></span>

</dd> <dt>

<span data-ttu-id="92063-122"><span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**dados internos**</span><span class="sxs-lookup"><span data-stu-id="92063-122"><span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**inner data**</span></span>
</dt> <dd>

<span data-ttu-id="92063-123">Todos os dados codificados usados como a mensagem para outra mensagem codificada.</span><span class="sxs-lookup"><span data-stu-id="92063-123">Any encoded data used as the message for another encoded message.</span></span> <span data-ttu-id="92063-124">Por exemplo, uma mensagem envelopada e seu valor de hash podem ser os dados internos de uma segunda mensagem.</span><span class="sxs-lookup"><span data-stu-id="92063-124">For example, an enveloped message and its hash value may be the inner data for a second message.</span></span>

</dd> <dt>

<span data-ttu-id="92063-125"><span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**conteúdo interno**</span><span class="sxs-lookup"><span data-stu-id="92063-125"><span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**inner content**</span></span>
</dt> <dd>

<span data-ttu-id="92063-126">Dados aprimorados, como com uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="92063-126">Data that is enhanced, such as with a digital signature.</span></span> <span data-ttu-id="92063-127">Esse termo é usado principalmente ao discutir dados aprimorados em uma \# mensagem PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="92063-127">This term is used primarily when discussing enhanced data in a PKCS \#7 message.</span></span>

</dd> <dt>

<span data-ttu-id="92063-128"><span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**verifica**</span><span class="sxs-lookup"><span data-stu-id="92063-128"><span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**integrity**</span></span>
</dt> <dd>

<span data-ttu-id="92063-129">A integridade e a precisão de uma mensagem após ela ser enviada ou armazenada.</span><span class="sxs-lookup"><span data-stu-id="92063-129">The completeness and accuracy of a message after it has been sent or stored.</span></span>

</dd> <dt>

<span data-ttu-id="92063-130"><span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**SID de integridade**</span><span class="sxs-lookup"><span data-stu-id="92063-130"><span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**integrity SID**</span></span>
</dt> <dd>

<span data-ttu-id="92063-131">Um SID ( [*identificador de segurança*](s-gly.md) ) que representa um nível de integridade.</span><span class="sxs-lookup"><span data-stu-id="92063-131">A [*security identifier*](s-gly.md) (SID) that represents an integrity level.</span></span> <span data-ttu-id="92063-132">Um SID de integridade na SACL ( [*lista de controle de acesso do sistema*](s-gly.md) ) do descritor de segurança de um objeto especifica o nível de integridade do objeto.</span><span class="sxs-lookup"><span data-stu-id="92063-132">An integrity SID in the [*system access control list*](s-gly.md) (SACL) of an object's security descriptor specifies the integrity level of the object.</span></span> <span data-ttu-id="92063-133">Os SIDs de integridade em um token de acesso especificam o nível de integridade do token.</span><span class="sxs-lookup"><span data-stu-id="92063-133">Integrity SIDs in an access token specify the integrity level of the token.</span></span>

</dd> <dt>

<span data-ttu-id="92063-134"><span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**</span><span class="sxs-lookup"><span data-stu-id="92063-134"><span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**</span></span>
</dt> <dd>

<span data-ttu-id="92063-135">Um IRQL (nível de solicitação de interrupção) define a prioridade de hardware na qual um processador opera em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="92063-135">An interrupt request level (IRQL) defines the hardware priority at which a processor operates at any given time.</span></span> <span data-ttu-id="92063-136">Na Windows Driver Model, um thread em execução em um IRQL baixo pode ser interrompido para executar o código em um IRQL mais alto.</span><span class="sxs-lookup"><span data-stu-id="92063-136">In the Windows Driver Model, a thread running at a low IRQL can be interrupted to run code at a higher IRQL.</span></span>

</dd> <dt>

<span data-ttu-id="92063-137"><span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**IV**</span><span class="sxs-lookup"><span data-stu-id="92063-137"><span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**IV**</span></span>
</dt> <dd>

<span data-ttu-id="92063-138">Consulte *vetor de inicialização*.</span><span class="sxs-lookup"><span data-stu-id="92063-138">See *initialization vector*.</span></span>

</dd> </dl>

 

 



