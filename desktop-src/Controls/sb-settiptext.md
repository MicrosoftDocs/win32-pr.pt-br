---
title: Mensagem de SB_SETTIPTEXT (commctrl. h)
description: Define o texto da dica de ferramenta para uma parte em uma barra de status. A barra de status deve ter sido criada com o \_ estilo de dicas de ferramenta SBT para habilitar dicas de ferramenta.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- Controles de SB_SETTIPTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SETTIPTEXT
- SB_SETTIPTEXTA
- SB_SETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d5ddb3f4fdfe18525e2b444438295f8a926180
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455606"
---
# <a name="sb_settiptext-message"></a><span data-ttu-id="be270-105">\_Mensagem de SETTIPTEXT SB</span><span class="sxs-lookup"><span data-stu-id="be270-105">SB\_SETTIPTEXT message</span></span>

<span data-ttu-id="be270-106">Define o texto da dica de ferramenta para uma parte em uma barra de status.</span><span class="sxs-lookup"><span data-stu-id="be270-106">Sets the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="be270-107">A barra de status deve ter sido criada com o estilo de [**\_ dicas de ferramenta SBT**](status-bar-styles.md) para habilitar dicas de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="be270-107">The status bar must have been created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="be270-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be270-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be270-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be270-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be270-110">O índice de base zero da parte que receberá o texto da dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="be270-110">Zero-based index of the part that will receive the tooltip text.</span></span>

</dd> <dt>

<span data-ttu-id="be270-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be270-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be270-112">Ponteiro para um buffer de caracteres que contém o novo texto de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="be270-112">Pointer to a character buffer that contains the new tooltip text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be270-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be270-113">Return value</span></span>

<span data-ttu-id="be270-114">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="be270-114">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="be270-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="be270-115">Remarks</span></span>

<span data-ttu-id="be270-116">Esse texto de dica de ferramenta é exibido em duas situações:</span><span class="sxs-lookup"><span data-stu-id="be270-116">This tooltip text is displayed in two situations:</span></span>

-   <span data-ttu-id="be270-117">Quando o painel correspondente na barra de status contém apenas um ícone.</span><span class="sxs-lookup"><span data-stu-id="be270-117">When the corresponding pane in the status bar contains only an icon.</span></span>
-   <span data-ttu-id="be270-118">Quando o painel correspondente na barra de status contém texto truncado devido ao tamanho do painel.</span><span class="sxs-lookup"><span data-stu-id="be270-118">When the corresponding pane in the status bar contains text that is truncated due to the size of the pane.</span></span>

## <a name="requirements"></a><span data-ttu-id="be270-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be270-119">Requirements</span></span>



| <span data-ttu-id="be270-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="be270-120">Requirement</span></span> | <span data-ttu-id="be270-121">Valor</span><span class="sxs-lookup"><span data-stu-id="be270-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be270-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be270-122">Minimum supported client</span></span><br/> | <span data-ttu-id="be270-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be270-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be270-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be270-124">Minimum supported server</span></span><br/> | <span data-ttu-id="be270-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be270-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be270-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be270-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="be270-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="be270-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="be270-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="be270-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="be270-129">**SB \_ SETTIPTEXTW** (Unicode) e **SB \_ SETTIPTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="be270-129">**SB\_SETTIPTEXTW** (Unicode) and **SB\_SETTIPTEXTA** (ANSI)</span></span><br/>               |



 

 





