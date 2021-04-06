---
description: O objeto TrustedDomain armazena informações sobre uma relação de confiança com um domínio.
ms.assetid: fab69367-2143-49ef-a1b9-9c1d846fd4e1
title: Objeto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837d8a9e56273a87b22b9697ef4e5917d73bcc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826978"
---
# <a name="trusteddomain-object"></a><span data-ttu-id="36310-103">Objeto TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="36310-103">TrustedDomain Object</span></span>

<span data-ttu-id="36310-104">O objeto **TrustedDomain** armazena informações sobre uma relação de confiança com um domínio.</span><span class="sxs-lookup"><span data-stu-id="36310-104">The **TrustedDomain** object stores information about a trust relationship with a domain.</span></span> <span data-ttu-id="36310-105">Um objeto **TrustedDomain** é criado no sistema confiante para identificar uma conta dentro do domínio confiável que pode ser usado para enviar solicitações de autenticação e para executar outras operações, como traduções de nome e Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="36310-105">A **TrustedDomain** object is created on the trusting system to identify an account within the trusted domain that can be used to submit authentication requests and to perform other operations, such as name and [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) translations.</span></span>

<span data-ttu-id="36310-106">As informações armazenadas em um objeto **TrustedDomain** incluem:</span><span class="sxs-lookup"><span data-stu-id="36310-106">The information stored in a **TrustedDomain** object includes:</span></span>

-   <span data-ttu-id="36310-107">O SID do domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="36310-107">The SID of the trusted domain.</span></span> <span data-ttu-id="36310-108">Essas informações não são modificáveis e devem ser exclusivas entre todos os objetos **TrustedDomain** .</span><span class="sxs-lookup"><span data-stu-id="36310-108">This information is not modifiable and must be unique among all **TrustedDomain** objects.</span></span>
-   <span data-ttu-id="36310-109">O nome do domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="36310-109">The name of the trusted domain.</span></span> <span data-ttu-id="36310-110">Essas informações não são modificáveis e devem ser exclusivas entre todos os objetos **TrustedDomain** .</span><span class="sxs-lookup"><span data-stu-id="36310-110">This information is not modifiable and must be unique among all **TrustedDomain** objects.</span></span>
-   <span data-ttu-id="36310-111">O nome da conta no domínio confiável usado para enviar solicitações de autenticação e para executar traduções de nome e SID.</span><span class="sxs-lookup"><span data-stu-id="36310-111">The name of the account in the trusted domain used to submit authentication requests and to perform name and SID translations.</span></span> <span data-ttu-id="36310-112">Esse nome não é modificável.</span><span class="sxs-lookup"><span data-stu-id="36310-112">This name is not modifiable.</span></span>
-   <span data-ttu-id="36310-113">A senha usada para enviar solicitações de autenticação e executar traduções de nome e SID.</span><span class="sxs-lookup"><span data-stu-id="36310-113">The password used to submit authentication requests and perform name and SID translations.</span></span>

<span data-ttu-id="36310-114">Para obter mais informações, consulte [o tipo de objeto TrustedDomain](the-trusteddomain-object-type.md).</span><span class="sxs-lookup"><span data-stu-id="36310-114">For more information, see [The TrustedDomain Object Type](the-trusteddomain-object-type.md).</span></span>

 

 
