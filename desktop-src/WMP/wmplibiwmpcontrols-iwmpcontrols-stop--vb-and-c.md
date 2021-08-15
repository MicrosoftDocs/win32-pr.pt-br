---
title: Método IWMPControls Stop
description: O método Stop interrompe a reprodução do item de mídia. | Método IWMPControls Stop
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- Windows Media Player do método Stop
- método stop Windows Media Player, interface IWMPControls
- Windows Media Player de interface IWMPControls, método stop
topic_type:
- apiref
api_name:
- IWMPControls.stop
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f941ac90fa86cdd16dedf5349c0a6d614c57f49bc91009f5d62c56bb83144bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332070"
---
# <a name="iwmpcontrolsstop-method"></a>Método IWMPControls:: Stop

O método **Stop** interrompe a reprodução do item de mídia.

## <a name="syntax"></a>Sintaxe


```CSharp
public void stop();
```


```VB

Public Sub stop()
Implements IWMPControls.stop
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

esse método faz Windows Media Player liberar os recursos do sistema que está usando, como o dispositivo de áudio. O item de mídia atual, no entanto, não é liberado.

quando Windows Media Player é interrompido, a posição de reprodução atual no item de mídia é redefinida para o início do item. Posteriormente, chamar **IWMPControls. Play** iniciará a reprodução desde o início do item de mídia. Para interromper uma operação de reprodução sem alterar a posição atual, use o método **IWMPControls. Pause** .

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **Stop** para interromper o item de mídia atual em resposta ao evento Click de um botão. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
private void stopButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("stop"))
    {
        controls.stop();
    }
}
```


```VB

Public Sub stopButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles stopButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;stop&quot;)) Then

        controls.stop()

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

[**IWMPControls. Next (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[**IWMPControls. PAUSE (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Previous (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





