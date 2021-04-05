---
title: Mensagem de WM_PSD_YAFULLPAGERECT (Commdlg. h)
description: Notifica o procedimento de gancho de uma caixa de diálogo de configuração de página, PagePaintHook, que a caixa de diálogo está prestes a desenhar a parte de endereço de retorno de uma página de exemplo de envelope.
ms.assetid: 1f6aea69-a1bd-41ea-b508-44b4f5c38757
keywords:
- Caixas de diálogo de WM_PSD_YAFULLPAGERECT mensagem
topic_type:
- apiref
api_name:
- WM_PSD_YAFULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb325a8d408724cd865f5f9b70cfe7369fe6ffe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009721"
---
# <a name="wm_psd_yafullpagerect-message"></a><span data-ttu-id="cce32-104">\_Mensagem YAFULLPAGERECT do PSD do WM \_</span><span class="sxs-lookup"><span data-stu-id="cce32-104">WM\_PSD\_YAFULLPAGERECT message</span></span>

<span data-ttu-id="cce32-105">Notifica o procedimento de gancho de uma caixa de diálogo de **configuração de página** , [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), que a caixa de diálogo está prestes a desenhar a parte de endereço de retorno de uma página de exemplo de envelope.</span><span class="sxs-lookup"><span data-stu-id="cce32-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the return address portion of an envelope sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_YAFULLPAGERECT   (WM_USER+6)
```



## <a name="parameters"></a><span data-ttu-id="cce32-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cce32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cce32-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cce32-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cce32-108">Um identificador para o contexto do dispositivo para a página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="cce32-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="cce32-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cce32-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cce32-110">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém as coordenadas, em pixels, da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="cce32-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the sample page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cce32-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cce32-111">Return value</span></span>

<span data-ttu-id="cce32-112">Se o procedimento de gancho retornar **true**, a caixa de diálogo não desenhará a parte de endereço de retorno de uma página de exemplo de envelope.</span><span class="sxs-lookup"><span data-stu-id="cce32-112">If the hook procedure returns **TRUE**, the dialog box does not draw the return address portion of an envelope sample page.</span></span>

<span data-ttu-id="cce32-113">Se o procedimento de gancho retornar **false**, a caixa de diálogo desenhará a parte de endereço de retorno de uma página de exemplo de envelope.</span><span class="sxs-lookup"><span data-stu-id="cce32-113">If the hook procedure returns **FALSE**, the dialog box draws the return address portion of an envelope sample page.</span></span>

<span data-ttu-id="cce32-114">Se o tipo de papel não for um envelope, o valor de retorno não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="cce32-114">If the paper type is not an envelope, the return value has no effect.</span></span>

## <a name="remarks"></a><span data-ttu-id="cce32-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cce32-115">Remarks</span></span>

<span data-ttu-id="cce32-116">A caixa de diálogo **Configurar página** inclui uma imagem de uma página de exemplo que mostra como as seleções do usuário afetam a aparência da saída impressa.</span><span class="sxs-lookup"><span data-stu-id="cce32-116">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="cce32-117">Ao chamar a função [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , você pode fornecer um procedimento de gancho de [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar a aparência da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="cce32-117">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="cce32-118">Sempre que a caixa de diálogo estiver prestes a desenhar o conteúdo da página de exemplo, a caixa de diálogo enviará uma sequência de mensagens para o procedimento de gancho.</span><span class="sxs-lookup"><span data-stu-id="cce32-118">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="cce32-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cce32-119">Requirements</span></span>



| <span data-ttu-id="cce32-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cce32-120">Requirement</span></span> | <span data-ttu-id="cce32-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cce32-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cce32-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cce32-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cce32-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cce32-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cce32-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cce32-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cce32-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cce32-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cce32-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cce32-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cce32-127"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cce32-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cce32-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="cce32-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="cce32-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="cce32-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cce32-130">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="cce32-130">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="cce32-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cce32-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cce32-132">**\_PAGESETUPDLG de PSD do WM \_**</span><span class="sxs-lookup"><span data-stu-id="cce32-132">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="cce32-133">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="cce32-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cce32-134">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="cce32-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

