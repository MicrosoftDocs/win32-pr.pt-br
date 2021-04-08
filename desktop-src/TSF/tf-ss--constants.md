---
title: Constantes de TF_SS_ (msctf. h)
description: O TF \_ SS \_ \ Constants, definido antes do tempo de execução na estrutura de status de TF \_ , descreve os Estados de documento estático.
ms.assetid: 371aeeda-f081-4506-ba51-79c6a8bc8768
topic_type:
- apiref
api_name:
- TF_SS_DISJOINTSEL
- TF_SS_REGIONS
- TF_SS_TRANSITORY
- TF_SS_TKBAUTOCORRECTENABLE
- TF_SS_TKBPREDICTIONENABLE
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1028b78e74ed10c572feb904baa8ec395087ee3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009472"
---
# <a name="tf_ss_-constants"></a><span data-ttu-id="c3559-103">Constantes de TF \_ SS \_ \*</span><span class="sxs-lookup"><span data-stu-id="c3559-103">TF\_SS\_\* Constants</span></span>

<span data-ttu-id="c3559-104">As \_ constantes TF SS \_ \* , definidas antes do tempo de execução na estrutura de [**\_ status de TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) , descrevem os Estados de documento estático.</span><span class="sxs-lookup"><span data-stu-id="c3559-104">The TF\_SS\_\* constants, defined before run time in the [**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) structure, describe static document states.</span></span>



| <span data-ttu-id="c3559-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="c3559-105">Constant/value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="c3559-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3559-106">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <span data-ttu-id="c3559-107"><dt>**TF \_ SS \_ DISJOINTSEL**</dt> <dt>(TS \_ SS \_ DISJOINTSEL)</dt></span><span class="sxs-lookup"><span data-stu-id="c3559-107"><dt>**TF\_SS\_DISJOINTSEL**</dt> <dt>( TS\_SS\_DISJOINTSEL )</dt></span></span> </dl>                                     | <span data-ttu-id="c3559-108">O documento dá suporte a várias seleções.</span><span class="sxs-lookup"><span data-stu-id="c3559-108">The document supports multiple selections.</span></span><br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <span data-ttu-id="c3559-109"><dt>**TF \_ \_regiões do SS**</dt> <dt>( \_ regiões do TS SS \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="c3559-109"><dt>**TF\_SS\_REGIONS**</dt> <dt>( TS\_SS\_REGIONS )</dt></span></span> </dl>                                                     | <span data-ttu-id="c3559-110">O documento pode conter várias regiões.</span><span class="sxs-lookup"><span data-stu-id="c3559-110">The document can contain multiple regions.</span></span><br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <span data-ttu-id="c3559-111"><dt>**TF \_ \_transitório de SS**</dt> <dt>(transitório de TS \_ SS \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="c3559-111"><dt>**TF\_SS\_TRANSITORY**</dt> <dt>( TS\_SS\_TRANSITORY )</dt></span></span> </dl>                                         | <span data-ttu-id="c3559-112">Espera-se que o documento tenha um pequeno ciclo de uso.</span><span class="sxs-lookup"><span data-stu-id="c3559-112">The document is expected to have a short usage cycle.</span></span><br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <span data-ttu-id="c3559-113"><dt>**TF \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(TS \_ SS \_ TKBAUTOCORRECTENABLE)</dt></span><span class="sxs-lookup"><span data-stu-id="c3559-113"><dt>**TF\_SS\_TKBAUTOCORRECTENABLE**</dt> <dt>( TS\_SS\_TKBAUTOCORRECTENABLE )</dt></span></span> </dl> | <span data-ttu-id="c3559-114">**A partir do Windows 8:** O documento dá suporte à correção automática fornecida pelo teclado de toque.</span><span class="sxs-lookup"><span data-stu-id="c3559-114">**Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard.</span></span><br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <span data-ttu-id="c3559-115"><dt>**TF \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(TS \_ SS \_ TKBPREDICTIONENABLE)</dt></span><span class="sxs-lookup"><span data-stu-id="c3559-115"><dt>**TF\_SS\_TKBPREDICTIONENABLE**</dt> <dt>( TS\_SS\_TKBPREDICTIONENABLE )</dt></span></span> </dl>     | <span data-ttu-id="c3559-116">**A partir do Windows 8:** O documento dá suporte a sugestões de texto fornecidas pelo teclado de toque.</span><span class="sxs-lookup"><span data-stu-id="c3559-116">**Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c3559-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3559-117">Remarks</span></span>

<span data-ttu-id="c3559-118">O membro **dwStaticFlags** da estrutura de \_ status tf usa essas constantes.</span><span class="sxs-lookup"><span data-stu-id="c3559-118">The **dwStaticFlags** member of the TF\_STATUS structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3559-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3559-119">Requirements</span></span>



| <span data-ttu-id="c3559-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3559-120">Requirement</span></span> | <span data-ttu-id="c3559-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c3559-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c3559-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3559-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c3559-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c3559-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c3559-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3559-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c3559-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c3559-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c3559-126">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c3559-126">Redistributable</span></span><br/>          | <span data-ttu-id="c3559-127">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c3559-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="c3559-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3559-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3559-129"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3559-129"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="c3559-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="c3559-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c3559-131"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c3559-131"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3559-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3559-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="c3559-133">[**STATUS de TF \_**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c3559-133">[**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> </dl>

 

