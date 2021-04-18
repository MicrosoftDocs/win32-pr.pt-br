---
title: Método IWMPError clearErrorQueue
description: O método clearErrorQueue limpa os erros da fila de erros. | Método IWMPError clearErrorQueue
ms.assetid: a8e8e666-56e4-4e75-9ed5-2714d272ce7c
keywords:
- método clearErrorQueue Windows Media Player
- método clearErrorQueue Windows Media Player, interface IWMPError
- Interface IWMPError Windows Media Player, método clearErrorQueue
topic_type:
- apiref
api_name:
- IWMPError.clearErrorQueue
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c3f422a9bc32049106d83c970bd8d2c9b2110f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784669"
---
# <a name="iwmperrorclearerrorqueue-method"></a><span data-ttu-id="f0500-107">Método IWMPError:: clearErrorQueue</span><span class="sxs-lookup"><span data-stu-id="f0500-107">IWMPError::clearErrorQueue method</span></span>

<span data-ttu-id="f0500-108">O método **clearErrorQueue** limpa os erros da fila de erros.</span><span class="sxs-lookup"><span data-stu-id="f0500-108">The **clearErrorQueue** method clears the errors from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0500-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0500-109">Syntax</span></span>


```CSharp
public void clearErrorQueue();
```


```VB

Public Sub clearErrorQueue()
Implements IWMPError.clearErrorQueue
```





## <a name="parameters"></a><span data-ttu-id="f0500-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0500-110">Parameters</span></span>

<span data-ttu-id="f0500-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f0500-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0500-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0500-112">Return value</span></span>

<span data-ttu-id="f0500-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f0500-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0500-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0500-114">Remarks</span></span>

<span data-ttu-id="f0500-115">Use esse método para limpar a fila de erros depois que uma série de erros for processada.</span><span class="sxs-lookup"><span data-stu-id="f0500-115">Use this method to clear the error queue after a series of errors has been processed.</span></span>

<span data-ttu-id="f0500-116">Você deve definir **IWMPSettings. enableErrorDialogs** como **false** se optar por exibir mensagens de erro personalizadas.</span><span class="sxs-lookup"><span data-stu-id="f0500-116">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="f0500-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f0500-117">Examples</span></span>

<span data-ttu-id="f0500-118">O exemplo a seguir usa **clearErrorQueue** em um manipulador de eventos de erro para esvaziar a fila de erros após a exibição de todas as descrições de erro.</span><span class="sxs-lookup"><span data-stu-id="f0500-118">The following example uses **clearErrorQueue** in an Error event handler to empty the error queue after all error descriptions have been displayed.</span></span> <span data-ttu-id="f0500-119">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="f0500-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_clearErrorQueue(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Loop through the list of errors.
    for (int i = 0; i < max; i++)
    {
        // Get the description for this error.
        string errDesc = player.Error.get_Item(i).errorDescription;

        // Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc);
    }

    // Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue();
}
```


```VB

Public Sub player_ErrorEvent_clearErrorQueue(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Loop through the list of errors.
    For i As Integer = 0 To (max - 1)

        &#39; Get the description for this error.
        Dim errDesc As String = player.Error.Item(i).errorDescription

        &#39; Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc)

    Next i

    &#39; Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f0500-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0500-120">Requirements</span></span>



| <span data-ttu-id="f0500-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0500-121">Requirement</span></span> | <span data-ttu-id="f0500-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f0500-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0500-123">Versão</span><span class="sxs-lookup"><span data-stu-id="f0500-123">Version</span></span><br/>   | <span data-ttu-id="f0500-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="f0500-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f0500-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0500-125">Namespace</span></span><br/> | <span data-ttu-id="f0500-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f0500-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f0500-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="f0500-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f0500-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f0500-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0500-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0500-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0500-130">**Interface IWMPError (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f0500-130">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f0500-131">**IWMPSettings. enableErrorDialogs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f0500-131">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





