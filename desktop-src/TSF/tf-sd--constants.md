---
title: Constantes de TF_SD_ (msctf. h)
description: As \_ constantes TF SD \_ \ descrevem o status do documento.
ms.assetid: 953d39cd-8af1-4c86-8fb8-8b8ec917c631
topic_type:
- apiref
api_name:
- TF_SD_READONLY
- TF_SD_LOADING
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ed0d68c8a8afd9299b908eb81a04a31fbd3d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085230"
---
# <a name="tf_sd_-constants"></a><span data-ttu-id="59b96-103">TF \_ as \_ \* constantes do SD</span><span class="sxs-lookup"><span data-stu-id="59b96-103">TF\_SD\_\* Constants</span></span>

<span data-ttu-id="59b96-104">As \_ constantes TF SD \_ \* descrevem o status do documento.</span><span class="sxs-lookup"><span data-stu-id="59b96-104">The TF\_SD\_\* constants describe the document status.</span></span>



| <span data-ttu-id="59b96-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="59b96-105">Constant/value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="59b96-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="59b96-106">Description</span></span>                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <span data-ttu-id="59b96-107"><dt>**TF \_ SD \_ ReadOnly**</dt> <dt>(TS \_ SD \_ ReadOnly)</dt></span><span class="sxs-lookup"><span data-stu-id="59b96-107"><dt>**TF\_SD\_READONLY**</dt> <dt>( TS\_SD\_READONLY )</dt></span></span> </dl> | <span data-ttu-id="59b96-108">O documento é somente leitura e não pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="59b96-108">The document is read-only and cannot be modified.</span></span><br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <span data-ttu-id="59b96-109"><dt>**TF \_ \_carregamento de SD**</dt> <dt>( \_ carregamento de TS SD \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="59b96-109"><dt>**TF\_SD\_LOADING**</dt> <dt>( TS\_SD\_LOADING )</dt></span></span> </dl>     | <span data-ttu-id="59b96-110">O documento está sendo carregado e pode estar incompleto.</span><span class="sxs-lookup"><span data-stu-id="59b96-110">The document is loading and can be incomplete.</span></span><br/>    |



## <a name="remarks"></a><span data-ttu-id="59b96-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="59b96-111">Remarks</span></span>

<span data-ttu-id="59b96-112">O membro **dwDynamicFlags** da estrutura [de \_ status tf](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) usa essas constantes.</span><span class="sxs-lookup"><span data-stu-id="59b96-112">The **dwDynamicFlags** member of the [TF\_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b96-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59b96-113">Requirements</span></span>



| <span data-ttu-id="59b96-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="59b96-114">Requirement</span></span> | <span data-ttu-id="59b96-115">Valor</span><span class="sxs-lookup"><span data-stu-id="59b96-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="59b96-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59b96-116">Minimum supported client</span></span><br/> | <span data-ttu-id="59b96-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="59b96-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="59b96-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59b96-118">Minimum supported server</span></span><br/> | <span data-ttu-id="59b96-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="59b96-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="59b96-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="59b96-120">Redistributable</span></span><br/>          | <span data-ttu-id="59b96-121">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="59b96-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="59b96-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59b96-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="59b96-123"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="59b96-123"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="59b96-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="59b96-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="59b96-125"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="59b96-125"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59b96-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="59b96-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="59b96-127">[STATUS de TF \_](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="59b96-127">[TF\_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="59b96-128">Constantes de TS \_ SD \_ \*</span><span class="sxs-lookup"><span data-stu-id="59b96-128">TS\_SD\_\* Constants</span></span>](ts-sd--constants.md)
</dt> <dt>

[<span data-ttu-id="59b96-129">ITfContextOwner:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="59b96-129">ITfContextOwner::GetStatus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[<span data-ttu-id="59b96-130">ITfContextOwnerServices:: OnStatusChange</span><span class="sxs-lookup"><span data-stu-id="59b96-130">ITfContextOwnerServices::OnStatusChange</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[<span data-ttu-id="59b96-131">ITextStoreACP:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="59b96-131">ITextStoreACP::GetStatus</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[<span data-ttu-id="59b96-132">ITfStatusSunk:: OnStatusChange</span><span class="sxs-lookup"><span data-stu-id="59b96-132">ITfStatusSunk::OnStatusChange</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

