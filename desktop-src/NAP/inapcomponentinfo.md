---
title: Interface INapComponentInfo (NapCommon. h)
description: Fornece métodos que os componentes de plug-in (como SHAs e SHVs) devem implementar para que o sistema NAP se comunique com eles.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- INapComponentInfo da interface NAP
- INapComponentInfo interface NAP, descrita
topic_type:
- apiref
api_name:
- INapComponentInfo
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba38c71cb79eb7222f619e6702008b31c41e7e2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918241"
---
# <a name="inapcomponentinfo-interface"></a><span data-ttu-id="407a5-105">Interface INapComponentInfo</span><span class="sxs-lookup"><span data-stu-id="407a5-105">INapComponentInfo interface</span></span>

> [!Note]  
> <span data-ttu-id="407a5-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="407a5-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="407a5-107">A interface **INapComponentInfo** fornece métodos que os componentes de plug-in (como Shas e SHVs) devem implementar para que o sistema NAP se comunique com eles.</span><span class="sxs-lookup"><span data-stu-id="407a5-107">The **INapComponentInfo** interface provides methods that plug-in components (such as SHAs and SHVs) must implement for the NAP system to communicate with them.</span></span> <span data-ttu-id="407a5-108">O sistema NAP chama a implementação desses métodos para recuperar informações administrativas estáticas (por exemplo, nome amigável ou cadeias de caracteres localizadas).</span><span class="sxs-lookup"><span data-stu-id="407a5-108">The NAP system calls your implementation of these methods to retrieve static administrative information (for example, friendly name or localized strings).</span></span>

## <a name="members"></a><span data-ttu-id="407a5-109">Membros</span><span class="sxs-lookup"><span data-stu-id="407a5-109">Members</span></span>

<span data-ttu-id="407a5-110">A interface **INapComponentInfo** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="407a5-110">The **INapComponentInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="407a5-111">**INapComponentInfo** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="407a5-111">**INapComponentInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="407a5-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="407a5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="407a5-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="407a5-113">Methods</span></span>

<span data-ttu-id="407a5-114">A interface **INapComponentInfo** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="407a5-114">The **INapComponentInfo** interface has these methods.</span></span>



| <span data-ttu-id="407a5-115">Método</span><span class="sxs-lookup"><span data-stu-id="407a5-115">Method</span></span>                                                                                                         | <span data-ttu-id="407a5-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="407a5-116">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="407a5-117">**INapComponentInfo::ConvertErrorCodeToMessageId**</span><span class="sxs-lookup"><span data-stu-id="407a5-117">**INapComponentInfo::ConvertErrorCodeToMessageId**</span></span>](inapcomponentinfo-converterrorcodetomessageid-method.md) | <span data-ttu-id="407a5-118">Usado pelo sistema NAP para solicitar que o cliente de integridade Converta um código de erro HRESULT em uma ID de mensagem.</span><span class="sxs-lookup"><span data-stu-id="407a5-118">Used by the NAP System to request the health client convert an HRESULT error code to a message ID.</span></span><br/> |
| [<span data-ttu-id="407a5-119">**INapComponentInfo:: GetDescription**</span><span class="sxs-lookup"><span data-stu-id="407a5-119">**INapComponentInfo::GetDescription**</span></span>](inapcomponentinfo-getdescription-method.md)                           | <span data-ttu-id="407a5-120">Usado pelo sistema NAP para obter a descrição de um cliente de integridade.</span><span class="sxs-lookup"><span data-stu-id="407a5-120">Used by the NAP System to get the description of a health client.</span></span><br/>                                  |
| [<span data-ttu-id="407a5-121">**INapComponentInfo:: getfriendlyname**</span><span class="sxs-lookup"><span data-stu-id="407a5-121">**INapComponentInfo::GetFriendlyName**</span></span>](inapcomponentinfo-getfriendlyname-method.md)                         | <span data-ttu-id="407a5-122">Usado pelo sistema NAP para obter o nome amigável de um cliente de integridade.</span><span class="sxs-lookup"><span data-stu-id="407a5-122">Used by the NAP System to get the friendly name of a health client.</span></span><br/>                                |
| [<span data-ttu-id="407a5-123">**INapComponentInfo:: GetIcon**</span><span class="sxs-lookup"><span data-stu-id="407a5-123">**INapComponentInfo::GetIcon**</span></span>](inapcomponentinfo-geticon-method.md)                                         | <span data-ttu-id="407a5-124">Usado pelo sistema NAP para obter o ícone de um cliente de integridade.</span><span class="sxs-lookup"><span data-stu-id="407a5-124">Used by the NAP System to get the icon of a health client.</span></span><br/>                                         |
| [<span data-ttu-id="407a5-125">**INapComponentInfo:: gettraduzistring**</span><span class="sxs-lookup"><span data-stu-id="407a5-125">**INapComponentInfo::GetLocalizedString**</span></span>](inapcomponentinfo-getlocalizedstring-method.md)                   | <span data-ttu-id="407a5-126">Usado pelo sistema NAP para obter cadeias de caracteres localizadas.</span><span class="sxs-lookup"><span data-stu-id="407a5-126">Used by the NAP System to get localized strings.</span></span><br/>                                                   |
| [<span data-ttu-id="407a5-127">**INapComponentInfo:: getvendoname**</span><span class="sxs-lookup"><span data-stu-id="407a5-127">**INapComponentInfo::GetVendorName**</span></span>](inapcomponentinfo-getvendorname-method.md)                             | <span data-ttu-id="407a5-128">Usado pelo sistema NAP para obter o nome do fornecedor de um cliente de integridade.</span><span class="sxs-lookup"><span data-stu-id="407a5-128">Used by the NAP System to get the vendor name of a health client.</span></span><br/>                                  |
| [<span data-ttu-id="407a5-129">**INapComponentInfo:: GetVersion**</span><span class="sxs-lookup"><span data-stu-id="407a5-129">**INapComponentInfo::GetVersion**</span></span>](inapcomponentinfo-getversion-method.md)                                   | <span data-ttu-id="407a5-130">Usado pelo sistema NAP para obter a versão de um cliente de integridade.</span><span class="sxs-lookup"><span data-stu-id="407a5-130">Used by the NAP System to get the version of a health client.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="407a5-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="407a5-131">Requirements</span></span>



| <span data-ttu-id="407a5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="407a5-132">Requirement</span></span> | <span data-ttu-id="407a5-133">Valor</span><span class="sxs-lookup"><span data-stu-id="407a5-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="407a5-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="407a5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="407a5-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="407a5-135">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="407a5-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="407a5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="407a5-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="407a5-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="407a5-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="407a5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="407a5-139"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="407a5-139"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="407a5-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="407a5-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="407a5-141"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="407a5-141"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="407a5-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="407a5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="407a5-143">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="407a5-143">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="407a5-144">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="407a5-144">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

