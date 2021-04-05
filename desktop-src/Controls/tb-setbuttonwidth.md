---
title: Mensagem de TB_SETBUTTONWIDTH (commctrl. h)
description: Define as larguras mínima e máxima do botão no controle da barra de ferramentas.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- Controles de TB_SETBUTTONWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETBUTTONWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e105770d72e90108b9c31311f77599520cecea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085582"
---
# <a name="tb_setbuttonwidth-message"></a><span data-ttu-id="9ed2f-104">TB de \_ mensagem SETBUTTONWIDTH</span><span class="sxs-lookup"><span data-stu-id="9ed2f-104">TB\_SETBUTTONWIDTH message</span></span>

<span data-ttu-id="9ed2f-105">Define as larguras mínima e máxima do botão no controle da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="9ed2f-105">Sets the minimum and maximum button widths in the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ed2f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ed2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed2f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ed2f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed2f-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9ed2f-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9ed2f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ed2f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed2f-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a largura mínima do botão, em pixels.</span><span class="sxs-lookup"><span data-stu-id="9ed2f-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum button width, in pixels.</span></span> <span data-ttu-id="9ed2f-111">Os botões da barra de ferramentas nunca serão mais estreitos que esse valor.</span><span class="sxs-lookup"><span data-stu-id="9ed2f-111">Toolbar buttons will never be narrower than this value.</span></span>

<span data-ttu-id="9ed2f-112">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a largura máxima do botão, em pixels.</span><span class="sxs-lookup"><span data-stu-id="9ed2f-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum button width, in pixels.</span></span> <span data-ttu-id="9ed2f-113">Se o texto do botão for muito grande, o controle o exibirá com pontos de reticências.</span><span class="sxs-lookup"><span data-stu-id="9ed2f-113">If button text is too wide, the control displays it with ellipsis points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed2f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ed2f-114">Return value</span></span>

<span data-ttu-id="9ed2f-115">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="9ed2f-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ed2f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ed2f-116">Remarks</span></span>

<span data-ttu-id="9ed2f-117">Use **TB \_ SETBUTTONWIDTH** para definir as larguras máximas e mínimas permitidas para botões antes de serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="9ed2f-117">Use **TB\_SETBUTTONWIDTH** to set the maximum and minimum allowed widths for buttons before they are added.</span></span> <span data-ttu-id="9ed2f-118">Use [**TB \_ SetButtons**](tb-setbuttonsize.md) para definir o tamanho real dos botões.</span><span class="sxs-lookup"><span data-stu-id="9ed2f-118">Use [**TB\_SETBUTTONSIZE**](tb-setbuttonsize.md) to set the actual size of buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ed2f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ed2f-119">Requirements</span></span>



| <span data-ttu-id="9ed2f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ed2f-120">Requirement</span></span> | <span data-ttu-id="9ed2f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9ed2f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed2f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ed2f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9ed2f-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ed2f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ed2f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ed2f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9ed2f-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ed2f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ed2f-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ed2f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ed2f-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ed2f-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

