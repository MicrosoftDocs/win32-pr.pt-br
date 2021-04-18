---
title: Método de etapa IWMPControls2
description: O método Step faz com que o item de mídia de vídeo atual passe para o próximo quadro ou para o quadro anterior e congele a reprodução.
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- método Step Windows Media Player
- método Step Windows Media Player, interface IWMPControls2
- Interface IWMPControls2 Windows Media Player, método Step
topic_type:
- apiref
api_name:
- IWMPControls2.step
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfb65dd20de506a8f303121b23668e2fbf14dc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784053"
---
# <a name="iwmpcontrols2step-method"></a>Método IWMPControls2:: Step

O método **Step** faz com que o item de mídia de vídeo atual passe para o próximo quadro ou para o quadro anterior e congele a reprodução.

## <a name="syntax"></a>Sintaxe


```CSharp
public void step(
  System.Int32 lStep
);
```


```VB

Public Sub step( _
  ByVal lStep As System.Int32 _
)
Implements IWMPControls2.step
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lStep* \[ no\]
</dt> <dd>

Um valor **System. Int32** que indica quantos quadros depurar antes de congelar. Deve ser definido como 1 ou-1.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método atualmente dá suporte apenas aos parâmetros 1 ou-1, de modo que você só pode passar um quadro por vez.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPControls2 (VB e C#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**Interface IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





