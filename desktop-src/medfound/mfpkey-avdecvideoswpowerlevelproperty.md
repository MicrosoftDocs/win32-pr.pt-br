---
description: Especifica o nível de energia para o decodificador.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: Propriedade MFPKEY_AVDecVideoSWPowerLevel (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2180e26d3e14263c14f2f3603c8c92cf8c11daec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763262"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a><span data-ttu-id="7aadd-103">\_Propriedade MFPKEY AVDecVideoSWPowerLevel</span><span class="sxs-lookup"><span data-stu-id="7aadd-103">MFPKEY\_AVDecVideoSWPowerLevel Property</span></span>

<span data-ttu-id="7aadd-104">Especifica o nível de energia para o decodificador.</span><span class="sxs-lookup"><span data-stu-id="7aadd-104">Specifies the power level for the decoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7aadd-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7aadd-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7aadd-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="7aadd-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="7aadd-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="7aadd-107">Data Type</span></span>

<span data-ttu-id="7aadd-108">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="7aadd-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="7aadd-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="7aadd-109">Default Value</span></span>

<span data-ttu-id="7aadd-110">**100**</span><span class="sxs-lookup"><span data-stu-id="7aadd-110">**100**</span></span>

## <a name="remarks"></a><span data-ttu-id="7aadd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7aadd-111">Remarks</span></span>

<span data-ttu-id="7aadd-112">Essa propriedade deve ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7aadd-112">This property must be set to one of the following values.</span></span>



| <span data-ttu-id="7aadd-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7aadd-113">Value</span></span> | <span data-ttu-id="7aadd-114">Significado</span><span class="sxs-lookup"><span data-stu-id="7aadd-114">Meaning</span></span>                                                             |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="7aadd-115">0</span><span class="sxs-lookup"><span data-stu-id="7aadd-115">0</span></span>     | <span data-ttu-id="7aadd-116">O decodificador usa um nível de energia que é otimizado para a vida útil da bateria.</span><span class="sxs-lookup"><span data-stu-id="7aadd-116">The decoder uses a power level that is optimized for battery life.</span></span>  |
| <span data-ttu-id="7aadd-117">50</span><span class="sxs-lookup"><span data-stu-id="7aadd-117">50</span></span>    | <span data-ttu-id="7aadd-118">O decodificador usa um nível de energia equilibrado.</span><span class="sxs-lookup"><span data-stu-id="7aadd-118">The decoder uses a balanced power level.</span></span>                            |
| <span data-ttu-id="7aadd-119">100</span><span class="sxs-lookup"><span data-stu-id="7aadd-119">100</span></span>   | <span data-ttu-id="7aadd-120">O decodificador usa um nível de energia otimizado para qualidade de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7aadd-120">The decoder uses a power level that is optimized for video quality.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7aadd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7aadd-121">Requirements</span></span>



| <span data-ttu-id="7aadd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aadd-122">Requirement</span></span> | <span data-ttu-id="7aadd-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7aadd-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7aadd-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7aadd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7aadd-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7aadd-125">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="7aadd-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7aadd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7aadd-127">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="7aadd-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7aadd-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7aadd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7aadd-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7aadd-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aadd-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7aadd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aadd-131">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7aadd-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
