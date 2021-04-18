---
title: Interface IMsRdpClientAdvancedSettings7
description: Expõe métodos e propriedades que gerenciam as configurações avançadas do controle ActiveX.
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings7, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed28c5d26ecf280507ce3cce835a6d0a71fc3bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755160"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a><span data-ttu-id="345a9-105">Interface IMsRdpClientAdvancedSettings7</span><span class="sxs-lookup"><span data-stu-id="345a9-105">IMsRdpClientAdvancedSettings7 interface</span></span>

<span data-ttu-id="345a9-106">Expõe métodos e propriedades que gerenciam as configurações avançadas do controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="345a9-106">Exposes methods and properties that manage advanced settings of the ActiveX control.</span></span>

<span data-ttu-id="345a9-107">Para obter uma instância dessa interface, use a propriedade [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obter um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="345a9-107">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="345a9-108">Em seguida, chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro **IMsTscAdvancedSettings** e passe **\_ IMsRdpClientAdvancedSettings7 de IID** para **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="345a9-108">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings7** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="345a9-109">Membros</span><span class="sxs-lookup"><span data-stu-id="345a9-109">Members</span></span>

<span data-ttu-id="345a9-110">A interface **IMsRdpClientAdvancedSettings7** herda de **IMsRdpClientAdvancedSettings6**.</span><span class="sxs-lookup"><span data-stu-id="345a9-110">The **IMsRdpClientAdvancedSettings7** interface inherits from **IMsRdpClientAdvancedSettings6**.</span></span> <span data-ttu-id="345a9-111">**IMsRdpClientAdvancedSettings7** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="345a9-111">**IMsRdpClientAdvancedSettings7** also has these types of members:</span></span>

-   [<span data-ttu-id="345a9-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="345a9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="345a9-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="345a9-113">Properties</span></span>

<span data-ttu-id="345a9-114">A interface **IMsRdpClientAdvancedSettings7** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="345a9-114">The **IMsRdpClientAdvancedSettings7** interface has these properties.</span></span>



| <span data-ttu-id="345a9-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="345a9-115">Property</span></span>                                                                                                    | <span data-ttu-id="345a9-116">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="345a9-116">Access type</span></span>           | <span data-ttu-id="345a9-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="345a9-117">Description</span></span>                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="345a9-118">**AudioCaptureRedirectionMode**</span><span class="sxs-lookup"><span data-stu-id="345a9-118">**AudioCaptureRedirectionMode**</span></span>](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | <span data-ttu-id="345a9-119">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="345a9-119">Read/write</span></span><br/> | <span data-ttu-id="345a9-120">Especifica ou recupera um valor que indica se o dispositivo de entrada de áudio padrão é redirecionado do cliente para a sessão remota.</span><span class="sxs-lookup"><span data-stu-id="345a9-120">Specifies or retrieves a value that indicates whether the default audio input device is redirected from the client to the remote session.</span></span><br/> |
| [<span data-ttu-id="345a9-121">**AudioQualityMode**</span><span class="sxs-lookup"><span data-stu-id="345a9-121">**AudioQualityMode**</span></span>](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | <span data-ttu-id="345a9-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="345a9-122">Read/write</span></span><br/> | <span data-ttu-id="345a9-123">Especifica ou recupera um valor que indica a configuração do modo de qualidade de áudio para áudio Redirecionado.</span><span class="sxs-lookup"><span data-stu-id="345a9-123">Specifies or retrieves a value that indicates the audio quality mode setting for redirected audio.</span></span><br/>                                        |
| [<span data-ttu-id="345a9-124">**EnableSuperPan**</span><span class="sxs-lookup"><span data-stu-id="345a9-124">**EnableSuperPan**</span></span>](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | <span data-ttu-id="345a9-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="345a9-125">Read/write</span></span><br/> | <span data-ttu-id="345a9-126">Especifica ou recupera um valor que indica se SuperPan está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="345a9-126">Specifies or retrieves a value that indicates whether SuperPan is enabled or disabled.</span></span><br/>                                                    |
| [<span data-ttu-id="345a9-127">**NetworkConnectionType**</span><span class="sxs-lookup"><span data-stu-id="345a9-127">**NetworkConnectionType**</span></span>](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | <span data-ttu-id="345a9-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="345a9-128">Read/write</span></span><br/> | <span data-ttu-id="345a9-129">Especifica ou recupera um valor que indica o tipo de conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="345a9-129">Specifies or retrieves a value that indicates the network connection type.</span></span><br/>                                                                |
| [<span data-ttu-id="345a9-130">**RedirectDirectX**</span><span class="sxs-lookup"><span data-stu-id="345a9-130">**RedirectDirectX**</span></span>](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | <span data-ttu-id="345a9-131">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="345a9-131">Read/write</span></span><br/> | <span data-ttu-id="345a9-132">Essa propriedade não é usada.</span><span class="sxs-lookup"><span data-stu-id="345a9-132">This property is not used.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="345a9-133">**SuperPanAccelerationFactor**</span><span class="sxs-lookup"><span data-stu-id="345a9-133">**SuperPanAccelerationFactor**</span></span>](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | <span data-ttu-id="345a9-134">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="345a9-134">Read/write</span></span><br/> | <span data-ttu-id="345a9-135">Especifica ou recupera um valor que indica o fator de aceleração SuperPan.</span><span class="sxs-lookup"><span data-stu-id="345a9-135">Specifies or retrieves a value that indicates the SuperPan acceleration factor.</span></span><br/>                                                           |
| [<span data-ttu-id="345a9-136">**VideoPlaybackMode**</span><span class="sxs-lookup"><span data-stu-id="345a9-136">**VideoPlaybackMode**</span></span>](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | <span data-ttu-id="345a9-137">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="345a9-137">Read/write</span></span><br/> | <span data-ttu-id="345a9-138">Especifica ou recupera um valor que indica o modo de reprodução de vídeo.</span><span class="sxs-lookup"><span data-stu-id="345a9-138">Specifies or retrieves a value that indicates the video playback mode.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="345a9-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="345a9-139">Requirements</span></span>



| <span data-ttu-id="345a9-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="345a9-140">Requirement</span></span> | <span data-ttu-id="345a9-141">Valor</span><span class="sxs-lookup"><span data-stu-id="345a9-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="345a9-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="345a9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="345a9-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="345a9-143">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="345a9-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="345a9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="345a9-145">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="345a9-145">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="345a9-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="345a9-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="345a9-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="345a9-147"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="345a9-148">DLL</span><span class="sxs-lookup"><span data-stu-id="345a9-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="345a9-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="345a9-149"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="345a9-150">IID</span><span class="sxs-lookup"><span data-stu-id="345a9-150">IID</span></span><br/>                      | <span data-ttu-id="345a9-151">IID \_ IMsRdpClientAdvancedSettings7 é definido como 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="345a9-151">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="345a9-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="345a9-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="345a9-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="345a9-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="345a9-154">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="345a9-154">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="345a9-155">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="345a9-155">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="345a9-156">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="345a9-156">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="345a9-157">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="345a9-157">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="345a9-158">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="345a9-158">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="345a9-159">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="345a9-159">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

