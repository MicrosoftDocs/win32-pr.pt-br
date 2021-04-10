---
description: A Microsoft fornece o \_ pacote de autenticação MSV1 0 para logons do computador local que não exigem autenticação personalizada.
ms.assetid: 8b85588d-0a79-43af-b526-7a5fc8248f99
title: MSV1_0 pacote de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 662ae65f60bec61c30b12271a34dc9d3c2883d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170811"
---
# <a name="msv1_0-authentication-package"></a><span data-ttu-id="4d028-103">Pacote de autenticação do MSV1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4d028-103">MSV1\_0 Authentication Package</span></span>

<span data-ttu-id="4d028-104">A Microsoft fornece o \_ [*pacote de autenticação*](../secgloss/a-gly.md) MSV1 0 para logons do computador local que não exigem autenticação personalizada.</span><span class="sxs-lookup"><span data-stu-id="4d028-104">Microsoft provides the MSV1\_0 [*authentication package*](../secgloss/a-gly.md) for local machine logons that do not require custom authentication.</span></span> <span data-ttu-id="4d028-105">A [*autoridade de segurança local*](../secgloss/l-gly.md) (LSA) chama o \_ pacote de autenticação MSV1 0 para processar os dados de logon coletados pela [*Gina*](../secgloss/g-gly.md) para o processo de logon do [*Winlogon*](../secgloss/w-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4d028-105">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) calls the MSV1\_0 authentication package to process logon data collected by the [*GINA*](../secgloss/g-gly.md) for the [*Winlogon*](../secgloss/w-gly.md) logon process.</span></span> <span data-ttu-id="4d028-106">O \_ pacote MSV1 0 verifica o banco de dados do Sam (Gerenciador de contas de segurança) local para determinar se o logon pertence a uma [*entidade de segurança*](../secgloss/s-gly.md) válida e, em seguida, retorna o resultado da tentativa de logon para o LSA.</span><span class="sxs-lookup"><span data-stu-id="4d028-106">The MSV1\_0 package checks the local security accounts manager (SAM) database to determine whether the logon data belongs to a valid [*security principal*](../secgloss/s-gly.md) and then returns the result of the logon attempt to the LSA.</span></span>

<span data-ttu-id="4d028-107">O MSV1 \_ 0 também dá suporte a logons de domínio.</span><span class="sxs-lookup"><span data-stu-id="4d028-107">MSV1\_0 also supports domain logons.</span></span> <span data-ttu-id="4d028-108">MSV1 \_ 0 processa logons de domínio usando a autenticação de passagem, conforme ilustrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d028-108">MSV1\_0 processes domain logons using pass-through authentication, as illustrated in the following diagram.</span></span>

![pacote de autenticação do msv1 \- 0](images/lsaint4.png)

<span data-ttu-id="4d028-110">Na autenticação de passagem, a instância local do MSV1 \_ 0 usa o serviço Netlogon para chamar a instância do MSV1 \_ 0 em execução no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="4d028-110">In pass-through authentication, the local instance of MSV1\_0 uses the Netlogon service to call the instance of MSV1\_0 running on the domain controller.</span></span> <span data-ttu-id="4d028-111">A instância do controlador de domínio de MSV1 \_ 0 verifica o banco de dados Sam do controlador de domínio e retorna o resultado do logon à instância do MSV1 \_ 0 no computador local.</span><span class="sxs-lookup"><span data-stu-id="4d028-111">The domain controller's instance of MSV1\_0 then checks the SAM database of the domain controller and returns the logon result to the instance of MSV1\_0 on the local machine.</span></span> <span data-ttu-id="4d028-112">A versão local do MSV1 \_ 0 encaminha o resultado do logon para a instância do LSA no computador local.</span><span class="sxs-lookup"><span data-stu-id="4d028-112">The local version of MSV1\_0 forwards the logon result to the instance of the LSA on the local machine.</span></span>

<span data-ttu-id="4d028-113">Se o controlador de domínio não estiver disponível e a LSA contiver [*credenciais*](../secgloss/c-gly.md) armazenadas em cache para o usuário, a instância local do MSV1 \_ 0 poderá autenticar o usuário usando os dados de logon armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="4d028-113">If the domain controller is not available, and the LSA contains cached [*credentials*](../secgloss/c-gly.md) for the user, the local instance of MSV1\_0 can authenticate the user using the cached logon data.</span></span>

<span data-ttu-id="4d028-114">O \_ pacote de autenticação MSV1 0 também dá suporte a [pacotes de subautenticação](subauthentication-packages.md).</span><span class="sxs-lookup"><span data-stu-id="4d028-114">The MSV1\_0 authentication package also supports [subauthentication packages](subauthentication-packages.md).</span></span> <span data-ttu-id="4d028-115">Um pacote de subautenticação é uma DLL que pode substituir parte dos critérios de autenticação e validação usados pelo \_ pacote de autenticação MSV1 0.</span><span class="sxs-lookup"><span data-stu-id="4d028-115">A subauthentication package is a DLL that can replace part of the authentication and validation criteria used by the MSV1\_0 authentication package.</span></span>

<span data-ttu-id="4d028-116">O \_ pacote de autenticação MSV1 0 define um par de chaves/valor de cadeia de caracteres de [*credenciais primários*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4d028-116">The MSV1\_0 authentication package defines a [*primary credentials*](../secgloss/p-gly.md) key/string value pair.</span></span> <span data-ttu-id="4d028-117">A cadeia de credenciais primária contém as credenciais derivadas dos dados fornecidos no momento do logon.</span><span class="sxs-lookup"><span data-stu-id="4d028-117">The primary credentials string holds the credentials derived from the data provided at logon time.</span></span> <span data-ttu-id="4d028-118">Ele inclui o nome de usuário e as formas de diferenciação de maiúsculas e minúsculas da senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="4d028-118">It includes the user name and both case-sensitive and case-insensitive forms of the user's password.</span></span>

 

 
