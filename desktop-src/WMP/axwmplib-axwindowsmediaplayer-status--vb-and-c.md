---
title: Propriedade AxWindowsMediaPlayer. status
description: A propriedade status Obtém um valor que indica o status do Windows Media Player.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- Propriedade de status Windows Media Player
- Propriedade de status Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade status
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.status
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea7e8c36ad05e2f9a4573d8e2433d705f354239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781058"
---
# <a name="axwindowsmediaplayerstatus-property"></a>Propriedade AxWindowsMediaPlayer. status

A propriedade status Obtém um valor que indica o status do Windows Media Player.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a>Valor da propriedade

O System. String que é o status.

## <a name="remarks"></a>Comentários

Os valores contidos nessa propriedade estão sujeitos a alterações a qualquer momento e devem ser usados apenas para fins de exibição.

O AxWindowsMediaPlayer. O evento **StatusChange** é acionado sempre que essa propriedade altera o valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer. StatusChange (VB e C#)**](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





