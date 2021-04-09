---
description: Essa propriedade envia um comando para o dispositivo para procurar um código de tempo especificado. O driver de dispositivo UVC dá suporte a essa propriedade.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52125f0c2e7ddd292cc1f93577a212d5c78a76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009926"
---
# <a name="ksproperty_extxport_timecode_search"></a><span data-ttu-id="fb9f0-104">pesquisa de código de KSPROPERTY \_ EXTXPORT \_ \_</span><span class="sxs-lookup"><span data-stu-id="fb9f0-104">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span>

<span data-ttu-id="fb9f0-105">Essa propriedade envia um comando para o dispositivo para procurar um código de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="fb9f0-105">This property sends a command to the device to search for a specified time code.</span></span> <span data-ttu-id="fb9f0-106">O driver de dispositivo UVC dá suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="fb9f0-106">The UVC device driver supports this property.</span></span>



|                   |                                        |
|-------------------|----------------------------------------|
| <span data-ttu-id="fb9f0-107">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="fb9f0-107">Property Set GUID</span></span> | <span data-ttu-id="fb9f0-108">transporte de extensão propsetid \_ \_</span><span class="sxs-lookup"><span data-stu-id="fb9f0-108">PROPSETID\_EXT\_TRANSPORT</span></span>              |
| <span data-ttu-id="fb9f0-109">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="fb9f0-109">Property ID</span></span>       | <span data-ttu-id="fb9f0-110">pesquisa de código de KSPROPERTY \_ EXTXPORT \_ \_</span><span class="sxs-lookup"><span data-stu-id="fb9f0-110">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span> |
| <span data-ttu-id="fb9f0-111">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="fb9f0-111">Data Type</span></span>         | <span data-ttu-id="fb9f0-112">**KSPROPERTY \_ Estrutura EXTXPORT \_ S**</span><span class="sxs-lookup"><span data-stu-id="fb9f0-112">**KSPROPERTY\_EXTXPORT\_S** structure</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="fb9f0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb9f0-113">Remarks</span></span>

<span data-ttu-id="fb9f0-114">Preencha o membro de **código** de tempo da estrutura **KSPROPERTY \_ EXTXPORT \_ S** com o quadro desejado, segundo, minuto e hora.</span><span class="sxs-lookup"><span data-stu-id="fb9f0-114">Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour.</span></span> <span data-ttu-id="fb9f0-115">A estrutura **KSPROPERTY \_ EXTXPORT \_ S** é descrita no Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="fb9f0-115">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb9f0-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb9f0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb9f0-117">Conjunto de propriedades de transporte de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="fb9f0-117">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



