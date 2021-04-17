---
title: Propriedade errorCode IWMPErrorItem
description: A propriedade errorCode Obtém o código de erro atual.
ms.assetid: 00719067-685d-4ef2-9eec-72c7892fcdb9
keywords:
- Propriedade errorCode Windows Media Player
- Propriedade errorCode Windows Media Player, interface IWMPErrorItem
- Interface IWMPErrorItem Windows Media Player, Propriedade errorCode
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorCode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f284d5655fc1f4007695a1f681c744a9c5c6fc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812156"
---
# <a name="iwmperroritemerrorcode-property"></a><span data-ttu-id="72b8e-106">Propriedade IWMPErrorItem:: errorCode</span><span class="sxs-lookup"><span data-stu-id="72b8e-106">IWMPErrorItem::errorCode property</span></span>

<span data-ttu-id="72b8e-107">A propriedade **ErrorCode** Obtém o código de erro atual.</span><span class="sxs-lookup"><span data-stu-id="72b8e-107">The **errorCode** property gets the current error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b8e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="72b8e-108">Syntax</span></span>


```CSharp
public System.Int32 errorCode {get; set;}
```


```VB

Public ReadOnly Property errorCode As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="72b8e-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="72b8e-109">Property value</span></span>

<span data-ttu-id="72b8e-110">Um **System. Int32** que é o código de erro.</span><span class="sxs-lookup"><span data-stu-id="72b8e-110">A **System.Int32** that is the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="72b8e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="72b8e-111">Remarks</span></span>

<span data-ttu-id="72b8e-112">Você deve definir **IWMPSettings. enableErrorDialogs** como **false** se optar por exibir mensagens de erro personalizadas.</span><span class="sxs-lookup"><span data-stu-id="72b8e-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="72b8e-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="72b8e-113">Examples</span></span>

<span data-ttu-id="72b8e-114">O exemplo a seguir usa **ErrorCode** em um manipulador de eventos de erro para exibir o código de erro para o usuário.</span><span class="sxs-lookup"><span data-stu-id="72b8e-114">The following example uses **errorCode** in an Error event handler to display the error code to the user.</span></span> <span data-ttu-id="72b8e-115">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="72b8e-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorCode(object sender, System.EventArgs e)
{
    // Get the error code for the first error item.
    int errCode = player.Error.get_Item(0).errorCode;

    // Display the error code.
    System.Windows.Forms.MessageBox.Show("Error number: " + errCode.ToString());
}
```


```VB

Public Sub player_ErrorEvent_errorCode(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error code for the first error item.
    Dim errCode As Integer = player.Error.Item(0).errorCode

    &#39; Display the error code.
    System.Windows.Forms.MessageBox.Show(&quot;Error number: &quot; + errCode.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="72b8e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72b8e-116">Requirements</span></span>



| <span data-ttu-id="72b8e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="72b8e-117">Requirement</span></span> | <span data-ttu-id="72b8e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="72b8e-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72b8e-119">Versão</span><span class="sxs-lookup"><span data-stu-id="72b8e-119">Version</span></span><br/>   | <span data-ttu-id="72b8e-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="72b8e-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="72b8e-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="72b8e-121">Namespace</span></span><br/> | <span data-ttu-id="72b8e-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="72b8e-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="72b8e-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="72b8e-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="72b8e-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="72b8e-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72b8e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="72b8e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b8e-126">**Interface IWMPErrorItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="72b8e-126">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="72b8e-127">**IWMPSettings. enableErrorDialogs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="72b8e-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





