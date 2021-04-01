---
title: Constantes de TF_LBI_STATUS_ (Ctfutb. h)
description: As \_ constantes TF bin \_ status \_ \ Constants indicam o status de um item de barra de idiomas. Esses valores são usados com o método GetStatus ITfLangBarItem.
ms.assetid: 5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc
topic_type:
- apiref
api_name:
- TF_LBI_STATUS_HIDDEN
- TF_LBI_STATUS_DISABLED
- TF_LBI_STATUS_BTN_TOGGLED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de9dcf0272eaf79fd001461aa555d78c9d6ae30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645005"
---
# <a name="tf_lbi_status_-constants"></a><span data-ttu-id="6f3b9-104">Constantes de status de TF \_ ICB \_ \_ \*</span><span class="sxs-lookup"><span data-stu-id="6f3b9-104">TF\_LBI\_STATUS\_\* Constants</span></span>

<span data-ttu-id="6f3b9-105">As constantes \*\* \_ TF \_ bin \_ \* status\* _ indicam o status de um item da barra de idiomas.</span><span class="sxs-lookup"><span data-stu-id="6f3b9-105">The \**TF\_LBI\_STATUS\_\** _ constants indicate the status of a language bar item.</span></span> <span data-ttu-id="6f3b9-106">Esses valores são usados com o método [ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) .</span><span class="sxs-lookup"><span data-stu-id="6f3b9-106">These values are used with the [ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) method.</span></span>



| <span data-ttu-id="6f3b9-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="6f3b9-107">Constant/value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="6f3b9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f3b9-108">Description</span></span>                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <span data-ttu-id="6f3b9-109"><dt>_ \* TF \_ STATUS do ICB \_ \_ oculto \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6f3b9-109"><dt>_\*TF\_LBI\_STATUS\_HIDDEN\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="6f3b9-110">O item está oculto.</span><span class="sxs-lookup"><span data-stu-id="6f3b9-110">The item is hidden.</span></span> <span data-ttu-id="6f3b9-111">Esse estilo será ignorado se o item não incluir o estilo de \_ HIDDENSTATUSCONTROL do estilo de TF bin \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6f3b9-111">This style is ignored if the item does not include the TF\_LBI\_STYLE\_HIDDENSTATUSCONTROL style.</span></span><br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <span data-ttu-id="6f3b9-112"><dt>**TF \_ STATUS de ICB \_ \_ desabilitado**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="6f3b9-112"><dt>**TF\_LBI\_STATUS\_DISABLED**</dt> <dt>0x00000002</dt></span></span> </dl>           | <span data-ttu-id="6f3b9-113">O item está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6f3b9-113">The item is disabled.</span></span><br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <span data-ttu-id="6f3b9-114"><dt>**TF \_ BIN \_ status \_ BTN \_ toggleu**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="6f3b9-114"><dt>**TF\_LBI\_STATUS\_BTN\_TOGGLED**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="6f3b9-115">O item está no estado alternado ou pressionado.</span><span class="sxs-lookup"><span data-stu-id="6f3b9-115">The item is in the toggled or pressed state.</span></span> <span data-ttu-id="6f3b9-116">Esse estilo será ignorado se o item não incluir o estilo de \_ alternância TF bin \_ Style \_ BTN \_ .</span><span class="sxs-lookup"><span data-stu-id="6f3b9-116">This style is ignored if the item does not include the TF\_LBI\_STYLE\_BTN\_TOGGLE style.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6f3b9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f3b9-117">Requirements</span></span>



| <span data-ttu-id="6f3b9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f3b9-118">Requirement</span></span> | <span data-ttu-id="6f3b9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6f3b9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f3b9-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f3b9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6f3b9-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f3b9-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6f3b9-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f3b9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6f3b9-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f3b9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f3b9-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6f3b9-124">Redistributable</span></span><br/>          | <span data-ttu-id="6f3b9-125">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6f3b9-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="6f3b9-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f3b9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f3b9-127"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f3b9-127"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f3b9-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="6f3b9-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6f3b9-129"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6f3b9-129"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f3b9-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f3b9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f3b9-131">ITfLangBarItem:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="6f3b9-131">ITfLangBarItem::GetStatus</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





