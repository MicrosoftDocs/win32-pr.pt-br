---
title: Constantes de TS_IAS_ (Textstor. h)
description: As constantes do TS \_ ias \_ \ são usadas como sinalizadores de campo de bits para controlar a inserção de texto ou de objetos inseridos em uma seleção ou ponto de inserção.
ms.assetid: 58e0d13c-d90c-41d2-bd93-4eba5fe0a69a
topic_type:
- apiref
api_name:
- TS_IAS_NOQUERY
- TS_IAS_QUERYONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d59584295567c586ebd8db7e5f63366fd8272f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085601"
---
# <a name="ts_ias_-constants"></a><span data-ttu-id="4c7c2-103">Constantes do TS \_ ias \_ \*</span><span class="sxs-lookup"><span data-stu-id="4c7c2-103">TS\_IAS\_\* Constants</span></span>

<span data-ttu-id="4c7c2-104">As \_ constantes TS ias \_ \* são usadas como sinalizadores de campo de bits para controlar a inserção de texto ou de objetos inseridos em uma seleção ou ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="4c7c2-104">The TS\_IAS\_\* constants are used as bitfield flags to control insertion of text or embedded objects at a selection or insertion point.</span></span>



| <span data-ttu-id="4c7c2-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="4c7c2-105">Constant/value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="4c7c2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c7c2-106">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IAS_NOQUERY"></span><span id="ts_ias_noquery"></span><dl> <span data-ttu-id="4c7c2-107"><dt>**TS \_ \_NoConsulta do IAS**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="4c7c2-107"><dt>**TS\_IAS\_NOQUERY**</dt> <dt>( 0x1 )</dt></span></span> </dl>       | <span data-ttu-id="4c7c2-108">O texto é inserido e o ponteiro de intervalo é definido como **nulo** na saída.</span><span class="sxs-lookup"><span data-stu-id="4c7c2-108">Text is inserted and the range pointer is set to **NULL** upon exit.</span></span> <span data-ttu-id="4c7c2-109">Não pode ser combinado com o \_ sinalizador TS QUERYONLY do IAS \_ .</span><span class="sxs-lookup"><span data-stu-id="4c7c2-109">Cannot be combined with the TS\_IAS\_QUERYONLY flag.</span></span><br/>          |
| <span id="TS_IAS_QUERYONLY"></span><span id="ts_ias_queryonly"></span><dl> <span data-ttu-id="4c7c2-110"><dt>**TS \_ \_QUERYONLY**</dt> <dt>(0X2) do</dt> ias</span><span class="sxs-lookup"><span data-stu-id="4c7c2-110"><dt>**TS\_IAS\_QUERYONLY**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="4c7c2-111">Não execute a inserção.</span><span class="sxs-lookup"><span data-stu-id="4c7c2-111">Do not perform the insertion.</span></span> <span data-ttu-id="4c7c2-112">O chamador requer apenas o ponteiro de intervalo a ser definido.</span><span class="sxs-lookup"><span data-stu-id="4c7c2-112">Caller only requires the range pointer to be set.</span></span> <span data-ttu-id="4c7c2-113">Não pode ser combinado com o \_ \_ sinalizador noquery ias TS.</span><span class="sxs-lookup"><span data-stu-id="4c7c2-113">Cannot be combined with the TS\_IAS\_NOQUERY flag.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4c7c2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c7c2-114">Requirements</span></span>



| <span data-ttu-id="4c7c2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c7c2-115">Requirement</span></span> | <span data-ttu-id="4c7c2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4c7c2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c7c2-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c7c2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4c7c2-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c7c2-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4c7c2-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c7c2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4c7c2-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c7c2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4c7c2-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4c7c2-121">Redistributable</span></span><br/>          | <span data-ttu-id="4c7c2-122">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4c7c2-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="4c7c2-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c7c2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c7c2-124"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c7c2-124"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c7c2-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="4c7c2-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4c7c2-126"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4c7c2-126"><dt>Textstor.idl</dt></span></span> </dl> |



 

 





