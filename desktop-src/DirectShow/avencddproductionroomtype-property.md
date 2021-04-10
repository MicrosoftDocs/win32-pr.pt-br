---
description: Especifica o tipo de sala para um fluxo de áudio Dolby Digital. Essa propriedade se aplica aos codificadores Dolby Digital Audio.
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: Propriedade AVEncDDProductionRoomType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087832"
---
# <a name="avencddproductionroomtype-property"></a><span data-ttu-id="77207-104">Propriedade AVEncDDProductionRoomType</span><span class="sxs-lookup"><span data-stu-id="77207-104">AVEncDDProductionRoomType property</span></span>

<span data-ttu-id="77207-105">Especifica o tipo de sala para um fluxo de áudio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="77207-105">Specifies the room type for a Dolby Digital audio stream.</span></span> <span data-ttu-id="77207-106">Essa propriedade se aplica aos codificadores Dolby Digital Audio.</span><span class="sxs-lookup"><span data-stu-id="77207-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="77207-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="77207-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="77207-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="77207-108">Data type</span></span>

<span data-ttu-id="77207-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="77207-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="77207-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="77207-110">Property GUID</span></span>

<span data-ttu-id="77207-111">**CODECAPI \_ AVEncDDProductionRoomType**</span><span class="sxs-lookup"><span data-stu-id="77207-111">**CODECAPI\_AVEncDDProductionRoomType**</span></span>

## <a name="property-value"></a><span data-ttu-id="77207-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="77207-112">Property value</span></span>

<span data-ttu-id="77207-113">O valor dessa propriedade é um membro da enumeração [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) .</span><span class="sxs-lookup"><span data-stu-id="77207-113">The value of this property is a member of the [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="77207-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="77207-114">Remarks</span></span>

<span data-ttu-id="77207-115">*Tipo de sala* refere-se ao tamanho da sala usada durante a produção.</span><span class="sxs-lookup"><span data-stu-id="77207-115">*Room type* refers to the size of the room used during production.</span></span> <span data-ttu-id="77207-116">Se você definir essa propriedade, defina a propriedade [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="77207-116">If you set this property, set the [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) property to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="77207-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77207-117">Requirements</span></span>



| <span data-ttu-id="77207-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="77207-118">Requirement</span></span> | <span data-ttu-id="77207-119">Valor</span><span class="sxs-lookup"><span data-stu-id="77207-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77207-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77207-120">Minimum supported client</span></span><br/> | <span data-ttu-id="77207-121">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="77207-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="77207-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77207-122">Minimum supported server</span></span><br/> | <span data-ttu-id="77207-123">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="77207-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="77207-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77207-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="77207-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="77207-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77207-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="77207-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77207-127">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="77207-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="77207-128">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="77207-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

