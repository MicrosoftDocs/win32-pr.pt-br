---
title: Constantes de TS_IE_ (Textstor. h)
description: As \_ constantes TS IE \_ \ descrevem como inserir texto que pode conter objetos inseridos usados pelos serviços de texto.
ms.assetid: a455d712-42d5-472e-862d-85ae3ba9149f
topic_type:
- apiref
api_name:
- TS_IE_CORRECTION
- TS_IE_COMPOSITION
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9abdb05ba065ed9bf41b5379060c0643053884e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085364"
---
# <a name="ts_ie_-constants"></a><span data-ttu-id="e4c30-103">Constantes de TS \_ IE \_ \*</span><span class="sxs-lookup"><span data-stu-id="e4c30-103">TS\_IE\_\* Constants</span></span>

<span data-ttu-id="e4c30-104">As \_ constantes TS IE \_ \* descrevem como inserir texto que pode conter objetos incorporados usados pelos serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="e4c30-104">The TS\_IE\_\* constants describe how to insert text that can contain embedded objects used by text services.</span></span>



| <span data-ttu-id="e4c30-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="e4c30-105">Constant/value</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="e4c30-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4c30-106">Description</span></span>                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IE_CORRECTION"></span><span id="ts_ie_correction"></span><dl> <span data-ttu-id="e4c30-107"><dt>**TS \_ \_Correção do IE**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="e4c30-107"><dt>**TS\_IE\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>    | <span data-ttu-id="e4c30-108">O texto é uma transformação (correção) do conteúdo existente e qualquer informação especial de marcação de texto (metadados) é mantida, como dados de arquivo. wav ou um identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="e4c30-108">The text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/> |
| <span id="TS_IE_COMPOSITION"></span><span id="ts_ie_composition"></span><dl> <span data-ttu-id="e4c30-109"><dt>**TS \_ \_Composição do IE**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="e4c30-109"><dt>**TS\_IE\_COMPOSITION**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="e4c30-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="e4c30-110">Not used.</span></span><br/>                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="e4c30-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4c30-111">Remarks</span></span>

<span data-ttu-id="e4c30-112">Essas constantes são usadas no parâmetro *dwFlags* de [ITextStoreACP:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) e [ITextStoreAnchor:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).</span><span class="sxs-lookup"><span data-stu-id="e4c30-112">These constants are used in the *dwFlags* parameter of [ITextStoreACP::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) and [ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4c30-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4c30-113">Requirements</span></span>



| <span data-ttu-id="e4c30-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4c30-114">Requirement</span></span> | <span data-ttu-id="e4c30-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e4c30-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c30-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4c30-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e4c30-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4c30-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e4c30-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4c30-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e4c30-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4c30-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e4c30-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e4c30-120">Redistributable</span></span><br/>          | <span data-ttu-id="e4c30-121">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e4c30-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="e4c30-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4c30-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4c30-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4c30-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4c30-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="e4c30-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4c30-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4c30-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4c30-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4c30-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4c30-127">ITextStoreACP:: InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="e4c30-127">ITextStoreACP::InsertEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> <dt>

[<span data-ttu-id="e4c30-128">ITextStoreAnchor::InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="e4c30-128">ITextStoreAnchor::InsertEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)
</dt> </dl>

 

 





