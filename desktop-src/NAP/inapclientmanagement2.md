---
title: Interface INapClientManagement2 (NapManagement. h)
description: Fornece métodos para o gerenciamento de cliente NAP. | Interface INapClientManagement2 (NapManagement. h)
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- INapClientManagement2 da interface NAP
- INapClientManagement2 interface NAP, descrita
topic_type:
- apiref
api_name:
- INapClientManagement2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3441b52ddf776337765f39d23528bc223a17b1e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104012048"
---
# <a name="inapclientmanagement2-interface"></a><span data-ttu-id="ade1e-106">Interface INapClientManagement2</span><span class="sxs-lookup"><span data-stu-id="ade1e-106">INapClientManagement2 interface</span></span>

> [!Note]  
> <span data-ttu-id="ade1e-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="ade1e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ade1e-108">A interface **INapClientManagement2** fornece métodos para o gerenciamento de cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="ade1e-108">The **INapClientManagement2** interface provides methods for NAP client management.</span></span>

> [!Note]  
> <span data-ttu-id="ade1e-109">Essa interface herda todos os métodos de [**INapClientManagement**](inapclientmanagement.md) e deve ser usada em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="ade1e-109">This interface inherits all the methods of [**INapClientManagement**](inapclientmanagement.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="ade1e-110">Membros</span><span class="sxs-lookup"><span data-stu-id="ade1e-110">Members</span></span>

<span data-ttu-id="ade1e-111">A interface **INapClientManagement2** herda de [**INapClientManagement**](inapclientmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="ade1e-111">The **INapClientManagement2** interface inherits from [**INapClientManagement**](inapclientmanagement.md).</span></span> <span data-ttu-id="ade1e-112">**INapClientManagement2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ade1e-112">**INapClientManagement2** also has these types of members:</span></span>

-   [<span data-ttu-id="ade1e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ade1e-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ade1e-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="ade1e-114">Methods</span></span>

<span data-ttu-id="ade1e-115">A interface **INapClientManagement2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ade1e-115">The **INapClientManagement2** interface has these methods.</span></span>



| <span data-ttu-id="ade1e-116">Método</span><span class="sxs-lookup"><span data-stu-id="ade1e-116">Method</span></span>                                                                                                    | <span data-ttu-id="ade1e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="ade1e-117">Description</span></span>                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ade1e-118">**INapClientManagement2::GetSystemIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="ade1e-118">**INapClientManagement2::GetSystemIsolationInfoEx**</span></span>](inapclientmanagement2-getsystemisolationinfoex.md) | <span data-ttu-id="ade1e-119">Recupera informações sobre o estado de isolamento e o estado de isolamento estendido do cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="ade1e-119">Retrieves information about the isolation state and extended isolation state of the Nap client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ade1e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ade1e-120">Requirements</span></span>



| <span data-ttu-id="ade1e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ade1e-121">Requirement</span></span> | <span data-ttu-id="ade1e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ade1e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ade1e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ade1e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ade1e-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ade1e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ade1e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ade1e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ade1e-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ade1e-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ade1e-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ade1e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ade1e-128"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="ade1e-128"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="ade1e-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="ade1e-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ade1e-130"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ade1e-130"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="ade1e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ade1e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ade1e-132"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ade1e-132"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="ade1e-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ade1e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ade1e-134">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="ade1e-134">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> <dt>

[<span data-ttu-id="ade1e-135">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="ade1e-135">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ade1e-136">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="ade1e-136">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





