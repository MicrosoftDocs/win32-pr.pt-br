---
title: Keyarray (mmsystem. h)
description: Keyarray especifica um tipo usado para definir uma matriz de chaves.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- MIDIPATCHSIZE DE KEYARRAY
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e45e46417fb3b6653ecae605aa60f775c1d654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770162"
---
# <a name="keyarray"></a><span data-ttu-id="26424-104">Keyarray</span><span class="sxs-lookup"><span data-stu-id="26424-104">KEYARRAY</span></span>

<span data-ttu-id="26424-105">Keyarray especifica um tipo usado para definir uma matriz de chaves.</span><span class="sxs-lookup"><span data-stu-id="26424-105">KEYARRAY specifies a type used to define an array of keys.</span></span>


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

<span data-ttu-id="26424-106">**MIDIPATCHSIZE de keyarray \[\]**</span><span class="sxs-lookup"><span data-stu-id="26424-106">**KEYARRAY\[MIDIPATCHSIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="26424-107">Cada elemento na matriz corresponde a um patch de percussão baseado em chave com cada um dos 16 bits representando um dos 16 canais MIDI.</span><span class="sxs-lookup"><span data-stu-id="26424-107">Each element in the array corresponds to a key-based percussion patch with each of the 16 bits representing one of the 16 MIDI channels.</span></span> <span data-ttu-id="26424-108">Os bits são definidos para cada um dos canais que usam esse patch específico.</span><span class="sxs-lookup"><span data-stu-id="26424-108">Bits are set for each of the channels that use that particular patch.</span></span> <span data-ttu-id="26424-109">Por exemplo, se o patch de percussão para o número de chave 60 for usado pelos canais de MIDI física 9 e 15, o elemento 60 da matriz deverá ser definido como 0x8200.</span><span class="sxs-lookup"><span data-stu-id="26424-109">For example, if the percussion patch for key number 60 is used by physical MIDI channels 9 and 15, element 60 of the array should be set to 0x8200.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26424-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26424-110">Requirements</span></span>



| <span data-ttu-id="26424-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="26424-111">Requirement</span></span> | <span data-ttu-id="26424-112">Valor</span><span class="sxs-lookup"><span data-stu-id="26424-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26424-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26424-113">Minimum supported client</span></span><br/> | <span data-ttu-id="26424-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="26424-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="26424-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26424-115">Minimum supported server</span></span><br/> | <span data-ttu-id="26424-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="26424-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="26424-117">Versão</span><span class="sxs-lookup"><span data-stu-id="26424-117">Version</span></span><br/>                  | <span data-ttu-id="26424-118">MIDI (interface digital de instrumento musical), tipos de MIDI</span><span class="sxs-lookup"><span data-stu-id="26424-118">Musical Instrument Digital Interface (MIDI), MIDI Types</span></span><br/>                                        |
| <span data-ttu-id="26424-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26424-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="26424-120"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26424-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26424-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="26424-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26424-122">Tipos de MIDI</span><span class="sxs-lookup"><span data-stu-id="26424-122">MIDI Types</span></span>](midi-event-types.md)
</dt> </dl>

 

 





