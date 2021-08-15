---
title: Método Controls. Step
description: O método Step faz com que o item de mídia de vídeo atual congele a reprodução no próximo quadro ou no quadro anterior.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- método Step Windows Media Player
- método step Windows Media Player, classe Controls
- classe Controls Windows Media Player, método step
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4626ff80aee55ad6c22be7580a07ef2319afb6792a8c11b815d72af23b5727fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118839821"
---
# <a name="controlsstep-method"></a>Método Controls. Step

O método **Step** faz com que o item de mídia de vídeo atual congele a reprodução no próximo quadro ou no quadro anterior.

## <a name="syntax"></a>Sintaxe


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*frameCount* \[ no\]
</dt> <dd>

**Número** (**longo**) indicando quantos quadros passar antes de congelar. Deve ser definido no momento como 1 ou-1.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método atualmente só dá suporte aos parâmetros 1 ou-1, portanto, você só pode passar um quadro por vez.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Objeto de DVD**](dvd-object.md)
</dt> </dl>

 

 





