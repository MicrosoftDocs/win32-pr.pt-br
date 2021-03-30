---
title: Interface IMsRdpClientAdvancedSettings3
description: Gerencia configurações avançadas do cliente. Deriva da interface IMsRdpClientAdvancedSettings2.
ms.assetid: bfa9cf74-5943-45ca-9259-3ef0cc9ab2ab
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings3, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760ae7d40742a800556b3d62bc5a1609b89c986b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644611"
---
# <a name="imsrdpclientadvancedsettings3-interface"></a><span data-ttu-id="71d7d-106">Interface IMsRdpClientAdvancedSettings3</span><span class="sxs-lookup"><span data-stu-id="71d7d-106">IMsRdpClientAdvancedSettings3 interface</span></span>

<span data-ttu-id="71d7d-107">Gerencia configurações avançadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="71d7d-107">Manages advanced client settings.</span></span> <span data-ttu-id="71d7d-108">Deriva da interface [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="71d7d-108">Derives from the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span> <span data-ttu-id="71d7d-109">Essa interface inclui métodos para recuperar e definir propriedades avançadas (opcionais) para o controle ActiveX Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="71d7d-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="71d7d-110">Para obter uma instância dessa interface, use a propriedade [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obter um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="71d7d-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="71d7d-111">Em seguida, chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro **IMsTscAdvancedSettings** e passe **\_ IMsRdpClientAdvancedSettings3 de IID** para **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="71d7d-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings3** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="71d7d-112">Membros</span><span class="sxs-lookup"><span data-stu-id="71d7d-112">Members</span></span>

<span data-ttu-id="71d7d-113">A interface **IMsRdpClientAdvancedSettings3** herda de [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md).</span><span class="sxs-lookup"><span data-stu-id="71d7d-113">The **IMsRdpClientAdvancedSettings3** interface inherits from [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md).</span></span> <span data-ttu-id="71d7d-114">**IMsRdpClientAdvancedSettings3** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="71d7d-114">**IMsRdpClientAdvancedSettings3** also has these types of members:</span></span>

-   [<span data-ttu-id="71d7d-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="71d7d-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71d7d-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="71d7d-116">Properties</span></span>

<span data-ttu-id="71d7d-117">A interface **IMsRdpClientAdvancedSettings3** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="71d7d-117">The **IMsRdpClientAdvancedSettings3** interface has these properties.</span></span>



| <span data-ttu-id="71d7d-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="71d7d-118">Property</span></span>                                                                                                            | <span data-ttu-id="71d7d-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="71d7d-119">Access type</span></span>           | <span data-ttu-id="71d7d-120">Description</span><span class="sxs-lookup"><span data-stu-id="71d7d-120">Description</span></span>                                                                            |
|:--------------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="71d7d-121">**ConnectionBarShowMinimizeButton**</span><span class="sxs-lookup"><span data-stu-id="71d7d-121">**ConnectionBarShowMinimizeButton**</span></span>](imsrdpclientadvancedsettings3-connectionbarshowminimizebutton.md)<br/> | <span data-ttu-id="71d7d-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="71d7d-122">Read/write</span></span><br/> | <span data-ttu-id="71d7d-123">Especifica se o botão de **minimização** deve ser exibido na barra de conexão.</span><span class="sxs-lookup"><span data-stu-id="71d7d-123">Specifies whether to display the **Minimize** button on the connection bar.</span></span><br/> |
| [<span data-ttu-id="71d7d-124">**ConnectionBarShowRestoreButton**</span><span class="sxs-lookup"><span data-stu-id="71d7d-124">**ConnectionBarShowRestoreButton**</span></span>](imsrdpclientadvancedsettings3-connectionbarshowrestorebutton.md)<br/>   | <span data-ttu-id="71d7d-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="71d7d-125">Read/write</span></span><br/> | <span data-ttu-id="71d7d-126">Especifica se o botão de **restauração** deve ser exibido na barra de conexão.</span><span class="sxs-lookup"><span data-stu-id="71d7d-126">Specifies whether to display the **Restore** button on the connection bar.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="71d7d-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="71d7d-127">Remarks</span></span>

<span data-ttu-id="71d7d-128">Essa interface foi estendida pelas seguintes interfaces, com cada nova interface herdando todos os métodos e propriedades das interfaces anteriores:</span><span class="sxs-lookup"><span data-stu-id="71d7d-128">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="71d7d-129">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="71d7d-129">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="71d7d-130">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="71d7d-130">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="71d7d-131">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="71d7d-131">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="71d7d-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="71d7d-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
-   [<span data-ttu-id="71d7d-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="71d7d-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)

<span data-ttu-id="71d7d-134">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="71d7d-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71d7d-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71d7d-135">Requirements</span></span>



| <span data-ttu-id="71d7d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="71d7d-136">Requirement</span></span> | <span data-ttu-id="71d7d-137">Valor</span><span class="sxs-lookup"><span data-stu-id="71d7d-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71d7d-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71d7d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="71d7d-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71d7d-139">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="71d7d-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71d7d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="71d7d-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71d7d-141">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="71d7d-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="71d7d-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="71d7d-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71d7d-143"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="71d7d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="71d7d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71d7d-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71d7d-145"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="71d7d-146">IID</span><span class="sxs-lookup"><span data-stu-id="71d7d-146">IID</span></span><br/>                      | <span data-ttu-id="71d7d-147">IID \_ IMsRdpClientAdvancedSettings3 é definido como 19cd856b-C542-4c53-ACEE-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="71d7d-147">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71d7d-148">Consulte também</span><span class="sxs-lookup"><span data-stu-id="71d7d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d7d-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="71d7d-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="71d7d-150">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="71d7d-150">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="71d7d-151">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="71d7d-151">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="71d7d-152">Referência de Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="71d7d-152">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

