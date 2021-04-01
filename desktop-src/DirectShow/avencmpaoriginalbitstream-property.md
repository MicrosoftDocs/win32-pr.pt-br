---
description: Especifica a configuração padrão para o bit original no fluxo de áudio MPEG-1. Essa propriedade se aplica a codificadores de áudio MPEG.
ms.assetid: 62b56868-684f-4f28-90da-dac19cb07946
title: Propriedade AVEncMPAOriginalBitstream (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a49fda5bb605ac8735ebac4be758e7f73efb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825895"
---
# <a name="avencmpaoriginalbitstream-property"></a><span data-ttu-id="ad6d8-104">Propriedade AVEncMPAOriginalBitstream</span><span class="sxs-lookup"><span data-stu-id="ad6d8-104">AVEncMPAOriginalBitstream property</span></span>

<span data-ttu-id="ad6d8-105">Especifica a configuração padrão para o bit original no fluxo de áudio MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-105">Specifies the default setting for the original bit in the MPEG-1 audio stream.</span></span> <span data-ttu-id="ad6d8-106">Essa propriedade se aplica a codificadores de áudio MPEG.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="ad6d8-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ad6d8-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad6d8-108">Data type</span></span>

<span data-ttu-id="ad6d8-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="ad6d8-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ad6d8-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="ad6d8-110">Property GUID</span></span>

<span data-ttu-id="ad6d8-111">**CODECAPI \_ AVEncMPAOriginalBitstream**</span><span class="sxs-lookup"><span data-stu-id="ad6d8-111">**CODECAPI\_AVEncMPAOriginalBitstream**</span></span>

## <a name="property-value"></a><span data-ttu-id="ad6d8-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ad6d8-112">Property value</span></span>

<span data-ttu-id="ad6d8-113">Essa propriedade pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-113">This property can have the following values.</span></span>



| <span data-ttu-id="ad6d8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ad6d8-114">Value</span></span>          | <span data-ttu-id="ad6d8-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad6d8-115">Description</span></span>          |
|----------------|----------------------|
| <span data-ttu-id="ad6d8-116">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="ad6d8-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="ad6d8-117">O bit original está desativado.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-117">Original bit is off.</span></span> |
| <span data-ttu-id="ad6d8-118">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="ad6d8-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="ad6d8-119">O bit original está ativado.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-119">Original bit is on.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="ad6d8-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad6d8-120">Remarks</span></span>

<span data-ttu-id="ad6d8-121">O codificador pode substituir essa configuração, com base no conteúdo do fluxo de entrada.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-121">The encoder might override this setting, based on the contents of the input stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad6d8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad6d8-122">Requirements</span></span>



| <span data-ttu-id="ad6d8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad6d8-123">Requirement</span></span> | <span data-ttu-id="ad6d8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ad6d8-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad6d8-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad6d8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ad6d8-126">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ad6d8-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ad6d8-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad6d8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ad6d8-128">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ad6d8-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ad6d8-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad6d8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad6d8-130"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad6d8-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad6d8-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad6d8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad6d8-132">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="ad6d8-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ad6d8-133">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="ad6d8-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




