---
title: Método IMsTscAxEvents OnFocusReleased
description: Chamado quando a combinação de teclas de foco da versão é pressionada. Por exemplo, esse evento é chamado quando o usuário pressiona as teclas CTRL + ALT + seta para a esquerda ou CTRL + ALT + seta para a direita.
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnFocusReleased
- Método OnFocusReleased Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnFocusReleased
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFocusReleased
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eff03f95d4ebbb068bccbfd9f68a930c00f0b00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760126"
---
# <a name="imstscaxeventsonfocusreleased-method"></a><span data-ttu-id="7bd51-107">Método IMsTscAxEvents:: OnFocusReleased</span><span class="sxs-lookup"><span data-stu-id="7bd51-107">IMsTscAxEvents::OnFocusReleased method</span></span>

<span data-ttu-id="7bd51-108">Chamado quando a combinação de teclas de foco da versão é pressionada.</span><span class="sxs-lookup"><span data-stu-id="7bd51-108">Called when the release focus key combination is pressed.</span></span> <span data-ttu-id="7bd51-109">Por exemplo, esse evento é chamado quando o usuário pressiona as teclas CTRL + ALT + seta para a esquerda ou CTRL + ALT + seta para a direita.</span><span class="sxs-lookup"><span data-stu-id="7bd51-109">For example, this event is called when the user presses the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination.</span></span>

<span data-ttu-id="7bd51-110">Esse evento permite que o contêiner de controle ActiveX assuma o controle do controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="7bd51-110">This event enables the ActiveX control container to take away control from the ActiveX control.</span></span> <span data-ttu-id="7bd51-111">Por exemplo, isso é útil em um cenário em que você não tem um mouse e as combinações de teclas especiais, como ALT + TAB, estão sendo redirecionadas para o servidor.</span><span class="sxs-lookup"><span data-stu-id="7bd51-111">For example, this is useful in a scenario where you do not have a mouse, and special key combinations such as ALT+TAB are being redirected to the server.</span></span> <span data-ttu-id="7bd51-112">Nesse caso, você não tem uma maneira de retornar o foco do teclado de volta para a área de trabalho local.</span><span class="sxs-lookup"><span data-stu-id="7bd51-112">In this case, you do not have a way to return the keyboard focus back to the local desktop.</span></span> <span data-ttu-id="7bd51-113">No entanto, com a combinação CTRL + ALT + seta para a esquerda ou CTRL + ALT + seta para a direita, o contêiner ActiveX pode escutar esse evento e responder, tirando o foco do controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="7bd51-113">However, with the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination, the ActiveX container can listen for this event and respond by taking focus away from the ActiveX control.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bd51-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7bd51-114">Syntax</span></span>


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a><span data-ttu-id="7bd51-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bd51-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bd51-116">*iDirection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7bd51-116">*iDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bd51-117">O parâmetro de direção de 1 (CTRL + ALT + seta direita) ou 1 (CTRL + ALT + seta para esquerda).</span><span class="sxs-lookup"><span data-stu-id="7bd51-117">The direction parameter of 1 (CTRL+ALT+RIGHT ARROW) or  1 (CTRL+ALT+LEFT ARROW).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bd51-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7bd51-118">Return value</span></span>

<span data-ttu-id="7bd51-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7bd51-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bd51-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bd51-120">Remarks</span></span>

<span data-ttu-id="7bd51-121">Esse evento está disponível quando Conexão de Área de Trabalho Remota 6,0 é usado no cliente.</span><span class="sxs-lookup"><span data-stu-id="7bd51-121">This event is available when Remote Desktop Connection 6.0 is used on the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bd51-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bd51-122">Requirements</span></span>



| <span data-ttu-id="7bd51-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bd51-123">Requirement</span></span> | <span data-ttu-id="7bd51-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7bd51-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bd51-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7bd51-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7bd51-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7bd51-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7bd51-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7bd51-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7bd51-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bd51-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7bd51-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7bd51-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="7bd51-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bd51-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7bd51-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7bd51-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bd51-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bd51-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7bd51-133">IID</span><span class="sxs-lookup"><span data-stu-id="7bd51-133">IID</span></span><br/>                      | <span data-ttu-id="7bd51-134">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="7bd51-134">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="7bd51-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bd51-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bd51-136">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="7bd51-136">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





