---
title: Método Next IWMPControls
description: O método Next define o próximo item na playlist como o item atual.
ms.assetid: 3f82ef25-a1e0-4845-b0ed-dd6463719577
keywords:
- próximo método Windows Media Player
- próximo método Windows Media Player, interface IWMPControls
- Interface IWMPControls Windows Media Player, próximo método
topic_type:
- apiref
api_name:
- IWMPControls.next
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8444ba7d9209759cb64c4b582e1af9d074332ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768815"
---
# <a name="iwmpcontrolsnext-method"></a><span data-ttu-id="a056f-106">Método IWMPControls:: Next</span><span class="sxs-lookup"><span data-stu-id="a056f-106">IWMPControls::next method</span></span>

<span data-ttu-id="a056f-107">O método **Next** define o próximo item na playlist como o item atual.</span><span class="sxs-lookup"><span data-stu-id="a056f-107">The **next** method sets the next item in the playlist as the current item.</span></span>

## <a name="syntax"></a><span data-ttu-id="a056f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a056f-108">Syntax</span></span>


```CSharp
public void next();
```


```VB

Public Sub next()
Implements IWMPControls.next
```





## <a name="parameters"></a><span data-ttu-id="a056f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a056f-109">Parameters</span></span>

<span data-ttu-id="a056f-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a056f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a056f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a056f-111">Return value</span></span>

<span data-ttu-id="a056f-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a056f-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a056f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a056f-113">Remarks</span></span>

<span data-ttu-id="a056f-114">Se a lista de reprodução estiver na última entrada quando o **próximo** for invocado, a primeira entrada da lista de reprodução se tornará a atual.</span><span class="sxs-lookup"><span data-stu-id="a056f-114">If the playlist is on the last entry when **next** is invoked, the first entry in the playlist will become the current one.</span></span>

<span data-ttu-id="a056f-115">Para listas de reprodução do lado do servidor, esse método pula para o próximo item na lista de reprodução do lado do servidor, não a lista de reprodução do cliente.</span><span class="sxs-lookup"><span data-stu-id="a056f-115">For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.</span></span>

<span data-ttu-id="a056f-116">Ao reproduzir um DVD, esse método pula para o próximo capítulo lógico na sequência de reprodução, que pode não ser o próximo capítulo da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="a056f-116">When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist.</span></span> <span data-ttu-id="a056f-117">Ao reproduzir imagens de DVD ainda, esse método pula para a próxima imagem.</span><span class="sxs-lookup"><span data-stu-id="a056f-117">When playing DVD still images, this method skips to the next image.</span></span>

## <a name="examples"></a><span data-ttu-id="a056f-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a056f-118">Examples</span></span>

<span data-ttu-id="a056f-119">O exemplo a seguir usa **Next** para mover para o próximo item na playlist atual em resposta ao evento Click de um botão.</span><span class="sxs-lookup"><span data-stu-id="a056f-119">The following example uses **next** to move to the next item in the current playlist in response to the Click event of a button.</span></span> <span data-ttu-id="a056f-120">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="a056f-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void nextButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("next"))
    {
        controls.next();
    }
}
```


```VB

Public Sub nextButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles nextButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;next&quot;)) Then

        controls.next()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a056f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a056f-121">Requirements</span></span>



| <span data-ttu-id="a056f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a056f-122">Requirement</span></span> | <span data-ttu-id="a056f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a056f-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a056f-124">Versão</span><span class="sxs-lookup"><span data-stu-id="a056f-124">Version</span></span><br/>   | <span data-ttu-id="a056f-125">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="a056f-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a056f-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="a056f-126">Namespace</span></span><br/> | <span data-ttu-id="a056f-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a056f-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a056f-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="a056f-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a056f-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a056f-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a056f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a056f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a056f-131">**Interface IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a056f-131">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a056f-132">**IWMPControls. Previous (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a056f-132">**IWMPControls.previous (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a056f-133">**IWMPControls. Stop (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a056f-133">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





