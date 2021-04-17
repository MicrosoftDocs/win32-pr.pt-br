---
title: Propriedade IWMPError errorCount
description: A propriedade errorCount Obtém o número de erros na fila de erros.
ms.assetid: a30750c8-2025-4087-bd2b-f313ccbde38c
keywords:
- Propriedade errorCount Windows Media Player
- Propriedade errorCount Windows Media Player, interface IWMPError
- Interface IWMPError Windows Media Player, Propriedade errorCount
topic_type:
- apiref
api_name:
- IWMPError.errorCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62c16f07260847c91f1c9f18885587444a4ceb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762422"
---
# <a name="iwmperrorerrorcount-property"></a><span data-ttu-id="56c80-106">Propriedade IWMPError:: errorCount</span><span class="sxs-lookup"><span data-stu-id="56c80-106">IWMPError::errorCount property</span></span>

<span data-ttu-id="56c80-107">A propriedade **errorCount** Obtém o número de erros na fila de erros.</span><span class="sxs-lookup"><span data-stu-id="56c80-107">The **errorCount** property gets the number of errors in the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="56c80-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="56c80-108">Syntax</span></span>


```CSharp
public System.Int32 errorCount {get; set;}
```


```VB

Public ReadOnly Property errorCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="56c80-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="56c80-109">Property value</span></span>

<span data-ttu-id="56c80-110">Um **System. Int32** que é o número de erros.</span><span class="sxs-lookup"><span data-stu-id="56c80-110">A **System.Int32** that is the number of errors.</span></span>

## <a name="remarks"></a><span data-ttu-id="56c80-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="56c80-111">Remarks</span></span>

<span data-ttu-id="56c80-112">Você deve definir **IWMPSettings. enableErrorDialogs** como **false** se optar por exibir mensagens de erro personalizadas.</span><span class="sxs-lookup"><span data-stu-id="56c80-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="56c80-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="56c80-113">Examples</span></span>

<span data-ttu-id="56c80-114">O exemplo a seguir usa **errorCount** em um manipulador de eventos de erro para alertar o usuário sobre o erro mais recente na fila de erros.</span><span class="sxs-lookup"><span data-stu-id="56c80-114">The following example uses **errorCount** in an Error event handler to alert the user about the most recent error in the error queue.</span></span> <span data-ttu-id="56c80-115">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="56c80-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorCount(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Get the description of the last error. Error items start at zero,
    // so the item index will always be one less than the error count.
    string errDesc = player.Error.get_Item(max-1).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorCount(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Get the description of the last error. Error items start at zero,
    &#39; so the item index will always be one less than the error count.
    Dim errDesc As String = player.Error.Item(max - 1).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="56c80-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56c80-116">Requirements</span></span>



| <span data-ttu-id="56c80-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="56c80-117">Requirement</span></span> | <span data-ttu-id="56c80-118">Valor</span><span class="sxs-lookup"><span data-stu-id="56c80-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56c80-119">Versão</span><span class="sxs-lookup"><span data-stu-id="56c80-119">Version</span></span><br/>   | <span data-ttu-id="56c80-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="56c80-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="56c80-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="56c80-121">Namespace</span></span><br/> | <span data-ttu-id="56c80-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="56c80-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="56c80-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="56c80-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="56c80-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="56c80-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56c80-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="56c80-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56c80-126">**Interface IWMPError (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="56c80-126">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="56c80-127">**IWMPSettings. enableErrorDialogs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="56c80-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





