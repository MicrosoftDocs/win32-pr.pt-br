---
title: Erros comuns (AD DS)
description: A tabela a seguir contém uma lista de erros comuns que podem ocorrer com base no escopo do grupo que está sendo aninhado.
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- ANÚNCIOS de erros comuns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c719aad39690932de51c58d0f8081a8c855980bd
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2019
ms.locfileid: "104453830"
---
# <a name="common-errors-ad-ds"></a><span data-ttu-id="f17bb-104">Erros comuns (AD DS)</span><span class="sxs-lookup"><span data-stu-id="f17bb-104">Common Errors (AD DS)</span></span>

<span data-ttu-id="f17bb-105">A tabela a seguir contém uma lista de erros comuns que podem ocorrer com base no escopo do grupo que está sendo aninhado.</span><span class="sxs-lookup"><span data-stu-id="f17bb-105">The following table contains a list of common errors that can occur based on the scope of the group being nested.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f17bb-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f17bb-106">HRESULT</span></span></th>
<th><span data-ttu-id="f17bb-107">Description</span><span class="sxs-lookup"><span data-stu-id="f17bb-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f17bb-108">0x8007001F</span><span class="sxs-lookup"><span data-stu-id="f17bb-108">0x8007001F</span></span></td>
<td><span data-ttu-id="f17bb-109">Falha geral.</span><span class="sxs-lookup"><span data-stu-id="f17bb-109">General failure.</span></span> <span data-ttu-id="f17bb-110">Esse erro ocorrerá se você tentar:</span><span class="sxs-lookup"><span data-stu-id="f17bb-110">This error occurs if you attempt to:</span></span>
<ul>
<li><span data-ttu-id="f17bb-111">Adicione um grupo de domínio local a um grupo global ou universal ou a um grupo de domínio local em outro domínio.</span><span class="sxs-lookup"><span data-stu-id="f17bb-111">Add a domain local group to a global or universal group or a domain local group in another domain.</span></span> <span data-ttu-id="f17bb-112">Grupos locais de domínio só podem ser adicionados como membros a outros grupos locais de domínio no mesmo domínio.</span><span class="sxs-lookup"><span data-stu-id="f17bb-112">Domain local groups can only be added as members to other domain local groups in the same domain.</span></span></li>
<li><span data-ttu-id="f17bb-113">Adicione um grupo universal a um grupo global.</span><span class="sxs-lookup"><span data-stu-id="f17bb-113">Add a universal group to a global group.</span></span> <span data-ttu-id="f17bb-114">Grupos universais podem ser adicionados a grupos universais e locais de domínio, mas não a grupos globais.</span><span class="sxs-lookup"><span data-stu-id="f17bb-114">Universal groups can be added to universal and domain local groups, but not global groups.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f17bb-115">0x8007202F</span><span class="sxs-lookup"><span data-stu-id="f17bb-115">0x8007202F</span></span></td>
<td><span data-ttu-id="f17bb-116"><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>.</span><span class="sxs-lookup"><span data-stu-id="f17bb-116"><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>.</span></span> <span data-ttu-id="f17bb-117">Esse erro ocorrerá se você tentar adicionar um grupo de segurança a outro grupo em um domínio em execução no modo misto.</span><span class="sxs-lookup"><span data-stu-id="f17bb-117">This error occurs if you attempt to add a security group to another group in a domain running in mixed mode.</span></span> <span data-ttu-id="f17bb-118">Os grupos de segurança não podem ser aninhados no modo misto; os grupos de segurança só podem ser aninhados no modo nativo.</span><span class="sxs-lookup"><span data-stu-id="f17bb-118">Security groups cannot be nested in mixed mode; security groups can only be nested in native mode.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




