---
title: Propriedade IMsRdpExtendedSettings Property
description: Contém uma propriedade nomeada.
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de propriedade
- Propriedade de propriedade Serviços de Área de Trabalho Remota, interface IMsRdpExtendedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpExtendedSettings, Propriedade Property
topic_type:
- apiref
api_name:
- IMsRdpExtendedSettings.Property
- IMsRdpExtendedSettings.get_Property
- IMsRdpExtendedSettings.put_Property
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc8ce59e5a2bd50a4e61ad75b5124b24c21b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103645612"
---
# <a name="imsrdpextendedsettingsproperty-property"></a><span data-ttu-id="db634-106">IMsRdpExtendedSettings: Propriedade roperty de:P</span><span class="sxs-lookup"><span data-stu-id="db634-106">IMsRdpExtendedSettings::Property property</span></span>

<span data-ttu-id="db634-107">Contém uma propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="db634-107">Contains a named property.</span></span>

<span data-ttu-id="db634-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="db634-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="db634-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db634-109">Syntax</span></span>


```C++
HRESULT put_Property(
  [in]          BSTR    bstrPropertyName,
  [in]          VARIANT *pValue
);

HRESULT get_Property(
  [in]          BSTR    bstrPropertyName,
  [out, retval] VARIANT *pValue
);
```



## <a name="property-value"></a><span data-ttu-id="db634-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="db634-110">Property value</span></span>

<span data-ttu-id="db634-111">O valor da propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="db634-111">The named property value.</span></span>

