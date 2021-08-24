---
title: Método IWMPControls fastReverse
description: O método fastReverse inicia a reprodução rápida do item de mídia na direção inversa.
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- Windows Media Player do método fastReverse
- método fastReverse Windows Media Player, interface IWMPControls
- Windows Media Player de interface IWMPControls, método fastReverse
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bbc1442ca223765b498560d078879c9a7033011117b7f663d4d40ff26bdd93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761076"
---
# <a name="iwmpcontrolsfastreverse-method"></a>Método IWMPControls:: fastReverse

O método **fastReverse** inicia a reprodução rápida do item de mídia na direção inversa.

## <a name="syntax"></a>Sintaxe


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método **fastReverse** examina o clipe de forma inversa em cinco vezes a velocidade normal, exibindo apenas os quadros-chave se for um arquivo de vídeo. Chamar **fastReverse** é equivalente a especificar-5,0 para a taxa, definindo a propriedade **IWMPSettings. Rate** . se a taxa for alterada posteriormente, ou se **IWMPControls. play** ou **IWMPControls. stop** for chamado, Windows Media Player deixará de reverter rapidamente.

Se o item fizer parte de uma lista de reprodução, o **fastReverse** para no início da faixa atual. por exemplo, se track 3 estiver em **fastReverse**, quando o início do track 3 for atingido, Windows Media Player não vai para o track 2. A contagem de execuções não é incrementada ao chamar **fastReverse**.

Se você chamar **IWMPControls. Fastforward** enquanto **fastReverse** estiver em execução, **fastReverse** será interrompido e **IWMPControls. Fastforward** será iniciado.

Esse método não funciona para transmissões ao vivo e certos tipos de mídia digital. Para determinar se você pode usar a inversão rápida em um clipe, passe o valor de **System. String** "fastReverse" para a propriedade **IWMPControls. IsAvailable** (o método **IWMPControls. get \_ IsAvailable** no C#).

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **fastReverse** para reverter o item de mídia atual em resposta ao evento de clique de um botão. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

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

[**Interface IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. fastForward (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls. IsAvailable (VB e C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Stop (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. Rate (VB e C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





