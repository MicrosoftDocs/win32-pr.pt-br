---
title: Interface IMsRdpClientShell2
description: Expõe as propriedades que iniciam o cliente do Conexão de Área de Trabalho Remota do Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de outros portais da Web.
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientShell2
- Serviços de Área de Trabalho Remota da interface IMsRdpClientShell2, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientShell2
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb93fd938602b195f60877be884dbe0bd458a598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644412"
---
# <a name="imsrdpclientshell2-interface"></a><span data-ttu-id="8d78e-105">Interface IMsRdpClientShell2</span><span class="sxs-lookup"><span data-stu-id="8d78e-105">IMsRdpClientShell2 interface</span></span>

<span data-ttu-id="8d78e-106">Expõe as propriedades que iniciam o cliente do Conexão de Área de Trabalho Remota do Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de outros portais da Web.</span><span class="sxs-lookup"><span data-stu-id="8d78e-106">Exposes properties that launch the Remote Desktop Connection client from Remote Desktop Web Access (RD Web Access) or from other web portals.</span></span>

<span data-ttu-id="8d78e-107">Essa interface é implementada pelo controle de Acesso via Web de Serviços de Área de Trabalho Remota, que é um wrapper em volta do cliente Conexão de Área de Trabalho Remota (MsTscAx.dll) e o proxy de tempo de execução de conexões do RemoteApp e da área de trabalho (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="8d78e-107">This interface is implemented by the Remote Desktop Services Web Access Control, which is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="8d78e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8d78e-108">Members</span></span>

<span data-ttu-id="8d78e-109">A interface **IMsRdpClientShell2** herda de **IMsRdpClientShell**.</span><span class="sxs-lookup"><span data-stu-id="8d78e-109">The **IMsRdpClientShell2** interface inherits from **IMsRdpClientShell**.</span></span> <span data-ttu-id="8d78e-110">**IMsRdpClientShell2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8d78e-110">**IMsRdpClientShell2** also has these types of members:</span></span>

-   [<span data-ttu-id="8d78e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8d78e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d78e-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8d78e-112">Properties</span></span>

<span data-ttu-id="8d78e-113">A interface **IMsRdpClientShell2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8d78e-113">The **IMsRdpClientShell2** interface has these properties.</span></span>



| <span data-ttu-id="8d78e-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8d78e-114">Property</span></span>                                                                               | <span data-ttu-id="8d78e-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="8d78e-115">Access type</span></span>          | <span data-ttu-id="8d78e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d78e-116">Description</span></span>                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d78e-117">**MsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="8d78e-117">**MsRdpWorkspace**</span></span>](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | <span data-ttu-id="8d78e-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d78e-118">Read-only</span></span><br/> | <span data-ttu-id="8d78e-119">Recupera um ponteiro para a interface [**IMsRdpWorkspace**](imsrdpworkspace.md) , que é usada para gerenciar conexão de RemoteApp e área de trabalho credenciais e conexões.</span><span class="sxs-lookup"><span data-stu-id="8d78e-119">Retrieves a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface, which is used to manage RemoteApp and Desktop Connection credentials and connections.</span></span><br/> |
| [<span data-ttu-id="8d78e-120">**SecuredSettingsEnabled**</span><span class="sxs-lookup"><span data-stu-id="8d78e-120">**SecuredSettingsEnabled**</span></span>](imsrdpclientshell2-securedsettingsenabled.md)<br/> | <span data-ttu-id="8d78e-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d78e-121">Read-only</span></span><br/> | <span data-ttu-id="8d78e-122">Recupera um valor que indica se a página da Web atual está em uma zona de segurança de URL confiável do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8d78e-122">Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span><br/>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="8d78e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d78e-123">Requirements</span></span>



| <span data-ttu-id="8d78e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d78e-124">Requirement</span></span> | <span data-ttu-id="8d78e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8d78e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d78e-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d78e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8d78e-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8d78e-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8d78e-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d78e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8d78e-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d78e-129">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="8d78e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8d78e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d78e-131"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d78e-131"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d78e-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d78e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d78e-133">**IMsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="8d78e-133">**IMsRdpWorkspace**</span></span>](imsrdpworkspace.md)
</dt> </dl>

 

 





