---
title: Constantes de TF_LBI_ (Ctfutb. h)
description: As \_ constantes TF bin \_ \ são usadas com o método OnUpdate ITfLangBarItemSink para indicar quais itens da barra de idiomas foram alterados.
ms.assetid: ed84012f-19ba-43b3-bbb5-7373ed174c33
topic_type:
- apiref
api_name:
- TF_LBI_ICON
- TF_LBI_TEXT
- TF_LBI_TOOLTIP
- TF_LBI_BITMAP
- TF_LBI_BALLOON
- TF_LBI_STATUS
- TF_LBI_BMPALL
- TF_LBI_BMPBTNALL
- TF_LBI_BTNALL
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72b69f1cb5a5b4a24e78a2bdc1ca0e7a9d79cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760348"
---
# <a name="tf_lbi_-constants"></a><span data-ttu-id="7eb7c-103">Constantes de TF \_ ICB \_ \*</span><span class="sxs-lookup"><span data-stu-id="7eb7c-103">TF\_LBI\_\* Constants</span></span>

<span data-ttu-id="7eb7c-104">As constantes \*\* \_ TF \_ \* bin\* _ são usadas com o método [ITfLangBarItemSink:: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) para indicar quais itens da barra de idiomas foram alterados.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-104">The \**TF\_LBI\_\** _ constants are used with the [ITfLangBarItemSink::OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) method to indicate which language bar items changed.</span></span>



