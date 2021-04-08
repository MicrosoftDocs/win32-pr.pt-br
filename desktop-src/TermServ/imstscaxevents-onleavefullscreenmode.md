---
title: Método IMsTscAxEvents OnLeaveFullScreenMode
description: Chamado quando o cliente deixa o modo de tela inteira. Por exemplo, esse evento é chamado quando o usuário pressiona a combinação de teclas de atalho no modo de tela inteira (CTRL + ALT + BREAK).
ms.assetid: 95c5d427-b6e2-4a42-9816-b130ab533ac0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnLeaveFullScreenMode
- Método OnLeaveFullScreenMode Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnLeaveFullScreenMode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLeaveFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4ee414f2dceba35a17ff86bce03c83d75aab48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009511"
---
# <a name="imstscaxeventsonleavefullscreenmode-method"></a><span data-ttu-id="d46c2-107">Método IMsTscAxEvents:: OnLeaveFullScreenMode</span><span class="sxs-lookup"><span data-stu-id="d46c2-107">IMsTscAxEvents::OnLeaveFullScreenMode method</span></span>

<span data-ttu-id="d46c2-108">Chamado quando o cliente deixa o modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="d46c2-108">Called when the client leaves full-screen mode.</span></span> <span data-ttu-id="d46c2-109">Por exemplo, esse evento é chamado quando o usuário pressiona a combinação de [teclas de atalho](terminal-services-shortcut-keys.md) no modo de tela inteira (Ctrl + Alt + Break).</span><span class="sxs-lookup"><span data-stu-id="d46c2-109">For example, this event is called when the user presses the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

## <a name="syntax"></a><span data-ttu-id="d46c2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d46c2-110">Syntax</span></span>


```C++
void OnLeaveFullScreenMode();
```



## <a name="parameters"></a><span data-ttu-id="d46c2-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d46c2-111">Parameters</span></span>

<span data-ttu-id="d46c2-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d46c2-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d46c2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d46c2-113">Return value</span></span>

<span data-ttu-id="d46c2-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d46c2-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d46c2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d46c2-115">Remarks</span></span>

<span data-ttu-id="d46c2-116">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d46c2-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d46c2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d46c2-117">Requirements</span></span>



| <span data-ttu-id="d46c2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d46c2-118">Requirement</span></span> | <span data-ttu-id="d46c2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d46c2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d46c2-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d46c2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d46c2-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d46c2-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d46c2-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d46c2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d46c2-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d46c2-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d46c2-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d46c2-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="d46c2-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d46c2-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d46c2-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d46c2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d46c2-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d46c2-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d46c2-128">IID</span><span class="sxs-lookup"><span data-stu-id="d46c2-128">IID</span></span><br/>                      | <span data-ttu-id="d46c2-129">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="d46c2-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="d46c2-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d46c2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d46c2-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="d46c2-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





