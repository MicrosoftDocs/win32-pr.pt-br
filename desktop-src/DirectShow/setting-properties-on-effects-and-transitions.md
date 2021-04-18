---
description: Definindo propriedades em efeitos e transições
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: Definindo propriedades em efeitos e transições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ddd129eb9d4ab24ebef6f5c760a4211f26c9a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105810165"
---
# <a name="setting-properties-on-effects-and-transitions"></a><span data-ttu-id="5e947-103">Definindo propriedades em efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="5e947-103">Setting Properties on Effects and Transitions</span></span>

<span data-ttu-id="5e947-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="5e947-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="5e947-105">Muitos efeitos e transições de [serviços de edição do DirectShow](directshow-editing-services.md) dão suporte a propriedades que controlam seu comportamento.</span><span class="sxs-lookup"><span data-stu-id="5e947-105">Many [DirectShow Editing Services](directshow-editing-services.md) effects and transitions support properties that control their behavior.</span></span> <span data-ttu-id="5e947-106">Um aplicativo pode definir o valor de uma propriedade usando a interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="5e947-106">An application can set the value of a property using the [**IPropertySetter**](ipropertysetter.md) interface.</span></span> <span data-ttu-id="5e947-107">O objeto de transição ou efeito subjacente deve dar suporte a **IDispatch** para definir as propriedades.</span><span class="sxs-lookup"><span data-stu-id="5e947-107">The underlying effect or transition object must support **IDispatch** for setting the properties.</span></span> <span data-ttu-id="5e947-108">Com efeitos de vídeo e transições, o aplicativo pode definir um intervalo de valores que mudam ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="5e947-108">With video effects and transitions, the application can set a range of values that change over time.</span></span> <span data-ttu-id="5e947-109">(Por exemplo, você pode definir uma transição de apagamento para mover para frente e para trás pelo quadro.) Com efeitos de áudio, o valor da propriedade é estático e não pode ser alterado ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="5e947-109">(For example, you can set a wipe transition to move back and forth across the frame.) With audio effects, the value of the property is static and cannot change over time.</span></span> <span data-ttu-id="5e947-110">A única exceção é o efeito de [envelope de volume](volume-envelope-effect.md) , que dá suporte a uma propriedade dinâmica para o nível de volume.</span><span class="sxs-lookup"><span data-stu-id="5e947-110">The only exception is the [Volume Envelope](volume-envelope-effect.md) effect, which supports a dynamic property for the volume level.</span></span>

<span data-ttu-id="5e947-111">Para definir uma propriedade, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e947-111">To set a property, perform the following steps.</span></span>

