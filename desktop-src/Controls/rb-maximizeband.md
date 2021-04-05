---
title: Mensagem de RB_MAXIMIZEBAND (commctrl. h)
description: Redimensiona uma faixa em um controle rebar para o tamanho ideal ou maior.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- Controles de RB_MAXIMIZEBAND de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708a8fae7c0dd8e72eea8e5acefe43ab50054592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824584"
---
# <a name="rb_maximizeband-message"></a><span data-ttu-id="18507-104">\_Mensagem MAXIMIZEBAND RB</span><span class="sxs-lookup"><span data-stu-id="18507-104">RB\_MAXIMIZEBAND message</span></span>

<span data-ttu-id="18507-105">Redimensiona uma faixa em um controle rebar para o tamanho ideal ou maior.</span><span class="sxs-lookup"><span data-stu-id="18507-105">Resizes a band in a rebar control to either its ideal or largest size.</span></span>

## <a name="parameters"></a><span data-ttu-id="18507-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18507-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18507-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="18507-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18507-108">Índice de base zero da banda a ser maximizado.</span><span class="sxs-lookup"><span data-stu-id="18507-108">Zero-based index of the band to be maximized.</span></span>

</dd> <dt>

<span data-ttu-id="18507-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18507-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18507-110">Indica se a largura ideal da banda deve ser usada quando a banda é maximizada.</span><span class="sxs-lookup"><span data-stu-id="18507-110">Indicates if the ideal width of the band should be used when the band is maximized.</span></span> <span data-ttu-id="18507-111">Se esse valor for diferente de zero, a largura ideal será usada.</span><span class="sxs-lookup"><span data-stu-id="18507-111">If this value is nonzero, the ideal width will be used.</span></span> <span data-ttu-id="18507-112">Se esse valor for zero, a banda será feita o máximo possível.</span><span class="sxs-lookup"><span data-stu-id="18507-112">If this value is zero, the band will be made as large as possible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18507-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="18507-113">Return value</span></span>

<span data-ttu-id="18507-114">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="18507-114">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="18507-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18507-115">Requirements</span></span>



| <span data-ttu-id="18507-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="18507-116">Requirement</span></span> | <span data-ttu-id="18507-117">Valor</span><span class="sxs-lookup"><span data-stu-id="18507-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18507-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18507-118">Minimum supported client</span></span><br/> | <span data-ttu-id="18507-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18507-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="18507-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18507-120">Minimum supported server</span></span><br/> | <span data-ttu-id="18507-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="18507-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18507-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="18507-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="18507-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="18507-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18507-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="18507-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="18507-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="18507-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="18507-126">**\_SETBANDINFO RB**</span><span class="sxs-lookup"><span data-stu-id="18507-126">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
</dt> </dl>

 

 





