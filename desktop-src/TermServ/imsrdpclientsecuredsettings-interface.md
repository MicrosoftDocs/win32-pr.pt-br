---
title: Interface IMsRdpClientSecuredSettings
description: Inclui métodos para recuperar e definir as propriedades do Área de Trabalho Remota controle ActiveX que são restritos a zonas de segurança de URL específicas do Internet Explorer. | Interface IMsRdpClientSecuredSettings
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientSecuredSettings
- Serviços de Área de Trabalho Remota da interface IMsRdpClientSecuredSettings, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e6b58b2be0122076b5529b910423377417fa6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105783339"
---
# <a name="imsrdpclientsecuredsettings-interface"></a><span data-ttu-id="9dace-106">Interface IMsRdpClientSecuredSettings</span><span class="sxs-lookup"><span data-stu-id="9dace-106">IMsRdpClientSecuredSettings interface</span></span>

<span data-ttu-id="9dace-107">Inclui métodos para recuperar e definir as propriedades do Área de Trabalho Remota controle ActiveX que são restritos a zonas de segurança de URL específicas do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9dace-107">Includes methods to retrieve and set properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span>

## <a name="members"></a><span data-ttu-id="9dace-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9dace-108">Members</span></span>

<span data-ttu-id="9dace-109">A interface **IMsRdpClientSecuredSettings** herda de [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="9dace-109">The **IMsRdpClientSecuredSettings** interface inherits from [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span></span> <span data-ttu-id="9dace-110">**IMsRdpClientSecuredSettings** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9dace-110">**IMsRdpClientSecuredSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="9dace-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9dace-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9dace-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9dace-112">Properties</span></span>

<span data-ttu-id="9dace-113">A interface **IMsRdpClientSecuredSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9dace-113">The **IMsRdpClientSecuredSettings** interface has these properties.</span></span>



| <span data-ttu-id="9dace-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9dace-114">Property</span></span>                                                                                   | <span data-ttu-id="9dace-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="9dace-115">Access type</span></span>           | <span data-ttu-id="9dace-116">Description</span><span class="sxs-lookup"><span data-stu-id="9dace-116">Description</span></span>                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [<span data-ttu-id="9dace-117">**AudioRedirectionMode**</span><span class="sxs-lookup"><span data-stu-id="9dace-117">**AudioRedirectionMode**</span></span>](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | <span data-ttu-id="9dace-118">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9dace-118">Read/write</span></span><br/> | <span data-ttu-id="9dace-119">As configurações de redirecionamento de áudio.</span><span class="sxs-lookup"><span data-stu-id="9dace-119">The audio redirection settings.</span></span><br/>    |
| [<span data-ttu-id="9dace-120">**KeyboardHookMode**</span><span class="sxs-lookup"><span data-stu-id="9dace-120">**KeyboardHookMode**</span></span>](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | <span data-ttu-id="9dace-121">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9dace-121">Read/write</span></span><br/> | <span data-ttu-id="9dace-122">As configurações de redirecionamento de teclado.</span><span class="sxs-lookup"><span data-stu-id="9dace-122">The keyboard redirection settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9dace-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="9dace-123">Remarks</span></span>

<span data-ttu-id="9dace-124">Essas propriedades não podem ser definidas quando o controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="9dace-124">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="9dace-125">Consulte [fornecer para o RDP Client Security](providing-for-rdp-client-security.md) para obter mais informações sobre os métodos dessa interface.</span><span class="sxs-lookup"><span data-stu-id="9dace-125">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about the methods of this interface.</span></span>

<span data-ttu-id="9dace-126">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9dace-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9dace-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dace-127">Requirements</span></span>



| <span data-ttu-id="9dace-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dace-128">Requirement</span></span> | <span data-ttu-id="9dace-129">Valor</span><span class="sxs-lookup"><span data-stu-id="9dace-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dace-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9dace-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9dace-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9dace-131">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="9dace-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9dace-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9dace-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9dace-133">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="9dace-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9dace-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="9dace-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dace-135"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="9dace-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9dace-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dace-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dace-137"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="9dace-138">IID</span><span class="sxs-lookup"><span data-stu-id="9dace-138">IID</span></span><br/>                      | <span data-ttu-id="9dace-139">IID \_ IMsRdpClientSecuredSettings é definido como 605befcf-39c1-45CC-a811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="9dace-139">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9dace-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="9dace-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dace-141">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="9dace-141">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="9dace-142">Referência de Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="9dace-142">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





