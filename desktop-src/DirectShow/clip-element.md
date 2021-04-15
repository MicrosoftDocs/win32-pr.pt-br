---
description: O clipe epecifies uma fonte de mídia.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Elemento de clipe
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe975113f370b13e50ba695d6fb3388a43c3a74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456443"
---
# <a name="clip-element"></a><span data-ttu-id="be3fa-103">Elemento de clipe</span><span class="sxs-lookup"><span data-stu-id="be3fa-103">clip Element</span></span>

> [!Note]  
> <span data-ttu-id="be3fa-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="be3fa-104">\[Deprecated.</span></span> <span data-ttu-id="be3fa-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="be3fa-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="be3fa-106">O `clip` epecifies uma origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="be3fa-106">The `clip` epecifies a media source.</span></span>

## <a name="attributes"></a><span data-ttu-id="be3fa-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="be3fa-107">Attributes</span></span>

<span data-ttu-id="be3fa-108">[**CLSID**](clsid-attribute.md), [**taxa de quadros**](framerate-attribute.md), [**bloqueio**](lock-attribute.md), [**mLength**](mlength-attribute.md), [**mStart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mudo**](mute-attribute.md), [**src**](src-attribute.md), [**Iniciar**](start-attribute.md), [**parar**](stop-attribute.md), [**transmitir**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="be3fa-108">[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="be3fa-109">Informações de pai/filho</span><span class="sxs-lookup"><span data-stu-id="be3fa-109">Parent/Child Information</span></span>



|          |                                  |
|----------|----------------------------------|
| <span data-ttu-id="be3fa-110">Pai</span><span class="sxs-lookup"><span data-stu-id="be3fa-110">Parent</span></span>   | [<span data-ttu-id="be3fa-111">**controles**</span><span class="sxs-lookup"><span data-stu-id="be3fa-111">**track**</span></span>](track-element.md)   |
| <span data-ttu-id="be3fa-112">Children</span><span class="sxs-lookup"><span data-stu-id="be3fa-112">Children</span></span> | [<span data-ttu-id="be3fa-113">**funciona**</span><span class="sxs-lookup"><span data-stu-id="be3fa-113">**effect**</span></span>](effect-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="be3fa-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="be3fa-114">Remarks</span></span>

<span data-ttu-id="be3fa-115">O atributo **CLSID** especifica o CLSID de um filtro de origem a ser usado como a origem.</span><span class="sxs-lookup"><span data-stu-id="be3fa-115">The **clsid** attribute specifies the CLSID of a source filter to use as the source.</span></span> <span data-ttu-id="be3fa-116">Não especifique os atributos **src** e **CLSID** dentro do mesmo `clip` elemento.</span><span class="sxs-lookup"><span data-stu-id="be3fa-116">Do not specify the **src** and **clsid** attributes within the same `clip` element.</span></span>

<span data-ttu-id="be3fa-117">Especifique pelo menos um atributo de tempo de início (**Start** ou **mStart**) e um atributo de tempo de parada (**Stop** ou **mstop**).</span><span class="sxs-lookup"><span data-stu-id="be3fa-117">Specify at least one start-time attribute (**start** or **mstart**) and one stop-time attribute (**stop** or **mstop**).</span></span> <span data-ttu-id="be3fa-118">Se um dos atributos de tempo de inicialização não for especificado, o padrão será 0 (o início da linha do tempo para **início** ou o início do clipe para **mStart**).</span><span class="sxs-lookup"><span data-stu-id="be3fa-118">If one of the start-time attributes is unspecified, it defaults to 0 (the beginning of the timeline for **start**, or the beginning of the clip for **mstart**).</span></span> <span data-ttu-id="be3fa-119">Se um dos atributos de tempo de parada não for especificado, o DES assumirá uma taxa de reprodução normal e calculará a hora de parada não especificada adequadamente.</span><span class="sxs-lookup"><span data-stu-id="be3fa-119">If one of the stop-time attributes is unspecified, DES assumes a normal playback rate and calculates the unspecified stop time accordingly.</span></span> <span data-ttu-id="be3fa-120">Se ambas as horas de parada forem especificadas, a reprodução será mais rápida ou mais lenta do que o normal, se necessário.</span><span class="sxs-lookup"><span data-stu-id="be3fa-120">If both stop times are specified, playback is faster or slower than normal, if necessary.</span></span>

<span data-ttu-id="be3fa-121">No exemplo a seguir, a duração da linha do tempo é de sete segundos (**parar** menos **Iniciar**).</span><span class="sxs-lookup"><span data-stu-id="be3fa-121">In the following example, the timeline duration is seven seconds (**stop** minus **start**).</span></span> <span data-ttu-id="be3fa-122">A taxa de reprodução normal é assumida, portanto, o padrão da hora de parada da mídia é de 10 segundos (a duração mais **mStart**).</span><span class="sxs-lookup"><span data-stu-id="be3fa-122">Normal playback rate is assumed, so the media stop time defaults to 10 seconds (the duration plus **mstart**).</span></span>


```
<clip start="2" stop="9" mstart="3" />
```



<span data-ttu-id="be3fa-123">No próximo exemplo, a hora de início da mídia usa como padrão 0, forçando a duração da mídia a ser de 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="be3fa-123">In the next example, the media start time defaults to 0, forcing the media duration to be 10 seconds.</span></span> <span data-ttu-id="be3fa-124">A duração da linha do tempo é de cinco segundos, portanto, o clipe é reproduzido com duas vezes a taxa normal.</span><span class="sxs-lookup"><span data-stu-id="be3fa-124">The timeline duration is five seconds, so the clip plays back at twice the normal rate.</span></span>


```
<clip start="5" stop="10" mstop="10" />  
```



<span data-ttu-id="be3fa-125">Se o atributo **src** especificar uma imagem ainda, o des tentará carregar uma série de imagens ainda para criar uma animação.</span><span class="sxs-lookup"><span data-stu-id="be3fa-125">If the **src** attribute specifies a still image, DES attempts to load a series of still images to create an animation.</span></span> <span data-ttu-id="be3fa-126">Por exemplo, se o atributo **src** for IMAGE001.BMP, o des procurará IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="be3fa-126">For example, if the **src** attribute is IMAGE001.BMP, DES looks for IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, and so on.</span></span> <span data-ttu-id="be3fa-127">Supondo que eles existam, eles são exibidos em ordem numérica sequencial, na taxa especificada pelo atributo de **taxa de quadros** .</span><span class="sxs-lookup"><span data-stu-id="be3fa-127">Assuming they exist, they are displayed in sequential numerical order, at the rate specified by the **framerate** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="be3fa-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="be3fa-128">Examples</span></span>


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a><span data-ttu-id="be3fa-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="be3fa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be3fa-130">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="be3fa-130">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



