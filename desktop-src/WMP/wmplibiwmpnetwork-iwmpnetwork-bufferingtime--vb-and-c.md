---
title: Propriedade IWMPNetwork bufferingTime
description: A propriedade bufferingTime Obtém ou define a quantidade de tempo, em milissegundos, alocada para armazenar em buffer os dados de entrada antes do início da reprodução.
ms.assetid: b5936b21-a17b-4801-a5fc-c6d6521e05aa
keywords:
- Propriedade bufferingTime Windows Media Player
- Propriedade bufferingTime Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade bufferingTime
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8594d53797b028dd74a8ef11cb8f2fa64b3654cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761024"
---
# <a name="iwmpnetworkbufferingtime-property"></a><span data-ttu-id="0c1e0-106">Propriedade IWMPNetwork:: bufferingTime</span><span class="sxs-lookup"><span data-stu-id="0c1e0-106">IWMPNetwork::bufferingTime property</span></span>

<span data-ttu-id="0c1e0-107">A propriedade **bufferingTime** Obtém ou define a quantidade de tempo, em milissegundos, alocada para armazenar em buffer os dados de entrada antes do início da reprodução.</span><span class="sxs-lookup"><span data-stu-id="0c1e0-107">The **bufferingTime** property gets or sets the amount of time in milliseconds allocated for buffering incoming data before playback begins.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c1e0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c1e0-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingTime {get; set;}
```


```VB

Public Property bufferingTime As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="0c1e0-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0c1e0-109">Property value</span></span>

<span data-ttu-id="0c1e0-110">Um **System. Int32** que é o tempo de buffer em milissegundos, que varia de zero a 60.000 com um valor padrão de 5.000.</span><span class="sxs-lookup"><span data-stu-id="0c1e0-110">A **System.Int32** that is the buffering time in milliseconds, which ranges from zero to 60,000 with a default value of 5,000.</span></span>

## <a name="examples"></a><span data-ttu-id="0c1e0-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0c1e0-111">Examples</span></span>

<span data-ttu-id="0c1e0-112">O exemplo de código a seguir usa **bufferingTime** para especificar o número de segundos alocados para armazenar em buffer os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="0c1e0-112">The following code example uses **bufferingTime** to specify the number of seconds allocated for buffering incoming data.</span></span> <span data-ttu-id="0c1e0-113">Uma caixa de texto permite que o usuário insira um novo valor para **bufferingTime** e a propriedade seja atualizada em resposta ao evento de clique de um botão.</span><span class="sxs-lookup"><span data-stu-id="0c1e0-113">A text box allows the user to enter a new value for **bufferingTime**, and the property is updated in response to the Click event of a button.</span></span> <span data-ttu-id="0c1e0-114">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="0c1e0-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setBufTime_Click(object sender, System.EventArgs e)
{
    // Retrieve input from the user and convert it to an integer.
    int newTime = System.Convert.ToInt32(bufText.Text);

    // Test whether the integer is within the valid range. 
    if (newTime >= 0 & newTime <= 60) 
    {
        // Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000);
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("Buffering time must be between 0 and 60.");
    }
}
```


```VB

Public Sub setBufTime_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setBufTime.Click

    &#39; Retrieve input from the user and convert it to an integer.
    Dim newTime As Integer = System.Convert.ToInt32(bufText.Text)

    &#39; Test whether the integer is within the valid range. 
    If (newTime >= 0 And newTime <= 60) Then

        &#39; Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000)

    Else

        System.Windows.Forms.MessageBox.Show(&quot;Buffering time must be between 0 and 60.&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="0c1e0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c1e0-115">Requirements</span></span>



| <span data-ttu-id="0c1e0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c1e0-116">Requirement</span></span> | <span data-ttu-id="0c1e0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0c1e0-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c1e0-118">Versão</span><span class="sxs-lookup"><span data-stu-id="0c1e0-118">Version</span></span><br/>   | <span data-ttu-id="0c1e0-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="0c1e0-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0c1e0-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c1e0-120">Namespace</span></span><br/> | <span data-ttu-id="0c1e0-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0c1e0-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0c1e0-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="0c1e0-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0c1e0-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0c1e0-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c1e0-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c1e0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c1e0-125">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0c1e0-125">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





