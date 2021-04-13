---
title: Mensagem de RB_PUSHCHEVRON (commctrl. h)
description: Enviado a um controle rebar para enviar por push programaticamente uma divisa.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- Controles de RB_PUSHCHEVRON de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09e558d5574d4fd28cf01e9794657556dda4ae8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499540"
---
# <a name="rb_pushchevron-message"></a><span data-ttu-id="e05d3-104">\_Mensagem PUSHCHEVRON RB</span><span class="sxs-lookup"><span data-stu-id="e05d3-104">RB\_PUSHCHEVRON message</span></span>

<span data-ttu-id="e05d3-105">Enviado a um controle rebar para enviar por push programaticamente uma divisa.</span><span class="sxs-lookup"><span data-stu-id="e05d3-105">Sent to a rebar control to programmatically push a chevron.</span></span>

## <a name="parameters"></a><span data-ttu-id="e05d3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e05d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e05d3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e05d3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e05d3-108">Índice de base zero da faixa cuja divisa deve ser enviada por push.</span><span class="sxs-lookup"><span data-stu-id="e05d3-108">Zero-based index of the band whose chevron is to be pushed.</span></span>

</dd> <dt>

<span data-ttu-id="e05d3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e05d3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e05d3-110">Um valor de 32 bits definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e05d3-110">An application defined 32-bit value.</span></span> <span data-ttu-id="e05d3-111">Ele será passado de volta para o aplicativo como o membro **lParamNM** da estrutura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) que é passada com a notificação [ \_ CHEVRONPUSHED RBN](rbn-chevronpushed.md) .</span><span class="sxs-lookup"><span data-stu-id="e05d3-111">It will be passed back to the application as the **lParamNM** member of the [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure that is passed with the [RBN\_CHEVRONPUSHED](rbn-chevronpushed.md) notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e05d3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e05d3-112">Return value</span></span>

<span data-ttu-id="e05d3-113">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="e05d3-113">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e05d3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e05d3-114">Remarks</span></span>

<span data-ttu-id="e05d3-115">Quando essa mensagem é enviada, o controle rebar enviará ao aplicativo um código de notificação [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) , solicitando que ele exiba o menu de divisa.</span><span class="sxs-lookup"><span data-stu-id="e05d3-115">When this message is sent, the rebar control will send the application an [RBN\_CHEVRONPUSHED](rbn-chevronpushed.md) notification code, prompting it to display the chevron menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="e05d3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e05d3-116">Requirements</span></span>



| <span data-ttu-id="e05d3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e05d3-117">Requirement</span></span> | <span data-ttu-id="e05d3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e05d3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e05d3-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e05d3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e05d3-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e05d3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e05d3-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e05d3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e05d3-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e05d3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e05d3-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e05d3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e05d3-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e05d3-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





