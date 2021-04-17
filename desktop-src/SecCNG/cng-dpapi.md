---
description: A Microsoft introduziu a DPAPI (interface de programação de aplicativo de proteção de dados) no Windows 2000.
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: DPAPI CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd0771b9838b2dbcfbedb3d025a7f650429bba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755060"
---
# <a name="cng-dpapi"></a><span data-ttu-id="33165-103">DPAPI CNG</span><span class="sxs-lookup"><span data-stu-id="33165-103">CNG DPAPI</span></span>

<span data-ttu-id="33165-104">A Microsoft introduziu a DPAPI (interface de programação de aplicativo de proteção de dados) no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="33165-104">Microsoft introduced the data protection application programming interface (DPAPI) in Windows 2000.</span></span> <span data-ttu-id="33165-105">A API consiste em duas funções, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata).</span><span class="sxs-lookup"><span data-stu-id="33165-105">The API consists of two functions, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata).</span></span> <span data-ttu-id="33165-106">A DPAPI faz parte do CryptoAPI e foi destinada a desenvolvedores que sabiam muito pouco sobre o uso de criptografia.</span><span class="sxs-lookup"><span data-stu-id="33165-106">DPAPI is part of CryptoAPI and was intended for developers who knew very little about using cryptography.</span></span> <span data-ttu-id="33165-107">As duas funções podem ser usadas para criptografar e descriptografar dados estáticos em um único computador.</span><span class="sxs-lookup"><span data-stu-id="33165-107">The two functions could be used to encrypt and decrypt static data on a single computer.</span></span>

<span data-ttu-id="33165-108">A computação em nuvem, no entanto, geralmente requer que o conteúdo criptografado em um computador seja descriptografado em outro.</span><span class="sxs-lookup"><span data-stu-id="33165-108">Cloud computing, however, often requires that content encrypted on one computer be decrypted on another.</span></span> <span data-ttu-id="33165-109">Portanto, começando com o Windows 8, a Microsoft ampliou a ideia de usar uma API relativamente simples para abranger cenários de nuvem.</span><span class="sxs-lookup"><span data-stu-id="33165-109">Therefore, beginning with Windows 8, Microsoft extended the idea of using a relatively straightforward API to encompass cloud scenarios.</span></span> <span data-ttu-id="33165-110">Essa nova API, chamada de DPAPI-NG, permite que você compartilhe com segurança segredos (chaves, senhas, material da chave) e mensagens, protegendo-os a um conjunto de entidades que podem ser usadas para desprotegê-los em computadores diferentes após autenticação e autorização adequadas.</span><span class="sxs-lookup"><span data-stu-id="33165-110">This new API, called DPAPI-NG, enables you to securely share secrets (keys, passwords, key material) and messages by protecting them to a set of principals that can be used to unprotect them on different computers after proper authentication and authorization.</span></span> <span data-ttu-id="33165-111">Atualmente, há suporte para as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="33165-111">The following principals are currently supported:</span></span>

-   <span data-ttu-id="33165-112">Um grupo em uma floresta Active Directory.</span><span class="sxs-lookup"><span data-stu-id="33165-112">A group in an Active Directory forest.</span></span>
-   <span data-ttu-id="33165-113">Credenciais da Web.</span><span class="sxs-lookup"><span data-stu-id="33165-113">Web credentials.</span></span>

<span data-ttu-id="33165-114">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="33165-114">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="33165-115">Provedores de proteção</span><span class="sxs-lookup"><span data-stu-id="33165-115">Protection Providers</span></span>](protection-providers.md)
-   [<span data-ttu-id="33165-116">Descritores de proteção</span><span class="sxs-lookup"><span data-stu-id="33165-116">Protection Descriptors</span></span>](protection-descriptors.md)
-   [<span data-ttu-id="33165-117">Formato de dados protegidos</span><span class="sxs-lookup"><span data-stu-id="33165-117">Protected Data Format</span></span>](protected-data-format.md)

<span data-ttu-id="33165-118">O DPAPI-NG é criado com base na CNG (Cryptography Next Generation) e inclui as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="33165-118">DPAPI-NG is built on top of Cryptography Next Generation (CNG) and includes the following functions:</span></span>

-   [<span data-ttu-id="33165-119">**NCryptCreateProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="33165-119">**NCryptCreateProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
-   [<span data-ttu-id="33165-120">**NCryptCloseProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="33165-120">**NCryptCloseProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor)
-   [<span data-ttu-id="33165-121">**NCryptProtectSecret**</span><span class="sxs-lookup"><span data-stu-id="33165-121">**NCryptProtectSecret**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptprotectsecret)
-   [<span data-ttu-id="33165-122">**NCryptQueryProtectionDescriptorName**</span><span class="sxs-lookup"><span data-stu-id="33165-122">**NCryptQueryProtectionDescriptorName**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptqueryprotectiondescriptorname)
-   [<span data-ttu-id="33165-123">**NCryptRegisterProtectionDescriptorName**</span><span class="sxs-lookup"><span data-stu-id="33165-123">**NCryptRegisterProtectionDescriptorName**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname)
-   [<span data-ttu-id="33165-124">**NCryptStreamClose**</span><span class="sxs-lookup"><span data-stu-id="33165-124">**NCryptStreamClose**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamclose)
-   [<span data-ttu-id="33165-125">**NCryptStreamOpenToProtect**</span><span class="sxs-lookup"><span data-stu-id="33165-125">**NCryptStreamOpenToProtect**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect)
-   [<span data-ttu-id="33165-126">**NCryptStreamOpenToUnprotect**</span><span class="sxs-lookup"><span data-stu-id="33165-126">**NCryptStreamOpenToUnprotect**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect)
-   [<span data-ttu-id="33165-127">**NCryptStreamUpdate**</span><span class="sxs-lookup"><span data-stu-id="33165-127">**NCryptStreamUpdate**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamupdate)
-   [<span data-ttu-id="33165-128">**NCryptUnprotectSecret**</span><span class="sxs-lookup"><span data-stu-id="33165-128">**NCryptUnprotectSecret**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptunprotectsecret)

 

 
