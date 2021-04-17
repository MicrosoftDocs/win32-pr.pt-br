---
title: Constantes de TS_SS_ (Textstor. h)
description: As \_ constantes TS SS \_ , definidas antes do tempo de execução na \_ estrutura de status TS, descrevem os Estados de documento estático.
ms.assetid: 17264527-946a-4648-a4eb-30db751602ab
topic_type:
- apiref
api_name:
- TS_SS_DISJOINTSEL
- TS_SS_REGIONS
- TS_SS_TRANSITORY
- TS_SS_NOHIDDENTEXT
- TS_SS_TKBAUTOCORRECTENABLE
- TS_SS_TKBPREDICTIONENABLE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773645b8a75b7e8eeafa40ed9fa95067743628d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760172"
---
# <a name="ts_ss_-constants"></a><span data-ttu-id="ee46c-103">Constantes do TS \_ SS \_ \*</span><span class="sxs-lookup"><span data-stu-id="ee46c-103">TS\_SS\_\* Constants</span></span>

<span data-ttu-id="ee46c-104">As constantes do TS \_ SS \_ \* , definidas antes do tempo de execução na estrutura de [**\_ status do TS**](/windows/desktop/api/Textstor/ns-textstor-ts_status) , descrevem os Estados de documento estático.</span><span class="sxs-lookup"><span data-stu-id="ee46c-104">The TS\_SS\_\* constants, defined before run time in the [**TS\_STATUS**](/windows/desktop/api/Textstor/ns-textstor-ts_status) structure, describe static document states.</span></span>



| <span data-ttu-id="ee46c-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="ee46c-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="ee46c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee46c-106">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TS_SS_DISJOINTSEL"></span><span id="ts_ss_disjointsel"></span><dl> <span data-ttu-id="ee46c-107"><dt>**TS \_ SS \_ DISJOINTSEL**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="ee46c-107"><dt>**TS\_SS\_DISJOINTSEL**</dt> <dt>( 0x1 )</dt></span></span> </dl>                             | <span data-ttu-id="ee46c-108">O documento dá suporte a várias seleções.</span><span class="sxs-lookup"><span data-stu-id="ee46c-108">The document supports multiple selections.</span></span><br/>                                                          |
| <span id="TS_SS_REGIONS"></span><span id="ts_ss_regions"></span><dl> <span data-ttu-id="ee46c-109"><dt>**TS \_ \_Regiões SS**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="ee46c-109"><dt>**TS\_SS\_REGIONS**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                         | <span data-ttu-id="ee46c-110">O documento pode conter várias regiões.</span><span class="sxs-lookup"><span data-stu-id="ee46c-110">The document can contain multiple regions.</span></span><br/>                                                          |
| <span id="TS_SS_TRANSITORY"></span><span id="ts_ss_transitory"></span><dl> <span data-ttu-id="ee46c-111"><dt>**TS \_ \_Transitória de SS**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="ee46c-111"><dt>**TS\_SS\_TRANSITORY**</dt> <dt>( 0x4 )</dt></span></span> </dl>                                | <span data-ttu-id="ee46c-112">Espera-se que o documento tenha um pequeno ciclo de uso.</span><span class="sxs-lookup"><span data-stu-id="ee46c-112">The document is expected to have a short usage cycle.</span></span><br/>                                               |
| <span id="TS_SS_NOHIDDENTEXT"></span><span id="ts_ss_nohiddentext"></span><dl> <span data-ttu-id="ee46c-113"><dt>**TS \_ SS \_ NOHIDDENTEXT**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="ee46c-113"><dt>**TS\_SS\_NOHIDDENTEXT**</dt> <dt>( 0x8 )</dt></span></span> </dl>                          | <span data-ttu-id="ee46c-114">O documento nunca conterá texto oculto.</span><span class="sxs-lookup"><span data-stu-id="ee46c-114">The document will never contain hidden text.</span></span><br/>                                                        |
| <span id="TS_SS_TKBAUTOCORRECTENABLE"></span><span id="ts_ss_tkbautocorrectenable"></span><dl> <span data-ttu-id="ee46c-115"><dt>**TS \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="ee46c-115"><dt>**TS\_SS\_TKBAUTOCORRECTENABLE**</dt> <dt>( 0x10 )</dt></span></span> </dl> | <span data-ttu-id="ee46c-116">**A partir do Windows 8:** O documento dá suporte à correção automática fornecida pelo teclado de toque.</span><span class="sxs-lookup"><span data-stu-id="ee46c-116">**Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard.</span></span><br/>   |
| <span id="TS_SS_TKBPREDICTIONENABLE"></span><span id="ts_ss_tkbpredictionenable"></span><dl> <span data-ttu-id="ee46c-117"><dt>**TS \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="ee46c-117"><dt>**TS\_SS\_TKBPREDICTIONENABLE**</dt> <dt>( 0x20 )</dt></span></span> </dl>    | <span data-ttu-id="ee46c-118">**A partir do Windows 8:** O documento dá suporte a sugestões de texto fornecidas pelo teclado de toque.</span><span class="sxs-lookup"><span data-stu-id="ee46c-118">**Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ee46c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee46c-119">Remarks</span></span>

<span data-ttu-id="ee46c-120">O membro **dwStaticFlags** da estrutura **de \_ status TS** usa essas constantes.</span><span class="sxs-lookup"><span data-stu-id="ee46c-120">The **dwStaticFlags** member of the **TS\_STATUS** structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee46c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee46c-121">Requirements</span></span>



| <span data-ttu-id="ee46c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee46c-122">Requirement</span></span> | <span data-ttu-id="ee46c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ee46c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee46c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee46c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ee46c-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee46c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ee46c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee46c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ee46c-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee46c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee46c-128">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ee46c-128">Redistributable</span></span><br/>          | <span data-ttu-id="ee46c-129">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ee46c-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="ee46c-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee46c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee46c-131"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee46c-131"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee46c-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="ee46c-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ee46c-133"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ee46c-133"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee46c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee46c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee46c-135">**STATUS de TS \_**</span><span class="sxs-lookup"><span data-stu-id="ee46c-135">**TS\_STATUS**</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

<span data-ttu-id="ee46c-136">[**STATUS de TF \_**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ee46c-136">[**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> </dl>

 

