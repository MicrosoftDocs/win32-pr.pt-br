---
title: Mensagem de MM_ACM_FILTERCHOOSE (MSACM. h)
description: A \_ mensagem mm ACM \_ FILTERCHOOSE notifica uma função de gancho da caixa de diálogo acmFilterChoose antes de adicionar um elemento a uma das três caixas de listagem suspensas.
ms.assetid: f3c68240-a9aa-4771-96b9-1cb3bb5ea906
keywords:
- Multimídia do Windows de mensagem MM_ACM_FILTERCHOOSE
topic_type:
- apiref
api_name:
- MM_ACM_FILTERCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df28ad7f950b8ce995fd308622db8c429393cb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085242"
---
# <a name="mm_acm_filterchoose-message"></a><span data-ttu-id="7f9a4-104">\_Mensagem mm ACM \_ FILTERCHOOSE</span><span class="sxs-lookup"><span data-stu-id="7f9a4-104">MM\_ACM\_FILTERCHOOSE message</span></span>

<span data-ttu-id="7f9a4-105">A mensagem **mm \_ ACM \_ FILTERCHOOSE** notifica uma função de gancho da caixa de diálogo [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) antes de adicionar um elemento a uma das três caixas de listagem suspensas.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-105">The **MM\_ACM\_FILTERCHOOSE** message notifies an [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) dialog box hook function before adding an element to one of the three drop-down list boxes.</span></span> <span data-ttu-id="7f9a4-106">Essa mensagem permite que um aplicativo Personalize ainda mais as seleções disponíveis por meio da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-106">This message allows an application to further customize the selections available through the user interface.</span></span>


```C++
        MM_ACM_FILTERCHOOSE
        wParam = (WPARAM) wDropDown
        lParam = (LONG) lCustom
      
```



## <a name="parameters"></a><span data-ttu-id="7f9a4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f9a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f9a4-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span><span class="sxs-lookup"><span data-stu-id="7f9a4-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span></span>
</dt> <dd>

<span data-ttu-id="7f9a4-109">Caixa de listagem suspensa sendo inicializada e uma operação de verificação ou adição.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-109">Drop-down list box being initialized and a verify or add operation.</span></span>



| <span data-ttu-id="7f9a4-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f9a4-110">Requirement</span></span> | <span data-ttu-id="7f9a4-111">Valor</span><span class="sxs-lookup"><span data-stu-id="7f9a4-111">Value</span></span> |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f9a4-112">FILTERCHOOSE \_ de \_ verificação personalizada</span><span class="sxs-lookup"><span data-stu-id="7f9a4-112">FILTERCHOOSE\_CUSTOM\_VERIFY</span></span>    | <span data-ttu-id="7f9a4-113">O parâmetro *lParam* é um ponteiro para uma estrutura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) a ser adicionada à caixa de listagem suspensa nome personalizado.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-113">The *lParam* parameter is a pointer to a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the custom Name drop-down list box.</span></span>                                                                                                   |
| <span data-ttu-id="7f9a4-114">\_Adicionar filtro \_ FILTERCHOOSE</span><span class="sxs-lookup"><span data-stu-id="7f9a4-114">FILTERCHOOSE\_FILTER\_ADD</span></span>       | <span data-ttu-id="7f9a4-115">O parâmetro *lParam* é um ponteiro para um buffer que aceitará que uma estrutura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) seja adicionada à caixa de listagem suspensa de filtro.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-115">The *lParam* parameter is a pointer to a buffer that will accept a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the Filter drop-down list box.</span></span> <span data-ttu-id="7f9a4-116">O aplicativo deve copiar a estrutura do filtro a ser adicionada a esse buffer.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-116">The application must copy the filter structure to be added into this buffer.</span></span> |
| <span data-ttu-id="7f9a4-117">\_verificação de filtro FILTERCHOOSE \_</span><span class="sxs-lookup"><span data-stu-id="7f9a4-117">FILTERCHOOSE\_FILTER\_VERIFY</span></span>    | <span data-ttu-id="7f9a4-118">O parâmetro *lParam* é um ponteiro para uma estrutura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) a ser adicionada à caixa de listagem suspensa de filtro.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-118">The *lParam* parameter is a pointer to a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the Filter drop-down list box.</span></span>                                                                                                        |
| <span data-ttu-id="7f9a4-119">FILTERCHOOSE \_ FILTERTAG \_ Add</span><span class="sxs-lookup"><span data-stu-id="7f9a4-119">FILTERCHOOSE\_FILTERTAG\_ADD</span></span>    | <span data-ttu-id="7f9a4-120">O parâmetro *lParam* é um ponteiro para um **DWORD** que aceitará que uma marca de filtro de forma de onda seja adicionada à caixa de listagem suspensa marca de filtro.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-120">The *lParam* parameter is a pointer to a **DWORD** that will accept a waveform-audio filter tag to be added to the Filter Tag drop-down list box.</span></span>                                                                                        |
| <span data-ttu-id="7f9a4-121">FILTERCHOOSE \_ FILTERTAG \_ Verify</span><span class="sxs-lookup"><span data-stu-id="7f9a4-121">FILTERCHOOSE\_FILTERTAG\_VERIFY</span></span> | <span data-ttu-id="7f9a4-122">O parâmetro *lParam* é uma marca de filtro de onda-áudio a ser listada na caixa de listagem suspensa marca de filtro.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-122">The *lParam* parameter is a waveform-audio filter tag to be listed in the Filter Tag drop-down list box.</span></span>                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="7f9a4-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span><span class="sxs-lookup"><span data-stu-id="7f9a4-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span></span>
</dt> <dd>

