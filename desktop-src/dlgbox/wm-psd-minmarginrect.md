---
title: Mensagem de WM_PSD_MINMARGINRECT (Commdlg. h)
description: Notifica um procedimento de gancho PagePaintHook das coordenadas do retângulo de margem na página de exemplo. Uma caixa de diálogo Configurar página envia essa mensagem quando está prestes a desenhar o conteúdo da página de exemplo.
ms.assetid: 14977b52-7a6f-4c55-956a-716398a71613
keywords:
- Caixas de diálogo de WM_PSD_MINMARGINRECT mensagem
topic_type:
- apiref
api_name:
- WM_PSD_MINMARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ec7271026ba7557fcbe3fe17cd890d62eadbca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499561"
---
# <a name="wm_psd_minmarginrect-message"></a><span data-ttu-id="52190-105">\_Mensagem MINMARGINRECT do PSD do WM \_</span><span class="sxs-lookup"><span data-stu-id="52190-105">WM\_PSD\_MINMARGINRECT message</span></span>

<span data-ttu-id="52190-106">Notifica um procedimento de gancho [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) das coordenadas do retângulo de margem na página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="52190-106">Notifies a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure of the coordinates of the margin rectangle in the sample page.</span></span> <span data-ttu-id="52190-107">Uma caixa de diálogo **Configurar página** envia essa mensagem quando está prestes a desenhar o conteúdo da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="52190-107">A **Page Setup** dialog box sends this message when it is about to draw the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_MINMARGINRECT    (WM_USER+2)
```



## <a name="parameters"></a><span data-ttu-id="52190-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52190-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52190-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52190-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52190-110">Um identificador para o contexto do dispositivo para a página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="52190-110">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="52190-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52190-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52190-112">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém as coordenadas, em pixels, do retângulo de margem mínimo.</span><span class="sxs-lookup"><span data-stu-id="52190-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the minimum margin rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52190-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52190-113">Return value</span></span>

<span data-ttu-id="52190-114">Se o procedimento de gancho retornar **true**, a caixa de diálogo não enviará mais mensagens e não desenhará na página de exemplo até a próxima vez que o sistema precisar redesenhar a página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="52190-114">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="52190-115">Se o procedimento de gancho retornar **false**, a caixa de diálogo enviará as mensagens restantes da sequência de desenho.</span><span class="sxs-lookup"><span data-stu-id="52190-115">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="52190-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="52190-116">Remarks</span></span>

<span data-ttu-id="52190-117">A caixa de diálogo **Configurar página** inclui uma imagem de uma página de exemplo que mostra como as seleções do usuário afetam a aparência da saída impressa.</span><span class="sxs-lookup"><span data-stu-id="52190-117">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="52190-118">Ao chamar a função [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , você pode fornecer um procedimento de gancho de [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar a aparência da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="52190-118">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="52190-119">Sempre que a caixa de diálogo estiver prestes a desenhar o conteúdo da página de exemplo, a caixa de diálogo enviará uma sequência de mensagens para o procedimento de gancho.</span><span class="sxs-lookup"><span data-stu-id="52190-119">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="52190-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52190-120">Requirements</span></span>



| <span data-ttu-id="52190-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="52190-121">Requirement</span></span> | <span data-ttu-id="52190-122">Valor</span><span class="sxs-lookup"><span data-stu-id="52190-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52190-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52190-123">Minimum supported client</span></span><br/> | <span data-ttu-id="52190-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52190-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="52190-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52190-125">Minimum supported server</span></span><br/> | <span data-ttu-id="52190-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52190-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="52190-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="52190-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="52190-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52190-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52190-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="52190-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="52190-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="52190-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="52190-131">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="52190-131">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="52190-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="52190-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="52190-133">**\_PAGESETUPDLG de PSD do WM \_**</span><span class="sxs-lookup"><span data-stu-id="52190-133">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="52190-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="52190-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="52190-135">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="52190-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

