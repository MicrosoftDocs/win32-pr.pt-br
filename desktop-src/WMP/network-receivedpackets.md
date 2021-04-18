---
title: Network. receivedPackets
description: A propriedade receivedPackets recupera o número de pacotes recebidos.
ms.assetid: db4f6f08-c248-4db8-ab19-fdd5d2794085
keywords:
- Network. receivedPackets Windows Media Player
topic_type:
- apiref
api_name:
- Network.receivedPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc792330cd107ca428ad0fbec930fe262a2f131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788887"
---
# <a name="networkreceivedpackets"></a>Network. receivedPackets

A propriedade **receivedPackets** recupera o número de pacotes recebidos.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **receivedPackets**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="remarks"></a>Comentários

Toda vez que a reprodução de clipe é interrompida e reiniciada, essa propriedade é definida como zero. Ela não será redefinida se a reprodução do arquivo for pausada.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **receivedPackets** para exibir o número de pacotes recebidos. As informações são exibidas em um DIV HTML criado com ID = "RP". O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>

   var idI; // Variable for the interval id.

   // Test whether packets may be arriving.
   switch (NewState){
      case 1, 2, 4, 5, 7, 8, 9:
          window.clearInterval(idI);
          break;

      default:
         idI = window.setInterval("UpdateRP()", 1000);

   }</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRP(){
   RP.innerHTML = "";
   RP.innerHTML = "Packets received: " + Player.network.receivedPackets;         
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> </dl>

 

 





