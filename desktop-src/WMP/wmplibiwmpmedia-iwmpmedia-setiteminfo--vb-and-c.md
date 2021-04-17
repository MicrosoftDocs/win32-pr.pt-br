---
title: Método IWMPMedia setItemInfo
description: O método setItemInfo define o valor do atributo especificado para o item de mídia.
ms.assetid: 247bbba5-7d9b-489d-8e41-ae8ec6e266fd
keywords:
- método setItemInfo Windows Media Player
- método setItemInfo Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, método setItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6702c80c13090a370e2922ccecade49bc06645de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811779"
---
# <a name="iwmpmediasetiteminfo-method"></a><span data-ttu-id="ee1ef-106">Método IWMPMedia:: setItemInfo</span><span class="sxs-lookup"><span data-stu-id="ee1ef-106">IWMPMedia::setItemInfo method</span></span>

<span data-ttu-id="ee1ef-107">O método **setItemInfo** define o valor do atributo especificado para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="ee1ef-107">The **setItemInfo** method sets the value of the specified attribute for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee1ef-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee1ef-108">Syntax</span></span>


```CSharp
public void setItemInfo(
  System.String bstrItemName,
  System.String bstrVal
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrItemName As System.String, _
  ByVal bstrVal As System.String _
)
Implements IWMPMedia.setItemInfo
```





## <a name="parameters"></a><span data-ttu-id="ee1ef-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee1ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee1ef-110">*bstrItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee1ef-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee1ef-111">Um **System. String** que é o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="ee1ef-111">A **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="ee1ef-112">*bstrVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee1ef-112">*bstrVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee1ef-113">Um **System. String** que é o novo valor.</span><span class="sxs-lookup"><span data-stu-id="ee1ef-113">A **System.String** that is the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee1ef-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee1ef-114">Return value</span></span>

<span data-ttu-id="ee1ef-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ee1ef-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee1ef-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee1ef-116">Remarks</span></span>

<span data-ttu-id="ee1ef-117">A propriedade **attributeCount** Obtém o número de atributos disponíveis para um determinado item de mídia.</span><span class="sxs-lookup"><span data-stu-id="ee1ef-117">The **attributeCount** property gets the number of attributes available for a given media item.</span></span> <span data-ttu-id="ee1ef-118">Os números de índice podem ser usados com o método **GetAttributeName** para determinar os nomes dos atributos internos que podem ser usados com esse método.</span><span class="sxs-lookup"><span data-stu-id="ee1ef-118">Index numbers can then be used with the **getAttributeName** method to determine the names of the built-in attributes that can be used with this method.</span></span>

<span data-ttu-id="ee1ef-119">Antes de usar esse método, use o método **isReadOnlyItem** para descobrir se um atributo específico pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="ee1ef-119">Before using this method, use the **isReadOnlyItem** method to discover whether a particular attribute can be set.</span></span>

<span data-ttu-id="ee1ef-120">Antes de chamar esse método, você deve ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ee1ef-120">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="ee1ef-121">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ee1ef-121">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="ee1ef-122">Observação</span><span class="sxs-lookup"><span data-stu-id="ee1ef-122">Note</span></span>

<span data-ttu-id="ee1ef-123">Se você inserir o controle do Windows Media Player em seu aplicativo, os atributos de arquivo alterados não serão gravados no arquivo de mídia digital até que o usuário execute o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ee1ef-123">If you embed the Windows Media Player control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span>

## <a name="examples"></a><span data-ttu-id="ee1ef-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ee1ef-124">Examples</span></span>

<span data-ttu-id="ee1ef-125">O exemplo a seguir usa **setItemInfo** para alterar o valor do atributo gênero para o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="ee1ef-125">The following example uses **setItemInfo** to change the value of the Genre attribute for the current media item.</span></span> <span data-ttu-id="ee1ef-126">Uma caixa de texto permite que o usuário insira uma cadeia de caracteres, que é usada para alterar as informações de atributo em resposta ao evento de clique de um botão.</span><span class="sxs-lookup"><span data-stu-id="ee1ef-126">A text box allows the user to enter a string, which is then used to change the attribute information in response to the Click event of a button.</span></span> <span data-ttu-id="ee1ef-127">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="ee1ef-127">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setNewGenre_Click(object sender, System.EventArgs e)
{
    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Get the user input from the TextBox. 
    string atValue = genText.Text;

    // Test for read-only status of the attribute. 
    if( cm.isReadOnlyItem("Genre") == false )
    {
        // Change the attribute value. 
        cm.setItemInfo("Genre", atValue);
    } 
}
```


```VB

Public Sub setNewGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewGenre.Click

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Get the user input from the TextBox. 
    Dim atValue = genText.Text

    &#39; Test for read-only status of the attribute. 
    If (cm.isReadOnlyItem(&quot;Genre&quot;) = False) Then

        &#39; Change the attribute value. 
        cm.setItemInfo(&quot;Genre&quot;, atValue)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="ee1ef-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee1ef-128">Requirements</span></span>



| <span data-ttu-id="ee1ef-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee1ef-129">Requirement</span></span> | <span data-ttu-id="ee1ef-130">Valor</span><span class="sxs-lookup"><span data-stu-id="ee1ef-130">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1ef-131">Versão</span><span class="sxs-lookup"><span data-stu-id="ee1ef-131">Version</span></span><br/>   | <span data-ttu-id="ee1ef-132">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="ee1ef-132">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ee1ef-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee1ef-133">Namespace</span></span><br/> | <span data-ttu-id="ee1ef-134">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ee1ef-134">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ee1ef-135">Assembly</span><span class="sxs-lookup"><span data-stu-id="ee1ef-135">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ee1ef-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ee1ef-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee1ef-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee1ef-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee1ef-138">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ee1ef-138">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ee1ef-139">**IWMPMedia. attributeCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ee1ef-139">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ee1ef-140">**IWMPMedia. GetAttributeName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ee1ef-140">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ee1ef-141">**IWMPMedia. isReadOnlyItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ee1ef-141">**IWMPMedia.isReadOnlyItem (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)
</dt> </dl>

 

 





