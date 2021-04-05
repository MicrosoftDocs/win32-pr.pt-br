---
title: Método IMsTscAxEvents OnEnterFullScreenMode
description: Chamado quando o cliente entra no modo de tela inteira. Por exemplo, esse evento é chamado quando o usuário pressiona a combinação de teclas de atalho no modo de tela inteira (CTRL + ALT + BREAK).
ms.assetid: dc772492-59a2-4403-8b9a-0aff1801aa6f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnEnterFullScreenMode
- Método OnEnterFullScreenMode Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnEnterFullScreenMode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnEnterFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226054fc7b1371bb088deb70ec9e87ea5a340b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918649"
---
# <a name="imstscaxeventsonenterfullscreenmode-method"></a><span data-ttu-id="004b1-107">Método IMsTscAxEvents:: OnEnterFullScreenMode</span><span class="sxs-lookup"><span data-stu-id="004b1-107">IMsTscAxEvents::OnEnterFullScreenMode method</span></span>

<span data-ttu-id="004b1-108">Chamado quando o cliente entra no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="004b1-108">Called when the client enters full-screen mode.</span></span> <span data-ttu-id="004b1-109">Por exemplo, esse evento é chamado quando o usuário pressiona a combinação de [teclas de atalho](terminal-services-shortcut-keys.md) no modo de tela inteira (Ctrl + Alt + Break).</span><span class="sxs-lookup"><span data-stu-id="004b1-109">For example, this event is called when the user presses the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

## <a name="syntax"></a><span data-ttu-id="004b1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="004b1-110">Syntax</span></span>


```C++
void OnEnterFullScreenMode();
```



## <a name="parameters"></a><span data-ttu-id="004b1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="004b1-111">Parameters</span></span>

<span data-ttu-id="004b1-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="004b1-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="004b1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="004b1-113">Return value</span></span>

<span data-ttu-id="004b1-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="004b1-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="004b1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="004b1-115">Remarks</span></span>

<span data-ttu-id="004b1-116">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="004b1-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="004b1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="004b1-117">Requirements</span></span>



| <span data-ttu-id="004b1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="004b1-118">Requirement</span></span> | <span data-ttu-id="004b1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="004b1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="004b1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="004b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="004b1-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="004b1-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="004b1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="004b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="004b1-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="004b1-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="004b1-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="004b1-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="004b1-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="004b1-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="004b1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="004b1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="004b1-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="004b1-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="004b1-128">IID</span><span class="sxs-lookup"><span data-stu-id="004b1-128">IID</span></span><br/>                      | <span data-ttu-id="004b1-129">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="004b1-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="004b1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="004b1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="004b1-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="004b1-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





