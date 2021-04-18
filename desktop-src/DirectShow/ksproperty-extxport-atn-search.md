---
description: Essa propriedade envia um comando para o dispositivo para pesquisar um número de faixa absoluto (ATN). O driver de dispositivo UVC dá suporte a essa propriedade.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc8ff454386c444ed6b55bfbeede60196a75127c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105767673"
---
# <a name="ksproperty_extxport_atn_search"></a><span data-ttu-id="ec51d-104">KSPROPERTY \_ EXTXPORT \_ ATN \_ Search</span><span class="sxs-lookup"><span data-stu-id="ec51d-104">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>

<span data-ttu-id="ec51d-105">Essa propriedade envia um comando para o dispositivo para pesquisar um número de faixa absoluto (ATN).</span><span class="sxs-lookup"><span data-stu-id="ec51d-105">This property sends a command to the device to search for an absolute track number (ATN).</span></span> <span data-ttu-id="ec51d-106">O driver de dispositivo UVC dá suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="ec51d-106">The UVC device driver supports this property.</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="ec51d-107">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="ec51d-107">Property Set GUID</span></span> | <span data-ttu-id="ec51d-108">transporte de extensão propsetid \_ \_</span><span class="sxs-lookup"><span data-stu-id="ec51d-108">PROPSETID\_EXT\_TRANSPORT</span></span>             |
| <span data-ttu-id="ec51d-109">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="ec51d-109">Property ID</span></span>       | <span data-ttu-id="ec51d-110">KSPROPERTY \_ EXTXPORT \_ ATN \_ Search</span><span class="sxs-lookup"><span data-stu-id="ec51d-110">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>     |
| <span data-ttu-id="ec51d-111">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="ec51d-111">Data Type</span></span>         | <span data-ttu-id="ec51d-112">**KSPROPERTY \_ Estrutura EXTXPORT \_ S**</span><span class="sxs-lookup"><span data-stu-id="ec51d-112">**KSPROPERTY\_EXTXPORT\_S** structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ec51d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec51d-113">Remarks</span></span>

<span data-ttu-id="ec51d-114">Defina o membro **dwAbsTrackNumber** da estrutura **KSPROPERTY \_ EXTXPORT \_** como o seguinte valor:</span><span class="sxs-lookup"><span data-stu-id="ec51d-114">Set the **dwAbsTrackNumber** member of the **KSPROPERTY\_EXTXPORT\_S** structure to the following value:</span></span>


```
(absolute track number << 1) + continuity bit
```



<span data-ttu-id="ec51d-115">A especificação UVC não define como o dispositivo usa o bit de continuidade.</span><span class="sxs-lookup"><span data-stu-id="ec51d-115">The UVC specification does not define how the device uses the continuity bit.</span></span> <span data-ttu-id="ec51d-116">A estrutura **KSPROPERTY \_ EXTXPORT \_ S** é descrita no Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="ec51d-116">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec51d-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec51d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec51d-118">Conjunto de propriedades de transporte de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="ec51d-118">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



