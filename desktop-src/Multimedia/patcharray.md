---
title: PATCHARRAY (mmsystem. h)
description: PATCHARRAY é um tipo usado para definir uma matriz de patches de MIDI.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e07af0e878fc0d2fc79d6d17aafd48fbd991fb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824820"
---
# <a name="patcharray"></a><span data-ttu-id="473da-104">PATCHARRAY</span><span class="sxs-lookup"><span data-stu-id="473da-104">PATCHARRAY</span></span>

<span data-ttu-id="473da-105">PATCHARRAY é um tipo usado para definir uma matriz de patches de MIDI.</span><span class="sxs-lookup"><span data-stu-id="473da-105">PATCHARRAY is a type used to define an array of MIDI patches.</span></span>


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

<span data-ttu-id="473da-106">**PATCHARRAY \[ MIDIPATCHSIZE\]**</span><span class="sxs-lookup"><span data-stu-id="473da-106">**PATCHARRAY\[MIDIPATCHSIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="473da-107">Cada elemento na matriz corresponde a um patch com cada um dos 16 bits representando um dos 16 canais MIDI.</span><span class="sxs-lookup"><span data-stu-id="473da-107">Each element in the array corresponds to a patch with each of the 16 bits representing one of the 16 MIDI channels.</span></span> <span data-ttu-id="473da-108">Os bits são definidos para cada um dos canais que usam esse patch específico.</span><span class="sxs-lookup"><span data-stu-id="473da-108">Bits are set for each of the channels that use that particular patch.</span></span> <span data-ttu-id="473da-109">Por exemplo, se o número do patch 0 for usado pelos canais de MIDI física 0 e 8, o elemento 0 da matriz deverá ser definido como 0x0101.</span><span class="sxs-lookup"><span data-stu-id="473da-109">For example, if patch number 0 is used by physical MIDI channels 0 and 8, element 0 of the array should be set to 0x0101.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="473da-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="473da-110">Requirements</span></span>



| <span data-ttu-id="473da-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="473da-111">Requirement</span></span> | <span data-ttu-id="473da-112">Valor</span><span class="sxs-lookup"><span data-stu-id="473da-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="473da-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="473da-113">Minimum supported client</span></span><br/> | <span data-ttu-id="473da-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="473da-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="473da-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="473da-115">Minimum supported server</span></span><br/> | <span data-ttu-id="473da-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="473da-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="473da-117">Versão</span><span class="sxs-lookup"><span data-stu-id="473da-117">Version</span></span><br/>                  | <span data-ttu-id="473da-118">MIDI (interface digital de instrumento musical), tipos de MIDI</span><span class="sxs-lookup"><span data-stu-id="473da-118">Musical Instrument Digital Interface (MIDI), MIDI Types</span></span><br/>                                        |
| <span data-ttu-id="473da-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="473da-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="473da-120"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="473da-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="473da-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="473da-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="473da-122">Tipos de MIDI</span><span class="sxs-lookup"><span data-stu-id="473da-122">MIDI Types</span></span>](midi-event-types.md)
</dt> </dl>

 

 





