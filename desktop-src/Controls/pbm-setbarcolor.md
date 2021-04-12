---
title: Mensagem de PBM_SETBARCOLOR (commctrl. h)
description: Define a cor da barra de indicadores de progresso no controle da barra de progresso.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- Controles de PBM_SETBARCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1387e69622e84990a197dc5a374d1c3449393408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499544"
---
# <a name="pbm_setbarcolor-message"></a><span data-ttu-id="3da48-104">Mensagem do SETBARCOLOR do PBM \_</span><span class="sxs-lookup"><span data-stu-id="3da48-104">PBM\_SETBARCOLOR message</span></span>

<span data-ttu-id="3da48-105">Define a cor da barra de indicadores de progresso no controle da barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="3da48-105">Sets the color of the progress indicator bar in the progress bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3da48-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3da48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da48-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3da48-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3da48-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3da48-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3da48-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3da48-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3da48-110">O valor **COLORREF** que especifica a nova cor da barra de indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="3da48-110">The **COLORREF** value that specifies the new progress indicator bar color.</span></span> <span data-ttu-id="3da48-111">A especificação do \_ valor padrão CLR faz com que a barra de progresso Use sua cor de barra de indicador de andamento padrão.</span><span class="sxs-lookup"><span data-stu-id="3da48-111">Specifying the CLR\_DEFAULT value causes the progress bar to use its default progress indicator bar color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3da48-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3da48-112">Return value</span></span>

<span data-ttu-id="3da48-113">Retorna a cor da barra de indicadores de progresso anterior ou o \_ padrão CLR se a cor da barra de indicador de progresso for a cor padrão.</span><span class="sxs-lookup"><span data-stu-id="3da48-113">Returns the previous progress indicator bar color, or CLR\_DEFAULT if the progress indicator bar color is the default color.</span></span>

## <a name="remarks"></a><span data-ttu-id="3da48-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3da48-114">Remarks</span></span>

<span data-ttu-id="3da48-115">Quando os estilos visuais são habilitados, essa mensagem não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="3da48-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="3da48-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3da48-116">Requirements</span></span>



| <span data-ttu-id="3da48-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3da48-117">Requirement</span></span> | <span data-ttu-id="3da48-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3da48-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3da48-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3da48-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3da48-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3da48-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3da48-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3da48-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3da48-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3da48-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3da48-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3da48-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3da48-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3da48-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