<span data-ttu-id="7f9a4-124">Valor definido pela caixa de listagem especificada no parâmetro **wParam** .</span><span class="sxs-lookup"><span data-stu-id="7f9a4-124">Value defined by the list box specified in the **wParam** parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f9a4-125">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7f9a4-125">Return Value</span></span>

<span data-ttu-id="7f9a4-126">Retornará **true** se um aplicativo tratar essa mensagem ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-126">Returns **TRUE** if an application handles this message or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f9a4-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f9a4-127">Remarks</span></span>

<span data-ttu-id="7f9a4-128">Se o aplicativo processar a \_ operação de adição de filtro FILTERCHOOSE \_ , o tamanho do buffer de memória fornecido em *lParam* será determinado da função [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .</span><span class="sxs-lookup"><span data-stu-id="7f9a4-128">If the application processes the FILTERCHOOSE\_FILTER\_ADD operation, the size of the memory buffer supplied in *lParam* will be determined from the [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) function.</span></span>

<span data-ttu-id="7f9a4-129">Se o aplicativo processa uma operação de verificação, o aplicativo deve preceder o valor de retorno com **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long) **false**) para impedir que a caixa de diálogo liste essa seleção ou com **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**true**) para permitir que a caixa de diálogo listar essa seleção.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-129">If the application processes a verify operation, the application must precede the return value with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG) **FALSE**) to prevent the dialog box from listing this selection or with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**TRUE**) to allow the dialog box to list this selection.</span></span> <span data-ttu-id="7f9a4-130">Se estiver processando uma operação de adição, o aplicativo deverá preceder o retorno com **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**false**) para indicar que não é necessária mais adições ou com **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**true**) se mais adições forem necessárias.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-130">If processing an add operation, the application must precede the return with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**FALSE**) to indicate that no more additions are required or with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**TRUE**) if more additions are required.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f9a4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f9a4-131">Requirements</span></span>



| <span data-ttu-id="7f9a4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f9a4-132">Requirement</span></span> | <span data-ttu-id="7f9a4-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7f9a4-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f9a4-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f9a4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7f9a4-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7f9a4-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7f9a4-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f9a4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7f9a4-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7f9a4-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7f9a4-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7f9a4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f9a4-139"><dt>MSACM. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f9a4-139"><dt>Msacm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f9a4-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f9a4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f9a4-141">Gerenciador de compactação de áudio</span><span class="sxs-lookup"><span data-stu-id="7f9a4-141">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="7f9a4-142">Mensagens de compactação de áudio</span><span class="sxs-lookup"><span data-stu-id="7f9a4-142">Audio Compression Messages</span></span>](audio-compression-messages.md)
</dt> </dl>

 

 





