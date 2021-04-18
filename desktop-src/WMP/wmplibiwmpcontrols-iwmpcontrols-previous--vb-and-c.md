---
title: IWMPControls método anterior
description: O método anterior define o item anterior na playlist como o item atual.
ms.assetid: 380524f5-e8b6-45c4-9f6c-3dbb49b1ac9f
keywords:
- método anterior Windows Media Player
- método anterior Windows Media Player, interface IWMPControls
- Interface IWMPControls do Windows Media Player, método anterior
topic_type:
- apiref
api_name:
- IWMPControls.previous
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823038205a026afb7141491f562698eb60515a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789429"
---
# <a name="iwmpcontrolsprevious-method"></a><span data-ttu-id="7bd97-106">IWMPControls: método rior de:p</span><span class="sxs-lookup"><span data-stu-id="7bd97-106">IWMPControls::previous method</span></span>

<span data-ttu-id="7bd97-107">O método **anterior** define o item anterior na playlist como o item atual.</span><span class="sxs-lookup"><span data-stu-id="7bd97-107">The **previous** method sets the previous item in the playlist as the current item.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bd97-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7bd97-108">Syntax</span></span>


```CSharp
public void previous();
```


```VB

Public Sub previous()
Implements IWMPControls.previous
```





## <a name="parameters"></a><span data-ttu-id="7bd97-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bd97-109">Parameters</span></span>

<span data-ttu-id="7bd97-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7bd97-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7bd97-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7bd97-111">Return value</span></span>

<span data-ttu-id="7bd97-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7bd97-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bd97-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bd97-113">Remarks</span></span>

<span data-ttu-id="7bd97-114">Se a lista de reprodução estiver na primeira entrada quando a **anterior** for invocada, a última entrada na lista de reprodução se tornará a atual.</span><span class="sxs-lookup"><span data-stu-id="7bd97-114">If the playlist is on the first entry when **previous** is invoked, the last entry in the playlist will become the current one.</span></span>

## <a name="examples"></a><span data-ttu-id="7bd97-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7bd97-115">Examples</span></span>

<span data-ttu-id="7bd97-116">O exemplo a seguir usa **Previous** para mover para o item anterior na playlist atual em resposta ao evento Click de um botão.</span><span class="sxs-lookup"><span data-stu-id="7bd97-116">The following example uses **previous** to move to the previous item in the current playlist in response to the Click event of a button.</span></span> <span data-ttu-id="7bd97-117">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="7bd97-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void previousButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("previous"))
    {
        controls.previous();
    }
}
```


```VB

Public Sub previousButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles previousButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;previous&quot;)) Then

        controls.previous()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="7bd97-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bd97-118">Requirements</span></span>



| <span data-ttu-id="7bd97-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bd97-119">Requirement</span></span> | <span data-ttu-id="7bd97-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7bd97-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bd97-121">Versão</span><span class="sxs-lookup"><span data-stu-id="7bd97-121">Version</span></span><br/>   | <span data-ttu-id="7bd97-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="7bd97-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7bd97-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7bd97-123">Namespace</span></span><br/> | <span data-ttu-id="7bd97-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7bd97-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7bd97-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="7bd97-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7bd97-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7bd97-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bd97-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bd97-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bd97-128">**Interface IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7bd97-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7bd97-129">**IWMPControls. Next (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7bd97-129">**IWMPControls.next (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7bd97-130">**IWMPControls. Stop (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7bd97-130">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





