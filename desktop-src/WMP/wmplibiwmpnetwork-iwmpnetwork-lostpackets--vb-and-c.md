---
title: Propriedade IWMPNetwork lostPackets
description: A propriedade lostPackets Obtém o número de pacotes perdidos.
ms.assetid: 611218d3-c4d3-4d4e-835c-1e7a956b2718
keywords:
- Windows Media Player da propriedade lostPackets
- propriedade lostPackets Windows Media Player, interface IWMPNetwork
- Windows Media Player de interface IWMPNetwork, propriedade lostPackets
topic_type:
- apiref
api_name:
- IWMPNetwork.lostPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a60c85920d647f99ed8ba8478da51183c3ba63efa733c0bc627c16b040b70965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745907"
---
# <a name="iwmpnetworklostpackets-property"></a>Propriedade IWMPNetwork:: lostPackets

A propriedade **lostPackets** Obtém o número de pacotes perdidos.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 lostPackets {get; set;}
```


```VB

Public ReadOnly Property lostPackets As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o número de pacotes perdidos.

## <a name="remarks"></a>Comentários

Essa propriedade inclui somente pacotes de mídia de streaming e retornará zero ao usar o protocolo HTTP, que é sem perdas.

Os pacotes podem ser perdidos por vários motivos, como o tipo e a qualidade da conexão de rede.

Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é redefinida como zero. O valor não será redefinido se a reprodução for pausada. Essa propriedade obtém informações válidas somente durante o tempo de execução quando a URL para reprodução é definida usando a propriedade **AxWindowsMediaPlayer. URL** .

## <a name="examples"></a>Exemplos

O exemplo de código a seguir usa **lostPackets** para exibir o número total de pacotes perdidos durante a reprodução. As informações são exibidas em um rótulo quando o usuário clica em um botão. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
private void showLostPackets_Click(object sender, System.EventArgs e)
{
    lostPacketsLabel.Text = ("Packets lost: " + player.network.lostPackets.ToString());
}
```


```VB

Public Sub showLostPackets_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showLostPackets.Click

    lostPacketsLabel.Text = (&quot;Packets lost: &quot; + player.network.lostPackets.ToString())

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
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> </dl>

 

 





