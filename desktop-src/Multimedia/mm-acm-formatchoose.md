---
title: Mensagem de MM_ACM_FORMATCHOOSE (MSACM. h)
description: A \_ mensagem mm ACM \_ FORMATCHOOSE notifica uma função de gancho de caixa de diálogo acmFormatChoose antes de adicionar um elemento a uma das três caixas de listagem suspensas.
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- Multimídia do Windows de mensagem MM_ACM_FORMATCHOOSE
topic_type:
- apiref
api_name:
- MM_ACM_FORMATCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35808e06521cbd83d07f8d6c799779a16f50236b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645255"
---
# <a name="mm_acm_formatchoose-message"></a><span data-ttu-id="18b99-104">\_Mensagem mm ACM \_ FORMATCHOOSE</span><span class="sxs-lookup"><span data-stu-id="18b99-104">MM\_ACM\_FORMATCHOOSE message</span></span>

<span data-ttu-id="18b99-105">A mensagem **mm \_ ACM \_ FORMATCHOOSE** notifica uma função de gancho de caixa de diálogo [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) antes de adicionar um elemento a uma das três caixas de listagem suspensas.</span><span class="sxs-lookup"><span data-stu-id="18b99-105">The **MM\_ACM\_FORMATCHOOSE** message notifies an [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) dialog hook function before adding an element to one of the three drop-down list boxes.</span></span> <span data-ttu-id="18b99-106">Essa mensagem permite que um aplicativo Personalize ainda mais as seleções disponíveis por meio da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="18b99-106">This message allows an application to further customize the selections available through the user interface.</span></span>


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a><span data-ttu-id="18b99-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18b99-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18b99-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span><span class="sxs-lookup"><span data-stu-id="18b99-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span></span>
</dt> <dd>

<span data-ttu-id="18b99-109">Caixa de listagem suspensa sendo inicializada e uma operação de verificação ou adição.</span><span class="sxs-lookup"><span data-stu-id="18b99-109">Drop-down list box being initialized and a verify or add operation.</span></span>



| <span data-ttu-id="18b99-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="18b99-110">Requirement</span></span> | <span data-ttu-id="18b99-111">Valor</span><span class="sxs-lookup"><span data-stu-id="18b99-111">Value</span></span> |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18b99-112">FORMATCHOOSE \_ de \_ verificação personalizada</span><span class="sxs-lookup"><span data-stu-id="18b99-112">FORMATCHOOSE\_CUSTOM\_VERIFY</span></span>    | <span data-ttu-id="18b99-113">O parâmetro *lParam* é um ponteiro para uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) a ser adicionada à caixa de listagem suspensa nome personalizado.</span><span class="sxs-lookup"><span data-stu-id="18b99-113">The *lParam* parameter is a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the custom Name drop-down list box.</span></span>                                                                                                   |
| <span data-ttu-id="18b99-114">\_Adicionar formato \_ FORMATCHOOSE</span><span class="sxs-lookup"><span data-stu-id="18b99-114">FORMATCHOOSE\_FORMAT\_ADD</span></span>       | <span data-ttu-id="18b99-115">O parâmetro *lParam* é um ponteiro para um buffer que aceitará que uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) seja adicionada à caixa de listagem suspensa formato.</span><span class="sxs-lookup"><span data-stu-id="18b99-115">The *lParam* parameter is a pointer to a buffer that will accept a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the Format drop-down list box.</span></span> <span data-ttu-id="18b99-116">O aplicativo deve copiar a estrutura de formato a ser adicionada a esse buffer.</span><span class="sxs-lookup"><span data-stu-id="18b99-116">The application must copy the format structure to be added into this buffer.</span></span> |
| <span data-ttu-id="18b99-117">\_verificação de formato de FORMATCHOOSE \_</span><span class="sxs-lookup"><span data-stu-id="18b99-117">FORMATCHOOSE\_FORMAT\_VERIFY</span></span>    | <span data-ttu-id="18b99-118">O parâmetro *lParam* é um ponteiro para uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) a ser adicionada à caixa de listagem suspensa formato.</span><span class="sxs-lookup"><span data-stu-id="18b99-118">The *lParam* parameter is a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the Format drop-down list box.</span></span>                                                                                                        |
| <span data-ttu-id="18b99-119">FORMATCHOOSE \_ FORMATTAG \_ Add</span><span class="sxs-lookup"><span data-stu-id="18b99-119">FORMATCHOOSE\_FORMATTAG\_ADD</span></span>    | <span data-ttu-id="18b99-120">O parâmetro *lParam* é um ponteiro para uma variável que aceitará que uma marca de formato de onda-áudio seja adicionada à caixa de listagem suspensa de marca de formato.</span><span class="sxs-lookup"><span data-stu-id="18b99-120">The *lParam* parameter is a pointer to a variable that will accept a waveform-audio format tag to be added to the Format Tag drop-down list box.</span></span>                                                                                             |
| <span data-ttu-id="18b99-121">FORMATCHOOSE \_ FORMATTAG \_ Verify</span><span class="sxs-lookup"><span data-stu-id="18b99-121">FORMATCHOOSE\_FORMATTAG\_VERIFY</span></span> | <span data-ttu-id="18b99-122">O parâmetro *lParam* é uma marca de formato de áudio de forma de onda a ser listada na caixa de listagem suspensa Formatar marca.</span><span class="sxs-lookup"><span data-stu-id="18b99-122">The *lParam* parameter is a waveform-audio format tag to be listed in the Format Tag drop-down list box.</span></span>                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="18b99-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span><span class="sxs-lookup"><span data-stu-id="18b99-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span></span>
</dt> <dd>

