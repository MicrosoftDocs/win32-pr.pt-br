---
title: Network. encodedFrameRate
description: A propriedade encodedFrameRate recupera a taxa de quadros de vídeo especificada pelo autor do conteúdo em quadros por segundo.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- Network. encodedFrameRate Windows Media Player
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
ms.openlocfilehash: 0008eb5d648dc7d3f51b40329ca3d830c3590c49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772935"
---
# <a name="networkencodedframerate"></a>Network. encodedFrameRate

A propriedade **encodedFrameRate** recupera a taxa de quadros de vídeo especificada pelo autor do conteúdo em quadros por segundo.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **encodedFrameRate**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **encodedFrameRate** para exibir a taxa de quadros especificada quando o arquivo foi codificado. As informações são exibidas em um DIV HTML criado com ID = "FR". O objeto de **jogador** foi criado com ID = "Player".


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

 

 





