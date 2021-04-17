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
# <a name="iwmpnetworkbufferingtime-property"></a>Propriedade IWMPNetwork:: bufferingTime

A propriedade **bufferingTime** Obtém ou define a quantidade de tempo, em milissegundos, alocada para armazenar em buffer os dados de entrada antes do início da reprodução.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 bufferingTime {get; set;}
```


```VB

Public Property bufferingTime As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o tempo de buffer em milissegundos, que varia de zero a 60.000 com um valor padrão de 5.000.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir usa **bufferingTime** para especificar o número de segundos alocados para armazenar em buffer os dados de entrada. Uma caixa de texto permite que o usuário insira um novo valor para **bufferingTime** e a propriedade seja atualizada em resposta ao evento de clique de um botão. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


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





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





