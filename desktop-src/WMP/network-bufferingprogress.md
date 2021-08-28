---
title: Network. bufferingProgress
description: A propriedade bufferingProgress recupera a porcentagem de buffer concluído.
ms.assetid: d604159b-7c42-47f8-8085-53f859f24703
keywords:
- Windows Media Player Network. bufferingProgress
topic_type:
- apiref
api_name:
- Network.bufferingProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65de3f7b1b58dfb90f76436f324dcc3d4fc3fe9a24b7c60ca3db888771f9192d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901746"
---
# <a name="networkbufferingprogress"></a>Network. bufferingProgress

A propriedade **bufferingProgress** recupera a porcentagem de buffer concluído.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **bufferingProgress**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="remarks"></a>Comentários

Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é definida como zero. Ele não será redefinido se a reprodução for pausada.

O armazenamento em buffer só se aplica ao conteúdo de streaming. Essa propriedade retorna informações válidas somente durante o tempo de execução, quando o *Player*. A propriedade de **URL** está definida.

Use o evento *Player*. * * * * buffer * * * * para determinar quando o buffer inicia ou pára.

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript usa a *rede*. **bufferingProgress** para exibir a porcentagem de buffer concluído. As informações são exibidas em um DIV HTML criado com ID = "BP". O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.

   // Test whether buffering has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdateBP()", 1000);
   }

   else{
      // Buffering is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateBP(){
   BP.innerHTML = "";
   BP.innerHTML = "Buffering progress: " + Player.network.bufferingProgress;
   BP.innerHTML += " percent complete";
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

[**Evento Player. buffering**](player-player-buffering.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





