---
title: Mensagem de TB_ADDBUTTONS (commctrl. h)
description: Adiciona um ou mais botões a uma barra de ferramentas.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- Controles de TB_ADDBUTTONS de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_ADDBUTTONS
- TB_ADDBUTTONSA
- TB_ADDBUTTONSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f954e9a133f78a9415358d1c7f61d68008cd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919235"
---
# <a name="tb_addbuttons-message"></a><span data-ttu-id="f9dd6-104">\_Mensagem de HIPERbotãos TB</span><span class="sxs-lookup"><span data-stu-id="f9dd6-104">TB\_ADDBUTTONS message</span></span>

<span data-ttu-id="f9dd6-105">Adiciona um ou mais botões a uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="f9dd6-105">Adds one or more buttons to a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9dd6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9dd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9dd6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9dd6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9dd6-108">Número de botões a serem adicionados.</span><span class="sxs-lookup"><span data-stu-id="f9dd6-108">Number of buttons to add.</span></span>

</dd> <dt>

<span data-ttu-id="f9dd6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9dd6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9dd6-110">Ponteiro para uma matriz de estruturas [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que contêm informações sobre os botões a serem adicionados.</span><span class="sxs-lookup"><span data-stu-id="f9dd6-110">Pointer to an array of [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structures that contain information about the buttons to add.</span></span> <span data-ttu-id="f9dd6-111">Deve haver o mesmo número de elementos na matriz como botões especificados por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="f9dd6-111">There must be the same number of elements in the array as buttons specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9dd6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9dd6-112">Return value</span></span>

<span data-ttu-id="f9dd6-113">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f9dd6-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9dd6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9dd6-114">Remarks</span></span>

<span data-ttu-id="f9dd6-115">Se a barra de ferramentas foi criada usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , você deve enviar a mensagem [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) para a barra de ferramentas antes de enviar os **\_ botões addbotãors**.</span><span class="sxs-lookup"><span data-stu-id="f9dd6-115">If the toolbar was created using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, you must send the [**TB\_BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) message to the toolbar before sending **TB\_ADDBUTTONS**.</span></span>

<span data-ttu-id="f9dd6-116">Consulte [**TB \_ SetImageList**](tb-setimagelist.md) para obter uma discussão sobre como atribuir bitmaps a botões da barra de ferramentas de uma ou mais listas de imagens.</span><span class="sxs-lookup"><span data-stu-id="f9dd6-116">See [**TB\_SETIMAGELIST**](tb-setimagelist.md) for a discussion of how to assign bitmaps to toolbar buttons from one or more image lists.</span></span>

## <a name="examples"></a><span data-ttu-id="f9dd6-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9dd6-117">Examples</span></span>

<span data-ttu-id="f9dd6-118">O código de exemplo a seguir adiciona três botões a uma barra de ferramentas, usando o bitmap do sistema padrão para botões de exibição.</span><span class="sxs-lookup"><span data-stu-id="f9dd6-118">The following example code adds three buttons to a toolbar, using the standard system bitmap for view buttons.</span></span> <span data-ttu-id="f9dd6-119">A mensagem do [**\_ AddBitmap TB**](tb-addbitmap.md) retorna o índice da primeira imagem de botão na lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="f9dd6-119">The [**TB\_ADDBITMAP**](tb-addbitmap.md) message returns the index of the first button image within the image list.</span></span> <span data-ttu-id="f9dd6-120">As imagens individuais são identificadas por seus deslocamentos a partir desse valor.</span><span class="sxs-lookup"><span data-stu-id="f9dd6-120">Individual images are identified by their offsets from that value.</span></span>


```C++
TBADDBITMAP tbAddBitmap;
tbAddBitmap.hInst = HINST_COMMCTRL;
tbAddBitmap.nID = IDB_VIEW_SMALL_COLOR;

// There are 12 items in IDB_VIEW_SMALL_COLOR.  However, because this is a standard
// system-defined bitmap, the wParam (nButtons) is ignored.
//
// hWndToolbar is the handle of the toolbar window.
//
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was created
// by using CreateWindowEx.
//
int stdidx = SendMessage(hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tbAddBitmap);

// Define the buttons. 
// IDM_SETLARGEICONVIEW and so on are application-defined command IDs.

const int numButtons = 3;
TBBUTTON tbButtonsAdd[numButtons] = 
{
    {stdidx + VIEW_LARGEICONS, IDM_SETLARGEICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_SMALLICONS, IDM_SETSMALLICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_DETAILS, IDM_SETDETAILSVIEW, TBSTATE_ENABLED, BTNS_BUTTON}
}; 

// Add the view buttons.
SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)tbButtonsAdd);
```



## <a name="requirements"></a><span data-ttu-id="f9dd6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9dd6-121">Requirements</span></span>



| <span data-ttu-id="f9dd6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9dd6-122">Requirement</span></span> | <span data-ttu-id="f9dd6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f9dd6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9dd6-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9dd6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f9dd6-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9dd6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9dd6-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9dd6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f9dd6-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f9dd6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9dd6-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9dd6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9dd6-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9dd6-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f9dd6-130">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f9dd6-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f9dd6-131">**TB \_ ADDBUTTONSW** (Unicode) e **TB \_ AddButtons** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f9dd6-131">**TB\_ADDBUTTONSW** (Unicode) and **TB\_ADDBUTTONSA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f9dd6-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9dd6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9dd6-133">**Valores de índice da imagem do botão padrão da barra de ferramentas**</span><span class="sxs-lookup"><span data-stu-id="f9dd6-133">**Toolbar Standard Button Image Index Values**</span></span>](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

