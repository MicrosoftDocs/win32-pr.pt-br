---
title: Propriedade de taxa IWMPSettings
description: A propriedade rate obtém ou define a taxa de reprodução atual para vídeo.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- rate property Windows Media Player
- rate property Windows Media Player interface , IWMPSettings
- Interface IWMPSettings Windows Media Player , propriedade rate
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
ms.openlocfilehash: cc053861b9061df676455e10b011cd0ffe0fe9f06052b129ec163e00d4c8d71f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999696"
---
# <a name="iwmpsettingsrate-property"></a>Propriedade IWMPSettings::rate

A **propriedade rate** obtém ou define a taxa de reprodução atual para vídeo.

## <a name="syntax"></a>Syntax


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a>Valor da propriedade

Um **System.Double** que é a taxa de reprodução, com um valor padrão de 1,0.

## <a name="remarks"></a>Comentários

O valor recuperado por essa propriedade atua como um valor multiplicador que permite reproduzir um item de mídia a uma taxa mais rápida ou mais lenta. O valor padrão de 1,0 indica a velocidade de autor.

Observe que uma faixa de áudio torna-se difícil de entender em taxas inferiores a 0,5 ou superiores a 1,5. Uma taxa de reprodução de 2 indica duas vezes a velocidade de reprodução normal.

Windows Media Player tentar usar o mais eficaz dos quatro modos de reprodução diferentes a seguir

-   Reprodução suave de vídeo com tom de áudio mantido
-   Reprodução suave de vídeo com tom de áudio não mantido
-   Reprodução de vídeo suave sem áudio
-   Reprodução de vídeo de keyframe sem áudio

O modo escolhido por Windows Media Player depende de vários fatores, incluindo tipo de arquivo e local, sistema operacional, rede e servidor.

Outras considerações também se aplicam, dependendo do formato de mídia digital usado para criar o conteúdo:

-   **Windows Vídeo de mídia (WMV) e ASF.** Os valores ideais **para a propriedade** de taxa são de 1 a 10 ou de 1 a 10 para reprodução inversa. Os valores de 0,5 a 1,0 ou de -0,5 a -1.0 também podem funcionar bem em casos em que o tom de áudio pode ser mantido, como ao tocar arquivos localizados no computador local. Valores com uma magnitude absoluta maior que 10 são permitidos, mas não são muito significativos.
-   **Outros formatos de vídeo.** A **propriedade** rate pode variar de 0 a 9. Valores negativos não são permitidos. Valores menores que 1 representam movimento lento. Valores acima de 9 são permitidos, mas não são muito significativos.

O **método IWMPControls.fastForward** altera  o valor da taxa para 5,0, enquanto o **método IWMPControls.fastReverse** altera o valor da taxa para 5,0. 

A taxa de reprodução de alguns formatos de mídia digital não pode ser alterada. Use a propriedade **IWMPSettings.isAvailable** (em C# o método **IWMPSettings.get \_ isAvailable)** para descobrir se essa propriedade pode ser especificada para um item de mídia específico.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa um controle de updown numérico que permite que o usuário altere a velocidade de reprodução da mídia atual. Quando o usuário clica nas setas para cima ou para baixo do controle, a propriedade **rate** é definida como o novo valor. O intervalo possível de valores no controle é de 0,5 (meia velocidade) a 2,0 (velocidade dupla). O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


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
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMPControls.fastForward (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls.fastReverse (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.isAvailable (VB e C#)**](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.mute (VB e C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





