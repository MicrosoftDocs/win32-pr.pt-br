---
title: Mensagem de WM_DWMSENDICONICTHUMBNAIL (dwmapi. h)
description: Instrui uma janela para fornecer um bitmap estático a ser usado como uma representação em miniatura dessa janela.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- Mensagem de WM_DWMSENDICONICTHUMBNAIL Gerenciador de Janelas da Área de Trabalho
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICTHUMBNAIL
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded5b734278973afe35f5ed3d9fbb5b0aec9242b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455829"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a><span data-ttu-id="fc96b-104">Mensagem do WM \_ DWMSENDICONICTHUMBNAIL</span><span class="sxs-lookup"><span data-stu-id="fc96b-104">WM\_DWMSENDICONICTHUMBNAIL message</span></span>

<span data-ttu-id="fc96b-105">Instrui uma janela para fornecer um bitmap estático a ser usado como uma representação em miniatura dessa janela.</span><span class="sxs-lookup"><span data-stu-id="fc96b-105">Instructs a window to provide a static bitmap to use as a thumbnail representation of that window.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc96b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc96b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc96b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc96b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc96b-108">Não usado.</span><span class="sxs-lookup"><span data-stu-id="fc96b-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="fc96b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc96b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc96b-110">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) desse valor é a coordenada x máxima da miniatura.</span><span class="sxs-lookup"><span data-stu-id="fc96b-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of this value is the maximum x-coordinate of the thumbnail.</span></span> <span data-ttu-id="fc96b-111">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é a coordenada y máxima.</span><span class="sxs-lookup"><span data-stu-id="fc96b-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the maximum y-coordinate.</span></span> <span data-ttu-id="fc96b-112">Se uma miniatura tiver uma dimensão que exceda um ou ambos os valores, o DWM não aceitará a miniatura.</span><span class="sxs-lookup"><span data-stu-id="fc96b-112">If a thumbnail has a dimension that exceeds one or both of these values, the DWM does not accept the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc96b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc96b-113">Return value</span></span>

<span data-ttu-id="fc96b-114">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="fc96b-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc96b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc96b-115">Remarks</span></span>

<span data-ttu-id="fc96b-116">O DWM enviará essa mensagem para uma janela se todas as seguintes situações forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="fc96b-116">DWM sends this message to a window if all of the following situations are true:</span></span>

-   <span data-ttu-id="fc96b-117">O DWM está exibindo uma representação icônico da janela.</span><span class="sxs-lookup"><span data-stu-id="fc96b-117">DWM is displaying an iconic representation of the window.</span></span>
-   <span data-ttu-id="fc96b-118">O atributo [**DWMWA \_ tem \_ icônico \_ bitmap**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) está definido na janela.</span><span class="sxs-lookup"><span data-stu-id="fc96b-118">The [**DWMWA\_HAS\_ICONIC\_BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) attribute is set on the window.</span></span>
-   <span data-ttu-id="fc96b-119">A janela não definiu um bitmap armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="fc96b-119">The window did not set a cached bitmap.</span></span>
-   <span data-ttu-id="fc96b-120">Há espaço no cache para outro bitmap.</span><span class="sxs-lookup"><span data-stu-id="fc96b-120">There is room in the cache for another bitmap.</span></span>

<span data-ttu-id="fc96b-121">A janela que recebe essa mensagem deve responder gerando um bitmap que não seja maior do que o tamanho solicitado nos parâmetros da mensagem.</span><span class="sxs-lookup"><span data-stu-id="fc96b-121">The window that receives this message should respond by generating a bitmap that is not larger than the size that is requested in the message parameters.</span></span> <span data-ttu-id="fc96b-122">Em seguida, a janela chama a função [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) para substituir a miniatura padrão.</span><span class="sxs-lookup"><span data-stu-id="fc96b-122">The window then calls the [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) function to override the default thumbnail.</span></span> <span data-ttu-id="fc96b-123">Se a janela não fornecer um bitmap em um determinado período de tempo, o DWM usará sua própria representação icônico padrão para a janela.</span><span class="sxs-lookup"><span data-stu-id="fc96b-123">If the window does not supply a bitmap in a given amount of time, DWM uses its own default iconic representation for the window.</span></span>

<span data-ttu-id="fc96b-124">A janela deve pertencer ao processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="fc96b-124">The window must belong to the calling process.</span></span>

## <a name="examples"></a><span data-ttu-id="fc96b-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fc96b-125">Examples</span></span>

<span data-ttu-id="fc96b-126">O exemplo de código a seguir mostra como responder à mensagem do **WM \_ DWMSENDICONICTHUMBNAIL** .</span><span class="sxs-lookup"><span data-stu-id="fc96b-126">The following code example shows how to respond to the **WM\_DWMSENDICONICTHUMBNAIL** message.</span></span> <span data-ttu-id="fc96b-127">O exemplo chama [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), com um identificador para um bitmap personalizado independente de dispositivo a ser usado como a representação do Windows.</span><span class="sxs-lookup"><span data-stu-id="fc96b-127">The example calls [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), with a handle to a customized, device-indepedent bitmap to use as the windows' representation.</span></span>


```C++
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;
```



<span data-ttu-id="fc96b-128">Para obter o exemplo completo, consulte a amostra [personalizar uma miniatura do icônico e um bitmap de visualização dinâmica](dwm-sample-customizethumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="fc96b-128">For the complete example, see the [Customize an Iconic Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc96b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc96b-129">Requirements</span></span>



| <span data-ttu-id="fc96b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc96b-130">Requirement</span></span> | <span data-ttu-id="fc96b-131">Valor</span><span class="sxs-lookup"><span data-stu-id="fc96b-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fc96b-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc96b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fc96b-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fc96b-133">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fc96b-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc96b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fc96b-135">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="fc96b-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fc96b-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc96b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc96b-137"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc96b-137"><dt>Dwmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc96b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc96b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc96b-139">**DwmInvalidateIconicBitmaps**</span><span class="sxs-lookup"><span data-stu-id="fc96b-139">**DwmInvalidateIconicBitmaps**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[<span data-ttu-id="fc96b-140">**DWMSENDICONICLIVEPREVIEWBITMAP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="fc96b-140">**WM\_DWMSENDICONICLIVEPREVIEWBITMAP**</span></span>](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

