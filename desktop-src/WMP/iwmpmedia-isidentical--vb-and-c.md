---
title: IWMPMedia. isidêntico (VB e C)
description: A propriedade isidêntica (o \_ método Get Isidênticos em C \) Obtém um valor que indica se o item de mídia especificado é o mesmo que o atual.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- IWMPMedia. isidêntico (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPMedia.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a488ad300362c1f8dccfd0fa6f6c7e4dee7676
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758194"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a><span data-ttu-id="feaeb-104">IWMPMedia. isidêntico (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="feaeb-104">IWMPMedia.isIdentical (VB and C#)</span></span>

<span data-ttu-id="feaeb-105">A propriedade **isidêntica** (o método **Get \_ isidênticos** em C#) Obtém um valor que indica se o item de mídia especificado é o mesmo que o atual.</span><span class="sxs-lookup"><span data-stu-id="feaeb-105">The **isIdentical** property (the **get\_isIdentical** method in C#) gets a value indicating whether the specified media item is the same as the current one.</span></span>


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPMedia As IWMPMedia
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPMedia pIWMPMedia
);
```



## <a name="parameters"></a><span data-ttu-id="feaeb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="feaeb-106">Parameters</span></span>

<span data-ttu-id="feaeb-107">*pIWMPMedia*</span><span class="sxs-lookup"><span data-stu-id="feaeb-107">*pIWMPMedia*</span></span>

<span data-ttu-id="feaeb-108">Uma interface **WMPLib. IWMPMedia** para o item de mídia a ser comparado com o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="feaeb-108">A **WMPLib.IWMPMedia** interface to the media item to be compared with the current media item.</span></span>

## <a name="property-value"></a><span data-ttu-id="feaeb-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="feaeb-109">Property Value</span></span>

<span data-ttu-id="feaeb-110">Um valor **System. Boolean** que indica se os dois itens de mídia são idênticos.</span><span class="sxs-lookup"><span data-stu-id="feaeb-110">A **System.Boolean** value that indicates whether the two media items are identical.</span></span>

## <a name="remarks"></a><span data-ttu-id="feaeb-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="feaeb-111">Remarks</span></span>

<span data-ttu-id="feaeb-112">**IWMPMedia. isidêntico** é uma propriedade em Visual Basic que usa um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="feaeb-112">**IWMPMedia.isIdentical** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="feaeb-113">Em C#, ele é chamado de método **IWMPMedia. get \_ isidêntico** .</span><span class="sxs-lookup"><span data-stu-id="feaeb-113">In C# it is referred to as the **IWMPMedia.get\_isIdentical** method.</span></span>

## <a name="examples"></a><span data-ttu-id="feaeb-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="feaeb-114">Examples</span></span>

<span data-ttu-id="feaeb-115">O exemplo a seguir usa a propriedade **isidêntica** (o método **Get \_ isidêntico** em C#) para verificar se um item de mídia chamado newMedia é o mesmo que o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="feaeb-115">The following example uses the **isIdentical** property (the **get\_isIdentical** method in C#) to check whether a media item named newMedia is the same as the current media item.</span></span> <span data-ttu-id="feaeb-116">Se eles não forem iguais, o novo item de mídia será reproduzido.</span><span class="sxs-lookup"><span data-stu-id="feaeb-116">If they are not the same, the new media item is played.</span></span> <span data-ttu-id="feaeb-117">Caso contrário, a mídia atual continuará a ser executada sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="feaeb-117">Otherwise, the current media continues to play uninterrupted.</span></span> <span data-ttu-id="feaeb-118">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="feaeb-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
if (newMedia.get_isIdentical(player.currentMedia) != true)
{
    // Change the current media to the new media item.
    player.currentMedia = newMedia;

    // Play the new media item.
    player.Ctlcontrols.play();
}
```


```VB

If (newMedia.isIdentical(player.currentMedia) <> True) Then

    &#39; Change the current media to the new media item.
    player.currentMedia = newMedia

    &#39; Play the new media item.
    player.Ctlcontrols.play()

End If
```





## <a name="requirements"></a><span data-ttu-id="feaeb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="feaeb-119">Requirements</span></span>



| <span data-ttu-id="feaeb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="feaeb-120">Requirement</span></span> | <span data-ttu-id="feaeb-121">Valor</span><span class="sxs-lookup"><span data-stu-id="feaeb-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feaeb-122">Versão</span><span class="sxs-lookup"><span data-stu-id="feaeb-122">Version</span></span><br/>   | <span data-ttu-id="feaeb-123">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="feaeb-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="feaeb-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="feaeb-124">Namespace</span></span><br/> | <span data-ttu-id="feaeb-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="feaeb-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="feaeb-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="feaeb-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="feaeb-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="feaeb-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feaeb-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="feaeb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feaeb-129">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="feaeb-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





