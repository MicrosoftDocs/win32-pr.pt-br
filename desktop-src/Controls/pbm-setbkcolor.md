---
title: Mensagem de PBM_SETBKCOLOR (commctrl. h)
description: Define a cor do plano de fundo na barra de progresso.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- Controles de PBM_SETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfaf84695221cf998275d76a9d2d67773150da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644909"
---
# <a name="pbm_setbkcolor-message"></a><span data-ttu-id="3ed2e-104">Mensagem do SETBKCOLOR do PBM \_</span><span class="sxs-lookup"><span data-stu-id="3ed2e-104">PBM\_SETBKCOLOR message</span></span>

<span data-ttu-id="3ed2e-105">Define a cor do plano de fundo na barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="3ed2e-105">Sets the background color in the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ed2e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ed2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ed2e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ed2e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ed2e-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3ed2e-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3ed2e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ed2e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ed2e-110">Valor **COLORREF** que especifica a nova cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="3ed2e-110">**COLORREF** value that specifies the new background color.</span></span> <span data-ttu-id="3ed2e-111">Especifique o \_ valor padrão do CLR para fazer com que a barra de progresso Use sua cor de plano de fundo padrão.</span><span class="sxs-lookup"><span data-stu-id="3ed2e-111">Specify the CLR\_DEFAULT value to cause the progress bar to use its default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ed2e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ed2e-112">Return value</span></span>

<span data-ttu-id="3ed2e-113">Retorna a cor do plano de fundo anterior ou o \_ padrão CLR se a cor do plano de fundo for a cor padrão.</span><span class="sxs-lookup"><span data-stu-id="3ed2e-113">Returns the previous background color, or CLR\_DEFAULT if the background color is the default color.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ed2e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ed2e-114">Remarks</span></span>

<span data-ttu-id="3ed2e-115">Quando os estilos visuais são habilitados, essa mensagem não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="3ed2e-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ed2e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ed2e-116">Requirements</span></span>



| <span data-ttu-id="3ed2e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ed2e-117">Requirement</span></span> | <span data-ttu-id="3ed2e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3ed2e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed2e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ed2e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3ed2e-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ed2e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3ed2e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ed2e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3ed2e-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3ed2e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ed2e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ed2e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ed2e-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ed2e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





