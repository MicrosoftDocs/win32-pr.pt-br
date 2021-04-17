---
title: Elemento STARTtime
description: O elemento STARTtime define um índice de tempo do qual o Windows Media Player começará a renderizar o fluxo.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- Elemento STARTtime Windows Media Player
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a882da6c07ec76a94c8e214fe1da11c71680b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763788"
---
# <a name="starttime-element"></a><span data-ttu-id="6895a-104">Elemento STARTtime</span><span class="sxs-lookup"><span data-stu-id="6895a-104">STARTTIME Element</span></span>

<span data-ttu-id="6895a-105">O elemento **StartTime** define um índice de tempo do qual o Windows Media Player começará a renderizar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="6895a-105">The **STARTTIME** element defines a time index from which Windows Media Player will start rendering the stream.</span></span>

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="6895a-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="6895a-106">Attributes</span></span>

<span data-ttu-id="6895a-107">**Valor** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="6895a-107">**VALUE** (required)</span></span>

<span data-ttu-id="6895a-108">O índice de tempo (em horas, minutos, segundos e centésimos de segundo) do qual o Windows Media Player começa a reproduzir um fluxo definido no elemento associado.</span><span class="sxs-lookup"><span data-stu-id="6895a-108">The time index (in hours, minutes, seconds, and hundredths of a second) from which Windows Media Player starts playing a stream defined in the associated element.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="6895a-109">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="6895a-109">Parent/Child Elements</span></span>



| <span data-ttu-id="6895a-110">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="6895a-110">Hierarchy</span></span>       | <span data-ttu-id="6895a-111">Elementos</span><span class="sxs-lookup"><span data-stu-id="6895a-111">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="6895a-112">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6895a-112">Parent elements</span></span> | <span data-ttu-id="6895a-113">**entrada**, **ref**</span><span class="sxs-lookup"><span data-stu-id="6895a-113">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="6895a-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6895a-114">Child elements</span></span>  | <span data-ttu-id="6895a-115">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6895a-115">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="6895a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6895a-116">Remarks</span></span>

<span data-ttu-id="6895a-117">Esse elemento define um índice de tempo no conteúdo em que o Windows Media Player é para iniciar a renderização do fluxo.</span><span class="sxs-lookup"><span data-stu-id="6895a-117">This element defines a time index into the content where Windows Media Player is to start rendering the stream.</span></span> <span data-ttu-id="6895a-118">Esse elemento só pode ser usado com conteúdo armazenado sob demanda que foi indexado.</span><span class="sxs-lookup"><span data-stu-id="6895a-118">This element can be used only with stored, on-demand content that has been indexed.</span></span>

## <a name="examples"></a><span data-ttu-id="6895a-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6895a-119">Examples</span></span>


```XML
<STARTTIME VALUE="1:30.0" />
```



## <a name="requirements"></a><span data-ttu-id="6895a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6895a-120">Requirements</span></span>



| <span data-ttu-id="6895a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6895a-121">Requirement</span></span> | <span data-ttu-id="6895a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6895a-122">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="6895a-123">Versão</span><span class="sxs-lookup"><span data-stu-id="6895a-123">Version</span></span><br/> | <span data-ttu-id="6895a-124">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6895a-124">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6895a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6895a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6895a-126">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6895a-126">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="6895a-127">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6895a-127">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





