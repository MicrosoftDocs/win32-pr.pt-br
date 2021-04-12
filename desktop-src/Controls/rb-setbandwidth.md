---
title: Mensagem de RB_SETBANDWIDTH (commctrl. h)
description: Define a largura de uma faixa encaixada.
ms.assetid: dca9dfe9-3e5a-40bb-8de7-a296e6be7d06
keywords:
- Controles de RB_SETBANDWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_SETBANDWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790f42ab977cfc0554c9a0eca737d541e001b6c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455528"
---
# <a name="rb_setbandwidth-message"></a><span data-ttu-id="cbc20-104">\_Mensagem de largura de banda RB</span><span class="sxs-lookup"><span data-stu-id="cbc20-104">RB\_SETBANDWIDTH message</span></span>

<span data-ttu-id="cbc20-105">Define a largura de uma faixa encaixada.</span><span class="sxs-lookup"><span data-stu-id="cbc20-105">Sets the width for a docked band.</span></span>

## <a name="parameters"></a><span data-ttu-id="cbc20-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbc20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbc20-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cbc20-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbc20-108">Índice da banda.</span><span class="sxs-lookup"><span data-stu-id="cbc20-108">Index of the band.</span></span>

</dd> <dt>

<span data-ttu-id="cbc20-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cbc20-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbc20-110">Nova largura em pixels.</span><span class="sxs-lookup"><span data-stu-id="cbc20-110">New width in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbc20-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbc20-111">Return value</span></span>

<span data-ttu-id="cbc20-112">Retornará **true** se o valor tiver sido definido e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="cbc20-112">Returns **TRUE** if the value was set and **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbc20-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbc20-113">Requirements</span></span>



| <span data-ttu-id="cbc20-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbc20-114">Requirement</span></span> | <span data-ttu-id="cbc20-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cbc20-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc20-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbc20-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cbc20-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cbc20-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cbc20-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbc20-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cbc20-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cbc20-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cbc20-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbc20-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbc20-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbc20-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





