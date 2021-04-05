---
title: Constantes de armazenamento de texto diversos (Textstor. h)
description: As constantes de armazenamento de texto diversos definem determinadas propriedades para armazenamentos de texto.
ms.assetid: 6e05ed74-fff3-4bc4-a21e-9af9492af23b
topic_type:
- apiref
api_name:
- TS_DEFAULT_SELECTION
- TS_GEA_HIDDEN
- TS_GTA_HIDDEN
- TS_ST_CORRECTION
- TS_TC_CORRECTION
- TS_VCOOKIE_NUL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead33c21bb78035dd9fda443a53de575ffa64d9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086129"
---
# <a name="miscellaneous-text-store-constants"></a><span data-ttu-id="516df-103">Constantes de armazenamento de texto diversos</span><span class="sxs-lookup"><span data-stu-id="516df-103">Miscellaneous Text Store Constants</span></span>

<span data-ttu-id="516df-104">As constantes de armazenamento de texto diversos definem determinadas propriedades para armazenamentos de texto.</span><span class="sxs-lookup"><span data-stu-id="516df-104">The miscellaneous text store constants set certain properties for text stores.</span></span>



| <span data-ttu-id="516df-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="516df-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="516df-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="516df-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <span data-ttu-id="516df-107"><dt>**TS \_ \_Seleção padrão**</dt> <dt>((ULong)-1)</dt></span><span class="sxs-lookup"><span data-stu-id="516df-107"><dt>**TS\_DEFAULT\_SELECTION**</dt> <dt>( ( ULONG )-1 )</dt></span></span> </dl> | <span data-ttu-id="516df-108">Se o parâmetro *ulIndex* de [ITfContext::](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) GetQuery for definido como esse valor, a seleção padrão será obtida.</span><span class="sxs-lookup"><span data-stu-id="516df-108">If the *ulIndex* parameter of [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) is set to this value, the default selection is obtained.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <span data-ttu-id="516df-109"><dt>**TS \_ GEA \_ Hidden**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="516df-109"><dt>**TS\_GEA\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="516df-110">Se o parâmetro *dwFlags* de [ITextStoreAnchor:: getembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) for definido como esse valor, um objeto inserido poderá ser localizado dentro do texto oculto.</span><span class="sxs-lookup"><span data-stu-id="516df-110">If *dwFlags* parameter of [ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) is set to this value, an embedded object can be located within hidden text.</span></span><br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <span data-ttu-id="516df-111"><dt>**TS \_ GTA \_ oculto**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="516df-111"><dt>**TS\_GTA\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="516df-112">Não usado.</span><span class="sxs-lookup"><span data-stu-id="516df-112">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <span data-ttu-id="516df-113"><dt>**TS \_ \_**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="516df-113"><dt>**TS\_ST\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                     | <span data-ttu-id="516df-114">Se o parâmetro *dwFlags* de [ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)ou [ITextStoreACPSink:: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) for definido como esse valor, o texto será uma transformação (correção) do conteúdo existente e quaisquer informações especiais de marcação de texto (metadados) serão mantidas, como dados de arquivo. wav ou um identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="516df-114">If *dwFlags* parameter of [ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext), or [ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) is set to this value, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <span data-ttu-id="516df-115"><dt>**TS \_ \_Correção de TC**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="516df-115"><dt>**TS\_TC\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                     | <span data-ttu-id="516df-116">Se o parâmetro *dwFlags* de [ITextStoreAnchorSink:: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) for definido com esse valor, o texto será uma transformação (correção) do conteúdo existente e quaisquer informações especiais de marcação de texto (metadados) serão mantidas, como dados de arquivo. wav ou um identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="516df-116">If *dwFlags* parameter of [ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) is set to this value, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <span data-ttu-id="516df-117"><dt>**TS \_ VCOOKIE \_ nul**</dt> <dt>(0xFFFFFFFF)</dt></span><span class="sxs-lookup"><span data-stu-id="516df-117"><dt>**TS\_VCOOKIE\_NUL**</dt> <dt>( 0xffffffff )</dt></span></span> </dl>                    | <span data-ttu-id="516df-118">Usado internamente pelo TSF.</span><span class="sxs-lookup"><span data-stu-id="516df-118">Used internally by TSF.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a><span data-ttu-id="516df-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="516df-119">Requirements</span></span>



| <span data-ttu-id="516df-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="516df-120">Requirement</span></span> | <span data-ttu-id="516df-121">Valor</span><span class="sxs-lookup"><span data-stu-id="516df-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="516df-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="516df-122">Minimum supported client</span></span><br/> | <span data-ttu-id="516df-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="516df-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="516df-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="516df-124">Minimum supported server</span></span><br/> | <span data-ttu-id="516df-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="516df-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="516df-126">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="516df-126">Redistributable</span></span><br/>          | <span data-ttu-id="516df-127">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="516df-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="516df-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="516df-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="516df-129"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="516df-129"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="516df-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="516df-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="516df-131"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="516df-131"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="516df-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="516df-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="516df-133">ITfContext:: getseleções</span><span class="sxs-lookup"><span data-stu-id="516df-133">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="516df-134">ITextStoreACP:: SetText</span><span class="sxs-lookup"><span data-stu-id="516df-134">ITextStoreACP::SetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[<span data-ttu-id="516df-135">ITextStoreAnchor:: SetText</span><span class="sxs-lookup"><span data-stu-id="516df-135">ITextStoreAnchor::SetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[<span data-ttu-id="516df-136">ITextStoreAnchor:: getembedded</span><span class="sxs-lookup"><span data-stu-id="516df-136">ITextStoreAnchor::GetEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[<span data-ttu-id="516df-137">ITextStoreACPSink:: OnTextChange</span><span class="sxs-lookup"><span data-stu-id="516df-137">ITextStoreACPSink::OnTextChange</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[<span data-ttu-id="516df-138">ITextStoreAnchorSink::OnTextChange</span><span class="sxs-lookup"><span data-stu-id="516df-138">ITextStoreAnchorSink::OnTextChange</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[<span data-ttu-id="516df-139">Constantes de estrutura diversas</span><span class="sxs-lookup"><span data-stu-id="516df-139">Miscellaneous Framework Constants</span></span>](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





