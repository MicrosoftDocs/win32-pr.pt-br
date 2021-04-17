---
title: Propriedade MyItem. ScaleFactor
description: Recupera ou define o fator de escala usado para grafar o valor do contador.
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- Propriedade ScaleFactor SysMon
- Propriedade ScaleFactor SysMon, classe de coitem
- Classe monoitem SysMon, propriedade ScaleFactor
topic_type:
- apiref
api_name:
- CounterItem.ScaleFactor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9a04df634fe54c82230ade679afb3259519173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755773"
---
# <a name="counteritemscalefactor-property"></a><span data-ttu-id="abba7-106">Propriedade MyItem. ScaleFactor</span><span class="sxs-lookup"><span data-stu-id="abba7-106">CounterItem.ScaleFactor property</span></span>

<span data-ttu-id="abba7-107">Recupera ou define o fator de escala usado para grafar o valor do contador.</span><span class="sxs-lookup"><span data-stu-id="abba7-107">Retrieves or sets the scale factor used to graph the counter value.</span></span>

<span data-ttu-id="abba7-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="abba7-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="abba7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="abba7-109">Syntax</span></span>


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a><span data-ttu-id="abba7-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="abba7-110">Property value</span></span>

<span data-ttu-id="abba7-111">Fator de escala usado na exibição dos valores do contador grafado.</span><span class="sxs-lookup"><span data-stu-id="abba7-111">Scale factor used in displaying the graphed counter values.</span></span> <span data-ttu-id="abba7-112">Os valores válidos variam de-9 a 9 (os valores correspondem a 0, 1-100000000,0).</span><span class="sxs-lookup"><span data-stu-id="abba7-112">Valid values range from -9 to 9 (the values correspond to 0.000000001 - 100000000.0).</span></span>

<span data-ttu-id="abba7-113">**Antes do Windows Vista:** Os valores válidos variam de-7 a 7 (os valores correspondem a 0, 1-1000000,0).</span><span class="sxs-lookup"><span data-stu-id="abba7-113">**Prior to Windows Vista:** Valid values range from -7 to 7 (the values correspond to 0.0000001 - 1000000.0).</span></span>

## <a name="remarks"></a><span data-ttu-id="abba7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="abba7-114">Remarks</span></span>

<span data-ttu-id="abba7-115">Defina essa propriedade somente se desejar alterar o fator de escala padrão do contador (cada contador define seu próprio fator de escala).</span><span class="sxs-lookup"><span data-stu-id="abba7-115">Only set this property if you want to change the counter's default scale factor (each counter defines its own scale factor).</span></span> <span data-ttu-id="abba7-116">O valor dessa propriedade é definido como Integer. MaxValue se o contador estiver usando seu fator de escala padrão para grafar os valores.</span><span class="sxs-lookup"><span data-stu-id="abba7-116">The value of this property is set to Integer.MaxValue if the counter is using its default scale factor to graph the values.</span></span>

## <a name="requirements"></a><span data-ttu-id="abba7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abba7-117">Requirements</span></span>



| <span data-ttu-id="abba7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="abba7-118">Requirement</span></span> | <span data-ttu-id="abba7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="abba7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="abba7-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abba7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="abba7-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="abba7-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="abba7-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abba7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="abba7-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="abba7-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="abba7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="abba7-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abba7-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="abba7-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abba7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="abba7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abba7-127">**Item**</span><span class="sxs-lookup"><span data-stu-id="abba7-127">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="abba7-128">**SystemMonitor.ScaleToFit**</span><span class="sxs-lookup"><span data-stu-id="abba7-128">**SystemMonitor.ScaleToFit**</span></span>](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





