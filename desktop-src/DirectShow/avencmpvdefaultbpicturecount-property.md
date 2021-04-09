---
description: Especifica o número padrão de quadros B consecutivos entre quadros I e P.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Propriedade AVEncMPVDefaultBPictureCount (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2026ddcb6a2b4ce813bd8ba2f6144f0c4a32344
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010029"
---
# <a name="avencmpvdefaultbpicturecount-property"></a><span data-ttu-id="0d4d8-103">Propriedade AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="0d4d8-103">AVEncMPVDefaultBPictureCount property</span></span>

<span data-ttu-id="0d4d8-104">Especifica o número padrão de quadros B consecutivos entre quadros I e P.</span><span class="sxs-lookup"><span data-stu-id="0d4d8-104">Specifies the default number of consecutive B frames between I and P frames.</span></span>

<span data-ttu-id="0d4d8-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0d4d8-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="0d4d8-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0d4d8-106">Data type</span></span>

<span data-ttu-id="0d4d8-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="0d4d8-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="0d4d8-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="0d4d8-108">Property GUID</span></span>

<span data-ttu-id="0d4d8-109">**CODECAPI \_ AVEncMPVDefaultBPictureCount**</span><span class="sxs-lookup"><span data-stu-id="0d4d8-109">**CODECAPI\_AVEncMPVDefaultBPictureCount**</span></span>

## <a name="property-value"></a><span data-ttu-id="0d4d8-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0d4d8-110">Property value</span></span>

<span data-ttu-id="0d4d8-111">Esta propriedade tem um intervalo linear de valores.</span><span class="sxs-lookup"><span data-stu-id="0d4d8-111">This property has a linear range of values.</span></span> <span data-ttu-id="0d4d8-112">Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="0d4d8-112">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="0d4d8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d4d8-113">Remarks</span></span>

<span data-ttu-id="0d4d8-114">Antes do Windows 8, essa propriedade se aplica aos codificadores de vídeo MPEG.</span><span class="sxs-lookup"><span data-stu-id="0d4d8-114">Prior to Windows 8, this property applies to MPEG video encoders.</span></span> <span data-ttu-id="0d4d8-115">A partir do Windows 8, essa propriedade é usada por codificadores de vídeo MPEG, WMV e H. 264.</span><span class="sxs-lookup"><span data-stu-id="0d4d8-115">Starting with Windows 8, this property is used by MPEG, WMV, and H.264 video encoders.</span></span>

<span data-ttu-id="0d4d8-116">Se o codificador der suporte a essa propriedade, ele poderá ser usado para controlar a estrutura do grupo de imagens (GOP).</span><span class="sxs-lookup"><span data-stu-id="0d4d8-116">If the encoder supports this property, it can be used to control the group of pictures (GOP) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d4d8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d4d8-117">Requirements</span></span>



| <span data-ttu-id="0d4d8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d4d8-118">Requirement</span></span> | <span data-ttu-id="0d4d8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0d4d8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4d8-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d4d8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d4d8-121">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0d4d8-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="0d4d8-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d4d8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d4d8-123">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0d4d8-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0d4d8-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d4d8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d4d8-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d4d8-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d4d8-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d4d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d4d8-127">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="0d4d8-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="0d4d8-128">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="0d4d8-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




