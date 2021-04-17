---
description: Especifica se o codec usará o filtro de ruído durante a codificação.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: Propriedade MFPKEY_DENOISEOPTION (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f318e294f69095758fe300fce19043c23cf376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747866"
---
# <a name="mfpkey_denoiseoption-property"></a><span data-ttu-id="62584-103">\_Propriedade MFPKEY DENOISEOPTION</span><span class="sxs-lookup"><span data-stu-id="62584-103">MFPKEY\_DENOISEOPTION Property</span></span>

<span data-ttu-id="62584-104">Especifica se o codec usará o filtro de ruído durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="62584-104">Specifies whether the codec will use the noise filter when encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="62584-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="62584-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="62584-106">g \_ wszWMVCDenoiseOption</span><span class="sxs-lookup"><span data-stu-id="62584-106">g\_wszWMVCDenoiseOption</span></span>

## <a name="data-type"></a><span data-ttu-id="62584-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="62584-107">Data Type</span></span>

<span data-ttu-id="62584-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="62584-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="62584-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="62584-109">Default Value</span></span>

<span data-ttu-id="62584-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="62584-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="62584-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="62584-111">Remarks</span></span>

<span data-ttu-id="62584-112">O filtro de ruído pode melhorar a qualidade de fontes de vídeo ruidosas, como filme que contém muitos refinamentos ou capturas de vídeo em baixa luz.</span><span class="sxs-lookup"><span data-stu-id="62584-112">The noise filter can improve the quality of noisy video sources, such as film containing lots of grain or video shot in low light.</span></span> <span data-ttu-id="62584-113">Esse filtro pode ser usado em cenários de codificação ativa em que o pré-processamento externo não é uma opção.</span><span class="sxs-lookup"><span data-stu-id="62584-113">This filter can be used in live encoding scenarios where external preprocessing is not an option.</span></span>

<span data-ttu-id="62584-114">Esse filtro deve ser desabilitado para fontes de vídeo limpas, pois ele pode reduzir a qualidade da imagem quando a qualidade é boa para começar.</span><span class="sxs-lookup"><span data-stu-id="62584-114">This filter should be disabled for clean video sources since it can reduce image quality when the quality is good to start with.</span></span>

## <a name="requirements"></a><span data-ttu-id="62584-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62584-115">Requirements</span></span>



| <span data-ttu-id="62584-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="62584-116">Requirement</span></span> | <span data-ttu-id="62584-117">Valor</span><span class="sxs-lookup"><span data-stu-id="62584-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62584-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62584-118">Minimum supported client</span></span><br/> | <span data-ttu-id="62584-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="62584-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="62584-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62584-120">Minimum supported server</span></span><br/> | <span data-ttu-id="62584-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62584-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62584-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62584-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="62584-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="62584-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62584-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="62584-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62584-125">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62584-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




