---
description: Chamado quando o registro de uma janela do Shell é revogado.
title: Método DShellWindowsEvents. WindowRevoked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRevoked
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 92e8653f-7f41-4e0b-97e5-429fddc51951
ms.openlocfilehash: b036bdde2916c2fa037d1b6e286a2096d9e1d8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104970829"
---
# <a name="dshellwindowseventswindowrevoked-method"></a><span data-ttu-id="50092-103">Método DShellWindowsEvents. WindowRevoked</span><span class="sxs-lookup"><span data-stu-id="50092-103">DShellWindowsEvents.WindowRevoked method</span></span>

<span data-ttu-id="50092-104">Chamado quando o registro de uma janela do Shell é revogado.</span><span class="sxs-lookup"><span data-stu-id="50092-104">Called when a Shell window's registration is revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="50092-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50092-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="50092-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50092-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50092-107">*lCookie* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50092-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50092-108">Tipo: **inteiro**</span><span class="sxs-lookup"><span data-stu-id="50092-108">Type: **Integer**</span></span>

<span data-ttu-id="50092-109">O cookie que identifica a janela que foi revogada.</span><span class="sxs-lookup"><span data-stu-id="50092-109">The cookie that identifies the window that was revoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50092-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50092-110">Return value</span></span>

<span data-ttu-id="50092-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="50092-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50092-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="50092-112">Remarks</span></span>

<span data-ttu-id="50092-113">Uma janela recebe um cookie quando é registrada como uma janela do Shell.</span><span class="sxs-lookup"><span data-stu-id="50092-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="50092-114">Para obter mais informações, consulte [**registrar**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="50092-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="50092-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50092-115">Requirements</span></span>



| <span data-ttu-id="50092-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="50092-116">Requirement</span></span> | <span data-ttu-id="50092-117">Valor</span><span class="sxs-lookup"><span data-stu-id="50092-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50092-118">Produto</span><span class="sxs-lookup"><span data-stu-id="50092-118">Product</span></span><br/> | <span data-ttu-id="50092-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="50092-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="50092-120">DLL</span><span class="sxs-lookup"><span data-stu-id="50092-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="50092-121"><dt>Shdocvw.dll (versão 5.00.2014.0216 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="50092-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50092-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="50092-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50092-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="50092-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="50092-124">**WindowRegistered**</span><span class="sxs-lookup"><span data-stu-id="50092-124">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[<span data-ttu-id="50092-125">**Revogar**</span><span class="sxs-lookup"><span data-stu-id="50092-125">**Revoke**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




