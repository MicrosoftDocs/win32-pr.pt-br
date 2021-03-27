---
description: Recebe eventos de registro da janela IShellWindows.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: Objeto DShellWindowsEvents (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents
api_type:
- COM
api_location:
- Shdocvw.dll
ms.openlocfilehash: 7df1571556b5f2942f181b4c88b22ff3bc83f273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104970812"
---
# <a name="dshellwindowsevents-object"></a><span data-ttu-id="26010-103">Objeto DShellWindowsEvents</span><span class="sxs-lookup"><span data-stu-id="26010-103">DShellWindowsEvents object</span></span>

<span data-ttu-id="26010-104">Recebe eventos de registro da janela [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) .</span><span class="sxs-lookup"><span data-stu-id="26010-104">Receives [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) window registration events.</span></span>

## <a name="members"></a><span data-ttu-id="26010-105">Membros</span><span class="sxs-lookup"><span data-stu-id="26010-105">Members</span></span>

<span data-ttu-id="26010-106">O objeto **DShellWindowsEvents** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="26010-106">The **DShellWindowsEvents** object has these types of members:</span></span>

-   [<span data-ttu-id="26010-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="26010-107">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="26010-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="26010-108">Methods</span></span>

<span data-ttu-id="26010-109">O objeto **DShellWindowsEvents** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="26010-109">The **DShellWindowsEvents** object has these methods.</span></span>



| <span data-ttu-id="26010-110">Método</span><span class="sxs-lookup"><span data-stu-id="26010-110">Method</span></span>                                                           | <span data-ttu-id="26010-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="26010-111">Description</span></span>                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="26010-112">**WindowRegistered**</span><span class="sxs-lookup"><span data-stu-id="26010-112">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md) | <span data-ttu-id="26010-113">Chamado quando uma janela é registrada como uma janela de Shell.</span><span class="sxs-lookup"><span data-stu-id="26010-113">Called when a window is registered as a Shell window.</span></span> <br/> |
| [<span data-ttu-id="26010-114">**WindowRevoked**</span><span class="sxs-lookup"><span data-stu-id="26010-114">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)       | <span data-ttu-id="26010-115">Chamado quando o registro de uma janela do Shell é revogado.</span><span class="sxs-lookup"><span data-stu-id="26010-115">Called when a Shell window's registration is revoked.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="26010-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="26010-116">Remarks</span></span>

<span data-ttu-id="26010-117">Use **DShellWindowsEvents** para monitorar quando uma janela de Shell é registrada ou revogada.</span><span class="sxs-lookup"><span data-stu-id="26010-117">Use **DShellWindowsEvents** to monitor when a Shell window is registered or revoked.</span></span> <span data-ttu-id="26010-118">Para obter mais informações, consulte [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).</span><span class="sxs-lookup"><span data-stu-id="26010-118">For more information, see [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).</span></span>

## <a name="requirements"></a><span data-ttu-id="26010-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26010-119">Requirements</span></span>



| <span data-ttu-id="26010-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="26010-120">Requirement</span></span> | <span data-ttu-id="26010-121">Valor</span><span class="sxs-lookup"><span data-stu-id="26010-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26010-122">Produto</span><span class="sxs-lookup"><span data-stu-id="26010-122">Product</span></span><br/> | <span data-ttu-id="26010-123">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="26010-123">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="26010-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26010-124">Header</span></span><br/>  | <dl> <span data-ttu-id="26010-125"><dt>O textdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="26010-125"><dt>Exdisp.h</dt></span></span> </dl>                                      |
| <span data-ttu-id="26010-126">DLL</span><span class="sxs-lookup"><span data-stu-id="26010-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="26010-127"><dt>Shdocvw.dll (versão 5.00.2014.0216 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="26010-127"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |
| <span data-ttu-id="26010-128">IID</span><span class="sxs-lookup"><span data-stu-id="26010-128">IID</span></span><br/>     | <span data-ttu-id="26010-129">IShellWindows de IID \_</span><span class="sxs-lookup"><span data-stu-id="26010-129">IID\_IShellWindows</span></span><br/>                                                                                            |



## <a name="see-also"></a><span data-ttu-id="26010-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="26010-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26010-131">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="26010-131">**ShellWindows**</span></span>](shellwindows.md)
</dt> </dl>

 

 




