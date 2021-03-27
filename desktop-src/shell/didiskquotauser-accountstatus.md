---
description: Obtém o status da conta do usuário.
title: Propriedade DIDiskQuotaUser. AccountStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ff2234f7-4758-43c7-a3c2-8fb980b27c04
ms.openlocfilehash: 155ae627d70c5125fd0d1d501062224450fc8e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967327"
---
# <a name="didiskquotauseraccountstatus-property"></a><span data-ttu-id="eb291-103">Propriedade DIDiskQuotaUser. AccountStatus</span><span class="sxs-lookup"><span data-stu-id="eb291-103">DIDiskQuotaUser.AccountStatus property</span></span>

<span data-ttu-id="eb291-104">Obtém o status da conta do usuário.</span><span class="sxs-lookup"><span data-stu-id="eb291-104">Gets the status of the user's account.</span></span>

<span data-ttu-id="eb291-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="eb291-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb291-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb291-106">Syntax</span></span>


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a><span data-ttu-id="eb291-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="eb291-107">Property value</span></span>

<span data-ttu-id="eb291-108">Essa propriedade pode ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb291-108">This property can take one of the following values.</span></span>



| <span data-ttu-id="eb291-109">Status</span><span class="sxs-lookup"><span data-stu-id="eb291-109">Status</span></span>            | <span data-ttu-id="eb291-110">Valor</span><span class="sxs-lookup"><span data-stu-id="eb291-110">Value</span></span> | <span data-ttu-id="eb291-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb291-111">Description</span></span>                         |
|-------------------|-------|-------------------------------------|
| <span data-ttu-id="eb291-112">dqAcctResolved</span><span class="sxs-lookup"><span data-stu-id="eb291-112">dqAcctResolved</span></span>    | <span data-ttu-id="eb291-113">0</span><span class="sxs-lookup"><span data-stu-id="eb291-113">0</span></span>     | <span data-ttu-id="eb291-114">As informações da conta são resolvidas.</span><span class="sxs-lookup"><span data-stu-id="eb291-114">Account information is resolved.</span></span>    |
| <span data-ttu-id="eb291-115">dqAcctUnavailable</span><span class="sxs-lookup"><span data-stu-id="eb291-115">dqAcctUnavailable</span></span> | <span data-ttu-id="eb291-116">1</span><span class="sxs-lookup"><span data-stu-id="eb291-116">1</span></span>     | <span data-ttu-id="eb291-117">As informações da conta não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="eb291-117">Account information is unavailable.</span></span> |
| <span data-ttu-id="eb291-118">dqAcctDeleted</span><span class="sxs-lookup"><span data-stu-id="eb291-118">dqAcctDeleted</span></span>     | <span data-ttu-id="eb291-119">2</span><span class="sxs-lookup"><span data-stu-id="eb291-119">2</span></span>     | <span data-ttu-id="eb291-120">A conta foi excluída.</span><span class="sxs-lookup"><span data-stu-id="eb291-120">Account has been deleted.</span></span>           |
| <span data-ttu-id="eb291-121">dqAcctInvalid</span><span class="sxs-lookup"><span data-stu-id="eb291-121">dqAcctInvalid</span></span>     | <span data-ttu-id="eb291-122">3</span><span class="sxs-lookup"><span data-stu-id="eb291-122">3</span></span>     | <span data-ttu-id="eb291-123">A conta é inválida.</span><span class="sxs-lookup"><span data-stu-id="eb291-123">Account is invalid.</span></span>                 |
| <span data-ttu-id="eb291-124">dqAcctUnknown</span><span class="sxs-lookup"><span data-stu-id="eb291-124">dqAcctUnknown</span></span>     | <span data-ttu-id="eb291-125">4</span><span class="sxs-lookup"><span data-stu-id="eb291-125">4</span></span>     | <span data-ttu-id="eb291-126">Não é possível encontrar a conta.</span><span class="sxs-lookup"><span data-stu-id="eb291-126">Account cannot be found.</span></span>            |
| <span data-ttu-id="eb291-127">dqAcctUnresolved</span><span class="sxs-lookup"><span data-stu-id="eb291-127">dqAcctUnresolved</span></span>  | <span data-ttu-id="eb291-128">5</span><span class="sxs-lookup"><span data-stu-id="eb291-128">5</span></span>     | <span data-ttu-id="eb291-129">As informações da conta não são resolvidas.</span><span class="sxs-lookup"><span data-stu-id="eb291-129">Account information is unresolved.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="eb291-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb291-130">Requirements</span></span>



| <span data-ttu-id="eb291-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb291-131">Requirement</span></span> | <span data-ttu-id="eb291-132">Valor</span><span class="sxs-lookup"><span data-stu-id="eb291-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb291-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb291-133">Minimum supported client</span></span><br/> | <span data-ttu-id="eb291-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eb291-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eb291-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb291-135">Minimum supported server</span></span><br/> | <span data-ttu-id="eb291-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eb291-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="eb291-137">DLL</span><span class="sxs-lookup"><span data-stu-id="eb291-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb291-138"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="eb291-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb291-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb291-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb291-140">**Objeto DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="eb291-140">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




