---
title: IWMPError. Item (VB e C)
description: A Propriedade Item (o \_ método get item em C \) Obtém uma interface IWMPErrorItem no índice especificado na fila de erros.
ms.assetid: acfaaaa5-eb13-4ba0-8417-4229adc62c5d
keywords:
- IWMPError. Item (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPError.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9217ec772512171c828dd0dad06ec8fe3704dba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789537"
---
# <a name="iwmperroritem-vb-and-c"></a><span data-ttu-id="d5a26-104">IWMPError. Item (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="d5a26-104">IWMPError.Item (VB and C#)</span></span>

<span data-ttu-id="d5a26-105">A propriedade **Item** (o método **Get \_ Item** em C#) Obtém uma interface **IWMPErrorItem** no índice especificado na fila de erros.</span><span class="sxs-lookup"><span data-stu-id="d5a26-105">The **Item** property (the **get\_Item** method in C#) gets an **IWMPErrorItem** interface at the specified index in the error queue.</span></span>


```
[Visual Basic]
ReadOnly Property Item(
  dwIndex As System.Integer
) As IWMPErrorItem
```




```
[C#]
IWMPErrorItem get_Item (
  System.Int32 dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="d5a26-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5a26-106">Parameters</span></span>

<span data-ttu-id="d5a26-107">*dwIndex*</span><span class="sxs-lookup"><span data-stu-id="d5a26-107">*dwIndex*</span></span>

<span data-ttu-id="d5a26-108">Um **System. Int32** que é o índice de base zero de uma interface **IWMPErrorItem** na fila de erros.</span><span class="sxs-lookup"><span data-stu-id="d5a26-108">A **System.Int32** that is the zero-based index of an **IWMPErrorItem** interface in the error queue.</span></span>

## <a name="property-value"></a><span data-ttu-id="d5a26-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d5a26-109">Property Value</span></span>

<span data-ttu-id="d5a26-110">Uma interface **WMPLib. IWMPErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="d5a26-110">A **WMPLib.IWMPErrorItem** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5a26-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5a26-111">Remarks</span></span>

<span data-ttu-id="d5a26-112">O Windows Media Player pode gerar vários erros em resposta a uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="d5a26-112">Windows Media Player can generate a number of errors in response to an error condition.</span></span> <span data-ttu-id="d5a26-113">Essa propriedade Obtém um erro específico na fila usando um número de índice.</span><span class="sxs-lookup"><span data-stu-id="d5a26-113">This property gets a specific error in the queue by using an index number.</span></span> <span data-ttu-id="d5a26-114">Os números de índice para a fila de erros começam com zero.</span><span class="sxs-lookup"><span data-stu-id="d5a26-114">The index numbers for the error queue begin with zero.</span></span>

<span data-ttu-id="d5a26-115">Você deve definir **IWMPSettings. enableErrorDialogs** como **false** se optar por exibir mensagens de erro personalizadas.</span><span class="sxs-lookup"><span data-stu-id="d5a26-115">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="d5a26-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d5a26-116">Examples</span></span>

<span data-ttu-id="d5a26-117">O exemplo a seguir usa a propriedade **Item** (o método **Get \_ Item** em C#) em um manipulador de eventos de erro para recuperar e exibir informações sobre o erro mais recente na fila de erros.</span><span class="sxs-lookup"><span data-stu-id="d5a26-117">The following example uses the **Item** property (the **get\_Item** method in C#) in an Error event handler to retrieve and display information about the most recent error in the error queue.</span></span> <span data-ttu-id="d5a26-118">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="d5a26-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_get_Item(object sender, System.EventArgs e)
{
    // Store the index of the most recent error.
    int max = (player.Error.errorCount - 1);

    // Get an interface for the most recent error item. Cast it to
    // a WMPLib.IWMPErrorItem2 interface to get all of the available functionality.
    WMPLib.IWMPErrorItem2 errItem = (WMPLib.IWMPErrorItem2)player.Error.get_Item(max);

    // Use the interface to access and store the error info.
    int errNum = errItem.errorCode;
    string errDesc = errItem.errorDescription;

    // Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + ":  " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_get_Item(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the index of the most recent error.
    Dim max As Integer = (player.Error.errorCount - 1)

    &#39; Get an interface for the most recent error item. 
    Dim errItem As WMPLib.IWMPErrorItem2 = player.Error.Item(max)

    &#39; Use the interface to access and store the error info.
    Dim errNum As Integer = errItem.errorCode
    Dim errDesc As String = errItem.errorDescription

    &#39; Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + &quot;:  &quot; + errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="d5a26-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5a26-119">Requirements</span></span>



| <span data-ttu-id="d5a26-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5a26-120">Requirement</span></span> | <span data-ttu-id="d5a26-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d5a26-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a26-122">Versão</span><span class="sxs-lookup"><span data-stu-id="d5a26-122">Version</span></span><br/>   | <span data-ttu-id="d5a26-123">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="d5a26-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d5a26-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5a26-124">Namespace</span></span><br/> | <span data-ttu-id="d5a26-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d5a26-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d5a26-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="d5a26-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d5a26-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d5a26-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5a26-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5a26-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5a26-129">**Interface IWMPError (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d5a26-129">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d5a26-130">**Interface IWMPErrorItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d5a26-130">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d5a26-131">**IWMPSettings. enableErrorDialogs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d5a26-131">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





