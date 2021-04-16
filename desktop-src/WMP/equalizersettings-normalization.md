---
title: EQUALIZERSETTINGS. normalização
description: O atributo de normalização especifica ou recupera um valor que indica se a normalização está habilitada.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS. normalização do Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9714359e5d5e2af0c82a0d687555f7cfcbf1cf70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779422"
---
# <a name="equalizersettingsnormalization"></a><span data-ttu-id="12452-104">EQUALIZERSETTINGS. normalização</span><span class="sxs-lookup"><span data-stu-id="12452-104">EQUALIZERSETTINGS.normalization</span></span>

<span data-ttu-id="12452-105">O atributo de **normalização** especifica ou recupera um valor que indica se a normalização está habilitada.</span><span class="sxs-lookup"><span data-stu-id="12452-105">The **normalization** attribute specifies or retrieves a value indicating whether normalization is enabled.</span></span>

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a><span data-ttu-id="12452-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="12452-106">Possible Values</span></span>

<span data-ttu-id="12452-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="12452-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="12452-108">Valor</span><span class="sxs-lookup"><span data-stu-id="12452-108">Value</span></span> | <span data-ttu-id="12452-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="12452-109">Description</span></span>                         |
|-------|-------------------------------------|
| <span data-ttu-id="12452-110">true</span><span class="sxs-lookup"><span data-stu-id="12452-110">true</span></span>  | <span data-ttu-id="12452-111">A normalização está habilitada.</span><span class="sxs-lookup"><span data-stu-id="12452-111">Normalization is enabled.</span></span>           |
| <span data-ttu-id="12452-112">false</span><span class="sxs-lookup"><span data-stu-id="12452-112">false</span></span> | <span data-ttu-id="12452-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="12452-113">Default.</span></span> <span data-ttu-id="12452-114">A normalização está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="12452-114">Normalization is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="12452-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="12452-115">Remarks</span></span>

<span data-ttu-id="12452-116">Quando a normalização é habilitada, o sinal de áudio de um arquivo de mídia digital inteiro é dimensionado para o valor máximo.</span><span class="sxs-lookup"><span data-stu-id="12452-116">When normalization is enabled, the audio signal for an entire digital media file is scaled up to the maximum value.</span></span> <span data-ttu-id="12452-117">Isso permite que vários arquivos sejam reproduzidos em aproximadamente o mesmo volume sem a necessidade de ajustes de volume.</span><span class="sxs-lookup"><span data-stu-id="12452-117">This allows multiple files to be played at approximately the same volume without requiring volume adjustments.</span></span>

## <a name="requirements"></a><span data-ttu-id="12452-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12452-118">Requirements</span></span>



| <span data-ttu-id="12452-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="12452-119">Requirement</span></span> | <span data-ttu-id="12452-120">Valor</span><span class="sxs-lookup"><span data-stu-id="12452-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="12452-121">Versão</span><span class="sxs-lookup"><span data-stu-id="12452-121">Version</span></span><br/> | <span data-ttu-id="12452-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="12452-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12452-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="12452-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12452-124">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="12452-124">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="12452-125">**EQUALIZERSETTINGS.normalizationAverage**</span><span class="sxs-lookup"><span data-stu-id="12452-125">**EQUALIZERSETTINGS.normalizationAverage**</span></span>](equalizersettings-normalizationaverage.md)
</dt> <dt>

[<span data-ttu-id="12452-126">**EQUALIZERSETTINGS.normalizationPeak**</span><span class="sxs-lookup"><span data-stu-id="12452-126">**EQUALIZERSETTINGS.normalizationPeak**</span></span>](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





