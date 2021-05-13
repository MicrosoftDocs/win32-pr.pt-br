---
description: Obtém o status da conta do usuário.
title: Propriedade DIDiskQuotaUser.AccountStatus
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
ms.openlocfilehash: e27e86fadab02616f91a4838acfc4be93e985ebd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841647"
---
# <a name="didiskquotauseraccountstatus-property"></a><span data-ttu-id="bec57-103">Propriedade DIDiskQuotaUser.AccountStatus</span><span class="sxs-lookup"><span data-stu-id="bec57-103">DIDiskQuotaUser.AccountStatus property</span></span>

<span data-ttu-id="bec57-104">Obtém o status da conta do usuário.</span><span class="sxs-lookup"><span data-stu-id="bec57-104">Gets the status of the user's account.</span></span>

<span data-ttu-id="bec57-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="bec57-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bec57-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bec57-106">Syntax</span></span>


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a><span data-ttu-id="bec57-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bec57-107">Property value</span></span>

<span data-ttu-id="bec57-108">Essa propriedade pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bec57-108">This property can take one of the following values.</span></span>



| <span data-ttu-id="bec57-109">Status</span><span class="sxs-lookup"><span data-stu-id="bec57-109">Status</span></span>            | <span data-ttu-id="bec57-110">Valor</span><span class="sxs-lookup"><span data-stu-id="bec57-110">Value</span></span> | <span data-ttu-id="bec57-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="bec57-111">Description</span></span>                         |
|-------------------|-------|-------------------------------------|
| <span data-ttu-id="bec57-112">dqAcctResolved</span><span class="sxs-lookup"><span data-stu-id="bec57-112">dqAcctResolved</span></span>    | <span data-ttu-id="bec57-113">0</span><span class="sxs-lookup"><span data-stu-id="bec57-113">0</span></span>     | <span data-ttu-id="bec57-114">As informações da conta são resolvidas.</span><span class="sxs-lookup"><span data-stu-id="bec57-114">Account information is resolved.</span></span>    |
| <span data-ttu-id="bec57-115">dqAcctUnavailable</span><span class="sxs-lookup"><span data-stu-id="bec57-115">dqAcctUnavailable</span></span> | <span data-ttu-id="bec57-116">1</span><span class="sxs-lookup"><span data-stu-id="bec57-116">1</span></span>     | <span data-ttu-id="bec57-117">As informações da conta não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="bec57-117">Account information is unavailable.</span></span> |
| <span data-ttu-id="bec57-118">dqAcctDeleted</span><span class="sxs-lookup"><span data-stu-id="bec57-118">dqAcctDeleted</span></span>     | <span data-ttu-id="bec57-119">2</span><span class="sxs-lookup"><span data-stu-id="bec57-119">2</span></span>     | <span data-ttu-id="bec57-120">A conta foi excluída.</span><span class="sxs-lookup"><span data-stu-id="bec57-120">Account has been deleted.</span></span>           |
| <span data-ttu-id="bec57-121">dqAcctInvalid</span><span class="sxs-lookup"><span data-stu-id="bec57-121">dqAcctInvalid</span></span>     | <span data-ttu-id="bec57-122">3</span><span class="sxs-lookup"><span data-stu-id="bec57-122">3</span></span>     | <span data-ttu-id="bec57-123">A conta é inválida.</span><span class="sxs-lookup"><span data-stu-id="bec57-123">Account is invalid.</span></span>                 |
| <span data-ttu-id="bec57-124">dqAcctUnknown</span><span class="sxs-lookup"><span data-stu-id="bec57-124">dqAcctUnknown</span></span>     | <span data-ttu-id="bec57-125">4</span><span class="sxs-lookup"><span data-stu-id="bec57-125">4</span></span>     | <span data-ttu-id="bec57-126">A conta não pode ser encontrada.</span><span class="sxs-lookup"><span data-stu-id="bec57-126">Account cannot be found.</span></span>            |
| <span data-ttu-id="bec57-127">dqAcctUnresolved</span><span class="sxs-lookup"><span data-stu-id="bec57-127">dqAcctUnresolved</span></span>  | <span data-ttu-id="bec57-128">5</span><span class="sxs-lookup"><span data-stu-id="bec57-128">5</span></span>     | <span data-ttu-id="bec57-129">As informações da conta não estão resolvidas.</span><span class="sxs-lookup"><span data-stu-id="bec57-129">Account information is unresolved.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="bec57-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bec57-130">Requirements</span></span>



| <span data-ttu-id="bec57-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bec57-131">Requirement</span></span> | <span data-ttu-id="bec57-132">Valor</span><span class="sxs-lookup"><span data-stu-id="bec57-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bec57-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bec57-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bec57-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bec57-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bec57-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bec57-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bec57-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bec57-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bec57-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bec57-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bec57-138"><dt>Shell32.dll (versão 5.0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="bec57-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bec57-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="bec57-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bec57-140">**Objeto DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="bec57-140">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




