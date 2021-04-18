---
title: Propriedade de taxa de IWMPSettings
description: A propriedade Rate Obtém ou define a taxa de reprodução atual para vídeo.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- Propriedade de taxa Windows Media Player
- Propriedade de taxa Windows Media Player, interface IWMPSettings
- Interface IWMPSettings Windows Media Player, Propriedade Rate
topic_type:
- apiref
api_name:
- IWMPSettings.rate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f502bebdbd22523858637f8abccbe203db104cbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785219"
---
# <a name="iwmpsettingsrate-property"></a>Propriedade IWMPSettings:: Rate

A propriedade **Rate** Obtém ou define a taxa de reprodução atual para vídeo.

## <a name="syntax"></a>Syntax


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a>Valor da propriedade

Um **sistema. Double** que é a taxa de reprodução, com um valor padrão de 1,0.

## <a name="remarks"></a>Comentários

O valor recuperado por essa propriedade atua como um valor de multiplicador que permite reproduzir um item de mídia em uma taxa mais rápida ou mais lenta. O valor padrão de 1,0 indica a velocidade de criação.

Observe que uma faixa de áudio torna-se difícil de entender em taxas menores que 0,5 ou superiores a 1,5. Uma taxa de reprodução de 2 indica duas vezes a velocidade de reprodução normal.

O Windows Media Player tentará usar o mais efetivo dos quatro modos de reprodução diferentes a seguir

-   Reprodução de vídeo suave com densidade de áudio mantida
-   Reprodução de vídeo suave com densidade de áudio não mantida
-   Uma reprodução de vídeo suave sem áudio
-   Reprodução de vídeo com quadro-chave sem áudio

O modo escolhido pelo Windows Media Player depende de vários fatores, incluindo tipo de arquivo e local, sistema operacional, rede e servidor.

Outras considerações também se aplicam, dependendo do formato de mídia digital usado para criar o conteúdo:

-   **Windows Media Video (WMV) e ASF.** Os valores ideais para a propriedade **Rate** são de 1 a 10, ou de 1 a 10 para a reprodução reversa. Os valores de 0,5 a 1,0 ou de-0,5 a-1,0 também podem funcionar bem em casos em que a densidade de áudio pode ser mantida, como ao reproduzir arquivos localizados no computador local. Valores com uma magnitude absoluta maior que 10 são permitidos, mas não são muito significativos.
-   **Outros formatos de vídeo.** A propriedade **Rate** pode variar de 0 a 9. Valores negativos não são permitidos. Valores menores que 1 representam movimento lento. Os valores acima de 9 são permitidos, mas não são muito significativos.

O método **IWMPControls. Fastforward** altera o valor de **Rate** para 5,0, enquanto o método **IWMPControls. fastReverse** altera o valor de **Rate** para 5,0.

A taxa de reprodução de alguns formatos de mídia digital não pode ser alterada. Use a propriedade **IWMPSettings. IsAvailable** (em C#, o método **IWMPSettings. get \_ IsAvailable** ) para descobrir se essa propriedade pode ser especificada para um item de mídia específico.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa um controle intermediário numérico que permite ao usuário alterar a velocidade de reprodução da mídia atual. Quando o usuário clica nas setas para cima ou para baixo do controle, a propriedade **taxa** é definida com o novo valor. O intervalo de valores possível no controle é de 0,5 (meia velocidade) a 2,0 (velocidade dupla). O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
private void playbackRate_Click(object sender, System.EventArgs e)
{
    // Get the new value of the control, and cast it from decimal to double.
    double newRate = (double)((System.Windows.Forms.NumericUpDown)sender).Value;

    // Test whether playback rate can be set. 
    if( player.settings.get_isAvailable("Rate") )
    {
        // Set the playback rate to the new value.
        player.settings.rate = newRate;
    }
}
```


```VB

Public Sub playbackRate_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playbackRate.Click

    &#39;  Get the new value of the control as a double.
    Dim nUpDown As System.Windows.Forms.NumericUpDown = sender
    Dim newRate As Double = nUpDown.Value

    &#39;  Test whether playback rate can be set. 
    If (player.settings.isAvailable(&quot;Rate&quot;)) Then

        &#39;  Set the playback rate to the new value.
        player.settings.rate = newRate

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

[**IWMPControls. fastForward (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls. fastReverse (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. IsAvailable (VB e C#)**](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. mudo (VB e C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





