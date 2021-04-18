---
title: Network. taxa de quadros
description: A propriedade de taxa de quadros recupera a taxa de quadros de vídeo atual em quadros por centenas de segundos. Por exemplo, um valor de 2998 indica 29,98 quadros por segundo.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Rede. taxa de quadros Windows Media Player
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
ms.openlocfilehash: 30ec6e16a3cef86a385525a793d73a50c3124e21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781646"
---
# <a name="networkframerate"></a>Network. taxa de quadros

A propriedade de **taxa** de quadros recupera a taxa de quadros de vídeo atual em quadros por centenas de segundos. Por exemplo, um valor de 2998 indica 29,98 quadros por segundo.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **taxa de quadros**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. taxa **de quadros para exibir** a tarifa de quadros atual. As informações são exibidas em um DIV HTML criado com ID = "FR". O objeto de **jogador** foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> <dt>

[**Network. encodedFrameRate**](network-encodedframerate.md)
</dt> </dl>

 

 