<span data-ttu-id="18b99-124">Valor definido pela caixa de listagem especificada no parâmetro **wParam** .</span><span class="sxs-lookup"><span data-stu-id="18b99-124">Value defined by the listbox specified in the **wParam** parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18b99-125">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="18b99-125">Return Value</span></span>

<span data-ttu-id="18b99-126">Retornará **true** se um aplicativo tratar essa mensagem ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="18b99-126">Returns **TRUE** if an application handles this message or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="18b99-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="18b99-127">Remarks</span></span>

<span data-ttu-id="18b99-128">Se o aplicativo processar a \_ operação de adição de formato FILTERCHOOSE \_ , o tamanho do buffer de memória fornecido em *lParam* será determinado da função [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .</span><span class="sxs-lookup"><span data-stu-id="18b99-128">If the application processes the FILTERCHOOSE\_FORMAT\_ADD operation, the size of the memory buffer supplied in *lParam* will be determined from the [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) function.</span></span>

<span data-ttu-id="18b99-129">Se seu aplicativo estiver processando uma operação de verificação, ele poderá impedir que a caixa de diálogo liste essa seleção chamando a função **SetWindowLong** com *NINDEX* definida como DWL \_ MSGRESULT e *lNewLong* definida como **false** (conversão para um tipo de dados **Long** ).</span><span class="sxs-lookup"><span data-stu-id="18b99-129">If your application is processing a verify operation, it can prevent the dialog box from listing this selection by calling the **SetWindowLong** function with *nIndex* set to DWL\_MSGRESULT and *lNewLong* set to **FALSE** (cast to a **LONG** data type).</span></span> <span data-ttu-id="18b99-130">Para permitir que a caixa de diálogo liste essa seleção, chame essa função com *lNewLong* definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="18b99-130">To allow the dialog box to list this selection, call this function with *lNewLong* set to **TRUE**.</span></span>

<span data-ttu-id="18b99-131">Se seu aplicativo estiver processando uma operação de adição, ele poderá indicar que não é necessária mais adições chamando a função **SetWindowLong** com *NINDEX* definido como DWL \_ MSGRESULT e *lNewLong* definida como **false** (conversão para um tipo de dados **Long** ).</span><span class="sxs-lookup"><span data-stu-id="18b99-131">If your application is processing an add operation, it can indicate that no more additions are required by calling the **SetWindowLong** function with *nIndex* set to DWL\_MSGRESULT and *lNewLong* set to **FALSE** (cast to a **LONG** data type).</span></span> <span data-ttu-id="18b99-132">Para indicar que mais adições são necessárias, chame essa função com *lNewLong* definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="18b99-132">To indicate more additions are required, call this function with *lNewLong* set to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="18b99-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18b99-133">Requirements</span></span>



| <span data-ttu-id="18b99-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="18b99-134">Requirement</span></span> | <span data-ttu-id="18b99-135">Valor</span><span class="sxs-lookup"><span data-stu-id="18b99-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18b99-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18b99-136">Minimum supported client</span></span><br/> | <span data-ttu-id="18b99-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="18b99-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="18b99-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18b99-138">Minimum supported server</span></span><br/> | <span data-ttu-id="18b99-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="18b99-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="18b99-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="18b99-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="18b99-141"><dt>MSACM. h</dt></span><span class="sxs-lookup"><span data-stu-id="18b99-141"><dt>Msacm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18b99-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="18b99-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18b99-143">Gerenciador de compactação de áudio</span><span class="sxs-lookup"><span data-stu-id="18b99-143">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="18b99-144">Mensagens de compactação de áudio</span><span class="sxs-lookup"><span data-stu-id="18b99-144">Audio Compression Messages</span></span>](audio-compression-messages.md)
</dt> </dl>

 

