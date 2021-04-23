---
description: Essa propriedade envia um comando para o dispositivo para pesquisar um número de faixa absoluto (ATN). O driver de dispositivo UVC dá suporte a essa propriedade.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4115c7ff1c4bc878b4ee80e284f11821c37909a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909443"
---
# <a name="ksproperty_extxport_atn_search"></a><span data-ttu-id="216a2-104">KSPROPERTY \_ EXTXPORT \_ ATN \_ Search</span><span class="sxs-lookup"><span data-stu-id="216a2-104">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>

<span data-ttu-id="216a2-105">Essa propriedade envia um comando para o dispositivo para pesquisar um número de faixa absoluto (ATN).</span><span class="sxs-lookup"><span data-stu-id="216a2-105">This property sends a command to the device to search for an absolute track number (ATN).</span></span> <span data-ttu-id="216a2-106">O driver de dispositivo UVC dá suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="216a2-106">The UVC device driver supports this property.</span></span>



| <span data-ttu-id="216a2-107">Label</span><span class="sxs-lookup"><span data-stu-id="216a2-107">Label</span></span> | <span data-ttu-id="216a2-108">Valor</span><span class="sxs-lookup"><span data-stu-id="216a2-108">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="216a2-109">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="216a2-109">Property Set GUID</span></span> | <span data-ttu-id="216a2-110">transporte de extensão propsetid \_ \_</span><span class="sxs-lookup"><span data-stu-id="216a2-110">PROPSETID\_EXT\_TRANSPORT</span></span>             |
| <span data-ttu-id="216a2-111">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="216a2-111">Property ID</span></span>       | <span data-ttu-id="216a2-112">KSPROPERTY \_ EXTXPORT \_ ATN \_ Search</span><span class="sxs-lookup"><span data-stu-id="216a2-112">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>     |
| <span data-ttu-id="216a2-113">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="216a2-113">Data Type</span></span>         | <span data-ttu-id="216a2-114">**KSPROPERTY \_ Estrutura EXTXPORT \_ S**</span><span class="sxs-lookup"><span data-stu-id="216a2-114">**KSPROPERTY\_EXTXPORT\_S** structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="216a2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="216a2-115">Remarks</span></span>

<span data-ttu-id="216a2-116">Defina o membro **dwAbsTrackNumber** da estrutura **KSPROPERTY \_ EXTXPORT \_** como o seguinte valor:</span><span class="sxs-lookup"><span data-stu-id="216a2-116">Set the **dwAbsTrackNumber** member of the **KSPROPERTY\_EXTXPORT\_S** structure to the following value:</span></span>


```
(absolute track number << 1) + continuity bit
```



<span data-ttu-id="216a2-117">A especificação UVC não define como o dispositivo usa o bit de continuidade.</span><span class="sxs-lookup"><span data-stu-id="216a2-117">The UVC specification does not define how the device uses the continuity bit.</span></span> <span data-ttu-id="216a2-118">A estrutura **KSPROPERTY \_ EXTXPORT \_ S** é descrita no Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="216a2-118">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="216a2-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="216a2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="216a2-120">Conjunto de propriedades de transporte de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="216a2-120">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



