---
title: Interface IMsRdpWorkspace2
description: Expõe um método que associa Conexão de RemoteApp e Área de Trabalho credenciais a uma conexão.
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpWorkspace
- Serviços de Área de Trabalho Remota da interface IMsRdpWorkspace, descrita
topic_type:
- apiref
api_name:
- IMsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d6b5ff193eec393b67029d355a0f0c1bc67c0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009295"
---
# <a name="imsrdpworkspace2-interface"></a><span data-ttu-id="4abb8-105">Interface IMsRdpWorkspace2</span><span class="sxs-lookup"><span data-stu-id="4abb8-105">IMsRdpWorkspace2 interface</span></span>

<span data-ttu-id="4abb8-106">Expõe um método que associa Conexão de RemoteApp e Área de Trabalho credenciais a uma conexão.</span><span class="sxs-lookup"><span data-stu-id="4abb8-106">Exposes a method that associates RemoteApp and Desktop Connection credentials with a connection.</span></span> <span data-ttu-id="4abb8-107">Essa interface é implementada pelo controle de Acesso via Web de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="4abb8-107">This interface is implemented by the Remote Desktop Services Web Access Control.</span></span> <span data-ttu-id="4abb8-108">Esse controle é um wrapper em volta do cliente de Conexão de Área de Trabalho Remota (MsTscAx.dll) e o proxy de tempo de execução de conexões de RemoteApp e área de trabalho (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="4abb8-108">This control is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="4abb8-109">Membros</span><span class="sxs-lookup"><span data-stu-id="4abb8-109">Members</span></span>

<span data-ttu-id="4abb8-110">A interface **IMsRdpWorkspace** herda de [**IMsRdpWorkspace**](imsrdpworkspace.md).</span><span class="sxs-lookup"><span data-stu-id="4abb8-110">The **IMsRdpWorkspace** interface inherits from [**IMsRdpWorkspace**](imsrdpworkspace.md).</span></span> <span data-ttu-id="4abb8-111">**IMsRdpWorkspace2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4abb8-111">**IMsRdpWorkspace2** also has these types of members:</span></span>

-   [<span data-ttu-id="4abb8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4abb8-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4abb8-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4abb8-113">Methods</span></span>

<span data-ttu-id="4abb8-114">A interface **IMsRdpWorkspace** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4abb8-114">The **IMsRdpWorkspace** interface has these methods.</span></span>



| <span data-ttu-id="4abb8-115">Método</span><span class="sxs-lookup"><span data-stu-id="4abb8-115">Method</span></span>                                                        | <span data-ttu-id="4abb8-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="4abb8-116">Description</span></span>                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="4abb8-117">[**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4abb8-117">[**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85))</span></span> | <span data-ttu-id="4abb8-118">Associa credenciais de usuário e certificados com uma ID de conexão.</span><span class="sxs-lookup"><span data-stu-id="4abb8-118">Associates user credentials and certificates with a connection ID.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="4abb8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4abb8-119">Requirements</span></span>



| <span data-ttu-id="4abb8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4abb8-120">Requirement</span></span> | <span data-ttu-id="4abb8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4abb8-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4abb8-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4abb8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4abb8-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4abb8-123">Windows 8</span></span><br/>                                                                          |
| <span data-ttu-id="4abb8-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4abb8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4abb8-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4abb8-125">Windows Server 2012</span></span><br/>                                                                |
| <span data-ttu-id="4abb8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4abb8-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4abb8-127"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4abb8-127"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |
| <span data-ttu-id="4abb8-128">IID</span><span class="sxs-lookup"><span data-stu-id="4abb8-128">IID</span></span><br/>                      | <span data-ttu-id="4abb8-129">IID \_ IMsRdpWorkspace2 é definido como 145D0622-04CF-4FC3-A776-A82A9169CDF8</span><span class="sxs-lookup"><span data-stu-id="4abb8-129">IID\_IMsRdpWorkspace2 is defined as 145D0622-04CF-4FC3-A776-A82A9169CDF8</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="4abb8-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4abb8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4abb8-131">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="4abb8-131">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> <dt>

[<span data-ttu-id="4abb8-132">**IMsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="4abb8-132">**IMsRdpWorkspace**</span></span>](imsrdpworkspace.md)
</dt> </dl>

 

