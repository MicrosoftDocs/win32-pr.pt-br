---
description: Especifica se o codificador produz grupos abertos de imagens (GOPS segundos) ou GOPS segundos fechado. Essa propriedade se aplica a codificadores de vídeo MPEG.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: Propriedade AVEncMPVGOPOpen (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd971a6cc9926245b97794868f58758af814803
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646006"
---
# <a name="avencmpvgopopen-property"></a><span data-ttu-id="83157-104">Propriedade AVEncMPVGOPOpen</span><span class="sxs-lookup"><span data-stu-id="83157-104">AVEncMPVGOPOpen property</span></span>

<span data-ttu-id="83157-105">Especifica se o codificador produz grupos abertos de imagens (GOPS segundos) ou GOPS segundos fechado.</span><span class="sxs-lookup"><span data-stu-id="83157-105">Specifies whether the encoder produces open groups of pictures (GOPs) or closed GOPs.</span></span> <span data-ttu-id="83157-106">Essa propriedade se aplica a codificadores de vídeo MPEG.</span><span class="sxs-lookup"><span data-stu-id="83157-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="83157-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="83157-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="83157-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="83157-108">Data type</span></span>

<span data-ttu-id="83157-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="83157-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="83157-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="83157-110">Property GUID</span></span>

<span data-ttu-id="83157-111">**CODECAPI \_ AVEncMPVGOPOpen**</span><span class="sxs-lookup"><span data-stu-id="83157-111">**CODECAPI\_AVEncMPVGOPOpen**</span></span>

## <a name="property-value"></a><span data-ttu-id="83157-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="83157-112">Property value</span></span>



| <span data-ttu-id="83157-113">Valor</span><span class="sxs-lookup"><span data-stu-id="83157-113">Value</span></span>          | <span data-ttu-id="83157-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="83157-114">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="83157-115">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="83157-115">VARIANT\_FALSE</span></span> | <span data-ttu-id="83157-116">GOPS segundos fechado</span><span class="sxs-lookup"><span data-stu-id="83157-116">Closed GOPs</span></span> |
| <span data-ttu-id="83157-117">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="83157-117">VARIANT\_TRUE</span></span>  | <span data-ttu-id="83157-118">Abrir GOPS segundos</span><span class="sxs-lookup"><span data-stu-id="83157-118">Open GOPs</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="83157-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="83157-119">Remarks</span></span>

<span data-ttu-id="83157-120">Um GOP aberto contém quadros Delta que fazem referência a quadros do GOP anterior.</span><span class="sxs-lookup"><span data-stu-id="83157-120">An open GOP contains delta frames that reference frames from the previous GOP.</span></span> <span data-ttu-id="83157-121">Um GOP fechado não contém nenhum quadro Delta que referencie o GOP anterior.</span><span class="sxs-lookup"><span data-stu-id="83157-121">A closed GOP does not contain any delta frames that reference the previous GOP.</span></span>

## <a name="requirements"></a><span data-ttu-id="83157-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83157-122">Requirements</span></span>



| <span data-ttu-id="83157-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="83157-123">Requirement</span></span> | <span data-ttu-id="83157-124">Valor</span><span class="sxs-lookup"><span data-stu-id="83157-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83157-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83157-125">Minimum supported client</span></span><br/> | <span data-ttu-id="83157-126">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="83157-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="83157-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83157-127">Minimum supported server</span></span><br/> | <span data-ttu-id="83157-128">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="83157-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="83157-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="83157-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="83157-130"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="83157-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83157-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="83157-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83157-132">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="83157-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="83157-133">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="83157-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




