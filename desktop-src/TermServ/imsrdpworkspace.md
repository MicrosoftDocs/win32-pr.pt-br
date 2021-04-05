---
title: Interface IMsRdpWorkspace
description: Expõe métodos que gerenciam credenciais de Conexão de RemoteApp e Área de Trabalho e conexões.
ms.assetid: cddcdfc2-b30a-4d00-84c2-ad036ab6288f
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
ms.openlocfilehash: 0ba55a02c5d984bc87aa05caffd42b3a3b965c43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918071"
---
# <a name="imsrdpworkspace-interface"></a><span data-ttu-id="4571e-105">Interface IMsRdpWorkspace</span><span class="sxs-lookup"><span data-stu-id="4571e-105">IMsRdpWorkspace interface</span></span>

<span data-ttu-id="4571e-106">Expõe métodos que gerenciam credenciais de Conexão de RemoteApp e Área de Trabalho e conexões.</span><span class="sxs-lookup"><span data-stu-id="4571e-106">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span> <span data-ttu-id="4571e-107">Essa interface é implementada pelo controle de Acesso via Web de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="4571e-107">This interface is implemented by the Remote Desktop Services Web Access Control.</span></span> <span data-ttu-id="4571e-108">Esse controle é um wrapper em volta do cliente de Conexão de Área de Trabalho Remota (MsTscAx.dll) e o proxy de tempo de execução de conexões de RemoteApp e área de trabalho (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="4571e-108">This control is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="4571e-109">Membros</span><span class="sxs-lookup"><span data-stu-id="4571e-109">Members</span></span>

<span data-ttu-id="4571e-110">A interface **IMsRdpWorkspace** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="4571e-110">The **IMsRdpWorkspace** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4571e-111">**IMsRdpWorkspace** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4571e-111">**IMsRdpWorkspace** also has these types of members:</span></span>

-   [<span data-ttu-id="4571e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4571e-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4571e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4571e-113">Methods</span></span>

<span data-ttu-id="4571e-114">A interface **IMsRdpWorkspace** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4571e-114">The **IMsRdpWorkspace** interface has these methods.</span></span>



| <span data-ttu-id="4571e-115">Método</span><span class="sxs-lookup"><span data-stu-id="4571e-115">Method</span></span>                                                                                   | <span data-ttu-id="4571e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="4571e-116">Description</span></span>                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4571e-117">[**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4571e-117">[**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))</span></span>             | <span data-ttu-id="4571e-118">Exclui as credenciais de usuário associadas à ID de conexão especificada.</span><span class="sxs-lookup"><span data-stu-id="4571e-118">Deletes the user credentials associated with the specified connection ID.</span></span><br/>                                                                                  |
| <span data-ttu-id="4571e-119">[**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4571e-119">[**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))</span></span>                       | <span data-ttu-id="4571e-120">Desconecta todas as conexões existentes associadas à ID de conexão especificada e exclui as credenciais de usuário correspondentes do repositório de credenciais.</span><span class="sxs-lookup"><span data-stu-id="4571e-120">Disconnects all existing connections associated with the specified connection ID and deletes the corresponding user credentials from the credential store.</span></span><br/> |
| <span data-ttu-id="4571e-121">[**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4571e-121">[**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85))</span></span> | <span data-ttu-id="4571e-122">Determina se as credenciais do usuário existem para a ID de conexão especificada.</span><span class="sxs-lookup"><span data-stu-id="4571e-122">Determines whether user credentials exist for the specified connection ID.</span></span><br/>                                                                                 |
| <span data-ttu-id="4571e-123">[**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4571e-123">[**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))</span></span>                   | <span data-ttu-id="4571e-124">Determina se o SSO (logon único) está habilitado para Conexão de RemoteApp e Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="4571e-124">Determines whether single sign on (SSO) is enabled for RemoteApp and Desktop Connection.</span></span><br/>                                                                   |
| <span data-ttu-id="4571e-125">[**Onautenticado**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4571e-125">[**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))</span></span>                               | <span data-ttu-id="4571e-126">Marca a autenticação de credenciais do usuário para a ID de conexão e, posteriormente, mostra a notificação de conexão na área de notificação da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="4571e-126">Marks the authentication of user credentials for the connection ID, and subsequently shows the connect notification in the taskbar notification area.</span></span> <br/>     |
| <span data-ttu-id="4571e-127">[**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4571e-127">[**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))</span></span>                                 | <span data-ttu-id="4571e-128">Associa credenciais de usuário e certificados com uma ID de conexão.</span><span class="sxs-lookup"><span data-stu-id="4571e-128">Associates user credentials and certificates with a connection ID.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="4571e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4571e-129">Requirements</span></span>



| <span data-ttu-id="4571e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4571e-130">Requirement</span></span> | <span data-ttu-id="4571e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="4571e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4571e-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4571e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4571e-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4571e-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4571e-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4571e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4571e-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4571e-135">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="4571e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4571e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4571e-137"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4571e-137"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |
| <span data-ttu-id="4571e-138">IID</span><span class="sxs-lookup"><span data-stu-id="4571e-138">IID</span></span><br/>                      | <span data-ttu-id="4571e-139">IID \_ IMsRdpWorkspace é definido como 145D0621-04CF-4FC2-A766-A81A9069CDF8</span><span class="sxs-lookup"><span data-stu-id="4571e-139">IID\_IMsRdpWorkspace is defined as 145D0621-04CF-4FC2-A766-A81A9069CDF8</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4571e-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="4571e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4571e-141">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="4571e-141">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

