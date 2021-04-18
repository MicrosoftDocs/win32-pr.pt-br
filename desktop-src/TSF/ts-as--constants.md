---
title: Constantes de TS_AS_ (Textstor. h)
description: Os sinalizadores a seguir especificam os eventos que chamam os métodos AdviseSink.
ms.assetid: 8f406b67-f846-4712-b4be-811dbcc6ad55
topic_type:
- apiref
api_name:
- TS_AS_TEXT_CHANGE
- TS_AS_SEL_CHANGE
- TS_AS_LAYOUT_CHANGE
- TS_AS_ATTR_CHANGE
- TS_AS_STATUS_CHANGE
- TS_AS_ALL_SINKS
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b36bdc2c3b559693503b2a8e408a0782855f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758124"
---
# <a name="ts_as_-constants"></a><span data-ttu-id="348e5-103">TS \_ como \_ \* constantes</span><span class="sxs-lookup"><span data-stu-id="348e5-103">TS\_AS\_\* Constants</span></span>

<span data-ttu-id="348e5-104">Os sinalizadores a seguir especificam os eventos que chamam os métodos **AdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="348e5-104">The following flags specify the events that call the **AdviseSink** methods.</span></span>



| <span data-ttu-id="348e5-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="348e5-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="348e5-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="348e5-106">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <span data-ttu-id="348e5-107"><dt>**TS \_ \_ \_ Alteração de texto as**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="348e5-107"><dt>**TS\_AS\_TEXT\_CHANGE**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                                                                                               | <span data-ttu-id="348e5-108">O texto é alterado no documento.</span><span class="sxs-lookup"><span data-stu-id="348e5-108">Text is changed in the document.</span></span><br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <span data-ttu-id="348e5-109"><dt>**TS \_ \_ \_ Alteração de SEL**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="348e5-109"><dt>**TS\_AS\_SEL\_CHANGE**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="348e5-110">O texto é selecionado no documento.</span><span class="sxs-lookup"><span data-stu-id="348e5-110">Text is selected in the document.</span></span><br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <span data-ttu-id="348e5-111"><dt>**TS \_ COMO \_ \_ alteração de layout**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="348e5-111"><dt>**TS\_AS\_LAYOUT\_CHANGE**</dt> <dt>( 0x4 )</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="348e5-112">O layout do documento é alterado.</span><span class="sxs-lookup"><span data-stu-id="348e5-112">The layout of the document is changed.</span></span><br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <span data-ttu-id="348e5-113"><dt>**TS \_ COMO \_ \_ alteração de attr**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="348e5-113"><dt>**TS\_AS\_ATTR\_CHANGE**</dt> <dt>( 0x8 )</dt></span></span> </dl>                                                                                                               | <span data-ttu-id="348e5-114">Os atributos do documento são alterados.</span><span class="sxs-lookup"><span data-stu-id="348e5-114">The attributes of the document is changed.</span></span><br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <span data-ttu-id="348e5-115"><dt>**TS \_ COMO \_ \_ alteração de status**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="348e5-115"><dt>**TS\_AS\_STATUS\_CHANGE**</dt> <dt>( 0x10 )</dt></span></span> </dl>                                                                                                        | <span data-ttu-id="348e5-116">O status do documento é alterado.</span><span class="sxs-lookup"><span data-stu-id="348e5-116">The status of the document is changed.</span></span><br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <span data-ttu-id="348e5-117"><dt>**TS \_ COMO \_ todos os \_ coletores**</dt> <dt>(TS \_ como \_ texto \_ alteram \| o TS \_ como SEL alterar TS como alteração de layout TS como attr, altere \_ \_ \| \_ \_ \_ \| \_ \_ \_ \| TS \_ como alteração de \_ status \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="348e5-117"><dt>**TS\_AS\_ALL\_SINKS**</dt> <dt>( TS\_AS\_TEXT\_CHANGE \| TS\_AS\_SEL\_CHANGE \| TS\_AS\_LAYOUT\_CHANGE \| TS\_AS\_ATTR\_CHANGE \| TS\_AS\_STATUS\_CHANGE )</dt></span></span> </dl> | <span data-ttu-id="348e5-118">Um dos quatro eventos anteriores ocorreu no documento.</span><span class="sxs-lookup"><span data-stu-id="348e5-118">One of the previous four events occurred in the document.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="348e5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="348e5-119">Requirements</span></span>



| <span data-ttu-id="348e5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="348e5-120">Requirement</span></span> | <span data-ttu-id="348e5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="348e5-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="348e5-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="348e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="348e5-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="348e5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="348e5-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="348e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="348e5-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="348e5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="348e5-126">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="348e5-126">Redistributable</span></span><br/>          | <span data-ttu-id="348e5-127">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="348e5-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="348e5-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="348e5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="348e5-129"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="348e5-129"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="348e5-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="348e5-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="348e5-131"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="348e5-131"><dt>Textstor.idl</dt></span></span> </dl> |



 

 





