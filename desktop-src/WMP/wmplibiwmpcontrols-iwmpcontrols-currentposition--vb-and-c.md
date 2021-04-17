---
title: Propriedade IWMPControls currentPosition
description: A propriedade currentPosition Obtém ou define a posição atual no item de mídia em segundos desde o início.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- Propriedade currentPosition Windows Media Player
- Propriedade currentPosition Windows Media Player, interface IWMPControls
- Interface IWMPControls Windows Media Player, Propriedade currentPosition
topic_type:
- apiref
api_name:
- IWMPControls.currentPosition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee8c2c8244d6034069f21033978ce2883ff852d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761319"
---
# <a name="iwmpcontrolscurrentposition-property"></a><span data-ttu-id="d6b8f-106">Propriedade IWMPControls:: currentPosition</span><span class="sxs-lookup"><span data-stu-id="d6b8f-106">IWMPControls::currentPosition property</span></span>

<span data-ttu-id="d6b8f-107">A propriedade **CurrentPosition** Obtém ou define a posição atual no item de mídia em segundos desde o início.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-107">The **currentPosition** property gets or sets the current position in the media item in seconds from the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6b8f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6b8f-108">Syntax</span></span>


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a><span data-ttu-id="d6b8f-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d6b8f-109">Property value</span></span>

<span data-ttu-id="d6b8f-110">Um **sistema. Double** que é a posição atual.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-110">A **System.Double** that is the current position.</span></span>

## <a name="examples"></a><span data-ttu-id="d6b8f-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d6b8f-111">Examples</span></span>

<span data-ttu-id="d6b8f-112">O exemplo a seguir usa **CurrentPosition** para buscar uma posição fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-112">The following example uses **currentPosition** to seek to a position provided by the user.</span></span> <span data-ttu-id="d6b8f-113">Em resposta a um clique de botão, **CurrentPosition** é definido como o valor inserido em uma caixa de texto chamada NewPosition.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-113">In response to a button click, **currentPosition** is set to the value entered in a text box called newPosition.</span></span> <span data-ttu-id="d6b8f-114">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setPosition_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text);
}
```


```VB

Public Sub setPosition_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setPosition.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="d6b8f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6b8f-115">Requirements</span></span>



| <span data-ttu-id="d6b8f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6b8f-116">Requirement</span></span> | <span data-ttu-id="d6b8f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d6b8f-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b8f-118">Versão</span><span class="sxs-lookup"><span data-stu-id="d6b8f-118">Version</span></span><br/>   | <span data-ttu-id="d6b8f-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="d6b8f-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d6b8f-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6b8f-120">Namespace</span></span><br/> | <span data-ttu-id="d6b8f-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d6b8f-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d6b8f-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="d6b8f-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d6b8f-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d6b8f-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6b8f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6b8f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6b8f-125">**Interface IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d6b8f-125">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d6b8f-126">**IWMPControls. currentPositionString (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d6b8f-126">**IWMPControls.currentPositionString (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





