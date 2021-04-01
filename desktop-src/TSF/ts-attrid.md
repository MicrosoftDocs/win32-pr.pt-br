---
title: TS_ATTRID (Textstor. h)
description: O \_ tipo de dados TS ATTRID é usado para identificar um atributo de texto.
ms.assetid: 5e375609-3d3c-4c12-ae05-dcaa70779162
keywords:
- TS_ATTRID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ea3823a95c123fe9942f69a2a133fd94a8567a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644220"
---
# <a name="ts_attrid"></a><span data-ttu-id="b7edd-104">\_ATTRID TS</span><span class="sxs-lookup"><span data-stu-id="b7edd-104">TS\_ATTRID</span></span>

<span data-ttu-id="b7edd-105">O tipo de dados **TS \_ ATTRID** é usado para identificar um atributo de texto.</span><span class="sxs-lookup"><span data-stu-id="b7edd-105">The **TS\_ATTRID** data type is used to identify a text attribute.</span></span>


```C++
typedef GUID TS_ATTRID;
```



## <a name="remarks"></a><span data-ttu-id="b7edd-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7edd-106">Remarks</span></span>

<span data-ttu-id="b7edd-107">Uma lista de GUIDs predefinidos para TS \_ ATTRID está em tsattrs. h.</span><span class="sxs-lookup"><span data-stu-id="b7edd-107">A list of predefined GUIDs for TS\_ATTRID is in tsattrs.h.</span></span>

<span data-ttu-id="b7edd-108">Os GUIDs TSATTRID \_ Text \_ VERTICALWRITING e TSATTRID \_ Text \_ Orientation são úteis para que os aplicativos correspondam ao texto de entrada que deve ser corrigido.</span><span class="sxs-lookup"><span data-stu-id="b7edd-108">The GUIDs TSATTRID\_Text\_VerticalWriting and TSATTRID\_Text\_Orientation are useful for applications to match input text that is to be corrected.</span></span> <span data-ttu-id="b7edd-109">GUIDs adicionais definidos pelo usuário podem ser criados.</span><span class="sxs-lookup"><span data-stu-id="b7edd-109">Additional user-defined GUIDs can be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7edd-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7edd-110">Requirements</span></span>



| <span data-ttu-id="b7edd-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7edd-111">Requirement</span></span> | <span data-ttu-id="b7edd-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b7edd-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7edd-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7edd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b7edd-114">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b7edd-114">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="b7edd-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7edd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b7edd-116">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b7edd-116">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="b7edd-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b7edd-117">Redistributable</span></span><br/>          | <span data-ttu-id="b7edd-118">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b7edd-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="b7edd-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7edd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7edd-120"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7edd-120"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7edd-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="b7edd-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7edd-122"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7edd-122"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7edd-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7edd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7edd-124">**ITextStoreACP:: FindNextAttrTransition**</span><span class="sxs-lookup"><span data-stu-id="b7edd-124">**ITextStoreACP::FindNextAttrTransition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="b7edd-125">**ITextStoreACP:: RequestAttrsAtPosition**</span><span class="sxs-lookup"><span data-stu-id="b7edd-125">**ITextStoreACP::RequestAttrsAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrsatposition)
</dt> <dt>

[<span data-ttu-id="b7edd-126">**ITextStoreACP:: RequestAttrsTransitioningAtPosition**</span><span class="sxs-lookup"><span data-stu-id="b7edd-126">**ITextStoreACP::RequestAttrsTransitioningAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="b7edd-127">**ITextStoreACP:: RequestSupportedAttrs**</span><span class="sxs-lookup"><span data-stu-id="b7edd-127">**ITextStoreACP::RequestSupportedAttrs**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestsupportedattrs)
</dt> <dt>

[<span data-ttu-id="b7edd-128">**ITextStoreACPSink:: OnAttrsChange**</span><span class="sxs-lookup"><span data-stu-id="b7edd-128">**ITextStoreACPSink::OnAttrsChange**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onattrschange)
</dt> <dt>

[<span data-ttu-id="b7edd-129">**ITextStoreAnchor::FindNextAttrTransition**</span><span class="sxs-lookup"><span data-stu-id="b7edd-129">**ITextStoreAnchor::FindNextAttrTransition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="b7edd-130">**ITextStoreAnchor::RequestAttrsAtPosition**</span><span class="sxs-lookup"><span data-stu-id="b7edd-130">**ITextStoreAnchor::RequestAttrsAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrsatposition)
</dt> <dt>

[<span data-ttu-id="b7edd-131">**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**</span><span class="sxs-lookup"><span data-stu-id="b7edd-131">**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="b7edd-132">**ITextStoreAnchor::RequestSupportedAttrs**</span><span class="sxs-lookup"><span data-stu-id="b7edd-132">**ITextStoreAnchor::RequestSupportedAttrs**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestsupportedattrs)
</dt> <dt>

[<span data-ttu-id="b7edd-133">**ITextStoreAnchorSink::OnAttrsChange**</span><span class="sxs-lookup"><span data-stu-id="b7edd-133">**ITextStoreAnchorSink::OnAttrsChange**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onattrschange)
</dt> <dt>

[<span data-ttu-id="b7edd-134">**\_ATTRVAL TS**</span><span class="sxs-lookup"><span data-stu-id="b7edd-134">**TS\_ATTRVAL**</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> </dl>

 

 





