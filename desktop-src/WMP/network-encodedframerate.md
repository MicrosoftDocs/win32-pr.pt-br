---
title: Network. encodedFrameRate
description: A propriedade encodedFrameRate recupera a taxa de quadros de vídeo especificada pelo autor do conteúdo em quadros por segundo.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- Windows Media Player Network. encodedFrameRate
topic_type:
- apiref
api_name:
- Network.encodedFrameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f64b6f57b4cfd0e7bc94715f80c1066ebe23a601e64c173926cf2cd9e36393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901696"
---
# <a name="networkencodedframerate"></a>Network. encodedFrameRate

A propriedade **encodedFrameRate** recupera a taxa de quadros de vídeo especificada pelo autor do conteúdo em quadros por segundo.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **encodedFrameRate**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript usa a *rede*. **encodedFrameRate** para exibir a taxa de quadros especificada quando o arquivo foi codificado. As informações são exibidas em um DIV HTML criado com ID = "FR". O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the encoded frame rate.
          FR.innerHTML = "Encoded Frame Rate: ";
          FR.innerHTML += Player.network.encodedFrameRate;
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

[**Network. taxa de quadros**](network-framerate.md)
</dt> </dl>

 

 





