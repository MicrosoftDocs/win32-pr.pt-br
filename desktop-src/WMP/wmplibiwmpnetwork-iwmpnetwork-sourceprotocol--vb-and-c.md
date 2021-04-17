---
title: Propriedade IWMPNetwork sourceProtocol
description: A propriedade sourceProtocol Obtém o protocolo de origem usado para receber dados.
ms.assetid: db1d7651-3f25-4ac9-a3e1-dc3a8ddf8c40
keywords:
- Propriedade sourceProtocol Windows Media Player
- Propriedade sourceProtocol Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade sourceProtocol
topic_type:
- apiref
api_name:
- IWMPNetwork.sourceProtocol
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5017e1a053c124a1f7f50668c6f392eb541d57f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798403"
---
# <a name="iwmpnetworksourceprotocol-property"></a><span data-ttu-id="89685-106">Propriedade IWMPNetwork:: sourceProtocol</span><span class="sxs-lookup"><span data-stu-id="89685-106">IWMPNetwork::sourceProtocol property</span></span>

<span data-ttu-id="89685-107">A propriedade **sourceProtocol** Obtém o protocolo de origem usado para receber dados.</span><span class="sxs-lookup"><span data-stu-id="89685-107">The **sourceProtocol** property gets the source protocol used to receive data.</span></span>

## <a name="syntax"></a><span data-ttu-id="89685-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="89685-108">Syntax</span></span>


```CSharp
public System.String sourceProtocol {get; set;}
```


```VB

Public ReadOnly Property sourceProtocol As System.String
```





## <a name="property-value"></a><span data-ttu-id="89685-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="89685-109">Property value</span></span>

<span data-ttu-id="89685-110">Um **System. String** que é o nome do protocolo de origem.</span><span class="sxs-lookup"><span data-stu-id="89685-110">A **System.String** that is the name of the source protocol.</span></span>

## <a name="remarks"></a><span data-ttu-id="89685-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="89685-111">Remarks</span></span>

<span data-ttu-id="89685-112">Essa propriedade Obtém uma cadeia de caracteres de comprimento zero ("") ao reproduzir um CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="89685-112">This property gets a zero-length string ("") when playing a CD or DVD.</span></span>

## <a name="examples"></a><span data-ttu-id="89685-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="89685-113">Examples</span></span>

<span data-ttu-id="89685-114">O exemplo de código a seguir usa **sourceProtocol** para exibir o protocolo de origem usado para receber dados.</span><span class="sxs-lookup"><span data-stu-id="89685-114">The following code example uses **sourceProtocol** to display the source protocol used to receive data.</span></span> <span data-ttu-id="89685-115">As informações são exibidas em um rótulo, em resposta ao evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="89685-115">The information is displayed in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="89685-116">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="89685-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the network source protocol when the player is playing by testing for a 
    // play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3. 
    if (e.newState == 3) 
    {
        sourceProtocolLabel.Text = ("Source protocol: " + player.network.sourceProtocol);
    } 
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the network source protocol when the player is playing by testing for a 
    &#39; play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3.
    If (e.newState = 3) Then

        sourceProtocolLabel.Text = (&quot;Source protocol: &quot; + player.network.sourceProtocol)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="89685-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89685-117">Requirements</span></span>



| <span data-ttu-id="89685-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="89685-118">Requirement</span></span> | <span data-ttu-id="89685-119">Valor</span><span class="sxs-lookup"><span data-stu-id="89685-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89685-120">Versão</span><span class="sxs-lookup"><span data-stu-id="89685-120">Version</span></span><br/>   | <span data-ttu-id="89685-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="89685-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="89685-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="89685-122">Namespace</span></span><br/> | <span data-ttu-id="89685-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="89685-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="89685-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="89685-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="89685-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="89685-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89685-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="89685-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89685-127">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="89685-127">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





