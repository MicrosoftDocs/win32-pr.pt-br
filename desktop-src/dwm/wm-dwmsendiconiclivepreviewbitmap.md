---
title: Mensagem de WM_DWMSENDICONICLIVEPREVIEWBITMAP (dwmapi. h)
description: Instrui uma janela para fornecer um bitmap estático a ser usado como uma visualização dinâmica (também conhecida como visualização de inspeção) dessa janela.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- Mensagem de WM_DWMSENDICONICLIVEPREVIEWBITMAP Gerenciador de Janelas da Área de Trabalho
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21f73076ab313da66171bc8265f7f4e7d068f93e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455241"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a><span data-ttu-id="66c87-104">Mensagem do WM \_ DWMSENDICONICLIVEPREVIEWBITMAP</span><span class="sxs-lookup"><span data-stu-id="66c87-104">WM\_DWMSENDICONICLIVEPREVIEWBITMAP message</span></span>

<span data-ttu-id="66c87-105">Instrui uma janela para fornecer um bitmap estático a ser usado como uma *Visualização dinâmica* (também conhecida como *visualização de inspeção*) dessa janela.</span><span class="sxs-lookup"><span data-stu-id="66c87-105">Instructs a window to provide a static bitmap to use as a *live preview* (also known as a *Peek preview*) of that window.</span></span>

## <a name="parameters"></a><span data-ttu-id="66c87-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66c87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66c87-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66c87-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66c87-108">Não usado.</span><span class="sxs-lookup"><span data-stu-id="66c87-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="66c87-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66c87-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66c87-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="66c87-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66c87-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66c87-111">Return value</span></span>

<span data-ttu-id="66c87-112">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="66c87-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="66c87-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="66c87-113">Remarks</span></span>

<span data-ttu-id="66c87-114">Uma *Visualização dinâmica* (também conhecida como *visualização do Peek*) de uma janela é exibida quando um usuário move o ponteiro do mouse sobre a miniatura da janela na barra de tarefas ou dá o foco da miniatura na janela Alt + Tab.</span><span class="sxs-lookup"><span data-stu-id="66c87-114">A *live preview* (also known as a *Peek preview*) of a window appears when a user moves the mouse pointer over the window's thumbnail in the taskbar or gives the thumbnail focus in the ALT+TAB window.</span></span> <span data-ttu-id="66c87-115">Essa exibição é uma visualização de tamanho completo da janela e pode ser um instantâneo ao vivo ou uma representação icônico.</span><span class="sxs-lookup"><span data-stu-id="66c87-115">This view is a full-sized preview of the window and can be a live snapshot or an iconic representation.</span></span>

<span data-ttu-id="66c87-116">Gerenciador de Janelas da Área de Trabalho (DWM) enviará essa mensagem para uma janela se todas as seguintes situações forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="66c87-116">Desktop Window Manager (DWM) sends this message to a window if all of the following situations are true:</span></span>

-   <span data-ttu-id="66c87-117">A visualização dinâmica foi invocada na janela.</span><span class="sxs-lookup"><span data-stu-id="66c87-117">Live preview has been invoked on the window.</span></span>
-   <span data-ttu-id="66c87-118">O atributo [**DWMWA \_ tem \_ icônico \_ bitmap**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) está definido na janela.</span><span class="sxs-lookup"><span data-stu-id="66c87-118">The [**DWMWA\_HAS\_ICONIC\_BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) attribute is set on the window.</span></span>
-   <span data-ttu-id="66c87-119">Uma representação icônico é a única que existe para essa janela.</span><span class="sxs-lookup"><span data-stu-id="66c87-119">An iconic representation is the only one that exists for this window.</span></span>

<span data-ttu-id="66c87-120">A janela que recebe essa mensagem deve responder gerando um bitmap de escala completa.</span><span class="sxs-lookup"><span data-stu-id="66c87-120">The window that receives this message should respond by generating a full-scale bitmap.</span></span> <span data-ttu-id="66c87-121">Em seguida, a janela chama a função [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) para definir a visualização dinâmica.</span><span class="sxs-lookup"><span data-stu-id="66c87-121">The window then calls the [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function to set the live preview.</span></span> <span data-ttu-id="66c87-122">Se a janela não definir um bitmap em um determinado período de tempo, o DWM usará sua própria representação icônico padrão para a janela.</span><span class="sxs-lookup"><span data-stu-id="66c87-122">If the window does not set a bitmap in a given amount of time, DWM uses its own default iconic representation for the window.</span></span>

## <a name="examples"></a><span data-ttu-id="66c87-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66c87-123">Examples</span></span>

<span data-ttu-id="66c87-124">O exemplo a seguir demonstra uma resposta à **mensagem \_ DWMSENDICONICLIVEPREVIEWBITMAP do WM** .</span><span class="sxs-lookup"><span data-stu-id="66c87-124">The following example demonstrates a response to the **WM\_DWMSENDICONICLIVEPREVIEWBITMAP** message.</span></span> <span data-ttu-id="66c87-125">O exemplo chama a função [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) com um identificador para um bitmap personalizado independente de dispositivo a ser usado como a representação da janela.</span><span class="sxs-lookup"><span data-stu-id="66c87-125">The example calls the [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function with a handle to a customized, device-independent bitmap to use as the window's representation.</span></span>


```C++
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
```



<span data-ttu-id="66c87-126">Para obter o código completo, consulte a amostra [personalizar uma miniatura do icônico e um bitmap de visualização dinâmica](dwm-sample-customizethumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="66c87-126">For the complete code, see the [Customize an Iconic Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="66c87-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66c87-127">Requirements</span></span>



| <span data-ttu-id="66c87-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="66c87-128">Requirement</span></span> | <span data-ttu-id="66c87-129">Valor</span><span class="sxs-lookup"><span data-stu-id="66c87-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="66c87-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66c87-130">Minimum supported client</span></span><br/> | <span data-ttu-id="66c87-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="66c87-131">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="66c87-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66c87-132">Minimum supported server</span></span><br/> | <span data-ttu-id="66c87-133">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="66c87-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="66c87-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66c87-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="66c87-135"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="66c87-135"><dt>Dwmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66c87-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="66c87-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66c87-137">**DWMSENDICONICTHUMBNAIL do WM \_**</span><span class="sxs-lookup"><span data-stu-id="66c87-137">**WM\_DWMSENDICONICTHUMBNAIL**</span></span>](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[<span data-ttu-id="66c87-138">**DwmInvalidateIconicBitmaps**</span><span class="sxs-lookup"><span data-stu-id="66c87-138">**DwmInvalidateIconicBitmaps**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





