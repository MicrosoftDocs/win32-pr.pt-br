---
title: Propriedade IWMPErrorItem errorDescription
description: A propriedade errorDescription Obtém uma descrição do erro.
ms.assetid: a9914c24-1d10-422a-bcba-80be9fb85108
keywords:
- Propriedade errorDescription Windows Media Player
- Propriedade errorDescription Windows Media Player, interface IWMPErrorItem
- Interface IWMPErrorItem Windows Media Player, Propriedade errorDescription
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8725099d1ce49eae8f378b2571dc4030f60611e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797957"
---
# <a name="iwmperroritemerrordescription-property"></a><span data-ttu-id="111ea-106">Propriedade IWMPErrorItem:: errorDescription</span><span class="sxs-lookup"><span data-stu-id="111ea-106">IWMPErrorItem::errorDescription property</span></span>

<span data-ttu-id="111ea-107">A propriedade **errorDescription** Obtém uma descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="111ea-107">The **errorDescription** property gets a description of the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="111ea-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="111ea-108">Syntax</span></span>


```CSharp
public System.String errorDescription {get; set;}
```


```VB

Public ReadOnly Property errorDescription As System.String
```





## <a name="property-value"></a><span data-ttu-id="111ea-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="111ea-109">Property value</span></span>

<span data-ttu-id="111ea-110">Um **System. String** que é a descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="111ea-110">A **System.String** that is the error description.</span></span>

## <a name="remarks"></a><span data-ttu-id="111ea-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="111ea-111">Remarks</span></span>

<span data-ttu-id="111ea-112">Você deve definir **IWMPSettings. enableErrorDialogs** como **false** se optar por exibir mensagens de erro personalizadas.</span><span class="sxs-lookup"><span data-stu-id="111ea-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="111ea-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="111ea-113">Examples</span></span>

<span data-ttu-id="111ea-114">O exemplo a seguir usa **errorDescription** em um manipulador de eventos de erro para exibir a descrição do erro para o usuário.</span><span class="sxs-lookup"><span data-stu-id="111ea-114">The following example uses **errorDescription** in an Error event handler to display the error description to the user.</span></span> <span data-ttu-id="111ea-115">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="111ea-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorDescription(object sender, System.EventArgs e)
{
    // Get the error description for the first error item.
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show("Error: " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorDescription(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error description for the first error item.
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(&quot;Error: &quot; + errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="111ea-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="111ea-116">Requirements</span></span>



| <span data-ttu-id="111ea-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="111ea-117">Requirement</span></span> | <span data-ttu-id="111ea-118">Valor</span><span class="sxs-lookup"><span data-stu-id="111ea-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="111ea-119">Versão</span><span class="sxs-lookup"><span data-stu-id="111ea-119">Version</span></span><br/>   | <span data-ttu-id="111ea-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="111ea-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="111ea-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="111ea-121">Namespace</span></span><br/> | <span data-ttu-id="111ea-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="111ea-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="111ea-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="111ea-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="111ea-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="111ea-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="111ea-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="111ea-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="111ea-126">**Interface IWMPErrorItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="111ea-126">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="111ea-127">**IWMPSettings. enableErrorDialogs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="111ea-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





