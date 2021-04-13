---
title: Método IMsTscAxEvents OnRemoteWindowDisplayed
description: Chamado quando uma janela do RemoteApp é exibida.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnRemoteWindowDisplayed
- Método OnRemoteWindowDisplayed Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnRemoteWindowDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteWindowDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f03029f31e1ce2133c74c92c0d6d57f192e4d85f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369727"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a><span data-ttu-id="6c6a8-106">Método IMsTscAxEvents:: OnRemoteWindowDisplayed</span><span class="sxs-lookup"><span data-stu-id="6c6a8-106">IMsTscAxEvents::OnRemoteWindowDisplayed method</span></span>

<span data-ttu-id="6c6a8-107">Chamado quando uma janela do RemoteApp é exibida.</span><span class="sxs-lookup"><span data-stu-id="6c6a8-107">Called when a RemoteApp window is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c6a8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c6a8-108">Syntax</span></span>


```C++
void OnRemoteWindowDisplayed(
  [in] VARIANT_BOOL                   vbDisplayed,
  [in] HWND                           hwnd,
  [in] RemoteWindowDisplayedAttribute windowAttribute
);
```



## <a name="parameters"></a><span data-ttu-id="6c6a8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c6a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c6a8-110">*vbDisplayed* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c6a8-110">*vbDisplayed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6a8-111">Tipo: **\_ booliano de variante**</span><span class="sxs-lookup"><span data-stu-id="6c6a8-111">Type: **VARIANT\_BOOL**</span></span>

<span data-ttu-id="6c6a8-112">Indica se a janela do RemoteApp é exibida ou oculta.</span><span class="sxs-lookup"><span data-stu-id="6c6a8-112">Indicates whether the RemoteApp window is displayed or hidden.</span></span>

</dd> <dt>

<span data-ttu-id="6c6a8-113">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c6a8-113">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6a8-114">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="6c6a8-114">Type: **HWND**</span></span>

<span data-ttu-id="6c6a8-115">O identificador da janela exibida.</span><span class="sxs-lookup"><span data-stu-id="6c6a8-115">The handle of the window displayed.</span></span>

</dd> <dt>

<span data-ttu-id="6c6a8-116">*janelaattribute* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c6a8-116">*windowAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6a8-117">Tipo: **[ **RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**</span><span class="sxs-lookup"><span data-stu-id="6c6a8-117">Type: **[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**</span></span>

<span data-ttu-id="6c6a8-118">Um valor da enumeração [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) que especifica mais informações sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="6c6a8-118">A value of the [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) enumeration that specifies more information about the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c6a8-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c6a8-119">Return value</span></span>

<span data-ttu-id="6c6a8-120">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6c6a8-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c6a8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c6a8-121">Requirements</span></span>



| <span data-ttu-id="6c6a8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c6a8-122">Requirement</span></span> | <span data-ttu-id="6c6a8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6c6a8-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6a8-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c6a8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c6a8-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6c6a8-125">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="6c6a8-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c6a8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c6a8-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6c6a8-127">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="6c6a8-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6c6a8-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="6c6a8-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c6a8-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6c6a8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6c6a8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c6a8-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c6a8-131"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c6a8-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c6a8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c6a8-133">**RemoteWindowDisplayedAttribute**</span><span class="sxs-lookup"><span data-stu-id="6c6a8-133">**RemoteWindowDisplayedAttribute**</span></span>](remotewindowdisplayedattribute.md)
</dt> <dt>

[<span data-ttu-id="6c6a8-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="6c6a8-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





