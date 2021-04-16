---
title: Método Next IWMPControls
description: O método Next define o próximo item na playlist como o item atual.
ms.assetid: 3f82ef25-a1e0-4845-b0ed-dd6463719577
keywords:
- próximo método Windows Media Player
- próximo método Windows Media Player, interface IWMPControls
- Interface IWMPControls Windows Media Player, próximo método
topic_type:
- apiref
api_name:
- IWMPControls.next
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8444ba7d9209759cb64c4b582e1af9d074332ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768815"
---
# <a name="iwmpcontrolsnext-method"></a>Método IWMPControls:: Next

O método **Next** define o próximo item na playlist como o item atual.

## <a name="syntax"></a>Sintaxe


```CSharp
public void next();
```


```VB

Public Sub next()
Implements IWMPControls.next
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a lista de reprodução estiver na última entrada quando o **próximo** for invocado, a primeira entrada da lista de reprodução se tornará a atual.

Para listas de reprodução do lado do servidor, esse método pula para o próximo item na lista de reprodução do lado do servidor, não a lista de reprodução do cliente.

Ao reproduzir um DVD, esse método pula para o próximo capítulo lógico na sequência de reprodução, que pode não ser o próximo capítulo da lista de reprodução. Ao reproduzir imagens de DVD ainda, esse método pula para a próxima imagem.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **Next** para mover para o próximo item na playlist atual em resposta ao evento Click de um botão. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
private void nextButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("next"))
    {
        controls.next();
    }
}
```


```VB

Public Sub nextButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles nextButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;next&quot;)) Then

        controls.next()

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

[**IWMPControls. Previous (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Stop (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