| <span data-ttu-id="db634-112">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="db634-112">Property name</span></span> | <span data-ttu-id="db634-113">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="db634-113">Data type</span></span> | <span data-ttu-id="db634-114">Access</span><span class="sxs-lookup"><span data-stu-id="db634-114">Access</span></span> | <span data-ttu-id="db634-115">Pode ser alterado após a conexão ser iniciada</span><span class="sxs-lookup"><span data-stu-id="db634-115">Can be changed after connection started</span></span> | <span data-ttu-id="db634-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="db634-116">Description</span></span> |
|----------|-----------|--------|-----------------------------------------|-------------|
| <span data-ttu-id="db634-117">ConnectToChildSession</span><span class="sxs-lookup"><span data-stu-id="db634-117">ConnectToChildSession</span></span> | <span data-ttu-id="db634-118">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="db634-118">**VT\_BOOL**</span></span> | <span data-ttu-id="db634-119">Leitura/Gravação</span><span class="sxs-lookup"><span data-stu-id="db634-119">Read/Write</span></span> | <span data-ttu-id="db634-120">Sim</span><span class="sxs-lookup"><span data-stu-id="db634-120">Yes</span></span> | <span data-ttu-id="db634-121">Definir essa propriedade como **true** faz com que o controle de cliente se conecte à sessão filho no computador local, em vez de um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="db634-121">Setting this property to **True** causes the client control to connect to the child session on the local machine instead of a remote server.</span></span> <span data-ttu-id="db634-122">Se essa propriedade for definida como **true**, você não poderá se conectar a um servidor remoto, pois todas as conexões serão redirecionadas para localhost.</span><span class="sxs-lookup"><span data-stu-id="db634-122">If this property is set to **true**, you cannot connect to a remote server because all connections are redirected to localhost.</span></span> <span data-ttu-id="db634-123">Para obter mais informações sobre sessões filho, consulte [sessões filhas](child-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="db634-123">For more information about child sessions, see [Child Sessions](child-sessions.md).</span></span> |
| <span data-ttu-id="db634-124">DisableCredentialsDelegation</span><span class="sxs-lookup"><span data-stu-id="db634-124">DisableCredentialsDelegation</span></span> | <span data-ttu-id="db634-125">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="db634-125">**VT\_BOOL**</span></span> | <span data-ttu-id="db634-126">Leitura/Gravação</span><span class="sxs-lookup"><span data-stu-id="db634-126">Read/Write</span></span> | <span data-ttu-id="db634-127">Não</span><span class="sxs-lookup"><span data-stu-id="db634-127">No</span></span> | <span data-ttu-id="db634-128">Se **for true**, as credenciais não serão enviadas ao servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="db634-128">If **True**, credentials are not sent to the remote server.</span></span> |
| <span data-ttu-id="db634-129">EnableFrameBufferRedirection</span><span class="sxs-lookup"><span data-stu-id="db634-129">EnableFrameBufferRedirection</span></span> | <span data-ttu-id="db634-130">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="db634-130">**VT\_BOOL**</span></span> | <span data-ttu-id="db634-131">Leitura/Gravação</span><span class="sxs-lookup"><span data-stu-id="db634-131">Read/Write</span></span> | <span data-ttu-id="db634-132">Não</span><span class="sxs-lookup"><span data-stu-id="db634-132">No</span></span> | <span data-ttu-id="db634-133">Se for **true**, o redirecionamento de buffer de quadro será tentado.</span><span class="sxs-lookup"><span data-stu-id="db634-133">If **True**, frame buffer redirection is attempted.</span></span> <span data-ttu-id="db634-134">Para uma conexão de auto-retorno (o mesmo computador é cliente e servidor), o redirecionamento de buffer de quadro permite que a memória do buffer de quadros seja compartilhada entre as sessões.</span><span class="sxs-lookup"><span data-stu-id="db634-134">For a loopback connection (the same computer is both client and server) frame buffer redirection allows the memory for the frame buffer to be shared between the sessions.</span></span> |
| <span data-ttu-id="db634-135">EnableHardwareMode</span><span class="sxs-lookup"><span data-stu-id="db634-135">EnableHardwareMode</span></span> | <span data-ttu-id="db634-136">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="db634-136">**VT\_BOOL**</span></span>  | <span data-ttu-id="db634-137">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="db634-137">Write Only</span></span> | <span data-ttu-id="db634-138">Não</span><span class="sxs-lookup"><span data-stu-id="db634-138">No</span></span> | <span data-ttu-id="db634-139">Se for **true**, será feita uma tentativa de assistência de hardware com a decodificação de gráficos.</span><span class="sxs-lookup"><span data-stu-id="db634-139">If **True**, hardware assist with graphics decoding is attempted.</span></span> |
| <span data-ttu-id="db634-140">IgnoreCursors</span><span class="sxs-lookup"><span data-stu-id="db634-140">IgnoreCursors</span></span> | <span data-ttu-id="db634-141">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="db634-141">**VT\_BOOL**</span></span> | <span data-ttu-id="db634-142">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="db634-142">Write Only</span></span> | <span data-ttu-id="db634-143">Não</span><span class="sxs-lookup"><span data-stu-id="db634-143">No</span></span> | <span data-ttu-id="db634-144">Se **for true**, os cursores enviados pelo servidor remoto serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="db634-144">If **True**, cursors sent by the remote server are ignored.</span></span> |
| <span data-ttu-id="db634-145">ManualClipboardSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="db634-145">ManualClipboardSyncEnabled</span></span> | <span data-ttu-id="db634-146">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="db634-146">**VT\_BOOL**</span></span> | <span data-ttu-id="db634-147">Leitura/Gravação</span><span class="sxs-lookup"><span data-stu-id="db634-147">Read/Write</span></span> | <span data-ttu-id="db634-148">Sim</span><span class="sxs-lookup"><span data-stu-id="db634-148">Yes</span></span> | <span data-ttu-id="db634-149">Definir essa propriedade como **true** significa que as áreas de transferência locais e remotas não serão mantidas automaticamente em sincronia. Em vez disso, a interface [**IMsRdpClipboard**](imsrdpclipboard.md) deve ser usada para sincronizar formatos de área de transferência da área de transferência local para a área de transferência remota e a área de transferência remota para a área de transferência local.</span><span class="sxs-lookup"><span data-stu-id="db634-149">Setting this property to **True** means that the local and remote clipboards will not be automatically kept in sync. Instead the [**IMsRdpClipboard**](imsrdpclipboard.md) interface must be used to sync clipboard formats from the local clipboard to the remote clipboard and the remote clipboard to the local clipboard.</span></span> |
| <span data-ttu-id="db634-150">ZoomLevel</span><span class="sxs-lookup"><span data-stu-id="db634-150">ZoomLevel</span></span> | <span data-ttu-id="db634-151">\**_\_UI4 VT_*</span><span class="sxs-lookup"><span data-stu-id="db634-151">\**_VT\_UI4_*</span></span> | <span data-ttu-id="db634-152">Leitura/Gravação</span><span class="sxs-lookup"><span data-stu-id="db634-152">Read/Write</span></span> | <span data-ttu-id="db634-153">Sim</span><span class="sxs-lookup"><span data-stu-id="db634-153">Yes</span></span> | <span data-ttu-id="db634-154">Implementa o recurso de zoom usando o controle ActiveX RDP.</span><span class="sxs-lookup"><span data-stu-id="db634-154">Implements the Zoom feature by using the RDP ActiveX control.</span></span> <span data-ttu-id="db634-155">O recurso de zoom está disponível no menu do **sistema** do RDP.</span><span class="sxs-lookup"><span data-stu-id="db634-155">The Zoom feature is available from the **System** menu of RDP.</span></span> <span data-ttu-id="db634-156">A propriedade **ZoomLevel** não tem nenhum efeito no modo RemoteApp e no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="db634-156">The **ZoomLevel** property has no effect in RemoteApp mode and full-screen mode.</span></span> <span data-ttu-id="db634-157">[**IMsRdpClientAdvancedSettings:: SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) e **ZoomLevel** são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="db634-157">[**IMsRdpClientAdvancedSettings::SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) and **ZoomLevel** are mutually exclusive.</span></span> |

## <a name="requirements"></a><span data-ttu-id="db634-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db634-158">Requirements</span></span>



| <span data-ttu-id="db634-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="db634-159">Requirement</span></span> | <span data-ttu-id="db634-160">Valor</span><span class="sxs-lookup"><span data-stu-id="db634-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db634-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db634-161">Minimum supported client</span></span><br/> | <span data-ttu-id="db634-162">Windows 8</span><span class="sxs-lookup"><span data-stu-id="db634-162">Windows 8</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="db634-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db634-163">Minimum supported server</span></span><br/> | <span data-ttu-id="db634-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db634-164">Windows Server 2012</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="db634-165">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="db634-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="db634-166"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db634-166"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                         |
| <span data-ttu-id="db634-167">DLL</span><span class="sxs-lookup"><span data-stu-id="db634-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db634-168"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db634-168"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                         |
| <span data-ttu-id="db634-169">CLSID</span><span class="sxs-lookup"><span data-stu-id="db634-169">CLSID</span></span><br/>                    | <span data-ttu-id="db634-170">CLSID \_ MsRdpClient7NotSafeForScripting é definido como 54d38bf7-b1ef-4479-9674-1bd6ea465258</span><span class="sxs-lookup"><span data-stu-id="db634-170">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54d38bf7-b1ef-4479-9674-1bd6ea465258</span></span><br/> <span data-ttu-id="db634-171">CLSID \_ MsRdpClient8NotSafeForScripting é definido como A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="db634-171">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="db634-172">CLSID \_ MsRdpClient9NotSafeForScripting é definido como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="db634-172">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="db634-173">IID</span><span class="sxs-lookup"><span data-stu-id="db634-173">IID</span></span><br/>                      | <span data-ttu-id="db634-174">IID \_ IMsRdpExtendedSettings é definido como 302D8188-0052-4807-806A-362B628F9AC5</span><span class="sxs-lookup"><span data-stu-id="db634-174">IID\_IMsRdpExtendedSettings is defined as 302D8188-0052-4807-806A-362B628F9AC5</span></span><br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a><span data-ttu-id="db634-175">Consulte também</span><span class="sxs-lookup"><span data-stu-id="db634-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db634-176">**IMsRdpExtendedSettings**</span><span class="sxs-lookup"><span data-stu-id="db634-176">**IMsRdpExtendedSettings**</span></span>](imsrdpextendedsettings.md)
</dt> </dl>

 

 





