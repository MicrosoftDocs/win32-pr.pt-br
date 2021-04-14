---
title: Mensagem de WM_PSD_PAGESETUPDLG (Commdlg. h)
description: Notifica um procedimento de gancho PagePaintHook que a caixa de diálogo Configurar página está prestes a desenhar o conteúdo da página de exemplo. O procedimento de gancho pode usar essa mensagem para realizar tarefas de inicialização relacionadas ao desenho do conteúdo da página de exemplo.
ms.assetid: 0d95240b-7d77-4819-8e5c-cc25cd1b30f2
keywords:
- Caixas de diálogo de WM_PSD_PAGESETUPDLG mensagem
topic_type:
- apiref
api_name:
- WM_PSD_PAGESETUPDLG
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9706eff6d015dc31332d9f757c954081f0134b2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369892"
---
# <a name="wm_psd_pagesetupdlg-message"></a><span data-ttu-id="d3b40-105">\_Mensagem PAGESETUPDLG do PSD do WM \_</span><span class="sxs-lookup"><span data-stu-id="d3b40-105">WM\_PSD\_PAGESETUPDLG message</span></span>

<span data-ttu-id="d3b40-106">Notifica um procedimento de gancho [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) que a caixa de diálogo **Configurar página** está prestes a desenhar o conteúdo da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="d3b40-106">Notifies a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that the **Page Setup** dialog box is about to draw the contents of the sample page.</span></span> <span data-ttu-id="d3b40-107">O procedimento de gancho pode usar essa mensagem para realizar tarefas de inicialização relacionadas ao desenho do conteúdo da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="d3b40-107">The hook procedure can use this message to carry out initialization tasks related to drawing the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_PAGESETUPDLG     (WM_USER  )
```



## <a name="parameters"></a><span data-ttu-id="d3b40-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3b40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3b40-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3b40-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3b40-110">A palavra de ordem inferior Especifica um valor que indica o tamanho do papel.</span><span class="sxs-lookup"><span data-stu-id="d3b40-110">The low-order word specifies a value that indicates the paper size.</span></span> <span data-ttu-id="d3b40-111">Esse valor pode ser um dos valores **de \_ DMPAPER** listados na descrição da estrutura.</span><span class="sxs-lookup"><span data-stu-id="d3b40-111">This value can be one of the **DMPAPER\_** values listed in the description of the structure.</span></span> <span data-ttu-id="d3b40-112">A palavra de ordem superior especifica a orientação do papel ou do envelope e se a impressora é uma matriz de pontos ou HPPCL (linguagem de controle de impressora da Hewlett Packard).</span><span class="sxs-lookup"><span data-stu-id="d3b40-112">The high-order word specifies the orientation of the paper or envelope, and whether the printer is a dot matrix or HPPCL (Hewlett Packard Printer Control Language) device.</span></span> <span data-ttu-id="d3b40-113">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d3b40-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d3b40-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d3b40-114">Value</span></span>                                                                             | <span data-ttu-id="d3b40-115">Significado</span><span class="sxs-lookup"><span data-stu-id="d3b40-115">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="d3b40-116"><dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="d3b40-116"><dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="d3b40-117">Papel no modo paisagem (matriz de pontos)</span><span class="sxs-lookup"><span data-stu-id="d3b40-117">Paper in landscape mode (dot matrix)</span></span><br/>    |
| <dl> <span data-ttu-id="d3b40-118"><dt>0x0003</dt></span><span class="sxs-lookup"><span data-stu-id="d3b40-118"><dt>0x0003</dt></span></span> </dl> | <span data-ttu-id="d3b40-119">Papel no modo paisagem (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="d3b40-119">Paper in landscape mode (HPPCL)</span></span><br/>         |
| <dl> <span data-ttu-id="d3b40-120"><dt>0x0005</dt></span><span class="sxs-lookup"><span data-stu-id="d3b40-120"><dt>0x0005</dt></span></span> </dl> | <span data-ttu-id="d3b40-121">Papel no modo retrato (matriz de pontos)</span><span class="sxs-lookup"><span data-stu-id="d3b40-121">Paper in portrait mode (dot matrix)</span></span><br/>     |
| <dl> <span data-ttu-id="d3b40-122"><dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="d3b40-122"><dt>0x0007</dt></span></span> </dl> | <span data-ttu-id="d3b40-123">Papel no modo retrato (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="d3b40-123">Paper in portrait mode (HPPCL)</span></span><br/>          |
| <dl> <span data-ttu-id="d3b40-124"><dt>0x000b</dt></span><span class="sxs-lookup"><span data-stu-id="d3b40-124"><dt>0x000b</dt></span></span> </dl> | <span data-ttu-id="d3b40-125">Envelope no modo paisagem (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="d3b40-125">Envelope in landscape mode (HPPCL)</span></span><br/>      |
| <dl> <span data-ttu-id="d3b40-126"><dt>0x000d</dt></span><span class="sxs-lookup"><span data-stu-id="d3b40-126"><dt>0x000d</dt></span></span> </dl> | <span data-ttu-id="d3b40-127">Envelope no modo retrato (matriz de pontos)</span><span class="sxs-lookup"><span data-stu-id="d3b40-127">Envelope in portrait mode (dot matrix)</span></span><br/>  |
| <dl> <span data-ttu-id="d3b40-128"><dt>0x0019</dt></span><span class="sxs-lookup"><span data-stu-id="d3b40-128"><dt>0x0019</dt></span></span> </dl> | <span data-ttu-id="d3b40-129">Envelope no modo paisagem (matriz de pontos)</span><span class="sxs-lookup"><span data-stu-id="d3b40-129">Envelope in landscape mode (dot matrix)</span></span><br/> |
| <dl> <span data-ttu-id="d3b40-130"><dt>0x001F</dt></span><span class="sxs-lookup"><span data-stu-id="d3b40-130"><dt>0x001f</dt></span></span> </dl> | <span data-ttu-id="d3b40-131">Envelope no modo retrato (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="d3b40-131">Envelope in portrait mode (HPPCL)</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="d3b40-132">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3b40-132">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3b40-133">Um ponteiro para uma estrutura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) que contém informações usadas para inicializar a caixa de diálogo **Configurar página** .</span><span class="sxs-lookup"><span data-stu-id="d3b40-133">A pointer to a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure that contains information used to initialize the **Page Setup** dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3b40-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3b40-134">Return value</span></span>

<span data-ttu-id="d3b40-135">Se o procedimento de gancho retornar **true**, a caixa de diálogo não enviará mais mensagens e não desenhará na página de exemplo até a próxima vez que o sistema precisar redesenhar a página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="d3b40-135">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="d3b40-136">Se o procedimento de gancho retornar **false**, a caixa de diálogo enviará as mensagens restantes da sequência de desenho.</span><span class="sxs-lookup"><span data-stu-id="d3b40-136">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3b40-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3b40-137">Remarks</span></span>

<span data-ttu-id="d3b40-138">A caixa de diálogo **Configurar página** inclui uma imagem de uma página de exemplo que mostra como as seleções do usuário afetam a aparência da saída impressa.</span><span class="sxs-lookup"><span data-stu-id="d3b40-138">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="d3b40-139">Ao chamar a função [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , você pode fornecer um procedimento de gancho de [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar a aparência da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="d3b40-139">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="d3b40-140">Sempre que a caixa de diálogo estiver prestes a desenhar o conteúdo da página de exemplo, a caixa de diálogo enviará uma sequência de mensagens para o procedimento de gancho.</span><span class="sxs-lookup"><span data-stu-id="d3b40-140">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

<span data-ttu-id="d3b40-141">As três primeiras mensagens de uma sequência de desenho (**WM \_ PSD \_ PAGESETUPDLG**, [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)ou [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)) fornecem informações que o procedimento de gancho pode usar para desenhar o conteúdo da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="d3b40-141">The first three messages of a drawing sequence (**WM\_PSD\_PAGESETUPDLG**, [**WM\_PSD\_FULLPAGERECT**](wm-psd-fullpagerect.md), or [**WM\_PSD\_MINMARGINRECT**](wm-psd-minmarginrect.md)) provide information that the hook procedure can use to draw the contents of the sample page.</span></span> <span data-ttu-id="d3b40-142">As mensagens restantes ([**WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md), [**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notificam o procedimento de gancho que a caixa de diálogo está prestes a desenhar uma parte específica da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="d3b40-142">The remaining messages ([**WM\_PSD\_MARGINRECT**](wm-psd-marginrect.md), [**WM\_PSD\_GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM\_PSD\_ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM\_PSD\_YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notify the hook procedure that the dialog box is about to draw a specific portion of the sample page.</span></span> <span data-ttu-id="d3b40-143">Isso permite que o procedimento de conexão desenhe partes da página de exemplo de forma seletiva.</span><span class="sxs-lookup"><span data-stu-id="d3b40-143">This allows the hook procedure to selectively draw portions of the sample page.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b40-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3b40-144">Requirements</span></span>



| <span data-ttu-id="d3b40-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3b40-145">Requirement</span></span> | <span data-ttu-id="d3b40-146">Valor</span><span class="sxs-lookup"><span data-stu-id="d3b40-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b40-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3b40-147">Minimum supported client</span></span><br/> | <span data-ttu-id="d3b40-148">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d3b40-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d3b40-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3b40-149">Minimum supported server</span></span><br/> | <span data-ttu-id="d3b40-150">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d3b40-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d3b40-151">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d3b40-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3b40-152"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3b40-152"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3b40-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3b40-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="d3b40-154">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d3b40-154">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d3b40-155">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="d3b40-155">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="d3b40-156">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3b40-156">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d3b40-157">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="d3b40-157">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[<span data-ttu-id="d3b40-158">**\_ENVSTAMPRECT de PSD do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d3b40-158">**WM\_PSD\_ENVSTAMPRECT**</span></span>](wm-psd-envstamprect.md)
</dt> <dt>

[<span data-ttu-id="d3b40-159">**\_FULLPAGERECT de PSD do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d3b40-159">**WM\_PSD\_FULLPAGERECT**</span></span>](wm-psd-fullpagerect.md)
</dt> <dt>

[<span data-ttu-id="d3b40-160">**\_GREEKTEXTRECT de PSD do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d3b40-160">**WM\_PSD\_GREEKTEXTRECT**</span></span>](wm-psd-greektextrect.md)
</dt> <dt>

[<span data-ttu-id="d3b40-161">**\_MARGINRECT de PSD do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d3b40-161">**WM\_PSD\_MARGINRECT**</span></span>](wm-psd-marginrect.md)
</dt> <dt>

[<span data-ttu-id="d3b40-162">**\_MINMARGINRECT de PSD do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d3b40-162">**WM\_PSD\_MINMARGINRECT**</span></span>](wm-psd-minmarginrect.md)
</dt> <dt>

[<span data-ttu-id="d3b40-163">**\_YAFULLPAGERECT de PSD do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d3b40-163">**WM\_PSD\_YAFULLPAGERECT**</span></span>](wm-psd-yafullpagerect.md)
</dt> <dt>

<span data-ttu-id="d3b40-164">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="d3b40-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d3b40-165">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="d3b40-165">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

