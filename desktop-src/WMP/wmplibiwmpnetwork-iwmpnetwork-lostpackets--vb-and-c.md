---
title: Propriedade IWMPNetwork lostPackets
description: A propriedade lostPackets Obtém o número de pacotes perdidos.
ms.assetid: 611218d3-c4d3-4d4e-835c-1e7a956b2718
keywords:
- Propriedade lostPackets Windows Media Player
- Propriedade lostPackets Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade lostPackets
topic_type:
- apiref
api_name:
- IWMPNetwork.lostPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1adac5f4aa8b1f58c023a556af04b8eae4bd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756341"
---
# <a name="iwmpnetworklostpackets-property"></a><span data-ttu-id="7143d-106">Propriedade IWMPNetwork:: lostPackets</span><span class="sxs-lookup"><span data-stu-id="7143d-106">IWMPNetwork::lostPackets property</span></span>

<span data-ttu-id="7143d-107">A propriedade **lostPackets** Obtém o número de pacotes perdidos.</span><span class="sxs-lookup"><span data-stu-id="7143d-107">The **lostPackets** property gets the number of packets lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="7143d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7143d-108">Syntax</span></span>


```CSharp
public System.Int32 lostPackets {get; set;}
```


```VB

Public ReadOnly Property lostPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="7143d-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7143d-109">Property value</span></span>

<span data-ttu-id="7143d-110">Um **System. Int32** que é o número de pacotes perdidos.</span><span class="sxs-lookup"><span data-stu-id="7143d-110">A **System.Int32** that is the number of lost packets.</span></span>

## <a name="remarks"></a><span data-ttu-id="7143d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7143d-111">Remarks</span></span>

<span data-ttu-id="7143d-112">Essa propriedade inclui somente pacotes de mídia de streaming e retornará zero ao usar o protocolo HTTP, que é sem perdas.</span><span class="sxs-lookup"><span data-stu-id="7143d-112">This property includes streaming media packets only, and will return zero when using the HTTP protocol, which is lossless.</span></span>

<span data-ttu-id="7143d-113">Os pacotes podem ser perdidos por vários motivos, como o tipo e a qualidade da conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="7143d-113">Packets can be lost for a number of reasons, such as the type and quality of the network connection.</span></span>

<span data-ttu-id="7143d-114">Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é redefinida como zero.</span><span class="sxs-lookup"><span data-stu-id="7143d-114">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="7143d-115">O valor não será redefinido se a reprodução for pausada.</span><span class="sxs-lookup"><span data-stu-id="7143d-115">The value is not reset if playback is paused.</span></span> <span data-ttu-id="7143d-116">Essa propriedade obtém informações válidas somente durante o tempo de execução quando a URL para reprodução é definida usando a propriedade **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="7143d-116">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="7143d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7143d-117">Examples</span></span>

<span data-ttu-id="7143d-118">O exemplo de código a seguir usa **lostPackets** para exibir o número total de pacotes perdidos durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="7143d-118">The following code example uses **lostPackets** to display the total number of packets lost during playback.</span></span> <span data-ttu-id="7143d-119">As informações são exibidas em um rótulo quando o usuário clica em um botão.</span><span class="sxs-lookup"><span data-stu-id="7143d-119">The information is displayed in a label when the user clicks a button.</span></span> <span data-ttu-id="7143d-120">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="7143d-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void showLostPackets_Click(object sender, System.EventArgs e)
{
    lostPacketsLabel.Text = ("Packets lost: " + player.network.lostPackets.ToString());
}
```


```VB

Public Sub showLostPackets_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showLostPackets.Click

    lostPacketsLabel.Text = (&quot;Packets lost: &quot; + player.network.lostPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="7143d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7143d-121">Requirements</span></span>



| <span data-ttu-id="7143d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7143d-122">Requirement</span></span> | <span data-ttu-id="7143d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7143d-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7143d-124">Versão</span><span class="sxs-lookup"><span data-stu-id="7143d-124">Version</span></span><br/>   | <span data-ttu-id="7143d-125">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="7143d-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7143d-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="7143d-126">Namespace</span></span><br/> | <span data-ttu-id="7143d-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7143d-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7143d-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="7143d-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7143d-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7143d-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7143d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7143d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7143d-131">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7143d-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7143d-132">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7143d-132">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> </dl>

 

 





