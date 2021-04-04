---
title: Mensagem de TTM_ADJUSTRECT (commctrl. h)
description: Calcula o retângulo de exibição de texto de um controle de dica de ferramenta de seu retângulo de janela ou o retângulo da janela de dica de ferramenta necessário para exibir um retângulo de exibição de texto especificado.
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- Controles de TTM_ADJUSTRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af89374161d5e3f9d9ab6affc2b3b498a39cbf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918473"
---
# <a name="ttm_adjustrect-message"></a><span data-ttu-id="44865-104">\_Mensagem TTM ADJUSTRECT</span><span class="sxs-lookup"><span data-stu-id="44865-104">TTM\_ADJUSTRECT message</span></span>

<span data-ttu-id="44865-105">Calcula o retângulo de exibição de texto de um controle de dica de ferramenta de seu retângulo de janela ou o retângulo da janela de dica de ferramenta necessário para exibir um retângulo de exibição de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="44865-105">Calculates a tooltip control's text display rectangle from its window rectangle, or the tooltip window rectangle needed to display a specified text display rectangle.</span></span>

## <a name="parameters"></a><span data-ttu-id="44865-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44865-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44865-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44865-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44865-108">Valor que especifica qual operação deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="44865-108">Value that specifies which operation to perform.</span></span> <span data-ttu-id="44865-109">Se for **true**, *lParam* será usado para especificar um retângulo de exibição de texto e receberá o retângulo de janela correspondente.</span><span class="sxs-lookup"><span data-stu-id="44865-109">If **TRUE**, *lParam* is used to specify a text-display rectangle and it receives the corresponding window rectangle.</span></span> <span data-ttu-id="44865-110">Se for **false**, *lParam* será usado para especificar um retângulo de janela e receberá o retângulo de exibição de texto correspondente.</span><span class="sxs-lookup"><span data-stu-id="44865-110">If **FALSE**, *lParam* is used to specify a window rectangle and it receives the corresponding text display rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="44865-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44865-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44865-112">Estrutura **Rect** para manter um retângulo de janela de dica de ferramenta ou um retângulo de exibição de texto.</span><span class="sxs-lookup"><span data-stu-id="44865-112">**RECT** structure to hold either a tooltip window rectangle or a text display rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44865-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44865-113">Return value</span></span>

<span data-ttu-id="44865-114">Retornará um valor diferente de zero se o retângulo for ajustado com êxito e retornará zero se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="44865-114">Returns a nonzero value if the rectangle is successfully adjusted, and returns zero if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="44865-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="44865-115">Remarks</span></span>

<span data-ttu-id="44865-116">Essa mensagem é particularmente útil quando você deseja usar um controle ToolTip para exibir o texto completo de uma cadeia de caracteres que geralmente é truncada.</span><span class="sxs-lookup"><span data-stu-id="44865-116">This message is particularly useful when you want to use a tooltip control to display the full text of a string that is usually truncated.</span></span> <span data-ttu-id="44865-117">Normalmente, ele é usado com controles ListView e TreeView.</span><span class="sxs-lookup"><span data-stu-id="44865-117">It is commonly used with listview and treeview controls.</span></span> <span data-ttu-id="44865-118">Normalmente, você envia essa mensagem em resposta a um código de notificação [TTN \_ show](ttn-show.md) para que você possa posicionar o controle ToolTip corretamente.</span><span class="sxs-lookup"><span data-stu-id="44865-118">You typically send this message in response to a [TTN\_SHOW](ttn-show.md) notification code so that you can position the tooltip control properly.</span></span>

<span data-ttu-id="44865-119">O retângulo da janela de dica de ferramenta é um pouco maior do que o retângulo de exibição de texto que limita a cadeia de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="44865-119">The tooltip window rectangle is somewhat larger than the text display rectangle that bounds the tooltip string.</span></span> <span data-ttu-id="44865-120">A origem da janela também é deslocada para cima e para a esquerda da origem do retângulo de exibição de texto.</span><span class="sxs-lookup"><span data-stu-id="44865-120">The window origin is also offset up and to the left from the origin of the text display rectangle.</span></span> <span data-ttu-id="44865-121">Para posicionar o retângulo de exibição de texto, você deve calcular o retângulo de janela correspondente e usar esse retângulo para posicionar a dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="44865-121">To position the text display rectangle, you must calculate the corresponding window rectangle and use that rectangle to position the tooltip.</span></span> <span data-ttu-id="44865-122">**TTM \_ O ADJUSTRECT** lida com esse cálculo para você.</span><span class="sxs-lookup"><span data-stu-id="44865-122">**TTM\_ADJUSTRECT** handles this calculation for you.</span></span>

