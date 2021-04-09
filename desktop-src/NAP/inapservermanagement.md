---
title: Interface INapServerManagement (NapServerManagement. h)
description: São usados para gerenciar o servidor NAP.
ms.assetid: 5c4f9bf1-fe82-48f5-8aa4-5c73ab01a78a
keywords:
- INapServerManagement da interface NAP
- INapServerManagement interface NAP, descrita
topic_type:
- apiref
api_name:
- INapServerManagement
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5eed03f535653a3b9244ff1aa74fe499c1bf2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085711"
---
# <a name="inapservermanagement-interface"></a><span data-ttu-id="b6f67-105">Interface INapServerManagement</span><span class="sxs-lookup"><span data-stu-id="b6f67-105">INapServerManagement interface</span></span>

> [!Note]  
> <span data-ttu-id="b6f67-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="b6f67-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b6f67-107">O **INapServerManagement** fornece métodos que são usados para gerenciar o servidor NAP.</span><span class="sxs-lookup"><span data-stu-id="b6f67-107">The **INapServerManagement** provides methods that are used to manage the NAP Server.</span></span>

## <a name="members"></a><span data-ttu-id="b6f67-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b6f67-108">Members</span></span>

<span data-ttu-id="b6f67-109">A interface **INapServerManagement** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b6f67-109">The **INapServerManagement** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b6f67-110">**INapServerManagement** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b6f67-110">**INapServerManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="b6f67-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b6f67-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b6f67-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b6f67-112">Methods</span></span>

<span data-ttu-id="b6f67-113">A interface **INapServerManagement** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b6f67-113">The **INapServerManagement** interface has these methods.</span></span>



| <span data-ttu-id="b6f67-114">Método</span><span class="sxs-lookup"><span data-stu-id="b6f67-114">Method</span></span>                                                                                                                       | <span data-ttu-id="b6f67-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6f67-115">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="b6f67-116">**INapServerManagement::RegisterSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="b6f67-116">**INapServerManagement::RegisterSystemHealthValidator**</span></span>](inapservermanagement-registersystemhealthvalidator-method.md)     | <span data-ttu-id="b6f67-117">Registra um SHV.</span><span class="sxs-lookup"><span data-stu-id="b6f67-117">Registers an SHV.</span></span><br/>                         |
| [<span data-ttu-id="b6f67-118">**INapServerManagement::SetFailureCategoryMappings**</span><span class="sxs-lookup"><span data-stu-id="b6f67-118">**INapServerManagement::SetFailureCategoryMappings**</span></span>](inapservermanagement-setfailurecategorymappings-method.md)           | <span data-ttu-id="b6f67-119">Define os mapeamentos de categoria de falha do SHV.</span><span class="sxs-lookup"><span data-stu-id="b6f67-119">Sets the SHV's failure category mappings.</span></span><br/> |
| [<span data-ttu-id="b6f67-120">**INapServerManagement::UnregisterSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="b6f67-120">**INapServerManagement::UnregisterSystemHealthValidator**</span></span>](inapservermanagement-unregistersystemhealthvalidator-method.md) | <span data-ttu-id="b6f67-121">Cancela o registro de um SHV do servidor NAP.</span><span class="sxs-lookup"><span data-stu-id="b6f67-121">Deregisters an SHV from the NAP server.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="b6f67-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6f67-122">Requirements</span></span>



| <span data-ttu-id="b6f67-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6f67-123">Requirement</span></span> | <span data-ttu-id="b6f67-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b6f67-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f67-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6f67-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b6f67-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b6f67-126">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="b6f67-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6f67-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b6f67-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6f67-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b6f67-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6f67-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6f67-130"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6f67-130"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6f67-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="b6f67-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6f67-132"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6f67-132"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="b6f67-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b6f67-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6f67-134"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6f67-134"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="b6f67-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6f67-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6f67-136">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="b6f67-136">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="b6f67-137">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="b6f67-137">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

