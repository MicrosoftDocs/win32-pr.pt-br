---
title: Interface IMsRdpClientShell
description: As configurações de cliente Conexão de Área de Trabalho Remota (RDC) que são usadas para iniciar o cliente do Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de outros portais da Web.
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientShell
- Serviços de Área de Trabalho Remota da interface IMsRdpClientShell, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b529ed1819864e5fc6106472b33ddd00312560c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455493"
---
# <a name="imsrdpclientshell-interface"></a><span data-ttu-id="c034e-105">Interface IMsRdpClientShell</span><span class="sxs-lookup"><span data-stu-id="c034e-105">IMsRdpClientShell interface</span></span>

<span data-ttu-id="c034e-106">As configurações de cliente Conexão de Área de Trabalho Remota (RDC) que são usadas para iniciar o cliente do Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de outros portais da Web.</span><span class="sxs-lookup"><span data-stu-id="c034e-106">Remote Desktop Connection (RDC) client settings that are used to launch the client from Remote Desktop Web Access (RD Web Access) or from other web portals.</span></span>

## <a name="members"></a><span data-ttu-id="c034e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c034e-107">Members</span></span>

<span data-ttu-id="c034e-108">A interface **IMsRdpClientShell** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="c034e-108">The **IMsRdpClientShell** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c034e-109">**IMsRdpClientShell** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c034e-109">**IMsRdpClientShell** also has these types of members:</span></span>

-   [<span data-ttu-id="c034e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="c034e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c034e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c034e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c034e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c034e-112">Methods</span></span>

<span data-ttu-id="c034e-113">A interface **IMsRdpClientShell** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c034e-113">The **IMsRdpClientShell** interface has these methods.</span></span>



| <span data-ttu-id="c034e-114">Método</span><span class="sxs-lookup"><span data-stu-id="c034e-114">Method</span></span>                                                     | <span data-ttu-id="c034e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c034e-115">Description</span></span>                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| <span data-ttu-id="c034e-116">[**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c034e-116">[**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85))</span></span> | <span data-ttu-id="c034e-117">Recupera uma única propriedade RDP.</span><span class="sxs-lookup"><span data-stu-id="c034e-117">Retrieves a single RDP property.</span></span><br/>                  |
| [<span data-ttu-id="c034e-118">**Inicializar**</span><span class="sxs-lookup"><span data-stu-id="c034e-118">**Launch**</span></span>](imsrdpclientshell-launch.md)                 | <span data-ttu-id="c034e-119">Inicia o conteúdo do arquivo remoto no portal da Web.</span><span class="sxs-lookup"><span data-stu-id="c034e-119">Launches remote file content from the web portal.</span></span><br/> |
| <span data-ttu-id="c034e-120">[**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c034e-120">[**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85))</span></span> | <span data-ttu-id="c034e-121">Define uma única propriedade RDP.</span><span class="sxs-lookup"><span data-stu-id="c034e-121">Sets a single RDP property.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="c034e-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c034e-122">Properties</span></span>

<span data-ttu-id="c034e-123">A interface **IMsRdpClientShell** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c034e-123">The **IMsRdpClientShell** interface has these properties.</span></span>



| <span data-ttu-id="c034e-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c034e-124">Property</span></span>                                                                                              | <span data-ttu-id="c034e-125">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="c034e-125">Access type</span></span>           | <span data-ttu-id="c034e-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="c034e-126">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c034e-127">**IsRemoteProgramClientInstalled**</span><span class="sxs-lookup"><span data-stu-id="c034e-127">**IsRemoteProgramClientInstalled**</span></span>](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | <span data-ttu-id="c034e-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c034e-128">Read-only</span></span><br/>  | <span data-ttu-id="c034e-129">Recupera se o cliente de Conexão de Área de Trabalho Remota (RDC) dá suporte à funcionalidade do RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="c034e-129">Retrieves whether the Remote Desktop Connection (RDC) client supports RemoteApp functionality.</span></span><br/> |
| [<span data-ttu-id="c034e-130">**Públicomode**</span><span class="sxs-lookup"><span data-stu-id="c034e-130">**PublicMode**</span></span>](imsrdpclientshell-publicmode.md)<br/>                                         | <span data-ttu-id="c034e-131">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c034e-131">Read/write</span></span><br/> | <span data-ttu-id="c034e-132">Recupera se o modo público está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c034e-132">Retrieves whether public mode is enabled.</span></span><br/>                                                      |
| [<span data-ttu-id="c034e-133">**RdpFileContents**</span><span class="sxs-lookup"><span data-stu-id="c034e-133">**RdpFileContents**</span></span>](imsrdpclientshell-rdpfilecontents.md)<br/>                               | <span data-ttu-id="c034e-134">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c034e-134">Read/write</span></span><br/> | <span data-ttu-id="c034e-135">Versão de fluxo do arquivo de configuração de RDP.</span><span class="sxs-lookup"><span data-stu-id="c034e-135">Stream version of the RDP configuration file.</span></span><br/>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="c034e-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c034e-136">Requirements</span></span>



| <span data-ttu-id="c034e-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c034e-137">Requirement</span></span> | <span data-ttu-id="c034e-138">Valor</span><span class="sxs-lookup"><span data-stu-id="c034e-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c034e-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c034e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c034e-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c034e-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c034e-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c034e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c034e-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c034e-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c034e-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c034e-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="c034e-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c034e-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c034e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c034e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c034e-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c034e-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c034e-147">IID</span><span class="sxs-lookup"><span data-stu-id="c034e-147">IID</span></span><br/>                      | <span data-ttu-id="c034e-148">IID \_ IMsRdpClientShell é definido como d012ae6d-c19a-4bfe-B367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="c034e-148">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="c034e-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="c034e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c034e-150">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="c034e-150">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="c034e-151">Referência de Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="c034e-151">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

