---
title: Propriedade IMsRdpClientSecuredSettings AudioRedirectionMode
description: Especifica as configurações de redirecionamento de áudio, que especificam se deseja redirecionar sons ou reproduzir sons no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AudioRedirectionMode
- Propriedade AudioRedirectionMode Serviços de Área de Trabalho Remota, interface IMsRdpClientSecuredSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientSecuredSettings, Propriedade AudioRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.AudioRedirectionMode
- IMsRdpClientSecuredSettings.get_AudioRedirectionMode
- IMsRdpClientSecuredSettings.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 858342811ec97def95031ebed0605b5a81cf80fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499843"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a><span data-ttu-id="df5fc-106">Propriedade IMsRdpClientSecuredSettings:: AudioRedirectionMode</span><span class="sxs-lookup"><span data-stu-id="df5fc-106">IMsRdpClientSecuredSettings::AudioRedirectionMode property</span></span>

<span data-ttu-id="df5fc-107">Especifica as configurações de redirecionamento de áudio, que especificam se deseja redirecionar sons ou reproduzir sons no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="df5fc-107">Specifies the audio redirection settings, which specify whether to redirect sounds or play sounds at the Remote Desktop Session Host (RD Session Host) server.</span></span>

<span data-ttu-id="df5fc-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="df5fc-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="df5fc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="df5fc-109">Syntax</span></span>


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a><span data-ttu-id="df5fc-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="df5fc-110">Property value</span></span>

<span data-ttu-id="df5fc-111">As novas configurações.</span><span class="sxs-lookup"><span data-stu-id="df5fc-111">The new settings.</span></span> <span data-ttu-id="df5fc-112">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="df5fc-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="df5fc-113">0</span><span class="sxs-lookup"><span data-stu-id="df5fc-113">0</span></span>
</dt> <dd>

<span data-ttu-id="df5fc-114">Redirecionar sons para o cliente.</span><span class="sxs-lookup"><span data-stu-id="df5fc-114">Redirect sounds to the client.</span></span> <span data-ttu-id="df5fc-115">Este é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="df5fc-115">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="df5fc-116">1</span><span class="sxs-lookup"><span data-stu-id="df5fc-116">1</span></span>
</dt> <dd>

<span data-ttu-id="df5fc-117">Reproduzir sons no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="df5fc-117">Play sounds at the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="df5fc-118">2</span><span class="sxs-lookup"><span data-stu-id="df5fc-118">2</span></span>
</dt> <dd>

<span data-ttu-id="df5fc-119">Desabilitar o redirecionamento de som; não reproduza sons no servidor.</span><span class="sxs-lookup"><span data-stu-id="df5fc-119">Disable sound redirection; do not play sounds at the server.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="df5fc-120">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="df5fc-120">Error codes</span></span>

<span data-ttu-id="df5fc-121">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="df5fc-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="df5fc-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="df5fc-122">Remarks</span></span>

<span data-ttu-id="df5fc-123">Essas propriedades não podem ser definidas quando o controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="df5fc-123">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="df5fc-124">Consulte [fornecer para o RDP Client Security](providing-for-rdp-client-security.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="df5fc-124">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="df5fc-125">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="df5fc-125">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df5fc-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df5fc-126">Requirements</span></span>



| <span data-ttu-id="df5fc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="df5fc-127">Requirement</span></span> | <span data-ttu-id="df5fc-128">Valor</span><span class="sxs-lookup"><span data-stu-id="df5fc-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df5fc-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df5fc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="df5fc-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df5fc-130">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="df5fc-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df5fc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="df5fc-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df5fc-132">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="df5fc-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="df5fc-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="df5fc-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df5fc-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="df5fc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="df5fc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df5fc-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df5fc-136"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="df5fc-137">IID</span><span class="sxs-lookup"><span data-stu-id="df5fc-137">IID</span></span><br/>                      | <span data-ttu-id="df5fc-138">IID \_ IMsRdpClientSecuredSettings é definido como 605befcf-39c1-45CC-a811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="df5fc-138">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df5fc-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="df5fc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df5fc-140">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="df5fc-140">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





