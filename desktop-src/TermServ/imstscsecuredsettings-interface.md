---
title: Interface IMsTscSecuredSettings
description: Inclui métodos para recuperar e definir as propriedades do Área de Trabalho Remota controle ActiveX que são restritos a zonas de segurança de URL específicas do Internet Explorer. | Interface IMsTscSecuredSettings
ms.assetid: 1136dbc5-abe6-40e0-b44f-700a1460fbd2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsTscSecuredSettings
- Serviços de Área de Trabalho Remota da interface IMsTscSecuredSettings, descrita
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2037393147bd5a2e35d6eb803951890c9b5e7de5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105784062"
---
# <a name="imstscsecuredsettings-interface"></a><span data-ttu-id="27f24-106">Interface IMsTscSecuredSettings</span><span class="sxs-lookup"><span data-stu-id="27f24-106">IMsTscSecuredSettings interface</span></span>

<span data-ttu-id="27f24-107">Inclui métodos para recuperar e definir as propriedades do Área de Trabalho Remota controle ActiveX que são restritos a zonas de segurança de URL específicas do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="27f24-107">Includes methods to retrieve and set properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span> <span data-ttu-id="27f24-108">As propriedades incluem aquelas que especificam o modo do controle de cliente (modo de tela inteira ou modo de janela) e o programa a ser iniciado após a conexão com o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="27f24-108">Properties include those that specify the mode of the client control (full-screen mode or window mode) and the program to start upon connection to the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="27f24-109">Esses métodos também estão disponíveis por meio da interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="27f24-109">These methods are also available through the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="27f24-110">Membros</span><span class="sxs-lookup"><span data-stu-id="27f24-110">Members</span></span>

<span data-ttu-id="27f24-111">A interface **IMsTscSecuredSettings** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="27f24-111">The **IMsTscSecuredSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="27f24-112">**IMsTscSecuredSettings** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="27f24-112">**IMsTscSecuredSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="27f24-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="27f24-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27f24-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="27f24-114">Properties</span></span>

<span data-ttu-id="27f24-115">A interface **IMsTscSecuredSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="27f24-115">The **IMsTscSecuredSettings** interface has these properties.</span></span>



| <span data-ttu-id="27f24-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="27f24-116">Property</span></span>                                                              | <span data-ttu-id="27f24-117">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="27f24-117">Access type</span></span>           | <span data-ttu-id="27f24-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="27f24-118">Description</span></span>                                                                |
|:----------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="27f24-119">**FullScreen**</span><span class="sxs-lookup"><span data-stu-id="27f24-119">**FullScreen**</span></span>](imstscsecuredsettings-fullscreen.md)<br/>     | <span data-ttu-id="27f24-120">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="27f24-120">Read/write</span></span><br/> | <span data-ttu-id="27f24-121">O estado de tela inteira do controle de cliente.</span><span class="sxs-lookup"><span data-stu-id="27f24-121">The full-screen state of the client control.</span></span><br/>                    |
| [<span data-ttu-id="27f24-122">**StartProgram**</span><span class="sxs-lookup"><span data-stu-id="27f24-122">**StartProgram**</span></span>](imstscsecuredsettings-startprogram.md)<br/> | <span data-ttu-id="27f24-123">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="27f24-123">Read/write</span></span><br/> | <span data-ttu-id="27f24-124">O programa a ser iniciado no servidor remoto durante a conexão.</span><span class="sxs-lookup"><span data-stu-id="27f24-124">The program to be started on the remote server upon connection.</span></span><br/> |
| [<span data-ttu-id="27f24-125">**WorkDir**</span><span class="sxs-lookup"><span data-stu-id="27f24-125">**WorkDir**</span></span>](imstscsecuredsettings-workdir.md)<br/>           | <span data-ttu-id="27f24-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="27f24-126">Read/write</span></span><br/> | <span data-ttu-id="27f24-127">O diretório de trabalho do programa de início.</span><span class="sxs-lookup"><span data-stu-id="27f24-127">The working directory of the start program.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="27f24-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="27f24-128">Remarks</span></span>

<span data-ttu-id="27f24-129">Consulte [fornecer para o RDP Client Security](providing-for-rdp-client-security.md) para obter mais informações sobre os métodos dessa interface.</span><span class="sxs-lookup"><span data-stu-id="27f24-129">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about the methods of this interface.</span></span>

<span data-ttu-id="27f24-130">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="27f24-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27f24-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27f24-131">Requirements</span></span>



| <span data-ttu-id="27f24-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="27f24-132">Requirement</span></span> | <span data-ttu-id="27f24-133">Valor</span><span class="sxs-lookup"><span data-stu-id="27f24-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27f24-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27f24-134">Minimum supported client</span></span><br/> | <span data-ttu-id="27f24-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27f24-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="27f24-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27f24-136">Minimum supported server</span></span><br/> | <span data-ttu-id="27f24-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27f24-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="27f24-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="27f24-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="27f24-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27f24-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="27f24-140">DLL</span><span class="sxs-lookup"><span data-stu-id="27f24-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27f24-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27f24-141"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27f24-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="27f24-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27f24-143">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="27f24-143">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="27f24-144">Referência de Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="27f24-144">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

