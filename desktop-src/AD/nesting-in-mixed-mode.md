---
title: Aninhamento em modo misto
description: Este tópico lista as restrições de grupos de segurança em um domínio de modo misto.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Aninhamento no modo misto do AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d63d475edf77398a69a519a08f3803f69d67d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822260"
---
# <a name="nesting-in-mixed-mode"></a><span data-ttu-id="e35c7-104">Aninhamento em modo misto</span><span class="sxs-lookup"><span data-stu-id="e35c7-104">Nesting in Mixed Mode</span></span>

<span data-ttu-id="e35c7-105">Este tópico lista as restrições de grupos de segurança em um domínio de modo misto.</span><span class="sxs-lookup"><span data-stu-id="e35c7-105">This topic lists the restrictions of security groups in a mixed-mode domain.</span></span>

<span data-ttu-id="e35c7-106">Os grupos de segurança em um domínio de modo misto têm as seguintes restrições:</span><span class="sxs-lookup"><span data-stu-id="e35c7-106">Security groups in a mixed-mode domain have the following restrictions:</span></span>

-   <span data-ttu-id="e35c7-107">Os grupos universais não podem ser criados em domínios de modo misto porque há suporte para o escopo universal somente em domínios de modo nativo do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e35c7-107">Universal groups cannot be created in mixed-mode domains because the universal scope is supported only in Windows 2000 native-mode domains.</span></span>
-   <span data-ttu-id="e35c7-108">Um grupo global pode conter contas do mesmo domínio ao qual o grupo pertence.</span><span class="sxs-lookup"><span data-stu-id="e35c7-108">A global group can contain accounts from the same domain to which the group belongs.</span></span> <span data-ttu-id="e35c7-109">Um grupo global não pode conter grupos universais, qualquer grupo global ou uma conta de outro domínio.</span><span class="sxs-lookup"><span data-stu-id="e35c7-109">A global group cannot contain any universal groups, any global group, or an account from another domain.</span></span>
-   <span data-ttu-id="e35c7-110">Um grupo de domínio local pode conter grupos globais e contas de qualquer domínio ou floresta.</span><span class="sxs-lookup"><span data-stu-id="e35c7-110">A domain local group can contain global groups and accounts from any domain or forest.</span></span> <span data-ttu-id="e35c7-111">Um grupo de domínio local não pode conter nenhum outro grupo local de domínio.</span><span class="sxs-lookup"><span data-stu-id="e35c7-111">A domain local group cannot contain any other domain local group.</span></span>

<span data-ttu-id="e35c7-112">Lembre-se de que os grupos de distribuição podem ser aninhados de acordo com as regras de aninhamento do modo nativo.</span><span class="sxs-lookup"><span data-stu-id="e35c7-112">Be aware that distribution groups can be nested according to the nesting rules for native mode.</span></span>

 

 




