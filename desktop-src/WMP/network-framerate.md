---
title: Network.frameRate
description: A propriedade frameRate recupera a taxa de quadros de vídeo atual em quadros por centenas de segundos. Por exemplo, um valor de 2998 indica 29,98 quadros por segundo.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Network.frameRate Windows Media Player
topic_type:
- apiref
api_name:
- Network.frameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da4a0f292c4693c263115dc1ad59ea3c71946d81838d427e6d8e043ac499709
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901646"
---
# <a name="networkframerate"></a>Network.frameRate

A **propriedade frameRate** recupera a taxa de quadros de vídeo atual em quadros por centenas de segundos. Por exemplo, um valor de 2998 indica 29,98 quadros por segundo.

## <a name="syntax"></a>Syntax

*player*. *network*. **taxa de quadros**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um Número somente **leitura** (**long**).

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *Rede*. **frameRate** para exibir a taxa de quadros atual. As informações são exibidas em um HTML DIV criado com ID = "FR". O **objeto** Player foi criado com ID = "Player".


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the current frame rate.
          FR.innerHTML = "Frame Rate: ";
          FR.innerHTML += Player.network.frameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> <dt>

[**Network.encodedFrameRate**](network-encodedframerate.md)
</dt> </dl>

 

 





