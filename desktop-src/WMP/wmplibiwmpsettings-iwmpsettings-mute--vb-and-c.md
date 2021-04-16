---
title: Propriedade IWMPSettings mudo
description: A propriedade MUTE Obtém ou define um valor que indica se o áudio está mudo.
ms.assetid: d99e47db-70cc-41e0-aca9-b765b075e7b4
keywords:
- Propriedade sem áudio Windows Media Player
- Propriedade sem áudio Windows Media Player, interface IWMPSettings
- Interface IWMPSettings Windows Media Player, Propriedade mudo
topic_type:
- apiref
api_name:
- IWMPSettings.mute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67518bb9a6eccee13e4cc262f37341d30689439e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765030"
---
# <a name="iwmpsettingsmute-property"></a><span data-ttu-id="3dbd4-106">Propriedade IWMPSettings:: MUTE</span><span class="sxs-lookup"><span data-stu-id="3dbd4-106">IWMPSettings::mute property</span></span>

<span data-ttu-id="3dbd4-107">A propriedade **MUTE** Obtém ou define um valor que indica se o áudio está mudo.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-107">The **mute** property gets or sets a value indicating whether audio is muted.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dbd4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3dbd4-108">Syntax</span></span>


```CSharp
public System.Boolean mute {get; set;}
```


```VB

Public Property mute As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="3dbd4-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3dbd4-109">Property value</span></span>

<span data-ttu-id="3dbd4-110">Um valor **System. booliano** que indica se o áudio está mudo.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-110">A **System.Boolean** value indicating whether audio is muted.</span></span> <span data-ttu-id="3dbd4-111">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-111">The default is **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="3dbd4-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3dbd4-112">Examples</span></span>

<span data-ttu-id="3dbd4-113">O exemplo a seguir cria uma caixa de seleção e alterna a propriedade **mudo** para áudio sem áudio quando o estado de ativação da caixa é alterado.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-113">The following example creates a check box, and toggles the **mute** property to mute and un-mute audio when the checked state of the box is changed.</span></span> <span data-ttu-id="3dbd4-114">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-114">**AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void Mute_CheckStateChanged(object sender, System.EventArgs e)
{
    System.Windows.Forms.CheckBox Mute = (System.Windows.Forms.CheckBox)sender;

    // Change the check box text depending on the checked state.
    Mute.Text = Mute.Checked ? "Un-mute Audio" : Mute.Text = "Mute Audio";

    // Use the checked state to set the mute property. 
    player.settings.mute = Mute.Checked;
}
```


```VB

Public Sub Mute_CheckStateChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles Mute.CheckStateChanged

    Dim cb As System.Windows.Forms.CheckBox = sender

    &#39;  Change the check box text depending on the checked state.
    If (cb.Checked) Then

        cb.Text = &quot;Un-mute Audio&quot;

    Else

        cb.Text = &quot;Mute Audio&quot;

    End If

    &#39;  Use the checked state to set the mute property. 
    player.settings.mute = cb.Checked

End Sub
```





## <a name="requirements"></a><span data-ttu-id="3dbd4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dbd4-115">Requirements</span></span>



| <span data-ttu-id="3dbd4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dbd4-116">Requirement</span></span> | <span data-ttu-id="3dbd4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3dbd4-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dbd4-118">Versão</span><span class="sxs-lookup"><span data-stu-id="3dbd4-118">Version</span></span><br/>   | <span data-ttu-id="3dbd4-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="3dbd4-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3dbd4-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="3dbd4-120">Namespace</span></span><br/> | <span data-ttu-id="3dbd4-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3dbd4-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3dbd4-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="3dbd4-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3dbd4-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3dbd4-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dbd4-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dbd4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dbd4-125">**Interface IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3dbd4-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3dbd4-126">**IWMPSettings. Rate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3dbd4-126">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





