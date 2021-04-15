---
title: Interface IMsRdpPreferredRedirectionInfo
description: Fornece uma propriedade para controlar o uso de um servidor de redirecionamento.
ms.assetid: 1EAD9B15-4A84-4179-8A92-F0736B04B4F1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpPreferredRedirectionInfo
- Serviços de Área de Trabalho Remota da interface IMsRdpPreferredRedirectionInfo, descrita
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8ea28c36ca06548128954298e35c0cc20de5b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454780"
---
# <a name="imsrdppreferredredirectioninfo-interface"></a><span data-ttu-id="cd7f6-105">Interface IMsRdpPreferredRedirectionInfo</span><span class="sxs-lookup"><span data-stu-id="cd7f6-105">IMsRdpPreferredRedirectionInfo interface</span></span>

<span data-ttu-id="cd7f6-106">Fornece uma propriedade para controlar o uso de um servidor de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="cd7f6-106">Provides a property to control using a redirection server.</span></span>

## <a name="members"></a><span data-ttu-id="cd7f6-107">Membros</span><span class="sxs-lookup"><span data-stu-id="cd7f6-107">Members</span></span>

<span data-ttu-id="cd7f6-108">A interface **IMsRdpPreferredRedirectionInfo** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cd7f6-108">The **IMsRdpPreferredRedirectionInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cd7f6-109">**IMsRdpPreferredRedirectionInfo** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cd7f6-109">**IMsRdpPreferredRedirectionInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="cd7f6-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cd7f6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd7f6-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cd7f6-111">Properties</span></span>

<span data-ttu-id="cd7f6-112">A interface **IMsRdpPreferredRedirectionInfo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cd7f6-112">The **IMsRdpPreferredRedirectionInfo** interface has these properties.</span></span>



| <span data-ttu-id="cd7f6-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cd7f6-113">Property</span></span>                                                                                               | <span data-ttu-id="cd7f6-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="cd7f6-114">Access type</span></span>           | <span data-ttu-id="cd7f6-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd7f6-115">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="cd7f6-116">**UseRedirectionServerName**</span><span class="sxs-lookup"><span data-stu-id="cd7f6-116">**UseRedirectionServerName**</span></span>](imsrdppreferredredirectioninfo-useredirectionservername.md)<br/> | <span data-ttu-id="cd7f6-117">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd7f6-117">Read/write</span></span><br/> | <span data-ttu-id="cd7f6-118">Obtém e define se deve ser usado o nome do servidor de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="cd7f6-118">Gets and sets whether to use the redirection server name.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cd7f6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd7f6-119">Requirements</span></span>



| <span data-ttu-id="cd7f6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd7f6-120">Requirement</span></span> | <span data-ttu-id="cd7f6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cd7f6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd7f6-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd7f6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cd7f6-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cd7f6-123">Windows 8</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="cd7f6-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd7f6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cd7f6-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd7f6-125">Windows Server 2012</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="cd7f6-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cd7f6-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="cd7f6-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd7f6-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cd7f6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="cd7f6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd7f6-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd7f6-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cd7f6-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="cd7f6-130">CLSID</span></span><br/>                    | <span data-ttu-id="cd7f6-131">CLSID \_ MsRdpClient10 é definido como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span><span class="sxs-lookup"><span data-stu-id="cd7f6-131">CLSID\_MsRdpClient10 is defined as C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span></span><br/> <span data-ttu-id="cd7f6-132">CLSID \_ MsRdpClient10NotSafeForScripting é definido como A0C63C30-F08D-4AB4-907C-34905D770C7D</span><span class="sxs-lookup"><span data-stu-id="cd7f6-132">CLSID\_MsRdpClient10NotSafeForScripting is defined as A0C63C30-F08D-4AB4-907C-34905D770C7D</span></span><br/> <span data-ttu-id="cd7f6-133">CLSID \_ MsRdpClient7 é definido como A9D7038D-B5ED-472e-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="cd7f6-133">CLSID\_MsRdpClient7 is defined as A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span><br/> <span data-ttu-id="cd7f6-134">CLSID \_ MsRdpClient7NotSafeForScripting é definido como 54D38BF7-B1EF-4479-9674-1BD6EA465258</span><span class="sxs-lookup"><span data-stu-id="cd7f6-134">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span><br/> <span data-ttu-id="cd7f6-135">CLSID \_ MsRdpClient8 é definido como 5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="cd7f6-135">CLSID\_MsRdpClient8 is defined as 5F681803-2900-4C43-A1CC-CF405404A676</span></span><br/> <span data-ttu-id="cd7f6-136">CLSID \_ MsRdpClient8NotSafeForScripting é definido como A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="cd7f6-136">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="cd7f6-137">CLSID \_ MsRdpClient9 é definido como 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="cd7f6-137">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="cd7f6-138">CLSID \_ MsRdpClient9NotSafeForScripting é definido como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="cd7f6-138">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="cd7f6-139">IID</span><span class="sxs-lookup"><span data-stu-id="cd7f6-139">IID</span></span><br/>                      | <span data-ttu-id="cd7f6-140">IID \_ IMsRdpPreferredRedirectionInfo é definido como FDD029F9-9574-4DEF-8529-64B521CCCAA4</span><span class="sxs-lookup"><span data-stu-id="cd7f6-140">IID\_IMsRdpPreferredRedirectionInfo is defined as FDD029F9-9574-4DEF-8529-64B521CCCAA4</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

