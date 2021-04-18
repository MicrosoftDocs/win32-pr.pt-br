---
title: Constantes de TF_IAS_ (msctf. h)
description: As \_ constantes TF ias \_ \ são usadas como sinalizadores de campo de bits em métodos que inserem texto ou objetos inseridos em uma seleção ou ponto de inserção.
ms.assetid: adc5c539-fdb1-4829-ad17-2f54ec179c47
topic_type:
- apiref
api_name:
- TF_IAS_NOQUERY
- TF_IAS_QUERYONLY
- TF_IAS_NO_DEFAULT_COMPOSITION
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a025e295d80ac9a58625c221c4b4c224233fbb26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105792636"
---
# <a name="tf_ias_-constants"></a><span data-ttu-id="6043d-103">TF \_ constantes do IAS \_ \*</span><span class="sxs-lookup"><span data-stu-id="6043d-103">TF\_IAS\_\* Constants</span></span>

<span data-ttu-id="6043d-104">As constantes do TF \_ ias \_ \* são usadas como sinalizadores de campo de bits em métodos que inserem texto ou objetos inseridos em uma seleção ou ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="6043d-104">The TF\_IAS\_\* constants are used as bitfield flags in methods that insert text or embedded objects at a selection or insertion point.</span></span>



| <span data-ttu-id="6043d-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="6043d-105">Constant/value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="6043d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="6043d-106">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_IAS_NOQUERY"></span><span id="tf_ias_noquery"></span><dl> <span data-ttu-id="6043d-107"><dt>**TF \_ \_NoConsulta do IAS**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="6043d-107"><dt>**TF\_IAS\_NOQUERY**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                                       | <span data-ttu-id="6043d-108">O texto é inserido e o ponteiro de intervalo é definido como **nulo** na saída.</span><span class="sxs-lookup"><span data-stu-id="6043d-108">Text is inserted and the range pointer is set to **NULL** upon exit.</span></span> <span data-ttu-id="6043d-109">Não pode ser combinado com o \_ sinalizador TF ias \_ QUERYONLY.</span><span class="sxs-lookup"><span data-stu-id="6043d-109">Cannot be combined with the TF\_IAS\_QUERYONLY flag.</span></span><br/>       |
| <span id="TF_IAS_QUERYONLY"></span><span id="tf_ias_queryonly"></span><dl> <span data-ttu-id="6043d-110"><dt>**TF \_ \_QUERYONLY**</dt> <dt>(0X2) do</dt> ias</span><span class="sxs-lookup"><span data-stu-id="6043d-110"><dt>**TF\_IAS\_QUERYONLY**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                                 | <span data-ttu-id="6043d-111">Não execute a inserção.</span><span class="sxs-lookup"><span data-stu-id="6043d-111">Do not perform the insert.</span></span> <span data-ttu-id="6043d-112">O chamador requer apenas o ponteiro de intervalo a ser definido.</span><span class="sxs-lookup"><span data-stu-id="6043d-112">Caller only requires the range pointer to be set.</span></span> <span data-ttu-id="6043d-113">Não pode ser combinado com o \_ sinalizador TF ias \_ noquery.</span><span class="sxs-lookup"><span data-stu-id="6043d-113">Cannot be combined with the TF\_IAS\_NOQUERY flag.</span></span><br/> |
| <span id="TF_IAS_NO_DEFAULT_COMPOSITION"></span><span id="tf_ias_no_default_composition"></span><dl> <span data-ttu-id="6043d-114"><dt>**TF \_ \_Nenhuma \_ \_ composição padrão do IAS**</dt> <dt>(0x80000000)</dt></span><span class="sxs-lookup"><span data-stu-id="6043d-114"><dt>**TF\_IAS\_NO\_DEFAULT\_COMPOSITION**</dt> <dt>( 0x80000000 )</dt></span></span> </dl> | <span data-ttu-id="6043d-115">O TSF não criará uma composição padrão se uma composição for necessária.</span><span class="sxs-lookup"><span data-stu-id="6043d-115">TSF will not create a default composition if a composition is required.</span></span> <span data-ttu-id="6043d-116">O chamador deve iniciar uma composição no intervalo.</span><span class="sxs-lookup"><span data-stu-id="6043d-116">Caller must start a composition over the range.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="6043d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6043d-117">Requirements</span></span>



| <span data-ttu-id="6043d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6043d-118">Requirement</span></span> | <span data-ttu-id="6043d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6043d-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6043d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6043d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6043d-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6043d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6043d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6043d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6043d-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6043d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6043d-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6043d-124">Redistributable</span></span><br/>          | <span data-ttu-id="6043d-125">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6043d-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="6043d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6043d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6043d-127"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="6043d-127"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="6043d-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="6043d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6043d-129"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6043d-129"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6043d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6043d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6043d-131">ITextStoreACP:: InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="6043d-131">ITextStoreACP::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="6043d-132">ITextStoreACP:: InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="6043d-132">ITextStoreACP::InsertTextAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection)
</dt> <dt>

[<span data-ttu-id="6043d-133">ITextStoreAnchor::InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="6043d-133">ITextStoreAnchor::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="6043d-134">ITextStoreAnchor::InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="6043d-134">ITextStoreAnchor::InsertTextAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection)
</dt> <dt>

[<span data-ttu-id="6043d-135">ITfInsertAtSelection::InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="6043d-135">ITfInsertAtSelection::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="6043d-136">ITfInsertAtSelection::InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="6043d-136">ITfInsertAtSelection::InsertTextAtSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-inserttextatselection)
</dt> </dl>

 

 





