---
description: Fonte de cores do vídeo
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: Fonte de cores do vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c751d74a78b027d50f033acb3709d18fe8f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170265"
---
# <a name="video-color-source"></a><span data-ttu-id="6ea58-103">Fonte de cores do vídeo</span><span class="sxs-lookup"><span data-stu-id="6ea58-103">Video Color Source</span></span>

> [!Note]  
> <span data-ttu-id="6ea58-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="6ea58-104">\[Deprecated.</span></span> <span data-ttu-id="6ea58-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6ea58-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6ea58-106">A fonte de cores do vídeo cria uma imagem de vídeo contínua de uma cor sólida.</span><span class="sxs-lookup"><span data-stu-id="6ea58-106">The Video Color Source creates a continuous video image of a solid color.</span></span>

<span data-ttu-id="6ea58-107">ID de classe (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**</span><span class="sxs-lookup"><span data-stu-id="6ea58-107">Class ID (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**</span></span>

<span data-ttu-id="6ea58-108">Nome da variável CLSID: **CLSID \_ Colorize**</span><span class="sxs-lookup"><span data-stu-id="6ea58-108">CLSID Variable Name: **CLSID\_ColorSource**</span></span>

<span data-ttu-id="6ea58-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6ea58-109">Properties</span></span>



| <span data-ttu-id="6ea58-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="6ea58-110">Property</span></span> | <span data-ttu-id="6ea58-111">Type</span><span class="sxs-lookup"><span data-stu-id="6ea58-111">Type</span></span>      | <span data-ttu-id="6ea58-112">Padrão</span><span class="sxs-lookup"><span data-stu-id="6ea58-112">Default</span></span> | <span data-ttu-id="6ea58-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ea58-113">Description</span></span>                                   |
|----------|-----------|---------|-----------------------------------------------|
| <span data-ttu-id="6ea58-114">Colorida</span><span class="sxs-lookup"><span data-stu-id="6ea58-114">"Color"</span></span>  | <span data-ttu-id="6ea58-115">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="6ea58-115">**DWORD**</span></span> | <span data-ttu-id="6ea58-116">0</span><span class="sxs-lookup"><span data-stu-id="6ea58-116">0</span></span>       | <span data-ttu-id="6ea58-117">Especifica a cor a ser gerada.</span><span class="sxs-lookup"><span data-stu-id="6ea58-117">Specifies the color to generate.</span></span> <span data-ttu-id="6ea58-118">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="6ea58-118">See Remarks.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6ea58-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ea58-119">Remarks</span></span>

<span data-ttu-id="6ea58-120">A fonte de cores do vídeo é usada com objetos de origem.</span><span class="sxs-lookup"><span data-stu-id="6ea58-120">The Video Color Source is used with source objects.</span></span> <span data-ttu-id="6ea58-121">Primeiro, crie um novo objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="6ea58-121">First, create a new source object.</span></span> <span data-ttu-id="6ea58-122">Em seguida, defina o GUID do subobjeto do objeto de origem como CLSID \_ colorname chamando o método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="6ea58-122">Then set the source object's subobject GUID to CLSID\_ColorSource, by calling the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="6ea58-123">Para definir a cor, crie um objeto [setter de propriedade](property-setter.md) e aplique a propriedade "Color" no tempo zero.</span><span class="sxs-lookup"><span data-stu-id="6ea58-123">To set the color, create a [Property Setter](property-setter.md) object and apply the "Color" property at time zero.</span></span> <span data-ttu-id="6ea58-124">O valor dessa propriedade é um número hexadecimal com o formato *0xAARRGGBB*, em que *AA* é o valor alfa, *RR* é o valor vermelho, *gg* é o valor verde e *BB* é o valor azul.</span><span class="sxs-lookup"><span data-stu-id="6ea58-124">The value of this property is a hexadecimal number with the format *0xAARRGGBB*, where *AA* is the alpha value, *RR* is the red value, *GG* is the green value, and *BB* is the blue value.</span></span> <span data-ttu-id="6ea58-125">Valores Alfa variam de 0x00 (transparente) a 0xFF (opaco).</span><span class="sxs-lookup"><span data-stu-id="6ea58-125">Alpha values range from 0x00 (transparent) to 0xFF (opaque).</span></span> <span data-ttu-id="6ea58-126">A propriedade é estática e deve ser aplicada no tempo zero.</span><span class="sxs-lookup"><span data-stu-id="6ea58-126">The property is static and must be applied at time zero.</span></span>

<span data-ttu-id="6ea58-127">Se você não especificar o valor alfa, o padrão será zero (transparente).</span><span class="sxs-lookup"><span data-stu-id="6ea58-127">If you do not specify the alpha value, it defaults to zero (transparent).</span></span> <span data-ttu-id="6ea58-128">Em um projeto de vídeo de cor de 32 bits, isso causará transições ou efeitos que usam alfa para renderizar a fonte de cores do vídeo como completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="6ea58-128">In a 32-bit-color video project, this will cause transitions or effects that use alpha to render the Video Color Source as completely transparent.</span></span> <span data-ttu-id="6ea58-129">Para ser seguro, sempre especifique o alfa.</span><span class="sxs-lookup"><span data-stu-id="6ea58-129">To be safe, always specify the alpha.</span></span> <span data-ttu-id="6ea58-130">Por exemplo, o preto opaco é **0xFF000000**.</span><span class="sxs-lookup"><span data-stu-id="6ea58-130">For example, opaque black is **0xFF000000**.</span></span>

<span data-ttu-id="6ea58-131">O exemplo de código a seguir mostra como usar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="6ea58-131">The following code example shows how to use this object.</span></span> <span data-ttu-id="6ea58-132">Para obter mais informações sobre como usar o [**IPropertySetter**](ipropertysetter.md), consulte [definindo propriedades em efeitos e transições](setting-properties-on-effects-and-transitions.md):</span><span class="sxs-lookup"><span data-stu-id="6ea58-132">For more information about using [**IPropertySetter**](ipropertysetter.md), see [Setting Properties on Effects and Transitions](setting-properties-on-effects-and-transitions.md):</span></span>


```C++
DWORD           dwYellow = 0xFFFF00;
IAMTimelineObj  *pSource = NULL;

// Create the source.
HRESULT hr = pTimeline->CreateEmptyNode(&pSource, TIMELINE_MAJOR_TYPE_SOURCE);
if (SUCCEEDED(hr))
{
    hr = pSource->SetStartStop(0, 50000000);
}

if (SUCCEEDED(hr))
{
    hr = pSource->SetSubObjectGUID(CLSID_ColorSource);
}

// Create a property setter.
if (SUCCEEDED(hr))
{
    IPropertySetter *pProp = NULL;
    
    hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pProp));

    if SUCCEEDED(hr))
    {
        // Set the color.    
        DEXTER_PARAM param;
        DEXTER_VALUE val;

        param.Name = SysAllocString(OLESTR("Color"));
        param.dispID = 0;
        param.nValues = 1;

        if (param.Name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            val.v.vt = VT_I4;
            val.v.lVal = dwYellow;
            val.rt = 0;  // Time must be zero.
            val.dwInterp = DEXTERF_JUMP;

            hr = pProp->AddProp(param, &val);
            
            SysFreeString(param.Name);
        }

        if (SUCCEEDED(hr))
        {
            hr = pSource->SetPropertySetter(pProp); 
        }
        pProp->Release();
    }
}
```



<span data-ttu-id="6ea58-133">O exemplo a seguir mostra a representação XML do objeto criado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="6ea58-133">The following example shows the XML representation of the object created in the previous example.</span></span> <span data-ttu-id="6ea58-134">Nesse caso, o elemento [**param**](param-element.md) não oferece suporte a elementos [**at**](at-element.md) ou [**lineares**](linear-element.md) , porque o objeto não oferece suporte a propriedades dinâmicas:</span><span class="sxs-lookup"><span data-stu-id="6ea58-134">In this case the [**param**](param-element.md) element does not support [**at**](at-element.md) or [**linear**](linear-element.md) elements, because the object does not support dynamic properties:</span></span>


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 



