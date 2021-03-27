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
ms.openlocfilehash: b12ed98c6b2a11e5886ed9e76d324a1a6842cda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104970825"
---
# <a name="dshellwindowseventswindowregistered-method"></a><span data-ttu-id="65a4a-103">Método DShellWindowsEvents. WindowRegistered</span><span class="sxs-lookup"><span data-stu-id="65a4a-103">DShellWindowsEvents.WindowRegistered method</span></span>

<span data-ttu-id="65a4a-104">Chamado quando uma janela é registrada como uma janela de Shell.</span><span class="sxs-lookup"><span data-stu-id="65a4a-104">Called when a window is registered as a Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="65a4a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65a4a-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="65a4a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65a4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65a4a-107">*lCookie* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65a4a-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a4a-108">Tipo: **inteiro**</span><span class="sxs-lookup"><span data-stu-id="65a4a-108">Type: **Integer**</span></span>

<span data-ttu-id="65a4a-109">O cookie que identifica a janela que foi registrada.</span><span class="sxs-lookup"><span data-stu-id="65a4a-109">The cookie that identifies the window that was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65a4a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65a4a-110">Return value</span></span>

<span data-ttu-id="65a4a-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="65a4a-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65a4a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="65a4a-112">Remarks</span></span>

<span data-ttu-id="65a4a-113">Uma janela recebe um cookie quando é registrada como uma janela do Shell.</span><span class="sxs-lookup"><span data-stu-id="65a4a-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="65a4a-114">Para obter mais informações, consulte [**registrar**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="65a4a-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="65a4a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65a4a-115">Requirements</span></span>



| <span data-ttu-id="65a4a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="65a4a-116">Requirement</span></span> | <span data-ttu-id="65a4a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="65a4a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65a4a-118">Produto</span><span class="sxs-lookup"><span data-stu-id="65a4a-118">Product</span></span><br/> | <span data-ttu-id="65a4a-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="65a4a-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="65a4a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="65a4a-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="65a4a-121"><dt>Shdocvw.dll (versão 5.00.2014.0216 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="65a4a-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65a4a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="65a4a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65a4a-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="65a4a-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="65a4a-124">**WindowRevoked**</span><span class="sxs-lookup"><span data-stu-id="65a4a-124">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[<span data-ttu-id="65a4a-125">**Registre-se**</span><span class="sxs-lookup"><span data-stu-id="65a4a-125">**Register**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[<span data-ttu-id="65a4a-126">**RegisterPending**</span><span class="sxs-lookup"><span data-stu-id="65a4a-126">**RegisterPending**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