<span data-ttu-id="44865-123">Se você definir *wParam* como **true**, **TTM \_ ADJUSTRECT** usará o tamanho e a posição do retângulo de exibição de texto de dica de ferramenta desejado e retornará o tamanho e a posição da janela de dica de ferramenta necessária para exibir o texto na posição especificada.</span><span class="sxs-lookup"><span data-stu-id="44865-123">If you set *wParam* to **TRUE**, **TTM\_ADJUSTRECT** takes the size and position of the desired tooltip text display rectangle, and passes back the size and position of the tooltip window needed to display the text in the specified position.</span></span> <span data-ttu-id="44865-124">Se você definir *wParam* como **false**, poderá especificar um retângulo de janela de dica de ferramenta e **TTM \_ ADJUSTRECT** retornará o tamanho e a posição de seu retângulo de texto.</span><span class="sxs-lookup"><span data-stu-id="44865-124">If you set *wParam* to **FALSE**, you can specify a tooltip window rectangle and **TTM\_ADJUSTRECT** will return the size and position of its text rectangle.</span></span>

<span data-ttu-id="44865-125">O fragmento de código a seguir ilustra o uso da mensagem **TTM \_ ADJUSTRECT** para posicionar um controle ToolTip para exibir o texto completo da cadeia de caracteres de um controle no lugar de uma cadeia de caracteres truncada.</span><span class="sxs-lookup"><span data-stu-id="44865-125">The following code fragment illustrates the use of the **TTM\_ADJUSTRECT** message to position a tooltip control to display the full text of a control's string in place of a truncated string.</span></span> <span data-ttu-id="44865-126">A função **GetMyItemRect** definida pelo aplicativo retorna o retângulo de texto que será necessário para exibir o texto da dica de ferramenta diretamente sobre a cadeia de caracteres truncada.</span><span class="sxs-lookup"><span data-stu-id="44865-126">The application-defined **GetMyItemRect** function returns the text rectangle that will be needed to display the tooltip text directly over the truncated string.</span></span> <span data-ttu-id="44865-127">Os detalhes de como essa função é implementada dependerão do controle específico.</span><span class="sxs-lookup"><span data-stu-id="44865-127">The details of how this function is implemented will depend on the particular control.</span></span> <span data-ttu-id="44865-128">**TTM \_ ADJUSTRECT** é usado para enviar este retângulo de texto para o controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="44865-128">**TTM\_ADJUSTRECT** is used to send this text rectangle to the tooltip control.</span></span> <span data-ttu-id="44865-129">Ele retorna um retângulo de janela dimensionado e posicionado adequadamente que é usado para posicionar a janela de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="44865-129">It returns an appropriately sized and positioned window rectangle that is then used to position the tooltip window.</span></span>


```
case TTN_SHOW:

if (MyStringIsTruncated) {
    RECT rc;
    
    GetMyItemRect(&rc);
    SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
    SetWindowPos(hwndToolTip,
                 NULL,
                 rc.left, rc.top,
                 0, 0,
                 SWP_NOSIZE|SWP_NOZORDER|SWP_NOACTIVATE);
} 
```



## <a name="requirements"></a><span data-ttu-id="44865-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44865-130">Requirements</span></span>



| <span data-ttu-id="44865-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="44865-131">Requirement</span></span> | <span data-ttu-id="44865-132">Valor</span><span class="sxs-lookup"><span data-stu-id="44865-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44865-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44865-133">Minimum supported client</span></span><br/> | <span data-ttu-id="44865-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44865-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44865-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44865-135">Minimum supported server</span></span><br/> | <span data-ttu-id="44865-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="44865-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44865-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44865-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="44865-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="44865-138"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





