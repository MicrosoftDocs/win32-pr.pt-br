---
title: Network. recoveredPackets
description: A propriedade recoveredPackets recupera o número de pacotes recuperados.
ms.assetid: ce10b906-2e8b-4b9f-83d0-56ba67cacd3f
keywords:
- Network. recoveredPackets Windows Media Player
topic_type:
- apiref
api_name:
- Network.recoveredPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4222033d7e124e6ef29714bc47faf5664950fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788886"
---
# <a name="networkrecoveredpackets"></a>Network. recoveredPackets

A propriedade **recoveredPackets** recupera o número de pacotes recuperados.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **recoveredPackets**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="remarks"></a>Comentários

Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é definida como zero. Ele não será redefinido se a reprodução for pausada.

Essa propriedade retorna informações válidas somente durante o tempo de execução e somente se o *jogador*. A propriedade **URL** também é definida. Ele será igual a zero ao usar o protocolo HTTP, que é sem perdas.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **recoveredPackets** para exibir o número de pacotes recuperados. As informações são exibidas em uma DIV HTML criada com ID = "PR". O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdatePR()", 1000);
   }
   else{
      // Not playing; stop the timer.
      window.clearInterval(idI);
   }   
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdatePR(){
   PR.innerHTML = "";
   PR.innerHTML = "Packets recovered: " + Player.network.recoveredPackets;
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

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





