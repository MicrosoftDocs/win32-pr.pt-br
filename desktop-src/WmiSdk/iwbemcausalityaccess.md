---
description: Controla as solicitações filhas que são geradas a partir de uma solicitação pai.
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: Interface IWbemCausalityAccess (Wbemint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: db4c7a76b04b659cd467f7a4a7a9a8c1ba42721f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748862"
---
# <a name="iwbemcausalityaccess-interface"></a><span data-ttu-id="be3d5-103">Interface IWbemCausalityAccess</span><span class="sxs-lookup"><span data-stu-id="be3d5-103">IWbemCausalityAccess interface</span></span>

<span data-ttu-id="be3d5-104">A interface **IWbemCausalityAccess** mantém o controle das solicitações filho que são geradas a partir de uma solicitação pai.</span><span class="sxs-lookup"><span data-stu-id="be3d5-104">The **IWbemCausalityAccess** interface keeps track of child requests that are generated from a parent request.</span></span> <span data-ttu-id="be3d5-105">Você pode obter um objeto **IWbemCausalityAccess** usando uma interface de consulta (QI) para [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext).</span><span class="sxs-lookup"><span data-stu-id="be3d5-105">You can obtain an **IWbemCausalityAccess** object by using a query interface (QI) for [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext).</span></span> <span data-ttu-id="be3d5-106">Cada solicitação é identificada por um GUID (identificador global exclusivo) e pode ter uma solicitação pai ou pode ser uma solicitação superior.</span><span class="sxs-lookup"><span data-stu-id="be3d5-106">Each request is identified by a Globally Unique Identifier (GUID) and can have a parent request or can be a top request.</span></span> <span data-ttu-id="be3d5-107">Um GUID é um número de bits de 128 exclusivo.</span><span class="sxs-lookup"><span data-stu-id="be3d5-107">A GUID is a unique 128-bit number.</span></span> <span data-ttu-id="be3d5-108">Por exemplo, 5b2fc63a-8af4-44cb-960C-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="be3d5-108">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

## <a name="members"></a><span data-ttu-id="be3d5-109">Membros</span><span class="sxs-lookup"><span data-stu-id="be3d5-109">Members</span></span>

<span data-ttu-id="be3d5-110">A interface **IWbemCausalityAccess** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="be3d5-110">The **IWbemCausalityAccess** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="be3d5-111">**IWbemCausalityAccess** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="be3d5-111">**IWbemCausalityAccess** also has these types of members:</span></span>

-   [<span data-ttu-id="be3d5-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="be3d5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="be3d5-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="be3d5-113">Methods</span></span>

<span data-ttu-id="be3d5-114">A interface **IWbemCausalityAccess** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="be3d5-114">The **IWbemCausalityAccess** interface has these methods.</span></span>



| <span data-ttu-id="be3d5-115">Método</span><span class="sxs-lookup"><span data-stu-id="be3d5-115">Method</span></span>                                                    | <span data-ttu-id="be3d5-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="be3d5-116">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be3d5-117">**Getsolicitid**</span><span class="sxs-lookup"><span data-stu-id="be3d5-117">**GetRequestId**</span></span>](iwbemcausalityaccess-getrequestid.md) | <span data-ttu-id="be3d5-118">Retorna um identificador GUID exclusivo para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="be3d5-118">Returns a unique GUID identifier for a request.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="be3d5-119">**IsChildOf**</span><span class="sxs-lookup"><span data-stu-id="be3d5-119">**IsChildOf**</span></span>](iwbemcausalityaccess-ischildof.md)       | <span data-ttu-id="be3d5-120">Determina se uma solicitação é um filho de uma solicitação pai especificada.</span><span class="sxs-lookup"><span data-stu-id="be3d5-120">Determines if a request is a child of a specified parent request.</span></span> <span data-ttu-id="be3d5-121">Uma solicitação pai pode ter várias solicitações filho, cada uma identificada por um valor GUID exclusivo.</span><span class="sxs-lookup"><span data-stu-id="be3d5-121">A parent request can have multiple child requests, each identified by a unique GUID value.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="be3d5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be3d5-122">Requirements</span></span>



| <span data-ttu-id="be3d5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="be3d5-123">Requirement</span></span> | <span data-ttu-id="be3d5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="be3d5-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be3d5-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be3d5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="be3d5-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be3d5-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be3d5-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be3d5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="be3d5-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be3d5-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be3d5-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be3d5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="be3d5-130"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="be3d5-130"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="be3d5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="be3d5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be3d5-132"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be3d5-132"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be3d5-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="be3d5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be3d5-134">API COM para WMI</span><span class="sxs-lookup"><span data-stu-id="be3d5-134">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> </dl>

 

