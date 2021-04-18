---
title: Propriedade IWMPNetwork framesSkipped
description: A propriedade framesSkipped Obtém o número total de quadros ignorados durante a reprodução.
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- Propriedade framesSkipped Windows Media Player
- Propriedade framesSkipped Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade framesSkipped
topic_type:
- apiref
api_name:
- IWMPNetwork.framesSkipped
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8409cec50089111184f96e4463f57cc9c4fbae07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749425"
---
# <a name="iwmpnetworkframesskipped-property"></a><span data-ttu-id="1a8d4-106">Propriedade IWMPNetwork:: framesSkipped</span><span class="sxs-lookup"><span data-stu-id="1a8d4-106">IWMPNetwork::framesSkipped property</span></span>

<span data-ttu-id="1a8d4-107">A propriedade **framesSkipped** Obtém o número total de quadros ignorados durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="1a8d4-107">The **framesSkipped** property gets the total number of frames skipped during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a8d4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a8d4-108">Syntax</span></span>


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="1a8d4-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1a8d4-109">Property value</span></span>

<span data-ttu-id="1a8d4-110">Um **System. Int32** que é o número de quadros ignorados.</span><span class="sxs-lookup"><span data-stu-id="1a8d4-110">A **System.Int32** that is the number of frames skipped.</span></span>

## <a name="examples"></a><span data-ttu-id="1a8d4-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1a8d4-111">Examples</span></span>

<span data-ttu-id="1a8d4-112">O exemplo de código a seguir usa **framesSkipped** para exibir o número total de quadros ignorados durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="1a8d4-112">The following code example uses **framesSkipped** to display the total number of frames skipped during playback.</span></span> <span data-ttu-id="1a8d4-113">As informações são exibidas em um rótulo quando o usuário clica em um botão.</span><span class="sxs-lookup"><span data-stu-id="1a8d4-113">The information is displayed in a label when the user clicks a button.</span></span> <span data-ttu-id="1a8d4-114">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="1a8d4-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void showFramesSkipped_Click(object sender, System.EventArgs e)
{
    framesSkippedLabel.Text = ("Frames skipped: " + player.network.framesSkipped.ToString());
}
```


```VB

Public Sub showFramesSkipped_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showFramesSkipped.Click

    framesSkippedLabel.Text = (&quot;Frames skipped: &quot; + player.network.framesSkipped.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1a8d4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a8d4-115">Requirements</span></span>



| <span data-ttu-id="1a8d4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a8d4-116">Requirement</span></span> | <span data-ttu-id="1a8d4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1a8d4-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a8d4-118">Versão</span><span class="sxs-lookup"><span data-stu-id="1a8d4-118">Version</span></span><br/>   | <span data-ttu-id="1a8d4-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="1a8d4-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1a8d4-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a8d4-120">Namespace</span></span><br/> | <span data-ttu-id="1a8d4-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1a8d4-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1a8d4-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="1a8d4-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1a8d4-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1a8d4-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a8d4-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a8d4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a8d4-125">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1a8d4-125">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





