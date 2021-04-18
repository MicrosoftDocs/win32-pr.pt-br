---
description: Especifica o nível de economia de energia de um decodificador de vídeo.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: Propriedade AVDecVideoSWPowerLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1196c45cf038085856b1d63a5cd3a1c7dc350d0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105756833"
---
# <a name="avdecvideoswpowerlevel-property"></a><span data-ttu-id="5e25d-103">Propriedade AVDecVideoSWPowerLevel</span><span class="sxs-lookup"><span data-stu-id="5e25d-103">AVDecVideoSWPowerLevel property</span></span>

<span data-ttu-id="5e25d-104">Especifica o nível de economia de energia de um decodificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5e25d-104">Specifies the power-saving level of a video decoder.</span></span>

<span data-ttu-id="5e25d-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5e25d-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="5e25d-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5e25d-106">Data type</span></span>

<span data-ttu-id="5e25d-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="5e25d-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5e25d-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="5e25d-108">Property GUID</span></span>

<span data-ttu-id="5e25d-109">**CODECAPI \_ AVDecVideoSWPowerLevel**</span><span class="sxs-lookup"><span data-stu-id="5e25d-109">**CODECAPI\_AVDecVideoSWPowerLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="5e25d-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5e25d-110">Property value</span></span>

<span data-ttu-id="5e25d-111">O intervalo de valores possíveis é \[ 0.. 100 \] , inclusive, com o significado a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e25d-111">The range of possible values is \[0..100\], inclusive, with the following meaning.</span></span>



| <span data-ttu-id="5e25d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5e25d-112">Value</span></span> | <span data-ttu-id="5e25d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e25d-113">Description</span></span>                 |
|-------|-----------------------------|
| <span data-ttu-id="5e25d-114">0</span><span class="sxs-lookup"><span data-stu-id="5e25d-114">0</span></span>     | <span data-ttu-id="5e25d-115">Otimizar para a vida útil da bateria.</span><span class="sxs-lookup"><span data-stu-id="5e25d-115">Optimize for battery life.</span></span>  |
| <span data-ttu-id="5e25d-116">100</span><span class="sxs-lookup"><span data-stu-id="5e25d-116">100</span></span>   | <span data-ttu-id="5e25d-117">Otimizar para qualidade de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5e25d-117">Optimize for video quality.</span></span> |



 

<span data-ttu-id="5e25d-118">A enumeração [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) define algumas constantes específicas dentro desse intervalo.</span><span class="sxs-lookup"><span data-stu-id="5e25d-118">The [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) enumeration defines some specific constants within this range.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e25d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e25d-119">Remarks</span></span>

<span data-ttu-id="5e25d-120">Você pode definir essa propriedade durante a reprodução para alterar o nível de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="5e25d-120">You can set this property during playback to change the pwoer-saving level.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e25d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e25d-121">Requirements</span></span>



| <span data-ttu-id="5e25d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e25d-122">Requirement</span></span> | <span data-ttu-id="5e25d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5e25d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e25d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e25d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5e25d-125">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5e25d-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="5e25d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e25d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5e25d-127">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5e25d-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5e25d-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e25d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e25d-129"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e25d-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e25d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e25d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e25d-131">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="5e25d-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="5e25d-132">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="5e25d-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




