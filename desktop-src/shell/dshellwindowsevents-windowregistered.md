---
description: Chamado quando uma janela é registrada como uma janela de Shell.
title: Método DShellWindowsEvents. WindowRegistered
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRegistered
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 7faf758a-daa0-47f5-9f95-61fe3d8286ea
ms.openlocfilehash: 64bf83a88584c5d97994726696d4fb3a1e971bdf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841447"
---
# <a name="dshellwindowseventswindowregistered-method"></a><span data-ttu-id="69add-103">Método DShellWindowsEvents. WindowRegistered</span><span class="sxs-lookup"><span data-stu-id="69add-103">DShellWindowsEvents.WindowRegistered method</span></span>

<span data-ttu-id="69add-104">Chamado quando uma janela é registrada como uma janela de Shell.</span><span class="sxs-lookup"><span data-stu-id="69add-104">Called when a window is registered as a Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="69add-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69add-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="69add-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69add-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69add-107">*lCookie* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69add-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69add-108">Tipo: **inteiro**</span><span class="sxs-lookup"><span data-stu-id="69add-108">Type: **Integer**</span></span>

<span data-ttu-id="69add-109">O cookie que identifica a janela que foi registrada.</span><span class="sxs-lookup"><span data-stu-id="69add-109">The cookie that identifies the window that was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69add-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69add-110">Return value</span></span>

<span data-ttu-id="69add-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="69add-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69add-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="69add-112">Remarks</span></span>

<span data-ttu-id="69add-113">Uma janela recebe um cookie quando é registrada como uma janela do Shell.</span><span class="sxs-lookup"><span data-stu-id="69add-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="69add-114">Para obter mais informações, consulte [**registrar**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="69add-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="69add-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69add-115">Requirements</span></span>



| <span data-ttu-id="69add-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="69add-116">Requirement</span></span> | <span data-ttu-id="69add-117">Valor</span><span class="sxs-lookup"><span data-stu-id="69add-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69add-118">Produto</span><span class="sxs-lookup"><span data-stu-id="69add-118">Product</span></span><br/> | <span data-ttu-id="69add-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="69add-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="69add-120">DLL</span><span class="sxs-lookup"><span data-stu-id="69add-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="69add-121"><dt>Shdocvw.dll (versão 5.00.2014.0216 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="69add-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69add-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="69add-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69add-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="69add-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="69add-124">**WindowRevoked**</span><span class="sxs-lookup"><span data-stu-id="69add-124">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[<span data-ttu-id="69add-125">**Registre-se**</span><span class="sxs-lookup"><span data-stu-id="69add-125">**Register**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[<span data-ttu-id="69add-126">**RegisterPending**</span><span class="sxs-lookup"><span data-stu-id="69add-126">**RegisterPending**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




