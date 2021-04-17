---
title: IWMPControls. IsAvailable (VB e C)
description: A propriedade IsAvailable (o \_ método Get IsAvailable em C \) Obtém um valor que indica se um tipo de informação especificado está disponível ou uma ação especificada pode ser executada.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- IWMPControls. IsAvailable (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPControls.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d5d9ffcd6cad6eefb7cdff25fd2cf34b76ccc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762067"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a><span data-ttu-id="e0a44-104">IWMPControls. IsAvailable (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="e0a44-104">IWMPControls.isAvailable (VB and C#)</span></span>

<span data-ttu-id="e0a44-105">A propriedade **IsAvailable** (o método **Get \_ IsAvailable** em C#) Obtém um valor que indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="e0a44-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value indicating whether a specified type of information is available or a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
bool get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a><span data-ttu-id="e0a44-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0a44-106">Parameters</span></span>

<span data-ttu-id="e0a44-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="e0a44-107">*bstrItem*</span></span>

<span data-ttu-id="e0a44-108">Um System. String que é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0a44-108">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="e0a44-109">Valor</span><span class="sxs-lookup"><span data-stu-id="e0a44-109">Value</span></span>           | <span data-ttu-id="e0a44-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0a44-110">Description</span></span>                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0a44-111">currentItem</span><span class="sxs-lookup"><span data-stu-id="e0a44-111">currentItem</span></span>     | <span data-ttu-id="e0a44-112">Descobre se o usuário pode definir a propriedade **IWMPControls. currentItem** .</span><span class="sxs-lookup"><span data-stu-id="e0a44-112">Discovers whether the user can set the **IWMPControls.currentItem** property.</span></span>                                                                                     |
| <span data-ttu-id="e0a44-113">currentMarker</span><span class="sxs-lookup"><span data-stu-id="e0a44-113">currentMarker</span></span>   | <span data-ttu-id="e0a44-114">Descobre se o usuário pode buscar um marcador específico.</span><span class="sxs-lookup"><span data-stu-id="e0a44-114">Discovers whether the user can seek to a specific marker.</span></span>                                                                                                         |
| <span data-ttu-id="e0a44-115">currentPosition</span><span class="sxs-lookup"><span data-stu-id="e0a44-115">currentPosition</span></span> | <span data-ttu-id="e0a44-116">Descobre se o usuário pode buscar uma posição específica no arquivo.</span><span class="sxs-lookup"><span data-stu-id="e0a44-116">Discovers whether the user can seek to a specific position in the file.</span></span> <span data-ttu-id="e0a44-117">Alguns arquivos não dão suporte à busca.</span><span class="sxs-lookup"><span data-stu-id="e0a44-117">Some files do not support seeking.</span></span>                                                        |
| <span data-ttu-id="e0a44-118">fastForward</span><span class="sxs-lookup"><span data-stu-id="e0a44-118">fastForward</span></span>     | <span data-ttu-id="e0a44-119">Descobre se o arquivo dá suporte ao encaminhamento rápido e se essa funcionalidade pode ser invocada.</span><span class="sxs-lookup"><span data-stu-id="e0a44-119">Discovers whether the file supports fast forwarding and whether that functionality can be invoked.</span></span> <span data-ttu-id="e0a44-120">Muitos tipos de arquivo (e transmissões ao vivo) não dão suporte a fastForward.</span><span class="sxs-lookup"><span data-stu-id="e0a44-120">Many file types (and live streams) do not support fastForward.</span></span> |
| <span data-ttu-id="e0a44-121">fastReverse</span><span class="sxs-lookup"><span data-stu-id="e0a44-121">fastReverse</span></span>     | <span data-ttu-id="e0a44-122">Descobre se o arquivo dá suporte a fastReverse e se essa funcionalidade pode ser invocada.</span><span class="sxs-lookup"><span data-stu-id="e0a44-122">Discovers whether the file supports fastReverse and whether that functionality can be invoked.</span></span> <span data-ttu-id="e0a44-123">Muitos tipos de arquivo (e transmissões ao vivo) não dão suporte a fastReverse.</span><span class="sxs-lookup"><span data-stu-id="e0a44-123">Many file types (and live streams) do not support fastReverse.</span></span>     |
| <span data-ttu-id="e0a44-124">Próximo</span><span class="sxs-lookup"><span data-stu-id="e0a44-124">next</span></span>            | <span data-ttu-id="e0a44-125">Descobre se o usuário pode buscar a próxima entrada em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="e0a44-125">Discovers whether the user can seek to the next entry in a playlist.</span></span>                                                                                              |
| <span data-ttu-id="e0a44-126">pause</span><span class="sxs-lookup"><span data-stu-id="e0a44-126">pause</span></span>           | <span data-ttu-id="e0a44-127">Descobre se o método **IWMPControls. Pause** está disponível.</span><span class="sxs-lookup"><span data-stu-id="e0a44-127">Discovers whether the **IWMPControls.pause** method is available.</span></span>                                                                                                 |
| <span data-ttu-id="e0a44-128">jogar</span><span class="sxs-lookup"><span data-stu-id="e0a44-128">play</span></span>            | <span data-ttu-id="e0a44-129">Descobre se o método **IWMPControls. Play** está disponível.</span><span class="sxs-lookup"><span data-stu-id="e0a44-129">Discovers whether the **IWMPControls.play** method is available.</span></span>                                                                                                  |
| <span data-ttu-id="e0a44-130">previous</span><span class="sxs-lookup"><span data-stu-id="e0a44-130">previous</span></span>        | <span data-ttu-id="e0a44-131">Descobre se o usuário pode buscar a entrada anterior em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="e0a44-131">Discovers whether the user can seek to the previous entry in a playlist.</span></span>                                                                                          |
| <span data-ttu-id="e0a44-132">Etapa</span><span class="sxs-lookup"><span data-stu-id="e0a44-132">step</span></span>            | <span data-ttu-id="e0a44-133">Descobre se o método **IWMPControls2. Step** está disponível durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="e0a44-133">Discovers whether the **IWMPControls2.step** method is available during playback.</span></span>                                                                                 |
| <span data-ttu-id="e0a44-134">parar</span><span class="sxs-lookup"><span data-stu-id="e0a44-134">stop</span></span>            | <span data-ttu-id="e0a44-135">Descobre se o método **IWMPControls. Stop** está disponível.</span><span class="sxs-lookup"><span data-stu-id="e0a44-135">Discovers whether the **IWMPControls.stop** method is available.</span></span>                                                                                                  |



 

## <a name="property-value"></a><span data-ttu-id="e0a44-136">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e0a44-136">Property Value</span></span>

<span data-ttu-id="e0a44-137">**System.Boolean**</span><span class="sxs-lookup"><span data-stu-id="e0a44-137">**System.Boolean**</span></span>

<span data-ttu-id="e0a44-138">Um **System. Boolean** que indica se um tipo especificado de informações está disponível ou se uma ação especificada pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="e0a44-138">A **System.Boolean** that indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0a44-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0a44-139">Remarks</span></span>

<span data-ttu-id="e0a44-140">**IWMPControls. IsAvailable** é uma propriedade em Visual Basic que usa um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e0a44-140">**IWMPControls.isAvailable** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="e0a44-141">Em C#, ele é conhecido como o método **IWMPControls. get \_ IsAvailable** .</span><span class="sxs-lookup"><span data-stu-id="e0a44-141">In C# it is referred to as the **IWMPControls.get\_isAvailable** method.</span></span>

## <a name="examples"></a><span data-ttu-id="e0a44-142">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0a44-142">Examples</span></span>

<span data-ttu-id="e0a44-143">O exemplo a seguir usa a propriedade **IsAvailable** (o método **Get \_ IsAvailable** em C#) para verificar se o item de mídia atual dá suporte à propriedade **CurrentPosition** .</span><span class="sxs-lookup"><span data-stu-id="e0a44-143">The following example uses the **isAvailable** property (the **get\_isAvailable** method in C#) to verify that the current media item supports the **currentPosition** property.</span></span> <span data-ttu-id="e0a44-144">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="e0a44-144">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// If the currentPosition property is supported, seek to position 0.
if (player.Ctlcontrols.get_isAvailable("currentPosition"))
{
    player.Ctlcontrols.currentPosition = 0;
}
```


```VB

' If the currentPosition property is supported, seek to position 0.
If (player.Ctlcontrols.isAvailable(&quot;currentPosition&quot;)) Then

    player.Ctlcontrols.currentPosition = 0

End If
```





## <a name="requirements"></a><span data-ttu-id="e0a44-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0a44-145">Requirements</span></span>



| <span data-ttu-id="e0a44-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0a44-146">Requirement</span></span> | <span data-ttu-id="e0a44-147">Valor</span><span class="sxs-lookup"><span data-stu-id="e0a44-147">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0a44-148">Versão</span><span class="sxs-lookup"><span data-stu-id="e0a44-148">Version</span></span><br/>   | <span data-ttu-id="e0a44-149">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="e0a44-149">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e0a44-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0a44-150">Namespace</span></span><br/> | <span data-ttu-id="e0a44-151">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e0a44-151">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e0a44-152">Assembly</span><span class="sxs-lookup"><span data-stu-id="e0a44-152">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e0a44-153"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e0a44-153"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0a44-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0a44-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0a44-155">**Interface IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0a44-155">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0a44-156">**IWMPControls. currentItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0a44-156">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0a44-157">**IWMPControls. PAUSE (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0a44-157">**IWMPControls.pause (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0a44-158">**IWMPControls. Play (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0a44-158">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0a44-159">**IWMPControls. Stop (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0a44-159">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0a44-160">**IWMPControls2. Step (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0a44-160">**IWMPControls2.step (VB and C#)**</span></span>](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





