---
title: IWMPSettings. IsAvailable (VB e C)
description: A propriedade IsAvailable (o \_ método Get IsAvailable em C \) Obtém um valor que indica se uma ação especificada pode ser executada.
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- IWMPSettings. IsAvailable (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPSettings.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932f0adb325c4c2f9f88e9f80d75ecaecd3ca85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781181"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a><span data-ttu-id="e3aff-104">IWMPSettings. IsAvailable (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="e3aff-104">IWMPSettings.isAvailable (VB and C#)</span></span>

<span data-ttu-id="e3aff-105">A propriedade **IsAvailable** (o método **Get \_ IsAvailable** em C#) Obtém um valor que indica se uma ação especificada pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="e3aff-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value that indicates whether a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a><span data-ttu-id="e3aff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3aff-106">Parameters</span></span>

<span data-ttu-id="e3aff-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="e3aff-107">*bstrItem*</span></span>

<span data-ttu-id="e3aff-108">Um **System. String** que é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e3aff-108">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="e3aff-109">Valor</span><span class="sxs-lookup"><span data-stu-id="e3aff-109">Value</span></span>              | <span data-ttu-id="e3aff-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3aff-110">Description</span></span>                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3aff-111">AutoStart</span><span class="sxs-lookup"><span data-stu-id="e3aff-111">AutoStart</span></span>          | <span data-ttu-id="e3aff-112">Descobre se a propriedade AutoStart pode ser definida para especificar que o Windows Media Player inicia automaticamente a reprodução.</span><span class="sxs-lookup"><span data-stu-id="e3aff-112">Discovers whether the autoStart property can be set to specify that Windows Media Player starts playback automatically.</span></span> |
| <span data-ttu-id="e3aff-113">Saldo</span><span class="sxs-lookup"><span data-stu-id="e3aff-113">Balance</span></span>            | <span data-ttu-id="e3aff-114">Descobre se a propriedade de saldo pode ser usada para definir o saldo de estéreo.</span><span class="sxs-lookup"><span data-stu-id="e3aff-114">Discovers whether the balance property can be used to set the stereo balance.</span></span>                                           |
| <span data-ttu-id="e3aff-115">BaseURL</span><span class="sxs-lookup"><span data-stu-id="e3aff-115">BaseURL</span></span>            | <span data-ttu-id="e3aff-116">Descobre se a propriedade baseURL pode ser definida para especificar uma URL base.</span><span class="sxs-lookup"><span data-stu-id="e3aff-116">Discovers whether the baseURL property can be set to specify a base URL.</span></span>                                                |
| <span data-ttu-id="e3aff-117">DefaultFrame</span><span class="sxs-lookup"><span data-stu-id="e3aff-117">DefaultFrame</span></span>       | <span data-ttu-id="e3aff-118">Descobre se a propriedade DefaultFrame pode ser definida para especificar o quadro padrão.</span><span class="sxs-lookup"><span data-stu-id="e3aff-118">Discovers whether the defaultFrame property can be set to specify the default frame.</span></span>                                    |
| <span data-ttu-id="e3aff-119">EnableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="e3aff-119">EnableErrorDialogs</span></span> | <span data-ttu-id="e3aff-120">Descobre se a propriedade enableErrorDialogs pode ser definida para habilitar ou desabilitar a exibição de caixas de diálogo de erro.</span><span class="sxs-lookup"><span data-stu-id="e3aff-120">Discovers whether the enableErrorDialogs property can be set to enable or disable displaying error dialog boxes.</span></span>        |
| <span data-ttu-id="e3aff-121">GetMode</span><span class="sxs-lookup"><span data-stu-id="e3aff-121">GetMode</span></span>            | <span data-ttu-id="e3aff-122">Descobre se o método GetMode pode ser usado para recuperar o modo de loop atual ou de ordem aleatória.</span><span class="sxs-lookup"><span data-stu-id="e3aff-122">Discovers whether the getMode method can be used to retrieve the current loop or shuffle mode.</span></span>                          |
| <span data-ttu-id="e3aff-123">InvokeURLs</span><span class="sxs-lookup"><span data-stu-id="e3aff-123">InvokeURLs</span></span>         | <span data-ttu-id="e3aff-124">Descobre se a propriedade invokeURLs pode ser definida para especificar se os eventos de URL devem iniciar um navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="e3aff-124">Discovers whether the invokeURLs property can be set to specify whether URL events should launch a Web browser.</span></span>         |
| <span data-ttu-id="e3aff-125">Mute</span><span class="sxs-lookup"><span data-stu-id="e3aff-125">Mute</span></span>               | <span data-ttu-id="e3aff-126">Descobre se a propriedade MUTE pode ser definida para especificar se a saída de áudio está ativada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="e3aff-126">Discovers whether the mute property can be set to specify whether the audio output is on or off.</span></span>                        |
| <span data-ttu-id="e3aff-127">PlayCount</span><span class="sxs-lookup"><span data-stu-id="e3aff-127">PlayCount</span></span>          | <span data-ttu-id="e3aff-128">Descobre se a propriedade playCount pode ser definida para especificar o número de vezes que um item de mídia será reproduzido.</span><span class="sxs-lookup"><span data-stu-id="e3aff-128">Discovers whether the playCount property can be set to specify the number times a media item will play.</span></span>                 |
| <span data-ttu-id="e3aff-129">Tarifa</span><span class="sxs-lookup"><span data-stu-id="e3aff-129">Rate</span></span>               | <span data-ttu-id="e3aff-130">Descobre se a propriedade de taxa pode ser definida para controlar a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="e3aff-130">Discovers whether the rate property can be set to control the playback rate.</span></span>                                            |
| <span data-ttu-id="e3aff-131">Setmode</span><span class="sxs-lookup"><span data-stu-id="e3aff-131">SetMode</span></span>            | <span data-ttu-id="e3aff-132">Descobre se o método setmode pode ser usado para especificar o modo de loop ou de ordem aleatória atual.</span><span class="sxs-lookup"><span data-stu-id="e3aff-132">Discovers whether the setMode method can be used to specify the current loop or shuffle mode.</span></span>                           |
| <span data-ttu-id="e3aff-133">Volume</span><span class="sxs-lookup"><span data-stu-id="e3aff-133">Volume</span></span>             | <span data-ttu-id="e3aff-134">Descobre se a propriedade do volume pode ser definida para especificar o volume de áudio.</span><span class="sxs-lookup"><span data-stu-id="e3aff-134">Discovers whether the volume property can be set to specify the audio volume.</span></span>                                           |



 

## <a name="property-value"></a><span data-ttu-id="e3aff-135">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e3aff-135">Property Value</span></span>

<span data-ttu-id="e3aff-136">Um valor **System. booliano** que indica se a ação especificada pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="e3aff-136">A **System.Boolean** value indicating whether the specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3aff-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3aff-137">Remarks</span></span>

<span data-ttu-id="e3aff-138">**IWMPSettings. isidêntico** é uma propriedade em Visual Basic que usa um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e3aff-138">**IWMPSettings.isIdentical** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="e3aff-139">Em C#, ele é chamado de método **IWMPSettings. get \_ isidêntico** .</span><span class="sxs-lookup"><span data-stu-id="e3aff-139">In C# it is referred to as the **IWMPSettings.get\_isIdentical** method.</span></span>

## <a name="examples"></a><span data-ttu-id="e3aff-140">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e3aff-140">Examples</span></span>

<span data-ttu-id="e3aff-141">O exemplo a seguir testa cada uma das propriedades **IWMPSettings** usando a propriedade **IsAvailable** (o método **Get \_ IsAvailable** em C#).</span><span class="sxs-lookup"><span data-stu-id="e3aff-141">The following example tests each of the **IWMPSettings** properties using the **isAvailable** property (the **get\_isAvailable** method in C#).</span></span> <span data-ttu-id="e3aff-142">O nome da propriedade e o resultado de cada teste são exibidos em uma caixa de texto de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="e3aff-142">The property name and the result of each test are displayed in a multi-line text box.</span></span> <span data-ttu-id="e3aff-143">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="e3aff-143">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create a string array that contains a list of IWMPSettings properties.
string[] propertyList = new string[12]{
    "AutoStart", "Balance", "BaseURL", "DefaultFrame", "EnableErrorDialogs",
    "GetMode", "InvokeURLs", "Mute", "PlayCount", "Rate", "SetMode", "Volume"
};

// Create another string array of the same size to hold the result of each
// call to get_isAvailable.
string[] results = new string[12];

// Test each property using get_isAvailable and add the name of the property
// and the result of the test to the results array.
for (int i = 0; i < propertyList.Length; i++)
{
    bool isAvailable = player.settings.get_isAvailable(propertyList[i]);

    results[i] = (propertyList[i] + " = " + isAvailable.ToString());
}

// Display the results in a multi-line text box.
playerSettings.Lines = results;
```


```VB

'  Create a string array that contains a list of IWMPSettings properties.
Dim propertyList As String() = New String(11) { _
    &quot;AutoStart&quot;, &quot;Balance&quot;, &quot;BaseURL&quot;, &quot;DefaultFrame&quot;, &quot;EnableErrorDialogs&quot;, _
    &quot;GetMode&quot;, &quot;InvokeURLs&quot;, &quot;Mute&quot;, &quot;PlayCount&quot;, &quot;Rate&quot;, &quot;SetMode&quot;, &quot;Volume&quot; _
}

&#39;  Create another string array of the same size to hold the result of each
&#39;  call to get_isAvailable.
Dim results(12) As String

&#39;  Test each property using isAvailable and add the name of the property
&#39;  and the result of the test to the results array.
For i As Integer = 0 To (propertyList.Length - 1)

    Dim isAvailable As Boolean = player.settings.isAvailable(propertyList(i))
    results(i) = (propertyList(i) + &quot; = &quot; + isAvailable.ToString())

Next i

&#39;  Display the results in a multi-line text box.
playerSettings.Lines = results
```





## <a name="requirements"></a><span data-ttu-id="e3aff-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3aff-144">Requirements</span></span>



| <span data-ttu-id="e3aff-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3aff-145">Requirement</span></span> | <span data-ttu-id="e3aff-146">Valor</span><span class="sxs-lookup"><span data-stu-id="e3aff-146">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3aff-147">Versão</span><span class="sxs-lookup"><span data-stu-id="e3aff-147">Version</span></span><br/>   | <span data-ttu-id="e3aff-148">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="e3aff-148">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e3aff-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3aff-149">Namespace</span></span><br/> | <span data-ttu-id="e3aff-150">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e3aff-150">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e3aff-151">Assembly</span><span class="sxs-lookup"><span data-stu-id="e3aff-151">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e3aff-152"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e3aff-152"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3aff-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3aff-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3aff-154">**Interface IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3aff-154">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3aff-155">**IWMPSettings. AutoStart (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3aff-155">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3aff-156">**IWMPSettings. Balance (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3aff-156">**IWMPSettings.balance (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3aff-157">**IWMPSettings. baseURL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3aff-157">**IWMPSettings.baseURL (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3aff-158">**IWMPSettings. DefaultFrame (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3aff-158">**IWMPSettings.defaultFrame (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3aff-159">**IWMPSettings. enableErrorDialogs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3aff-159">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3aff-160">**IWMPSettings. GetMode (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3aff-160">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3aff-161">**IWMPSettings. invokeURLs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3aff-161">**IWMPSettings.invokeURLs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3aff-162">**IWMPSettings. mudo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3aff-162">**IWMPSettings.mute (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3aff-163">**IWMPSettings. playCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3aff-163">**IWMPSettings.playCount (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3aff-164">**IWMPSettings. Rate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3aff-164">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3aff-165">**IWMPSettings. setMode (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3aff-165">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3aff-166">**IWMPSettings. volume (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3aff-166">**IWMPSettings.volume (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





