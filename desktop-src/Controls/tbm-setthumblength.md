---
title: Mensagem de TBM_SETTHUMBLENGTH (commctrl. h)
description: Define o comprimento do controle deslizante em um TrackBar. Essa mensagem será ignorada se o TrackBar não tiver o \_ estilo Cadeia TBS.
ms.assetid: 027fe341-a60a-4dbe-a48a-5ddaadef0b4a
keywords:
- Controles de TBM_SETTHUMBLENGTH de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETTHUMBLENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d4ac33d2df43a267766e14ab95fb9729692bbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499695"
---
# <a name="tbm_setthumblength-message"></a><span data-ttu-id="0edd3-105">\_Mensagem tbm SETTHUMBLENGTH</span><span class="sxs-lookup"><span data-stu-id="0edd3-105">TBM\_SETTHUMBLENGTH message</span></span>

<span data-ttu-id="0edd3-106">Define o comprimento do controle deslizante em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="0edd3-106">Sets the length of the slider in a trackbar.</span></span> <span data-ttu-id="0edd3-107">Essa mensagem será ignorada se o TrackBar não tiver o [**estilo \_ Cadeia TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0edd3-107">This message is ignored if the trackbar does not have the [**TBS\_FIXEDLENGTH**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="0edd3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0edd3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0edd3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0edd3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0edd3-110">Comprimento, em pixels, do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="0edd3-110">Length, in pixels, of the slider.</span></span>

</dd> <dt>

<span data-ttu-id="0edd3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0edd3-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0edd3-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0edd3-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0edd3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0edd3-113">Return value</span></span>

<span data-ttu-id="0edd3-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0edd3-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0edd3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0edd3-115">Requirements</span></span>



| <span data-ttu-id="0edd3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0edd3-116">Requirement</span></span> | <span data-ttu-id="0edd3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0edd3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0edd3-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0edd3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0edd3-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0edd3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0edd3-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0edd3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0edd3-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0edd3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0edd3-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0edd3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0edd3-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0edd3-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0edd3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0edd3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0edd3-125">**TBM \_ GETTHUMBLENGTH**</span><span class="sxs-lookup"><span data-stu-id="0edd3-125">**TBM\_GETTHUMBLENGTH**</span></span>](tbm-getthumblength.md)
</dt> </dl>

 

 





