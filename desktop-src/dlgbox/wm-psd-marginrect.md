---
title: Mensagem de WM_PSD_MARGINRECT (Commdlg. h)
description: Notifica o procedimento de gancho de uma caixa de diálogo de configuração de página, PagePaintHook, que a caixa de diálogo está prestes a desenhar o retângulo de margem da página de exemplo.
ms.assetid: 81c057ab-6faf-4dd8-8b0c-34a2753e572c
keywords:
- Caixas de diálogo de WM_PSD_MARGINRECT mensagem
topic_type:
- apiref
api_name:
- WM_PSD_MARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718cfbe16db53378544d9fca0ab44ade23ffb3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455563"
---
# <a name="wm_psd_marginrect-message"></a><span data-ttu-id="71355-104">\_Mensagem MARGINRECT do PSD do WM \_</span><span class="sxs-lookup"><span data-stu-id="71355-104">WM\_PSD\_MARGINRECT message</span></span>

<span data-ttu-id="71355-105">Notifica o procedimento de gancho de uma caixa de diálogo de **configuração de página** , [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), que a caixa de diálogo está prestes a desenhar o retângulo de margem da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="71355-105">Notifies the hook procedure of a **Page Setup** dialog box, [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the margin rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_MARGINRECT       (WM_USER+3)
```



## <a name="parameters"></a><span data-ttu-id="71355-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71355-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71355-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71355-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71355-108">Um identificador para o contexto do dispositivo para a página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="71355-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="71355-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71355-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71355-110">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém as coordenadas, em pixels, do retângulo da margem.</span><span class="sxs-lookup"><span data-stu-id="71355-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the margin rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71355-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71355-111">Return value</span></span>

<span data-ttu-id="71355-112">Se o procedimento de gancho retornar **true**, a caixa de diálogo não desenhará o retângulo de margem na página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="71355-112">If the hook procedure returns **TRUE**, the dialog box does not draw the margin rectangle in the sample page.</span></span>

<span data-ttu-id="71355-113">Se o procedimento de gancho retornar **false**, a caixa de diálogo desenhará o retângulo de margem na página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="71355-113">If the hook procedure returns **FALSE**, the dialog box draws the margin rectangle in the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="71355-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="71355-114">Remarks</span></span>

<span data-ttu-id="71355-115">A caixa de diálogo **Configurar página** inclui uma imagem de uma página de exemplo que mostra como as seleções do usuário afetam a aparência da saída impressa.</span><span class="sxs-lookup"><span data-stu-id="71355-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="71355-116">Ao chamar a função [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , você pode fornecer um procedimento de gancho de [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar a aparência da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="71355-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="71355-117">Sempre que a caixa de diálogo estiver prestes a desenhar o conteúdo da página de exemplo, a caixa de diálogo enviará uma sequência de mensagens para o procedimento de gancho.</span><span class="sxs-lookup"><span data-stu-id="71355-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="71355-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71355-118">Requirements</span></span>



| <span data-ttu-id="71355-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="71355-119">Requirement</span></span> | <span data-ttu-id="71355-120">Valor</span><span class="sxs-lookup"><span data-stu-id="71355-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71355-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71355-121">Minimum supported client</span></span><br/> | <span data-ttu-id="71355-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="71355-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="71355-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71355-123">Minimum supported server</span></span><br/> | <span data-ttu-id="71355-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="71355-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="71355-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="71355-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="71355-126"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71355-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71355-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="71355-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="71355-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="71355-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="71355-129">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="71355-129">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="71355-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="71355-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="71355-131">**\_PAGESETUPDLG de PSD do WM \_**</span><span class="sxs-lookup"><span data-stu-id="71355-131">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="71355-132">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="71355-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="71355-133">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="71355-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

