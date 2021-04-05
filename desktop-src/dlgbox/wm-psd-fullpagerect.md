---
title: Mensagem de WM_PSD_FULLPAGERECT (Commdlg. h)
description: Notifica um procedimento de gancho PagePaintHook das coordenadas do retângulo da página de exemplo na caixa de diálogo Configurar página. A caixa de diálogo envia essa mensagem quando está prestes a desenhar o conteúdo da página de exemplo.
ms.assetid: 88ca1d60-3335-480a-b874-c6f248a3c23a
keywords:
- Caixas de diálogo de WM_PSD_FULLPAGERECT mensagem
topic_type:
- apiref
api_name:
- WM_PSD_FULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5265144822ba1f46c470b71169e0b27f2e1c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918824"
---
# <a name="wm_psd_fullpagerect-message"></a><span data-ttu-id="899a0-105">\_Mensagem FULLPAGERECT do PSD do WM \_</span><span class="sxs-lookup"><span data-stu-id="899a0-105">WM\_PSD\_FULLPAGERECT message</span></span>

<span data-ttu-id="899a0-106">Notifica um procedimento de gancho [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) das coordenadas do retângulo da página de exemplo na caixa de diálogo **Configurar página** .</span><span class="sxs-lookup"><span data-stu-id="899a0-106">Notifies a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure of the coordinates of the sample page rectangle in the **Page Setup** dialog box.</span></span> <span data-ttu-id="899a0-107">A caixa de diálogo envia essa mensagem quando está prestes a desenhar o conteúdo da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="899a0-107">The dialog box sends this message when it is about to draw the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_FULLPAGERECT     (WM_USER+1)
```



## <a name="parameters"></a><span data-ttu-id="899a0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="899a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="899a0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="899a0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="899a0-110">Um identificador para o contexto do dispositivo para a página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="899a0-110">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="899a0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="899a0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="899a0-112">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém as coordenadas, em pixels, da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="899a0-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the sample page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="899a0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="899a0-113">Return value</span></span>

<span data-ttu-id="899a0-114">Se o procedimento de gancho retornar **true**, a caixa de diálogo não enviará mais mensagens e não desenhará na página de exemplo até a próxima vez que o sistema precisar redesenhar a página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="899a0-114">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="899a0-115">Se o procedimento de gancho retornar **false**, a caixa de diálogo enviará as mensagens restantes da sequência de desenho.</span><span class="sxs-lookup"><span data-stu-id="899a0-115">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="899a0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="899a0-116">Remarks</span></span>

<span data-ttu-id="899a0-117">A caixa de diálogo **Configurar página** inclui uma imagem de uma página de exemplo que mostra como as seleções do usuário afetam a aparência da saída impressa.</span><span class="sxs-lookup"><span data-stu-id="899a0-117">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="899a0-118">Ao chamar a função [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , você pode fornecer um procedimento de gancho de [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar a aparência da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="899a0-118">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="899a0-119">Sempre que a caixa de diálogo estiver prestes a desenhar o conteúdo da página de exemplo, a caixa de diálogo enviará uma sequência de mensagens para o procedimento de gancho.</span><span class="sxs-lookup"><span data-stu-id="899a0-119">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="899a0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="899a0-120">Requirements</span></span>



| <span data-ttu-id="899a0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="899a0-121">Requirement</span></span> | <span data-ttu-id="899a0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="899a0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="899a0-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="899a0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="899a0-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="899a0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="899a0-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="899a0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="899a0-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="899a0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="899a0-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="899a0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="899a0-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="899a0-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="899a0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="899a0-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="899a0-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="899a0-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="899a0-131">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="899a0-131">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="899a0-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="899a0-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="899a0-133">**\_PAGESETUPDLG de PSD do WM \_**</span><span class="sxs-lookup"><span data-stu-id="899a0-133">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="899a0-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="899a0-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="899a0-135">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="899a0-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

