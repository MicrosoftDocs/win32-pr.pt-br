---
title: Interface IMsRdpDrive
description: Contém informações sobre um objeto de unidade.
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpDrive
- Serviços de Área de Trabalho Remota da interface IMsRdpDrive, descrita
topic_type:
- apiref
api_name:
- IMsRdpDrive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 032e62ca54d6adccce9b27c8f7e95160c800759b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644272"
---
# <a name="imsrdpdrive-interface"></a><span data-ttu-id="1f536-105">Interface IMsRdpDrive</span><span class="sxs-lookup"><span data-stu-id="1f536-105">IMsRdpDrive interface</span></span>

<span data-ttu-id="1f536-106">Contém informações sobre um objeto de unidade.</span><span class="sxs-lookup"><span data-stu-id="1f536-106">Contains information about a drive object.</span></span>

## <a name="members"></a><span data-ttu-id="1f536-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1f536-107">Members</span></span>

<span data-ttu-id="1f536-108">A interface **IMsRdpDrive** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1f536-108">The **IMsRdpDrive** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1f536-109">**IMsRdpDrive** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1f536-109">**IMsRdpDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="1f536-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f536-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f536-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f536-111">Properties</span></span>

<span data-ttu-id="1f536-112">A interface **IMsRdpDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1f536-112">The **IMsRdpDrive** interface has these properties.</span></span>



| <span data-ttu-id="1f536-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1f536-113">Property</span></span>                                                            | <span data-ttu-id="1f536-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="1f536-114">Access type</span></span>           | <span data-ttu-id="1f536-115">Description</span><span class="sxs-lookup"><span data-stu-id="1f536-115">Description</span></span>                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [<span data-ttu-id="1f536-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="1f536-116">**Name**</span></span>](imsrdpdrive-name.md)<br/>                         | <span data-ttu-id="1f536-117">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f536-117">Read-only</span></span><br/>  | <span data-ttu-id="1f536-118">Recupera o nome da unidade.</span><span class="sxs-lookup"><span data-stu-id="1f536-118">Retrieves the name of the drive.</span></span><br/>              |
| [<span data-ttu-id="1f536-119">**De redirecionamento**</span><span class="sxs-lookup"><span data-stu-id="1f536-119">**RedirectionState**</span></span>](imsrdpdrive-redirectionstate.md)<br/> | <span data-ttu-id="1f536-120">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1f536-120">Read/write</span></span><br/> | <span data-ttu-id="1f536-121">Indica o estado de redirecionamento da unidade.</span><span class="sxs-lookup"><span data-stu-id="1f536-121">Indicates the redirection state of the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1f536-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f536-122">Requirements</span></span>



| <span data-ttu-id="1f536-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f536-123">Requirement</span></span> | <span data-ttu-id="1f536-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1f536-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f536-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f536-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1f536-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f536-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1f536-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f536-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1f536-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f536-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1f536-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1f536-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f536-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f536-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1f536-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1f536-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f536-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f536-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1f536-133">IID</span><span class="sxs-lookup"><span data-stu-id="1f536-133">IID</span></span><br/>                      | <span data-ttu-id="1f536-134">IID \_ IMsRdpDrive é definido como d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="1f536-134">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="1f536-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1f536-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f536-136">Referência de Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="1f536-136">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="1f536-137">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="1f536-137">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

