---
title: Mensagem de MCIWNDM_SETTIMEFORMAT (VFW. h)
description: A \_ mensagem MCIWNDM SETTIMEFORMAT define o formato de hora de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetTimeFormat.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETTIMEFORMAT
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcec1f0db5accad93211bf1eb6f1c9297e2b9f33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499253"
---
# <a name="mciwndm_settimeformat-message"></a><span data-ttu-id="21d3f-105">\_Mensagem MCIWNDM SETTIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="21d3f-105">MCIWNDM\_SETTIMEFORMAT message</span></span>

<span data-ttu-id="21d3f-106">A mensagem **MCIWNDM \_ SETTIMEFORMAT** define o formato de hora de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="21d3f-106">The **MCIWNDM\_SETTIMEFORMAT** message sets the time format of an MCI device.</span></span> <span data-ttu-id="21d3f-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="21d3f-107">You can send this message explicitly or by using the [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) macro.</span></span>


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="21d3f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21d3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21d3f-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="21d3f-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="21d3f-110">Ponteiro para um buffer que contém a cadeia de caracteres terminada em nulo que indica o formato de hora.</span><span class="sxs-lookup"><span data-stu-id="21d3f-110">Pointer to a buffer containing the null-terminated string indicating the time format.</span></span> <span data-ttu-id="21d3f-111">Especifique "frames" para definir o formato de hora como quadros ou "MS" para definir o formato de hora como milissegundos.</span><span class="sxs-lookup"><span data-stu-id="21d3f-111">Specify "frames" to set the time format to frames, or "ms" to set the time format to milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21d3f-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="21d3f-112">Return Value</span></span>

<span data-ttu-id="21d3f-113">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="21d3f-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="21d3f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="21d3f-114">Remarks</span></span>

<span data-ttu-id="21d3f-115">Um aplicativo pode especificar formatos de hora diferentes de quadros ou milissegundos, desde que os formatos tenham suporte do dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="21d3f-115">An application can specify time formats other than frames or milliseconds as long as the formats are supported by the MCI device.</span></span> <span data-ttu-id="21d3f-116">Formatos não contínuos, como trilhas e SMPTE, podem fazer com que o TrackBar se comporte incorretamente.</span><span class="sxs-lookup"><span data-stu-id="21d3f-116">Noncontinuous formats, such as tracks and SMPTE, can cause the trackbar to behave erratically.</span></span> <span data-ttu-id="21d3f-117">Para esses formatos de tempo, talvez você queira desativar a barra de ferramentas usando a macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) e especificando o \_ estilo de janela MCIWNDF NOPLAYBAR.</span><span class="sxs-lookup"><span data-stu-id="21d3f-117">For these time formats, you might want to turn off the toolbar by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro and specifying the MCIWNDF\_NOPLAYBAR window style.</span></span>

<span data-ttu-id="21d3f-118">Se você quiser definir o formato de hora como quadros ou milissegundos, também poderá usar a macro [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) ou [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) .</span><span class="sxs-lookup"><span data-stu-id="21d3f-118">If you want to set the time format to frames or milliseconds, you can also use the [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) or [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) macro.</span></span> <span data-ttu-id="21d3f-119">Para obter uma lista de formatos de hora, consulte a macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="21d3f-119">For a list of time formats, see the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="21d3f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21d3f-120">Requirements</span></span>



| <span data-ttu-id="21d3f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="21d3f-121">Requirement</span></span> | <span data-ttu-id="21d3f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="21d3f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="21d3f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21d3f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="21d3f-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="21d3f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="21d3f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21d3f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="21d3f-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="21d3f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="21d3f-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="21d3f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="21d3f-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="21d3f-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21d3f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="21d3f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21d3f-130">**MCIWndChangeStyles**</span><span class="sxs-lookup"><span data-stu-id="21d3f-130">**MCIWndChangeStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[<span data-ttu-id="21d3f-131">**MCIWndGetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="21d3f-131">**MCIWndGetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[<span data-ttu-id="21d3f-132">**MCIWndSetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="21d3f-132">**MCIWndSetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[<span data-ttu-id="21d3f-133">**MCIWndUseFrames**</span><span class="sxs-lookup"><span data-stu-id="21d3f-133">**MCIWndUseFrames**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[<span data-ttu-id="21d3f-134">**MCIWndUseTime**</span><span class="sxs-lookup"><span data-stu-id="21d3f-134">**MCIWndUseTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 





