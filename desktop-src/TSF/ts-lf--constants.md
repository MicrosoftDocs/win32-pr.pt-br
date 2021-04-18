---
title: Constantes de TS_LF_ (Textstor. h)
description: As \_ constantes TS LF = \_ especificam o tipo de bloqueio de documento.
ms.assetid: f0bb6ef9-a8fc-4331-9210-6c5ba1721a73
topic_type:
- apiref
api_name:
- TS_LF_SYNC
- TS_LF_READ
- TS_LF_READWRITE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6240511fd95e91a7f22477f631178dfab528f1e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780129"
---
# <a name="ts_lf_-constants"></a><span data-ttu-id="4cf7c-103">Constantes de TS \_ LF \_ \*</span><span class="sxs-lookup"><span data-stu-id="4cf7c-103">TS\_LF\_\* Constants</span></span>

<span data-ttu-id="4cf7c-104">As \_ constantes TS LF \_ \* especificam o tipo de bloqueio de documento.</span><span class="sxs-lookup"><span data-stu-id="4cf7c-104">The TS\_LF\_\* constants specify the type of document lock.</span></span>



| <span data-ttu-id="4cf7c-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="4cf7c-105">Constant/value</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="4cf7c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4cf7c-106">Description</span></span>                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span id="TS_LF_SYNC"></span><span id="ts_lf_sync"></span><dl> <span data-ttu-id="4cf7c-107"><dt>**TS \_ \_Sincronização de LF**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="4cf7c-107"><dt>**TS\_LF\_SYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                | <span data-ttu-id="4cf7c-108">O documento terá um bloqueio síncrono se esse sinalizador for combinado com outros sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="4cf7c-108">The document has a synchronous-lock if this flag is combined with other flags.</span></span><br/> |
| <span id="TS_LF_READ"></span><span id="ts_lf_read"></span><dl> <span data-ttu-id="4cf7c-109"><dt>**TS \_ LF de \_ leitura**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="4cf7c-109"><dt>**TS\_LF\_READ**</dt> <dt>( 0x2 )</dt></span></span> </dl>                | <span data-ttu-id="4cf7c-110">O documento tem um bloqueio somente leitura e não pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="4cf7c-110">The document has a read-only lock and cannot be modified.</span></span><br/>                      |
| <span id="TS_LF_READWRITE"></span><span id="ts_lf_readwrite"></span><dl> <span data-ttu-id="4cf7c-111"><dt>**TS \_ LF \_ ReadWrite**</dt> <dt>(0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="4cf7c-111"><dt>**TS\_LF\_READWRITE**</dt> <dt>( 0x6 )</dt></span></span> </dl> | <span data-ttu-id="4cf7c-112">O documento tem um bloqueio de leitura/gravação e pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="4cf7c-112">The document has a read/write lock and can be modified.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="4cf7c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cf7c-113">Requirements</span></span>



| <span data-ttu-id="4cf7c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cf7c-114">Requirement</span></span> | <span data-ttu-id="4cf7c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4cf7c-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf7c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cf7c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4cf7c-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4cf7c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4cf7c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cf7c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4cf7c-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4cf7c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4cf7c-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4cf7c-120">Redistributable</span></span><br/>          | <span data-ttu-id="4cf7c-121">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4cf7c-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="4cf7c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4cf7c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cf7c-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cf7c-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="4cf7c-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="4cf7c-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4cf7c-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4cf7c-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cf7c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cf7c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf7c-127">Bloqueios de documentos</span><span class="sxs-lookup"><span data-stu-id="4cf7c-127">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="4cf7c-128">ITextStoreACP:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="4cf7c-128">ITextStoreACP::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[<span data-ttu-id="4cf7c-129">ITextStoreACPSink:: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="4cf7c-129">ITextStoreACPSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="4cf7c-130">ITextStoreAnchor:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="4cf7c-130">ITextStoreAnchor::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[<span data-ttu-id="4cf7c-131">ITextStoreAnchorSink:: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="4cf7c-131">ITextStoreAnchorSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> </dl>

 

 





