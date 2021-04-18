---
title: Interface IMsRdpClientAdvancedSettings5
description: Gerencia configurações avançadas do cliente. Deriva da interface IMsRdpClientAdvancedSettings4.
ms.assetid: a927cd4c-7f70-493e-a4f6-056d0352d56e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings5, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14e37eb28c1fb7a272291c44661c52ec3548708b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759944"
---
# <a name="imsrdpclientadvancedsettings5-interface"></a><span data-ttu-id="7a4db-106">Interface IMsRdpClientAdvancedSettings5</span><span class="sxs-lookup"><span data-stu-id="7a4db-106">IMsRdpClientAdvancedSettings5 interface</span></span>

<span data-ttu-id="7a4db-107">Gerencia configurações avançadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="7a4db-107">Manages advanced client settings.</span></span> <span data-ttu-id="7a4db-108">Deriva da interface [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="7a4db-108">Derives from the [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span>

<span data-ttu-id="7a4db-109">Para obter uma instância dessa interface, use a propriedade [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obter um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="7a4db-109">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="7a4db-110">Em seguida, chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro **IMsTscAdvancedSettings** e passe **\_ IMsRdpClientAdvancedSettings5 de IID** para **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="7a4db-110">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings5** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="7a4db-111">Membros</span><span class="sxs-lookup"><span data-stu-id="7a4db-111">Members</span></span>

<span data-ttu-id="7a4db-112">A interface **IMsRdpClientAdvancedSettings5** herda de [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md).</span><span class="sxs-lookup"><span data-stu-id="7a4db-112">The **IMsRdpClientAdvancedSettings5** interface inherits from [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md).</span></span> <span data-ttu-id="7a4db-113">**IMsRdpClientAdvancedSettings5** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7a4db-113">**IMsRdpClientAdvancedSettings5** also has these types of members:</span></span>

-   [<span data-ttu-id="7a4db-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7a4db-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a4db-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7a4db-115">Properties</span></span>

<span data-ttu-id="7a4db-116">A interface **IMsRdpClientAdvancedSettings5** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7a4db-116">The **IMsRdpClientAdvancedSettings5** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="7a4db-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7a4db-117">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="7a4db-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="7a4db-118">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="7a4db-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a4db-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7a4db-120"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="7a4db-120"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a4db-121">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7a4db-121">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a4db-122">O modo de redirecionamento de áudio.</span><span class="sxs-lookup"><span data-stu-id="7a4db-122">The audio redirection mode.</span></span> <span data-ttu-id="7a4db-123">A propriedade <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a> tem os seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="7a4db-123">The <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a> property has the following possible values.</span></span><br/><span data-ttu-id="7a4db-124">
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (o redirecionamento de áudio está habilitado e a opção para redirecionamento é &quot; levada para este computador &quot; .</span><span class="sxs-lookup"><span data-stu-id="7a4db-124">
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (Audio redirection is enabled and the option for redirection is &quot;Bring to this computer&quot;.</span></span> <span data-ttu-id="7a4db-125">Esse é o modo padrão.)</span><span class="sxs-lookup"><span data-stu-id="7a4db-125">This is the default mode.)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="7a4db-126"><dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (o redirecionamento de áudio é habilitado e a opção é &quot; deixada no computador remoto &quot; .</span><span class="sxs-lookup"><span data-stu-id="7a4db-126"><dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (Audio redirection is enabled and the option is &quot;Leave at remote computer&quot;.</span></span> <span data-ttu-id="7a4db-127">A &quot; opção deixar no computador remoto &quot; só tem suporte quando se conecta remotamente a um computador host que esteja executando o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7a4db-127">The &quot;Leave at remote computer&quot; option is supported only when connecting remotely to a host computer that is running Windows Vista.</span></span> <span data-ttu-id="7a4db-128">Se a conexão for para um computador host que esteja executando o Windows Server 2008, a opção &quot; deixar no computador remoto &quot; será alterada para &quot; não reproduzir &quot; .)</span><span class="sxs-lookup"><span data-stu-id="7a4db-128">If the connection is to a host computer that is running Windows Server 2008, the option &quot;Leave at remote computer&quot; is changed to &quot;Do not play&quot;.)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="7a4db-129"><dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (o redirecionamento de áudio está habilitado e o modo &quot; não é reproduzido &quot; .)</span><span class="sxs-lookup"><span data-stu-id="7a4db-129"><dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (Audio redirection is enabled and the mode is &quot;Do not play&quot;.)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7a4db-130"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="7a4db-130"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a4db-131">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7a4db-131">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a4db-132">Especifica o tamanho do arquivo de cache virtual para bitmaps de 32 bits por pixel (BPP).</span><span class="sxs-lookup"><span data-stu-id="7a4db-132">Specifies the virtual cache file size for 32 bits per pixel (bpp) bitmaps.</span></span> <span data-ttu-id="7a4db-133">O valor máximo é 48 megabytes (MB).</span><span class="sxs-lookup"><span data-stu-id="7a4db-133">The maximum value is 48 megabytes (MB).</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7a4db-134"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="7a4db-134"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a4db-135">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7a4db-135">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a4db-136">Especifica se o botão PIN deve ser mostrado na barra de conexão.</span><span class="sxs-lookup"><span data-stu-id="7a4db-136">Specifies whether the pin button should be shown on the connection bar.</span></span> <span data-ttu-id="7a4db-137">Por padrão, o valor é <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="7a4db-137">By default, the value is <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7a4db-138"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>Públicomode</strong></a></span><span class="sxs-lookup"><span data-stu-id="7a4db-138"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a4db-139">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7a4db-139">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a4db-140">Especifica se o modo público deve ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="7a4db-140">Specifies whether public mode should be enabled or disabled.</span></span> <span data-ttu-id="7a4db-141">Por padrão, o modo público é definido como <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="7a4db-141">By default, public mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7a4db-142"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a></span><span class="sxs-lookup"><span data-stu-id="7a4db-142"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a4db-143">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7a4db-143">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a4db-144">Especifica se o redirecionamento da área de transferência deve ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="7a4db-144">Specifies whether clipboard redirection should be enabled or disabled.</span></span> <span data-ttu-id="7a4db-145">Por padrão, o modo de redirecionamento da área de transferência é definido como <strong>true</strong> (habilitado).</span><span class="sxs-lookup"><span data-stu-id="7a4db-145">By default, clipboard redirection mode is set to <strong>TRUE</strong> (enabled).</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7a4db-146"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="7a4db-146"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a4db-147">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7a4db-147">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a4db-148">Especifica se os dispositivos redirecionados devem ser habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="7a4db-148">Specifies whether redirected devices should be enabled or disabled.</span></span> <span data-ttu-id="7a4db-149">Por padrão, o modo de dispositivos redirecionados é definido como <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="7a4db-149">By default, redirected devices mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7a4db-150"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="7a4db-150"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a4db-151">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7a4db-151">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a4db-152">Especifica se os dispositivos redirecionados de ponto de serviço devem ser habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="7a4db-152">Specifies whether Point of Service redirected devices should be enabled or disabled.</span></span> <span data-ttu-id="7a4db-153">Por padrão, o modo de dispositivos redirecionados de ponto de serviço é definido como <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="7a4db-153">By default, Point of Service redirected devices mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="7a4db-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a4db-154">Remarks</span></span>

<span data-ttu-id="7a4db-155">Essa interface foi estendida pelas seguintes interfaces, com cada nova interface herdando todos os métodos e propriedades das interfaces anteriores:</span><span class="sxs-lookup"><span data-stu-id="7a4db-155">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="7a4db-156">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7a4db-156">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="7a4db-157">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7a4db-157">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
-   [<span data-ttu-id="7a4db-158">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7a4db-158">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)

## <a name="requirements"></a><span data-ttu-id="7a4db-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a4db-159">Requirements</span></span>



| <span data-ttu-id="7a4db-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a4db-160">Requirement</span></span> | <span data-ttu-id="7a4db-161">Valor</span><span class="sxs-lookup"><span data-stu-id="7a4db-161">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a4db-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a4db-162">Minimum supported client</span></span><br/> | <span data-ttu-id="7a4db-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a4db-163">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="7a4db-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a4db-164">Minimum supported server</span></span><br/> | <span data-ttu-id="7a4db-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a4db-165">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="7a4db-166">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7a4db-166">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a4db-167"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a4db-167"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7a4db-168">DLL</span><span class="sxs-lookup"><span data-stu-id="7a4db-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a4db-169"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a4db-169"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7a4db-170">IID</span><span class="sxs-lookup"><span data-stu-id="7a4db-170">IID</span></span><br/>                      | <span data-ttu-id="7a4db-171">IID \_ IMsRdpClientAdvancedSettings5 é definido como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="7a4db-171">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a4db-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a4db-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a4db-173">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="7a4db-173">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="7a4db-174">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="7a4db-174">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="7a4db-175">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="7a4db-175">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="7a4db-176">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7a4db-176">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7a4db-177">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7a4db-177">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7a4db-178">Referência de Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="7a4db-178">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

