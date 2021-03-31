---
title: Interface INapSoHConstructor (NapProtocol. h)
description: São usados por SHAs para construir SoHRequests e por SHVs para construir SoHResponses.
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- INapSoHConstructor da interface NAP
- INapSoHConstructor interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSoHConstructor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546a6d3b4ec262fdd725af24211338e848b2b848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918050"
---
# <a name="inapsohconstructor-interface"></a><span data-ttu-id="25372-105">Interface INapSoHConstructor</span><span class="sxs-lookup"><span data-stu-id="25372-105">INapSoHConstructor interface</span></span>

> [!Note]  
> <span data-ttu-id="25372-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="25372-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="25372-107">O **INapSoHConstructor** fornece métodos que são usados por SHAs para construir [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) e por SHVs para construir **SoHResponses**.</span><span class="sxs-lookup"><span data-stu-id="25372-107">The **INapSoHConstructor** provides methods that are used by SHAs to construct [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) and by SHVs to construct **SoHResponses**.</span></span>

## <a name="members"></a><span data-ttu-id="25372-108">Membros</span><span class="sxs-lookup"><span data-stu-id="25372-108">Members</span></span>

<span data-ttu-id="25372-109">A interface **INapSoHConstructor** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="25372-109">The **INapSoHConstructor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="25372-110">**INapSoHConstructor** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="25372-110">**INapSoHConstructor** also has these types of members:</span></span>

-   [<span data-ttu-id="25372-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="25372-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="25372-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="25372-112">Methods</span></span>

<span data-ttu-id="25372-113">A interface **INapSoHConstructor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="25372-113">The **INapSoHConstructor** interface has these methods.</span></span>



| <span data-ttu-id="25372-114">Método</span><span class="sxs-lookup"><span data-stu-id="25372-114">Method</span></span>                                                                                   | <span data-ttu-id="25372-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="25372-115">Description</span></span>                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [<span data-ttu-id="25372-116">**INapSoHConstructor:: AppendAttribute**</span><span class="sxs-lookup"><span data-stu-id="25372-116">**INapSoHConstructor::AppendAttribute**</span></span>](inapsohconstructor-appendattribute-method.md) | <span data-ttu-id="25372-117">Adiciona um TLV ao final do buffer SoH.</span><span class="sxs-lookup"><span data-stu-id="25372-117">Adds a TLV to the end of the SoH buffer.</span></span><br/> |
| [<span data-ttu-id="25372-118">**INapSoHConstructor::GetSoH**</span><span class="sxs-lookup"><span data-stu-id="25372-118">**INapSoHConstructor::GetSoH**</span></span>](inapsohconstructor-getsoh-method.md)                   | <span data-ttu-id="25372-119">Recupera o pacote SoH construído.</span><span class="sxs-lookup"><span data-stu-id="25372-119">Retrieves the constructed SoH packet.</span></span><br/>    |
| [<span data-ttu-id="25372-120">**INapSoHConstructor:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="25372-120">**INapSoHConstructor::Initialize**</span></span>](inapsohconstructor-initialize-method.md)           | <span data-ttu-id="25372-121">Inicializa o pacote SoH.</span><span class="sxs-lookup"><span data-stu-id="25372-121">Initializes the SoH packet.</span></span><br/>              |
| [<span data-ttu-id="25372-122">**INapSoHConstructor:: Validate**</span><span class="sxs-lookup"><span data-stu-id="25372-122">**INapSoHConstructor::Validate**</span></span>](inapsohconstructor-validate-method.md)               | <span data-ttu-id="25372-123">Verifica a validade do pacote SoH.</span><span class="sxs-lookup"><span data-stu-id="25372-123">Checks the validity of the SoH packet.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="25372-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25372-124">Requirements</span></span>



| <span data-ttu-id="25372-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="25372-125">Requirement</span></span> | <span data-ttu-id="25372-126">Valor</span><span class="sxs-lookup"><span data-stu-id="25372-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="25372-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25372-127">Minimum supported client</span></span><br/> | <span data-ttu-id="25372-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25372-128">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="25372-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25372-129">Minimum supported server</span></span><br/> | <span data-ttu-id="25372-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="25372-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="25372-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="25372-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="25372-132"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="25372-132"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="25372-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="25372-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="25372-134"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="25372-134"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="25372-135">DLL</span><span class="sxs-lookup"><span data-stu-id="25372-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25372-136"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25372-136"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="25372-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="25372-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25372-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="25372-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="25372-139">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="25372-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

