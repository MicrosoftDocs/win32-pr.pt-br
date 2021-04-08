---
description: Explica os dois tipos de credenciais com os quais a API de gerenciamento de credenciais funciona.
ms.assetid: eaf1c298-f0af-4b29-a09a-f399da20335d
title: Tipos de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30968484b2cfc89b9238f624d9299fb75c72bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921900"
---
# <a name="kinds-of-credentials"></a><span data-ttu-id="64d4e-103">Tipos de credenciais</span><span class="sxs-lookup"><span data-stu-id="64d4e-103">Kinds of Credentials</span></span>

<span data-ttu-id="64d4e-104">A API de gerenciamento de credenciais funciona com dois tipos de credenciais:</span><span class="sxs-lookup"><span data-stu-id="64d4e-104">The Credentials Management API works with two kinds of credentials:</span></span>

-   [<span data-ttu-id="64d4e-105">Credenciais do domínio</span><span class="sxs-lookup"><span data-stu-id="64d4e-105">Domain Credentials</span></span>](#domain-credentials)
-   [<span data-ttu-id="64d4e-106">Credenciais genéricas</span><span class="sxs-lookup"><span data-stu-id="64d4e-106">Generic Credentials</span></span>](#generic-credentials)

## <a name="domain-credentials"></a><span data-ttu-id="64d4e-107">Credenciais do domínio</span><span class="sxs-lookup"><span data-stu-id="64d4e-107">Domain Credentials</span></span>

<span data-ttu-id="64d4e-108">As credenciais de domínio são usadas pelo sistema operacional e autenticadas pela autoridade de segurança local (LSA).</span><span class="sxs-lookup"><span data-stu-id="64d4e-108">Domain credentials are used by the operating system and authenticated by the Local Security Authority (LSA).</span></span> <span data-ttu-id="64d4e-109">Normalmente, as credenciais de domínio são estabelecidas para um usuário quando um pacote de segurança registrado, como o protocolo Kerberos, autentica os dados de logon fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="64d4e-109">Typically, domain credentials are established for a user when a registered security package, such as the Kerberos protocol, authenticates logon data that is provided by the user.</span></span> <span data-ttu-id="64d4e-110">As credenciais de logon são armazenadas em cache pelo sistema operacional para que um logon único forneça ao usuário acesso a vários recursos diferentes.</span><span class="sxs-lookup"><span data-stu-id="64d4e-110">The logon credentials are cached by the operating system so that a single sign-on gives the user access to many different resources.</span></span> <span data-ttu-id="64d4e-111">Por exemplo, as conexões de rede podem ocorrer de forma transparente e o acesso a objetos protegidos do sistema pode ser concedido com base nas credenciais de domínio em cache do usuário.</span><span class="sxs-lookup"><span data-stu-id="64d4e-111">For example, network connections can occur transparently, and access to protected system objects can be granted based on the user's cached domain credentials.</span></span>

<span data-ttu-id="64d4e-112">As funções de gerenciamento de credenciais fornecem um mecanismo para que os aplicativos solicitem a um usuário as credenciais de domínio depois que o usuário faz logon e que o sistema operacional autentique as informações fornecidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="64d4e-112">Credentials Management functions provide a mechanism for applications to prompt a user for domain credentials after the user logs on, and to have the operating system authenticate the information that is provided by the user.</span></span>

<span data-ttu-id="64d4e-113">A parte secreta das credenciais de domínio, a senha, é protegida pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="64d4e-113">The secret part of domain credentials, the password, is protected by the operating system.</span></span> <span data-ttu-id="64d4e-114">Somente o código em execução no processo com o LSA pode ler e gravar credenciais de domínio.</span><span class="sxs-lookup"><span data-stu-id="64d4e-114">Only code running in-process with the LSA can read and write domain credentials.</span></span> <span data-ttu-id="64d4e-115">Os aplicativos são limitados à gravação de credenciais de domínio.</span><span class="sxs-lookup"><span data-stu-id="64d4e-115">Applications are limited to writing domain credentials.</span></span>

<span data-ttu-id="64d4e-116">O Windows dá suporte ao uso expandido de credenciais de cartão inteligente e certificado.</span><span class="sxs-lookup"><span data-stu-id="64d4e-116">Windows supports expanded use of smart card and certificate credentials.</span></span> <span data-ttu-id="64d4e-117">Para ajudar a garantir a segurança, a API de gerenciamento de credenciais nunca armazena o PIN do cartão inteligente no computador.</span><span class="sxs-lookup"><span data-stu-id="64d4e-117">To help ensure security, the Credentials Management API never stores the smart card PIN on the computer.</span></span>

## <a name="generic-credentials"></a><span data-ttu-id="64d4e-118">Credenciais genéricas</span><span class="sxs-lookup"><span data-stu-id="64d4e-118">Generic Credentials</span></span>

<span data-ttu-id="64d4e-119">As credenciais genéricas são definidas e autenticadas por aplicativos que gerenciam a autorização e a segurança diretamente em vez de delegar essas tarefas para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="64d4e-119">Generic credentials are defined and authenticated by applications that manage authorization and security directly instead of delegating these tasks to the operating system.</span></span> <span data-ttu-id="64d4e-120">Por exemplo, um aplicativo pode exigir que os usuários insiram um nome de usuário e senha fornecidos pelo aplicativo ou produzam um [*certificado*](../secgloss/c-gly.md) para acessar um site.</span><span class="sxs-lookup"><span data-stu-id="64d4e-120">For example, an application can require users to enter a user name and password provided by the application or to produce a [*certificate*](../secgloss/c-gly.md) to access a website.</span></span>

<span data-ttu-id="64d4e-121">Os aplicativos usam funções de gerenciamento de credenciais para solicitar aos usuários informações de credenciais, genéricas e definidas pelo aplicativo, como nome de usuário, certificado, cartão inteligente ou senha.</span><span class="sxs-lookup"><span data-stu-id="64d4e-121">Applications use Credentials Management functions to prompt users for application-defined, generic, credential information, such as user name, certificate, smart card, or password.</span></span> <span data-ttu-id="64d4e-122">As informações inseridas pelo usuário são retornadas ao aplicativo para autenticação.</span><span class="sxs-lookup"><span data-stu-id="64d4e-122">The information entered by the user is returned to the application for authentication.</span></span>

<span data-ttu-id="64d4e-123">O gerenciamento de credenciais fornece gerenciamento de cache personalizável e armazenamento de longo prazo para credenciais genéricas.</span><span class="sxs-lookup"><span data-stu-id="64d4e-123">Credentials Management provides customizable cache management and long-term storage for generic credentials.</span></span> <span data-ttu-id="64d4e-124">As credenciais genéricas podem ser lidas e gravadas por processos de usuário.</span><span class="sxs-lookup"><span data-stu-id="64d4e-124">Generic credentials can be read and written by user processes.</span></span>

 

 
