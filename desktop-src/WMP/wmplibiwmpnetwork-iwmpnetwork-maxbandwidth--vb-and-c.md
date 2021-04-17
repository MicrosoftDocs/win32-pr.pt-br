---
title: Propriedade IWMPNetwork maxBandwidth
description: A propriedade maxBandwidth Obtém ou define a largura de banda máxima permitida.
ms.assetid: ff7548d8-b80f-4cb4-bdd6-86d585fef329
keywords:
- Propriedade maxBandwidth Windows Media Player
- Propriedade maxBandwidth Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade maxBandwidth
topic_type:
- apiref
api_name:
- IWMPNetwork.maxBandwidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620d609db0f1786da673923f54d726b3c99994a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747283"
---
# <a name="iwmpnetworkmaxbandwidth-property"></a>Propriedade IWMPNetwork:: maxBandwidth

A propriedade **maxBandwidth** Obtém ou define a largura de banda máxima permitida.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 maxBandwidth {get; set;}
```


```VB

Public Property maxBandwidth As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é a largura de banda máxima.

## <a name="remarks"></a>Comentários

Esta propriedade não tem um valor padrão. O valor pode ser especificado enquanto o Windows Media Player está em execução, mas a alteração não entrará em vigor até que o item de mídia atual seja liberado abrindo outro ou chamando **AxWindowsMediaPlayer. Close**. O Windows Media Player tenta atingir a maior largura de banda possível. Nenhuma redução intencional da largura de banda ocorrerá a menos que esse valor seja definido.

Essa configuração é útil para reduzir a quantidade de largura de banda usada, principalmente no caso de um fluxo de taxa de bits múltipla (MBR). Um fluxo MBR contém vários fluxos com taxas de bits diferentes. Em alguns casos, pode ser desejável usar um fluxo com uma taxa de bits inferior à necessária pelo cliente. Nesse caso, a especificação de uma taxa de bits inferior com a propriedade **IWMPNetwork. maxBandwidth** selecionará um fluxo de taxa de bits inferior. Por exemplo, um fluxo MBR pode incluir fluxos codificados a 20 kilobits por segundo (Kbps), 37 kbps e 200 Kbps. Usar **IWMPNetwork. maxBandwidth** para especificar uma taxa de bits de 50.000 (50 kbps) selecionará o fluxo de 37 Kbps em vez do fluxo de 200 Kbps.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AxWindowsMediaPlayer. Close (VB e C#)**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**Interface IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