| <span data-ttu-id="7eb7c-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="7eb7c-105">Constant/value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="7eb7c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7eb7c-106">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_ICON"></span><span id="tf_lbi_icon"></span><dl> <span data-ttu-id="7eb7c-107"><dt>_ \* TF \_ Ícone de ICB \_ \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="7eb7c-107"><dt>_\*TF\_LBI\_ICON\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                                                        | <span data-ttu-id="7eb7c-108">O ícone do item foi alterado.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-108">The icon of the item has changed.</span></span> <span data-ttu-id="7eb7c-109">A barra de idiomas chama [ITfLangBarItemButton:: GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) em resposta a essa notificação.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-109">The language bar calls [ITfLangBarItemButton::GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) in response to this notification.</span></span><br/>                                                                                                                                             |
| <span id="TF_LBI_TEXT"></span><span id="tf_lbi_text"></span><dl> <span data-ttu-id="7eb7c-110"><dt>**TF \_ \_Texto de ICB**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="7eb7c-110"><dt>**TF\_LBI\_TEXT**</dt> <dt>0x00000002</dt></span></span> </dl>                                                        | <span data-ttu-id="7eb7c-111">O texto de um botão ou item de botão de bitmap foi alterado.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-111">The text of a button or bitmap button item has changed.</span></span> <span data-ttu-id="7eb7c-112">A barra de idiomas chama [ITfLangBarItemButton:: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) ou [ITfLangBarItemBitmapButton:: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), o que for apropriado, em resposta a essa notificação.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-112">The language bar calls [ITfLangBarItemButton::GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) or [ITfLangBarItemBitmapButton::GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), whichever is appropriate, in response to this notification.</span></span><br/>           |
| <span id="TF_LBI_TOOLTIP"></span><span id="tf_lbi_tooltip"></span><dl> <span data-ttu-id="7eb7c-113"><dt>**TF \_ \_Dica de ferramenta bin**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="7eb7c-113"><dt>**TF\_LBI\_TOOLTIP**</dt> <dt>0x00000004</dt></span></span> </dl>                                               | <span data-ttu-id="7eb7c-114">O texto da dica de ferramenta do item alterado.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-114">The tooltip text of the item changed.</span></span> <span data-ttu-id="7eb7c-115">A barra de idiomas chama [ITfLangBarItem:: Gettooltipstring](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) em resposta a esta notificação.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-115">The language bar calls [ITfLangBarItem::GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) in response to this notification.</span></span><br/>                                                                                                                                   |
| <span id="TF_LBI_BITMAP"></span><span id="tf_lbi_bitmap"></span><dl> <span data-ttu-id="7eb7c-116"><dt>**TF \_ 0x00000008 de \_ bitmap bin**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7eb7c-116"><dt>**TF\_LBI\_BITMAP**</dt> <dt>0x00000008</dt></span></span> </dl>                                                  | <span data-ttu-id="7eb7c-117">O bitmap de um item de botão bitmap ou bitmap foi alterado.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-117">The bitmap of a bitmap or bitmap button item changed.</span></span> <span data-ttu-id="7eb7c-118">A barra de idiomas chama [ITfLangBarItemBitmap::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) ou [ITfLangBarItemBitmapButton::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), o que for apropriado, em resposta a essa notificação.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-118">The language bar calls [ITfLangBarItemBitmap::DrawBitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) or [ITfLangBarItemBitmapButton::DrawBitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), whichever is appropriate, in response to this notification.</span></span><br/> |
| <span id="TF_LBI_BALLOON"></span><span id="tf_lbi_balloon"></span><dl> <span data-ttu-id="7eb7c-119"><dt>**TF \_ \_Balão de bin**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="7eb7c-119"><dt>**TF\_LBI\_BALLOON**</dt> <dt>0x00000010</dt></span></span> </dl>                                               | <span data-ttu-id="7eb7c-120">As informações de um item de balão foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-120">The information for a balloon item changed.</span></span> <span data-ttu-id="7eb7c-121">A barra de idiomas chama [ITfLangBarItemBalloon:: GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) em resposta a essa notificação.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-121">The language bar calls [ITfLangBarItemBalloon::GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) in response to this notification.</span></span><br/>                                                                                                                   |
| <span id="TF_LBI_STATUS"></span><span id="tf_lbi_status"></span><dl> <span data-ttu-id="7eb7c-122"><dt>**TF \_ 0x00010000 de \_ status bin**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7eb7c-122"><dt>**TF\_LBI\_STATUS**</dt> <dt>0x00010000</dt></span></span> </dl>                                                  | <span data-ttu-id="7eb7c-123">O status do item foi alterado.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-123">The item status changed.</span></span> <span data-ttu-id="7eb7c-124">A barra de idiomas chama [ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) em resposta a esta notificação.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-124">The language bar calls [ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) in response to this notification.</span></span><br/>                                                                                                                                                              |
| <span id="TF_LBI_BMPALL"></span><span id="tf_lbi_bmpall"></span><dl> <span data-ttu-id="7eb7c-125"><dt>**TF \_ \_BMPALL**</dt> de <dt> \_ \_ \| \_ \_ ferramentas de mapa de bitmap</dt> do ICB de TF ICB</span><span class="sxs-lookup"><span data-stu-id="7eb7c-125"><dt>**TF\_LBI\_BMPALL**</dt> <dt>TF\_LBI\_BITMAP\| TF\_LBI\_TOOLTIP</dt></span></span> </dl>                          | <span data-ttu-id="7eb7c-126">Combina o \_ bitmap do TF bin \_ e a \_ dica de ferramenta TF bin \_ .</span><span class="sxs-lookup"><span data-stu-id="7eb7c-126">Combines TF\_LBI\_BITMAP and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="TF_LBI_BMPBTNALL"></span><span id="tf_lbi_bmpbtnall"></span><dl> <span data-ttu-id="7eb7c-127"><dt>**TF \_ BIN \_ BMPBTNALL**</dt> <dt>TF \_ bin \_ bitmap \| TF \_ bin \_ texto \| TF \_ bin \_ dica de ferramenta</dt></span><span class="sxs-lookup"><span data-stu-id="7eb7c-127"><dt>**TF\_LBI\_BMPBTNALL**</dt> <dt>TF\_LBI\_BITMAP\| TF\_LBI\_TEXT\| TF\_LBI\_TOOLTIP</dt></span></span> </dl> | <span data-ttu-id="7eb7c-128">Combina o \_ bitmap do TF bin \_ , o tf \_ bin \_ Text e o tf \_ bin \_ TOOLTIP.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-128">Combines TF\_LBI\_BITMAP, TF\_LBI\_TEXT and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="TF_LBI_BTNALL"></span><span id="tf_lbi_btnall"></span><dl> <span data-ttu-id="7eb7c-129"><dt>**TF \_ BIN \_ BTNALL**</dt> <dt>TF \_ \_ Icon ícone \| TF \_ bin \_ texto \| TF \_ bin \_ dica de ferramenta</dt></span><span class="sxs-lookup"><span data-stu-id="7eb7c-129"><dt>**TF\_LBI\_BTNALL**</dt> <dt>TF\_LBI\_ICON\| TF\_LBI\_TEXT\| TF\_LBI\_TOOLTIP</dt></span></span> </dl>            | <span data-ttu-id="7eb7c-130">Combina o \_ ícone TF bin \_ , TF \_ bin \_ Text e TF \_ bin \_ TOOLTIP.</span><span class="sxs-lookup"><span data-stu-id="7eb7c-130">Combines TF\_LBI\_ICON, TF\_LBI\_TEXT and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="7eb7c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eb7c-131">Requirements</span></span>



| <span data-ttu-id="7eb7c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eb7c-132">Requirement</span></span> | <span data-ttu-id="7eb7c-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7eb7c-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7eb7c-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7eb7c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7eb7c-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7eb7c-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7eb7c-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7eb7c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7eb7c-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7eb7c-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7eb7c-138">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7eb7c-138">Redistributable</span></span><br/>          | <span data-ttu-id="7eb7c-139">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7eb7c-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="7eb7c-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7eb7c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7eb7c-141"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="7eb7c-141"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="7eb7c-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="7eb7c-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7eb7c-143"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7eb7c-143"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eb7c-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="7eb7c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eb7c-145">ITfLangBarItemSink:: OnUpdate</span><span class="sxs-lookup"><span data-stu-id="7eb7c-145">ITfLangBarItemSink::OnUpdate</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)
</dt> </dl>

 

 





