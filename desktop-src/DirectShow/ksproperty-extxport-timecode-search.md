---
description: Essa propriedade envia um comando para o dispositivo para procurar um código de tempo especificado. O driver de dispositivo UVC dá suporte a essa propriedade.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6852dc44e6ef10eebb59721f16a276ac5d4306a3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909434"
---
# <a name="ksproperty_extxport_timecode_search"></a><span data-ttu-id="cd786-104">pesquisa de código de KSPROPERTY \_ EXTXPORT \_ \_</span><span class="sxs-lookup"><span data-stu-id="cd786-104">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span>

<span data-ttu-id="cd786-105">Essa propriedade envia um comando para o dispositivo para procurar um código de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="cd786-105">This property sends a command to the device to search for a specified time code.</span></span> <span data-ttu-id="cd786-106">O driver de dispositivo UVC dá suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cd786-106">The UVC device driver supports this property.</span></span>



| <span data-ttu-id="cd786-107">Label</span><span class="sxs-lookup"><span data-stu-id="cd786-107">Label</span></span> | <span data-ttu-id="cd786-108">Valor</span><span class="sxs-lookup"><span data-stu-id="cd786-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="cd786-109">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="cd786-109">Property Set GUID</span></span> | <span data-ttu-id="cd786-110">transporte de extensão propsetid \_ \_</span><span class="sxs-lookup"><span data-stu-id="cd786-110">PROPSETID\_EXT\_TRANSPORT</span></span>              |
| <span data-ttu-id="cd786-111">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="cd786-111">Property ID</span></span>       | <span data-ttu-id="cd786-112">pesquisa de código de KSPROPERTY \_ EXTXPORT \_ \_</span><span class="sxs-lookup"><span data-stu-id="cd786-112">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span> |
| <span data-ttu-id="cd786-113">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="cd786-113">Data Type</span></span>         | <span data-ttu-id="cd786-114">**KSPROPERTY \_ Estrutura EXTXPORT \_ S**</span><span class="sxs-lookup"><span data-stu-id="cd786-114">**KSPROPERTY\_EXTXPORT\_S** structure</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="cd786-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd786-115">Remarks</span></span>

<span data-ttu-id="cd786-116">Preencha o membro de **código** de tempo da estrutura **KSPROPERTY \_ EXTXPORT \_ S** com o quadro desejado, segundo, minuto e hora.</span><span class="sxs-lookup"><span data-stu-id="cd786-116">Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour.</span></span> <span data-ttu-id="cd786-117">A estrutura **KSPROPERTY \_ EXTXPORT \_ S** é descrita no Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="cd786-117">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd786-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd786-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd786-119">Conjunto de propriedades de transporte de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="cd786-119">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



