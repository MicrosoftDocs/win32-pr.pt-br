---
title: DACLs nulas e DACLs vazias (AD DS)
description: A presença de uma DACL (lista de controle de acesso condicional) nula no atributo nTSecurityDescriptor de qualquer objeto pode criar um risco de segurança sério.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- DACLs nulas e anúncios de DACLs vazios
- DACLs AD, NULL e Empty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b841bb0253547fea291232fb4c9e6e0f3377d18
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917112"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a><span data-ttu-id="fd2ad-105">DACLs nulas e DACLs vazias (AD DS)</span><span class="sxs-lookup"><span data-stu-id="fd2ad-105">Null DACLs and Empty DACLs (AD DS)</span></span>

<span data-ttu-id="fd2ad-106">A presença de uma DACL (lista de controle de acesso condicional) nula no atributo [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) de qualquer objeto pode criar um risco de segurança sério.</span><span class="sxs-lookup"><span data-stu-id="fd2ad-106">The presence of a null discretionary access-control list (DACL) in the [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) attribute of any object can create a serious security risk.</span></span> <span data-ttu-id="fd2ad-107">Uma DACL nula concede acesso completo a qualquer usuário que o solicita; a verificação de segurança normal não é executada em relação ao objeto.</span><span class="sxs-lookup"><span data-stu-id="fd2ad-107">A null DACL grants full access to any user that requests it; normal security checking is not performed with respect to the object.</span></span> <span data-ttu-id="fd2ad-108">Uma DACL nula não deve ser confundida com uma DACL vazia.</span><span class="sxs-lookup"><span data-stu-id="fd2ad-108">A null DACL should not be confused with an empty DACL.</span></span> <span data-ttu-id="fd2ad-109">Uma DACL vazia é uma DACL corretamente alocada e inicializada que não contém ACEs (entradas de controle de acesso).</span><span class="sxs-lookup"><span data-stu-id="fd2ad-109">An empty DACL is a properly allocated and initialized DACL containing no access-control entries (ACEs).</span></span> <span data-ttu-id="fd2ad-110">Uma DACL vazia não concede acesso ao objeto ao qual está atribuída.</span><span class="sxs-lookup"><span data-stu-id="fd2ad-110">An empty DACL grants no access to the object it is assigned to.</span></span>

<span data-ttu-id="fd2ad-111">Para obter mais informações, consulte [DACLs nulas e DACLs vazias](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).</span><span class="sxs-lookup"><span data-stu-id="fd2ad-111">For more information, see [Null DACLs and Empty DACLs](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).</span></span>

 

 