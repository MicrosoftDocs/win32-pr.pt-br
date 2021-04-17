---
description: A \_ estrutura do mapa PID contém identifica o conteúdo de uma ID de pacote de fluxo de transporte MPEG-2.
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: Estrutura de PID_MAP (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PID_MAP
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 98b238c61ccfcfb93e4ddcc0a051d9084228f604
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782838"
---
# <a name="pid_map-structure"></a><span data-ttu-id="dc056-103">\_Estrutura do mapa PID</span><span class="sxs-lookup"><span data-stu-id="dc056-103">PID\_MAP structure</span></span>

<span data-ttu-id="dc056-104">A `PID_MAP` estrutura contém identifica o conteúdo de uma ID de pacote de fluxo de transporte MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="dc056-104">The `PID_MAP` structure contains identifies the contents of an MPEG-2 transport stream packet ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc056-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc056-105">Syntax</span></span>


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a><span data-ttu-id="dc056-106">Membros</span><span class="sxs-lookup"><span data-stu-id="dc056-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc056-107">**ulPID**</span><span class="sxs-lookup"><span data-stu-id="dc056-107">**ulPID**</span></span>
</dt> <dd>

<span data-ttu-id="dc056-108">Especifica a ID do pacote (PID)</span><span class="sxs-lookup"><span data-stu-id="dc056-108">Specifies the packet ID (PID)</span></span>

</dd> <dt>

<span data-ttu-id="dc056-109">**MediaSampleContent**</span><span class="sxs-lookup"><span data-stu-id="dc056-109">**MediaSampleContent**</span></span>
</dt> <dd>

<span data-ttu-id="dc056-110">Especifica o conteúdo da carga do pacote, como um tipo de enumeração de [**\_ \_ conteúdo de exemplo de mídia**](media-sample-content.md) .</span><span class="sxs-lookup"><span data-stu-id="dc056-110">Specifies the contents of the packet payload, as a [**MEDIA\_SAMPLE\_CONTENT**](media-sample-content.md) enumeration type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc056-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc056-111">Requirements</span></span>



| <span data-ttu-id="dc056-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc056-112">Requirement</span></span> | <span data-ttu-id="dc056-113">Valor</span><span class="sxs-lookup"><span data-stu-id="dc056-113">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc056-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc056-114">Header</span></span><br/> | <dl> <span data-ttu-id="dc056-115"><dt>Bdatypes. h (incluir Bdaiface. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc056-115"><dt>Bdatypes.h (include Bdaiface.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc056-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc056-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc056-117">Estruturas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="dc056-117">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="dc056-118">**Interface IEnumPIDMap**</span><span class="sxs-lookup"><span data-stu-id="dc056-118">**IEnumPIDMap Interface**</span></span>](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




