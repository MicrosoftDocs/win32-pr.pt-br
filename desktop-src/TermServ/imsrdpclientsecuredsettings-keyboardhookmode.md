---
title: Propriedade IMsRdpClientSecuredSettings KeyboardHookMode
description: Especifica as configurações de redirecionamento de teclado, que especificam como e quando aplicar o atalho de teclado do Windows (por exemplo, ALT + TAB).
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade KeyboardHookMode
- Propriedade KeyboardHookMode Serviços de Área de Trabalho Remota, interface IMsRdpClientSecuredSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientSecuredSettings, Propriedade KeyboardHookMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.KeyboardHookMode
- IMsRdpClientSecuredSettings.get_KeyboardHookMode
- IMsRdpClientSecuredSettings.put_KeyboardHookMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 948069b689d8799a98805148017a204b719d7645
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369434"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a><span data-ttu-id="f7c33-106">Propriedade IMsRdpClientSecuredSettings:: KeyboardHookMode</span><span class="sxs-lookup"><span data-stu-id="f7c33-106">IMsRdpClientSecuredSettings::KeyboardHookMode property</span></span>

<span data-ttu-id="f7c33-107">Especifica as configurações de redirecionamento de teclado, que especificam como e quando aplicar o atalho de teclado do Windows (por exemplo, ALT + TAB).</span><span class="sxs-lookup"><span data-stu-id="f7c33-107">Specifies the keyboard redirection settings, which specify how and when to apply Windows keyboard shortcut (for example, ALT+TAB).</span></span>

<span data-ttu-id="f7c33-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f7c33-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c33-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7c33-109">Syntax</span></span>


```C++
HRESULT put_KeyboardHookMode(
  [in]  LONG keyboardHookMode
);

HRESULT get_KeyboardHookMode(
  [out] LONG *pkeyboardHookMode
);
```



## <a name="property-value"></a><span data-ttu-id="f7c33-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f7c33-110">Property value</span></span>

<span data-ttu-id="f7c33-111">As novas configurações.</span><span class="sxs-lookup"><span data-stu-id="f7c33-111">The new settings.</span></span> <span data-ttu-id="f7c33-112">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f7c33-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="f7c33-113">0</span><span class="sxs-lookup"><span data-stu-id="f7c33-113">0</span></span>
</dt> <dd>

<span data-ttu-id="f7c33-114">Aplicar combinações de teclas somente localmente no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="f7c33-114">Apply key combinations only locally at the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="f7c33-115">1</span><span class="sxs-lookup"><span data-stu-id="f7c33-115">1</span></span>
</dt> <dd>

<span data-ttu-id="f7c33-116">Aplicar combinações de chaves no servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="f7c33-116">Apply key combinations at the remote server.</span></span>

</dd> <dt>

<span data-ttu-id="f7c33-117">2</span><span class="sxs-lookup"><span data-stu-id="f7c33-117">2</span></span>
</dt> <dd>

<span data-ttu-id="f7c33-118">Aplique combinações de teclas ao servidor remoto somente quando o cliente estiver sendo executado no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="f7c33-118">Apply key combinations to the remote server only when the client is running in full-screen mode.</span></span> <span data-ttu-id="f7c33-119">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="f7c33-119">This is the default value.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="f7c33-120">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f7c33-120">Error codes</span></span>

<span data-ttu-id="f7c33-121">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f7c33-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7c33-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7c33-122">Remarks</span></span>

<span data-ttu-id="f7c33-123">Essas propriedades não podem ser definidas quando o controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="f7c33-123">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="f7c33-124">Consulte [fornecer para o RDP Client Security](providing-for-rdp-client-security.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f7c33-124">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="f7c33-125">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f7c33-125">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7c33-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7c33-126">Requirements</span></span>



| <span data-ttu-id="f7c33-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7c33-127">Requirement</span></span> | <span data-ttu-id="f7c33-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f7c33-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7c33-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7c33-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f7c33-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7c33-130">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="f7c33-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7c33-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f7c33-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7c33-132">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="f7c33-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f7c33-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7c33-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7c33-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="f7c33-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f7c33-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7c33-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7c33-136"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="f7c33-137">IID</span><span class="sxs-lookup"><span data-stu-id="f7c33-137">IID</span></span><br/>                      | <span data-ttu-id="f7c33-138">IID \_ IMsRdpClientSecuredSettings é definido como 605befcf-39c1-45CC-a811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="f7c33-138">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f7c33-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7c33-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7c33-140">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="f7c33-140">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





