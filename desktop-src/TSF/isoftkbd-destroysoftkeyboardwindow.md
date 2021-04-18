---
title: Método ISoftKbd DestroySoftKeyboardWindow (Softkbdc. h)
description: O método ISoftKbd DestroySoftKeyboardWindow destrói uma janela de teclado flexível.
ms.assetid: 44030934-7b4a-46c1-95ea-709fc9004e43
keywords:
- Estrutura de serviços de texto do método DestroySoftKeyboardWindow
- Método DestroySoftKeyboardWindow de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método DestroySoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.DestroySoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb0c460912e8b891503771425fc72484fcc471ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761826"
---
# <a name="isoftkbddestroysoftkeyboardwindow-method"></a><span data-ttu-id="7e046-106">ISoftKbd: método estroySoftKeyboardWindow de:D</span><span class="sxs-lookup"><span data-stu-id="7e046-106">ISoftKbd::DestroySoftKeyboardWindow method</span></span>

<span data-ttu-id="7e046-107">O método **ISoftKbd::D estroysoftkeyboardwindow** destrói uma janela de teclado flexível.</span><span class="sxs-lookup"><span data-stu-id="7e046-107">The **ISoftKbd::DestroySoftKeyboardWindow** method destroys a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e046-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e046-108">Syntax</span></span>


```C++
HRESULT DestroySoftKeyboardWindow();
```



## <a name="parameters"></a><span data-ttu-id="7e046-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e046-109">Parameters</span></span>

<span data-ttu-id="7e046-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7e046-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e046-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e046-111">Return value</span></span>

<span data-ttu-id="7e046-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="7e046-112">This method can return one of these values.</span></span>



| <span data-ttu-id="7e046-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7e046-113">Value</span></span>                                                                                | <span data-ttu-id="7e046-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e046-114">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="7e046-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7e046-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7e046-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7e046-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7e046-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e046-117">Remarks</span></span>

<span data-ttu-id="7e046-118">Esse método remove uma janela de teclado flexível criada anteriormente com uma chamada para [**ISoftKbd:: CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).</span><span class="sxs-lookup"><span data-stu-id="7e046-118">This method removes a soft keyboard window previously created with a call to [**ISoftKbd::CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e046-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e046-119">Requirements</span></span>



| <span data-ttu-id="7e046-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e046-120">Requirement</span></span> | <span data-ttu-id="7e046-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7e046-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e046-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e046-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7e046-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7e046-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7e046-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e046-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7e046-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7e046-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7e046-126">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7e046-126">Redistributable</span></span><br/>          | <span data-ttu-id="7e046-127">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7e046-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="7e046-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7e046-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e046-129"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e046-129"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="7e046-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="7e046-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7e046-131"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7e046-131"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="7e046-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7e046-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e046-133"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e046-133"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e046-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e046-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e046-135">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="7e046-135">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="7e046-136">**ISoftKbd::CreateSoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="7e046-136">**ISoftKbd::CreateSoftKeyboardWindow**</span></span>](isoftkbd-createsoftkeyboardwindow.md)
</dt> </dl>

 

 





