---
title: Propriedade IMsTscSecuredSettings fullscreen
description: Especifica o estado de tela inteira do controle de cliente.
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade fullscreen
- Serviços de Área de Trabalho Remota da propriedade fullscreen, interface IMsTscSecuredSettings
- Serviços de Área de Trabalho Remota de interface IMsTscSecuredSettings, Propriedade fullscreen
- Serviços de Área de Trabalho Remota da propriedade fullscreen, interface IMsRdpClientSecuredSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientSecuredSettings, Propriedade fullscreen
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.Fullscreen
- IMsTscSecuredSettings.get_Fullscreen
- IMsTscSecuredSettings.put_Fullscreen
- IMsRdpClientSecuredSettings.Fullscreen
- IMsRdpClientSecuredSettings.get_Fullscreen
- IMsRdpClientSecuredSettings.put_Fullscreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c3b3208edf3476fcd110d7729d97d9817cb929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811909"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a><span data-ttu-id="967f2-108">Propriedade IMsTscSecuredSettings:: fullscreen</span><span class="sxs-lookup"><span data-stu-id="967f2-108">IMsTscSecuredSettings::Fullscreen property</span></span>

<span data-ttu-id="967f2-109">Especifica o estado de tela inteira do controle de cliente.</span><span class="sxs-lookup"><span data-stu-id="967f2-109">Specifies the full-screen state of the client control.</span></span>

<span data-ttu-id="967f2-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="967f2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="967f2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="967f2-111">Syntax</span></span>


```C++
HRESULT put_Fullscreen(
  [in]  BOOL fFullScreen
);

HRESULT get_Fullscreen(
  [out] BOOL *pfFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="967f2-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="967f2-112">Property value</span></span>

<span data-ttu-id="967f2-113">Defina esse parâmetro como **true** se o controle deve usar o modo de tela inteira e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="967f2-113">Set this parameter to **TRUE** if the control should use full-screen mode and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="967f2-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="967f2-114">Error codes</span></span>

<span data-ttu-id="967f2-115">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="967f2-115">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="967f2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="967f2-116">Remarks</span></span>

<span data-ttu-id="967f2-117">Para obter mais informações sobre esse método, consulte [fornecendo para o RDP Client Security](providing-for-rdp-client-security.md).</span><span class="sxs-lookup"><span data-stu-id="967f2-117">For more information about this method, see [Providing for RDP Client Security](providing-for-rdp-client-security.md).</span></span>

<span data-ttu-id="967f2-118">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="967f2-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

<span data-ttu-id="967f2-119">Observe que, embora o uso dessa propriedade seja restrito às zonas de segurança de URL do Internet Explorer permitidas, um usuário sempre poderá mudar para o modo de tela inteira depois que a conexão for estabelecida pressionando a combinação de [teclas de atalho](terminal-services-shortcut-keys.md) no modo de tela inteira (Ctrl + Alt + Break).</span><span class="sxs-lookup"><span data-stu-id="967f2-119">Note that although the use of this property is restricted to the allowed Internet Explorer URL security zones, a user can always change to full-screen mode after the connection has been established by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="967f2-120">Esse método pode ser chamado enquanto a conexão do cliente é estabelecida.</span><span class="sxs-lookup"><span data-stu-id="967f2-120">This method can be called while the client connection is established.</span></span>

<span data-ttu-id="967f2-121">Você deve chamar o método [**IMsRdpClientNonScriptable3::p UT \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) antes de chamar o método **IMsTscSecuredSettings::p UT \_ fullscreen** ou o método [**IMsRdpClient::p UT \_ fullscreen**](imsrdpclient-fullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="967f2-121">You must call the [**IMsRdpClientNonScriptable3::put\_ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) method before you call the **IMsTscSecuredSettings::put\_Fullscreen** method or the [**IMsRdpClient::put\_Fullscreen**](imsrdpclient-fullscreen.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="967f2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="967f2-122">Requirements</span></span>



| <span data-ttu-id="967f2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="967f2-123">Requirement</span></span> | <span data-ttu-id="967f2-124">Valor</span><span class="sxs-lookup"><span data-stu-id="967f2-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="967f2-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="967f2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="967f2-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="967f2-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="967f2-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="967f2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="967f2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="967f2-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="967f2-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="967f2-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="967f2-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="967f2-130"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="967f2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="967f2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="967f2-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="967f2-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="967f2-133">IID</span><span class="sxs-lookup"><span data-stu-id="967f2-133">IID</span></span><br/>                      | <span data-ttu-id="967f2-134">IID \_ IMsTscSecuredSettings é definido como c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="967f2-134">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="967f2-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="967f2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="967f2-136">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="967f2-136">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="967f2-137">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="967f2-137">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