1.  <span data-ttu-id="5e947-112">Crie uma instância do setter de propriedade (CLSID \_ PropertySetter).</span><span class="sxs-lookup"><span data-stu-id="5e947-112">Create an instance of the property setter (CLSID\_PropertySetter).</span></span>
2.  <span data-ttu-id="5e947-113">Preencha as estruturas [**Dexter \_ param**](dexter-param.md) e [**Dexter \_ Value**](dexter-value.md) com os dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5e947-113">Fill [**DEXTER\_PARAM**](dexter-param.md) and [**DEXTER\_VALUE**](dexter-value.md) structures with the property data.</span></span> <span data-ttu-id="5e947-114">Essas estruturas são discutidas abaixo.</span><span class="sxs-lookup"><span data-stu-id="5e947-114">These structures are discussed below.</span></span>
3.  <span data-ttu-id="5e947-115">Passe as estruturas [**Dexter \_ param**](dexter-param.md) e [**Dexter \_ Value**](dexter-value.md) para o método [**IPropertySetter:: addprop**](ipropertysetter-addprop.md) .</span><span class="sxs-lookup"><span data-stu-id="5e947-115">Pass the [**DEXTER\_PARAM**](dexter-param.md) and [**DEXTER\_VALUE**](dexter-value.md) structures to the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method.</span></span>
4.  <span data-ttu-id="5e947-116">Repita as etapas 2 e 3 para cada propriedade que você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="5e947-116">Repeat steps 2 and 3 for each property you want to set.</span></span>
5.  <span data-ttu-id="5e947-117">Passe o ponteiro de interface [**IPropertySetter**](ipropertysetter.md) para o método [**IAMTimelineObj:: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="5e947-117">Pass the [**IPropertySetter**](ipropertysetter.md) interface pointer to the [**IAMTimelineObj::SetPropertySetter**](iamtimelineobj-setpropertysetter.md) method.</span></span>

<span data-ttu-id="5e947-118">A estrutura do [**\_ parâmetro Dexter**](dexter-param.md) especifica qual propriedade está sendo definida.</span><span class="sxs-lookup"><span data-stu-id="5e947-118">The [**DEXTER\_PARAM**](dexter-param.md) structure specifies which property is being set.</span></span> <span data-ttu-id="5e947-119">Ele contém os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e947-119">It contains the following members.</span></span>

-   <span data-ttu-id="5e947-120">**Nome**: o nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="5e947-120">**Name**: Name of the property</span></span>
-   <span data-ttu-id="5e947-121">**DISPID**: reservado, deve ser zero</span><span class="sxs-lookup"><span data-stu-id="5e947-121">**dispID**: Reserved, must be zero</span></span>
-   <span data-ttu-id="5e947-122">**nValores**: número de valores</span><span class="sxs-lookup"><span data-stu-id="5e947-122">**nValues**: Number of values</span></span>

<span data-ttu-id="5e947-123">A \_ estrutura de valor Dexter especifica o valor de uma propriedade em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="5e947-123">The DEXTER\_VALUE structure specifies the value of a property at a given time.</span></span> <span data-ttu-id="5e947-124">Ele contém os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e947-124">It contains the following members.</span></span>

-   <span data-ttu-id="5e947-125">**v**: tipo Variant que especifica um novo valor para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="5e947-125">**v**: VARIANT type that specifies a new value for the property.</span></span> <span data-ttu-id="5e947-126">O membro **VT** dessa variante define o tipo de dados da propriedade.</span><span class="sxs-lookup"><span data-stu-id="5e947-126">The **vt** member of this VARIANT defines the data type of the property.</span></span> <span data-ttu-id="5e947-127">Para obter mais informações sobre o tipo **Variant** , consulte a SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="5e947-127">For more information on the **VARIANT** type, see the Windows SDK.</span></span>
-   <span data-ttu-id="5e947-128">**RT**: tempo de referência quando a propriedade assume esse valor, em relação à hora de início do efeito ou da transição.</span><span class="sxs-lookup"><span data-stu-id="5e947-128">**rt**: Reference time when the property assumes this value, relative to the starting time of the effect or transition.</span></span> <span data-ttu-id="5e947-129">A hora de início do efeito ou da transição é relativa à hora de início de seu objeto pai.</span><span class="sxs-lookup"><span data-stu-id="5e947-129">The start time of the effect or transition is relative to the start time of its parent object.</span></span>
-   <span data-ttu-id="5e947-130">**dwInterp**: sinalizador que especifica como a propriedade é alterada do valor anterior para o novo valor.</span><span class="sxs-lookup"><span data-stu-id="5e947-130">**dwInterp**: Flag that specifies how the property changes from the previous value to the new value.</span></span> <span data-ttu-id="5e947-131">Com o \_ sinalizador de salto DEXTERF, a propriedade salta instantaneamente para o novo valor na hora especificada.</span><span class="sxs-lookup"><span data-stu-id="5e947-131">With the DEXTERF\_JUMP flag, the property jumps instantly to the new value at the specified time.</span></span> <span data-ttu-id="5e947-132">Com o \_ sinalizador interpolação DEXTERF, a propriedade é interpolada linearmente do valor anterior.</span><span class="sxs-lookup"><span data-stu-id="5e947-132">With the DEXTERF\_INTERPOLATE flag, the property is interpolated linearly from the previous value.</span></span>

<span data-ttu-id="5e947-133">Se você definir o membro **VT** como VT \_ BSTR, o setter da propriedade fará as conversões necessárias.</span><span class="sxs-lookup"><span data-stu-id="5e947-133">If you set the **vt** member to VT\_BSTR, the property setter makes any necessary conversions.</span></span> <span data-ttu-id="5e947-134">Para valores de ponto flutuante, inclua o zero à esquerda antes da casa decimal.</span><span class="sxs-lookup"><span data-stu-id="5e947-134">For floating-point values, include the leading zero before the decimal place.</span></span> <span data-ttu-id="5e947-135">Por exemplo, 0,3, não. 3.</span><span class="sxs-lookup"><span data-stu-id="5e947-135">For example, 0.3, not .3.</span></span>

> [!Note]  
> <span data-ttu-id="5e947-136">Os aplicativos devem evitar depender da conversão de s **BSTR** para valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="5e947-136">Applications should avoid relying on the conversion from **BSTR** s to numeric values.</span></span> <span data-ttu-id="5e947-137">Se a propriedade tiver um valor numérico, use o tipo numérico **Variant** apropriado é possível.</span><span class="sxs-lookup"><span data-stu-id="5e947-137">If the property has a numeric value, use the appropriate numeric **VARIANT** type is possible.</span></span>

 

<span data-ttu-id="5e947-138">O valor de uma propriedade pode ser alterado com o passar do tempo, portanto, o método [**IPropertySetter:: addprop**](ipropertysetter-addprop.md) usa uma única estrutura de [**\_ parâmetro Dexter**](dexter-param.md) e um ponteiro para uma matriz de estruturas de [**\_ valor Dexter**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="5e947-138">The value of a property can change over time, so the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method takes a single [**DEXTER\_PARAM**](dexter-param.md) structure and a pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span> <span data-ttu-id="5e947-139">A matriz define um conjunto de valores baseados em tempo para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="5e947-139">The array defines a set of time-based values for the property.</span></span> <span data-ttu-id="5e947-140">Os membros da matriz devem estar em ordem crescente de tempo e o membro **nValores** da \_ estrutura param Dexter deve ser igual ao comprimento da matriz.</span><span class="sxs-lookup"><span data-stu-id="5e947-140">The members of the array must be in ascending time order, and the **nValues** member of the DEXTER\_PARAM structure must equal the length of the array.</span></span>

<span data-ttu-id="5e947-141">O exemplo de código a seguir cria dados de propriedade para a transição de [apagamento SMPTE](smpte-wipe-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="5e947-141">The following code example creates property data for the [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span> <span data-ttu-id="5e947-142">Ele define o código de apagamento como 120, que cria um apagamento oval.</span><span class="sxs-lookup"><span data-stu-id="5e947-142">It sets the wipe code to 120, which creates an oval wipe.</span></span> <span data-ttu-id="5e947-143">Ele define o tempo de referência como zero, indicando o início da transição.</span><span class="sxs-lookup"><span data-stu-id="5e947-143">It sets the reference time to zero, indicating the start of the transition.</span></span>


```C++
IPropertySetter     *pProp;   // Property setter
IAMTimelineObj      *pTransObj;  // Transition object
// Create an SMPTE Wipe transition object. (Not shown)

hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER,
    IID_IPropertySetter, (void**) &pProp);

// Error checking is omitted for clarity...

DEXTER_PARAM param;
DEXTER_VALUE *pValue = (DEXTER_VALUE*)CoTaskMemAlloc(sizeof(DEXTER_VALUE));

// Initialize the parameter. 
param.Name = SysAllocString(L"MaskNum");
param.dispID = 0;
param.nValues = 1;

// Initialize the value.
pValue->v.vt = VT_I4;
pValue->v.lVal = 120; // Oval
pValue->rt = 0;
pValue->dwInterp = DEXTERF_JUMP;

pProp->AddProp(param, pValue);

// Free allocated resources.
SysFreeString(param.Name);
VariantClear(&(pValue->v));
CoTaskMemFree(pValue);

// Set the property on the transition.
pTransObj->SetPropertySetter(pProp);
pProp->Release();
```



<span data-ttu-id="5e947-144">**Alterando dinamicamente as propriedades**</span><span class="sxs-lookup"><span data-stu-id="5e947-144">**Dynamically Changing Properties**</span></span>

<span data-ttu-id="5e947-145">Depois de renderizar um projeto de edição de vídeo, é possível modificar as propriedades de um efeito ou de um objeto de transição enquanto o grafo está em execução.</span><span class="sxs-lookup"><span data-stu-id="5e947-145">After you render a video editing project, it is possible to modify an effect or transition object's properties while the graph is running.</span></span> <span data-ttu-id="5e947-146">No entanto, isso só será possível se você definir propriedades nesse objeto antes do aplicativo chamado [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="5e947-146">However, this is possible only if you set properties on that object before the application called [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span> <span data-ttu-id="5e947-147">Nesse caso, você pode chamar [**IAMTimelineObj:: GetPropertySetter**](iamtimelineobj-getpropertysetter.md) sobre o efeito ou a transição, limpar ou modificar as propriedades, e as alterações ocorrerão dinamicamente à medida que o grafo estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="5e947-147">If so, you can call [**IAMTimelineObj::GetPropertySetter**](iamtimelineobj-getpropertysetter.md) on the effect or transition, clear or modify the properties, and the changes will happen dynamically as the graph is running.</span></span> <span data-ttu-id="5e947-148">Pode haver anomalias visuais enquanto a alteração ocorre, portanto, isso é recomendado apenas para visualização.</span><span class="sxs-lookup"><span data-stu-id="5e947-148">There may be visual anomalies while the change occurs, so this is recommended only for preview.</span></span> <span data-ttu-id="5e947-149">Não altere as propriedades enquanto estiver gravando o projeto em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e947-149">Do not change the properties while you are writing the project to a file.</span></span>

<span data-ttu-id="5e947-150">Se você não definiu nenhuma propriedade no objeto de efeito ou de transição antes de chamar **ConnectFrontEnd**, não será possível adicionar propriedades a ele enquanto o grafo estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="5e947-150">If you did not set any properties on the effect or transition object before you called **ConnectFrontEnd**, you cannot add properties to it while the graph is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e947-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e947-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e947-152">Trabalhando com efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="5e947-152">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



