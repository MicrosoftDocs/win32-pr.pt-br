---
title: Interface IMsRdpClientAdvancedSettings2
description: Gerencia configurações avançadas do cliente. Deriva da interface IMsRdpClientAdvancedSettings.
ms.assetid: 78cffdf5-bd99-4140-80b6-aa8632894487
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings2, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d7f9ad9b93c0f3cd1d62fdbbaddf4faa55ad9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295823"
---
# <a name="imsrdpclientadvancedsettings2-interface"></a><span data-ttu-id="0b39f-106">Interface IMsRdpClientAdvancedSettings2</span><span class="sxs-lookup"><span data-stu-id="0b39f-106">IMsRdpClientAdvancedSettings2 interface</span></span>

<span data-ttu-id="0b39f-107">Gerencia configurações avançadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="0b39f-107">Manages advanced client settings.</span></span> <span data-ttu-id="0b39f-108">Deriva da interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="0b39f-108">Derives from the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="0b39f-109">Essa interface inclui métodos para recuperar e definir propriedades avançadas (opcionais) para o controle ActiveX Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="0b39f-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="0b39f-110">Para obter uma instância dessa interface, use a propriedade [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obter um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="0b39f-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="0b39f-111">Em seguida, chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro **IMsTscAdvancedSettings** e passe **\_ IMsRdpClientAdvancedSettings2 de IID** para **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="0b39f-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings2** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="0b39f-112">Membros</span><span class="sxs-lookup"><span data-stu-id="0b39f-112">Members</span></span>

<span data-ttu-id="0b39f-113">A interface **IMsRdpClientAdvancedSettings2** herda de [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="0b39f-113">The **IMsRdpClientAdvancedSettings2** interface inherits from [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).</span></span> <span data-ttu-id="0b39f-114">**IMsRdpClientAdvancedSettings2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0b39f-114">**IMsRdpClientAdvancedSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="0b39f-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b39f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b39f-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b39f-116">Properties</span></span>

<span data-ttu-id="0b39f-117">A interface **IMsRdpClientAdvancedSettings2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0b39f-117">The **IMsRdpClientAdvancedSettings2** interface has these properties.</span></span>



| <span data-ttu-id="0b39f-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0b39f-118">Property</span></span>                                                                                      | <span data-ttu-id="0b39f-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="0b39f-119">Access type</span></span>           | <span data-ttu-id="0b39f-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b39f-120">Description</span></span>                                                                                                                                           |
|:----------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b39f-121">**CanAutoReconnect**</span><span class="sxs-lookup"><span data-stu-id="0b39f-121">**CanAutoReconnect**</span></span>](imsrdpclientadvancedsettings2-canautoreconnect.md)<br/>         | <span data-ttu-id="0b39f-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b39f-122">Read-only</span></span><br/>  | <span data-ttu-id="0b39f-123">Especifica se o controle de cliente é capaz de se reconectar automaticamente à sessão atual no caso de uma desconexão de rede.</span><span class="sxs-lookup"><span data-stu-id="0b39f-123">Specifies whether the client control is able to reconnect automatically to the current session in the event of a network disconnection.</span></span><br/>    |
| [<span data-ttu-id="0b39f-124">**EnableAutoReconnect**</span><span class="sxs-lookup"><span data-stu-id="0b39f-124">**EnableAutoReconnect**</span></span>](imsrdpclientadvancedsettings2-enableautoreconnect.md)<br/>   | <span data-ttu-id="0b39f-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b39f-125">Read/write</span></span><br/> | <span data-ttu-id="0b39f-126">Especifica se o controle de cliente deve ser habilitado para se reconectar automaticamente a uma sessão no caso de uma desconexão de rede.</span><span class="sxs-lookup"><span data-stu-id="0b39f-126">Specifies whether to enable the client control to reconnect automatically to a session in the event of a network disconnection.</span></span><br/>            |
| [<span data-ttu-id="0b39f-127">**MaxReconnectAttempts**</span><span class="sxs-lookup"><span data-stu-id="0b39f-127">**MaxReconnectAttempts**</span></span>](imsrdpclientadvancedsettings2-maxreconnectattempts.md)<br/> | <span data-ttu-id="0b39f-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b39f-128">Read/write</span></span><br/> | <span data-ttu-id="0b39f-129">Especifica o número de vezes para tentar se reconectar durante a reconexão automática.</span><span class="sxs-lookup"><span data-stu-id="0b39f-129">Specifies the number of times to try to reconnect during automatic reconnection.</span></span> <span data-ttu-id="0b39f-130">Os valores válidos dessa propriedade são de 0 a 200, inclusive.</span><span class="sxs-lookup"><span data-stu-id="0b39f-130">The valid values of this property are 0 to 200 inclusive.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b39f-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b39f-131">Remarks</span></span>

<span data-ttu-id="0b39f-132">Essa interface foi estendida pelas seguintes interfaces, com cada nova interface herdando todos os métodos e propriedades das interfaces anteriores:</span><span class="sxs-lookup"><span data-stu-id="0b39f-132">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="0b39f-133">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0b39f-133">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
-   [<span data-ttu-id="0b39f-134">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="0b39f-134">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="0b39f-135">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0b39f-135">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="0b39f-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0b39f-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="0b39f-137">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0b39f-137">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="0b39f-138">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0b39f-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b39f-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b39f-139">Requirements</span></span>



| <span data-ttu-id="0b39f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b39f-140">Requirement</span></span> | <span data-ttu-id="0b39f-141">Valor</span><span class="sxs-lookup"><span data-stu-id="0b39f-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b39f-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b39f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0b39f-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b39f-143">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="0b39f-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b39f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0b39f-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b39f-145">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="0b39f-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0b39f-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b39f-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b39f-147"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="0b39f-148">DLL</span><span class="sxs-lookup"><span data-stu-id="0b39f-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b39f-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b39f-149"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="0b39f-150">IID</span><span class="sxs-lookup"><span data-stu-id="0b39f-150">IID</span></span><br/>                      | <span data-ttu-id="0b39f-151">IID \_ IMsRdpClientAdvancedSettings2 é definido como 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="0b39f-151">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b39f-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b39f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b39f-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0b39f-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0b39f-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0b39f-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0b39f-155">Referência de Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="0b39f-155">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

