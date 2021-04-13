---
description: Especifica a configuração padrão para o bit de direitos autorais no fluxo de áudio MPEG-1. Essa propriedade se aplica a codificadores de áudio MPEG.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Propriedade AVEncMPACopyright (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4449c41448d59ce673e667be7400d4a713236dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370270"
---
# <a name="avencmpacopyright-property"></a><span data-ttu-id="8a97c-104">Propriedade AVEncMPACopyright</span><span class="sxs-lookup"><span data-stu-id="8a97c-104">AVEncMPACopyright property</span></span>

<span data-ttu-id="8a97c-105">Especifica a configuração padrão para o bit de direitos autorais no fluxo de áudio MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="8a97c-105">Specifies the default setting for the copyright bit in the MPEG-1 audio stream.</span></span> <span data-ttu-id="8a97c-106">Essa propriedade se aplica a codificadores de áudio MPEG.</span><span class="sxs-lookup"><span data-stu-id="8a97c-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="8a97c-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8a97c-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="8a97c-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8a97c-108">Data type</span></span>

<span data-ttu-id="8a97c-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="8a97c-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8a97c-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="8a97c-110">Property GUID</span></span>

<span data-ttu-id="8a97c-111">**CODECAPI \_ AVEncMPACopyright**</span><span class="sxs-lookup"><span data-stu-id="8a97c-111">**CODECAPI\_AVEncMPACopyright**</span></span>

## <a name="property-value"></a><span data-ttu-id="8a97c-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8a97c-112">Property value</span></span>

<span data-ttu-id="8a97c-113">Essa propriedade pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a97c-113">This property can have the following values.</span></span>



| <span data-ttu-id="8a97c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8a97c-114">Value</span></span>          | <span data-ttu-id="8a97c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a97c-115">Description</span></span>           |
|----------------|-----------------------|
| <span data-ttu-id="8a97c-116">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="8a97c-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="8a97c-117">O bit de Copyright está desativado.</span><span class="sxs-lookup"><span data-stu-id="8a97c-117">Copyright bit is off.</span></span> |
| <span data-ttu-id="8a97c-118">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="8a97c-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="8a97c-119">O bit de Copyright está ativado.</span><span class="sxs-lookup"><span data-stu-id="8a97c-119">Copyright bit is on.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="8a97c-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a97c-120">Remarks</span></span>

<span data-ttu-id="8a97c-121">O codificador pode substituir essa configuração, com base no conteúdo do fluxo de entrada.</span><span class="sxs-lookup"><span data-stu-id="8a97c-121">The encoder might override this setting, based on the contents of the input stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a97c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a97c-122">Requirements</span></span>



| <span data-ttu-id="8a97c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a97c-123">Requirement</span></span> | <span data-ttu-id="8a97c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8a97c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a97c-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a97c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8a97c-126">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8a97c-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8a97c-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a97c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8a97c-128">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8a97c-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8a97c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a97c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a97c-130"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a97c-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a97c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a97c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a97c-132">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="8a97c-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="8a97c-133">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="8a97c-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




