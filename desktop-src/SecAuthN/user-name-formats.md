---
description: Quando um aplicativo usa a API de gerenciamento de credenciais para solicitar credenciais, espera-se que o usuário insira informações que podem ser validadas pelo sistema operacional ou pelo aplicativo.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Formatos de nome de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fb99a9e6064cd3883a8d71c1e76ca853d88661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749759"
---
# <a name="user-name-formats"></a><span data-ttu-id="06f1f-103">Formatos de nome de usuário</span><span class="sxs-lookup"><span data-stu-id="06f1f-103">User Name Formats</span></span>

<span data-ttu-id="06f1f-104">Quando um aplicativo usa a API de gerenciamento de credenciais para solicitar credenciais, espera-se que o usuário insira informações que podem ser validadas pelo sistema operacional ou pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="06f1f-104">When an application uses the Credentials Management API to prompt for credentials, the user is expected to enter information that can be validated, either by the operating system or by the application.</span></span> <span data-ttu-id="06f1f-105">O usuário pode especificar informações de credenciais de domínio em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="06f1f-105">The user can specify domain credentials information in one of the following formats:</span></span>

-   [<span data-ttu-id="06f1f-106">Nome principal do usuário</span><span class="sxs-lookup"><span data-stu-id="06f1f-106">User Principal Name</span></span>](#user-principal-name)
-   [<span data-ttu-id="06f1f-107">Nome de logon de nível inferior</span><span class="sxs-lookup"><span data-stu-id="06f1f-107">Down-Level Logon Name</span></span>](#down-level-logon-name)

## <a name="user-principal-name"></a><span data-ttu-id="06f1f-108">Nome UPN</span><span class="sxs-lookup"><span data-stu-id="06f1f-108">User Principal Name</span></span>

<span data-ttu-id="06f1f-109">O formato UPN ( [*nome principal do usuário*](../secgloss/u-gly.md) ) é usado para especificar um nome de estilo de Internet, como <b>UserName@Example.Microsoft.com</b> .</span><span class="sxs-lookup"><span data-stu-id="06f1f-109">[*User principal name*](../secgloss/u-gly.md) (UPN) format is used to specify an Internet-style name, such as <b>UserName@Example.Microsoft.com</b>.</span></span> <span data-ttu-id="06f1f-110">A tabela a seguir resume as partes de um UPN.</span><span class="sxs-lookup"><span data-stu-id="06f1f-110">The following table summarizes the parts of a UPN.</span></span>



| <span data-ttu-id="06f1f-111">Parte</span><span class="sxs-lookup"><span data-stu-id="06f1f-111">Part</span></span>                                                        | <span data-ttu-id="06f1f-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="06f1f-112">Example</span></span>                                |
|-------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="06f1f-113">Nome da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="06f1f-113">User account name.</span></span> <span data-ttu-id="06f1f-114">Também conhecido como o nome de logon.</span><span class="sxs-lookup"><span data-stu-id="06f1f-114">Also known as the logon name.</span></span><br/> | <span data-ttu-id="06f1f-115">*UserName*</span><span class="sxs-lookup"><span data-stu-id="06f1f-115">*UserName*</span></span><br/>                  |
| <span data-ttu-id="06f1f-116">Caractere.</span><span class="sxs-lookup"><span data-stu-id="06f1f-116">Separator.</span></span> <span data-ttu-id="06f1f-117">Um literal de caractere, o sinal de arroba (@).</span><span class="sxs-lookup"><span data-stu-id="06f1f-117">A character literal, the at sign (@).</span></span><br/> | @<br/>                           |
| <span data-ttu-id="06f1f-118">Sufixo UPN.</span><span class="sxs-lookup"><span data-stu-id="06f1f-118">UPN suffix.</span></span> <span data-ttu-id="06f1f-119">Também conhecido como o nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="06f1f-119">Also known as the domain name.</span></span><br/>       | <span data-ttu-id="06f1f-120">*Example.Microsoft.com*</span><span class="sxs-lookup"><span data-stu-id="06f1f-120">*Example.Microsoft.com*</span></span> <br/> |



 

<span data-ttu-id="06f1f-121">Um UPN pode ser definido implicitamente ou explicitamente.</span><span class="sxs-lookup"><span data-stu-id="06f1f-121">A UPN can be implicitly or explicitly defined.</span></span> <span data-ttu-id="06f1f-122">Um UPN implícito está no formato <b>UserName@DNSDomainName.com</b> .</span><span class="sxs-lookup"><span data-stu-id="06f1f-122">An implicit UPN is of the form <b>UserName@DNSDomainName.com</b>.</span></span> <span data-ttu-id="06f1f-123">Um UPN implícito sempre é associado à conta do usuário, mesmo que um UPN explícito não esteja definido.</span><span class="sxs-lookup"><span data-stu-id="06f1f-123">An implicit UPN is always associated with the user's account, even if an explicit UPN is not defined.</span></span> <span data-ttu-id="06f1f-124">Um UPN explícito é do formulário <i><b>Name@Suffix</b></i> , onde as cadeias de caracteres de nome e sufixo são explicitamente definidas pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="06f1f-124">An explicit UPN is of the form <i><b>Name@Suffix</b></i>, where both the name and suffix strings are explicitly defined by the administrator.</span></span>

## <a name="down-level-logon-name"></a><span data-ttu-id="06f1f-125">Nome de logon do Down-Level</span><span class="sxs-lookup"><span data-stu-id="06f1f-125">Down-Level Logon Name</span></span>

<span data-ttu-id="06f1f-126">O formato de nome de logon de nível inferior é usado para especificar um domínio e uma conta de usuário nesse domínio, por exemplo, <i><b>domínio \\ username</b></i>.</span><span class="sxs-lookup"><span data-stu-id="06f1f-126">The down-level logon name format is used to specify a domain and a user account in that domain, for example, <i><b>DOMAIN\\UserName</b></i>.</span></span> <span data-ttu-id="06f1f-127">A tabela a seguir resume as partes de um nome de logon de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="06f1f-127">The following table summarizes the parts of a down-level logon name.</span></span>



| <span data-ttu-id="06f1f-128">Parte</span><span class="sxs-lookup"><span data-stu-id="06f1f-128">Part</span></span>                                                           | <span data-ttu-id="06f1f-129">Exemplo</span><span class="sxs-lookup"><span data-stu-id="06f1f-129">Example</span></span>               |
|----------------------------------------------------------------|-----------------------|
| <span data-ttu-id="06f1f-130">Nome de domínio NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="06f1f-130">NetBIOS domain name.</span></span><br/>                                | <span data-ttu-id="06f1f-131">*DOMAIN*</span><span class="sxs-lookup"><span data-stu-id="06f1f-131">*DOMAIN*</span></span><br/>   |
| <span data-ttu-id="06f1f-132">Caractere.</span><span class="sxs-lookup"><span data-stu-id="06f1f-132">Separator.</span></span> <span data-ttu-id="06f1f-133">Um literal de caractere, a barra invertida ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="06f1f-133">A character literal, the backslash (\\).</span></span><br/> | **\\**<br/>     |
| <span data-ttu-id="06f1f-134">Nome da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="06f1f-134">User account name.</span></span> <span data-ttu-id="06f1f-135">Também conhecido como o nome de logon.</span><span class="sxs-lookup"><span data-stu-id="06f1f-135">Also known as the logon name.</span></span><br/>    | <span data-ttu-id="06f1f-136">*UserName*</span><span class="sxs-lookup"><span data-stu-id="06f1f-136">*UserName*</span></span><br/> |



 

 

 
