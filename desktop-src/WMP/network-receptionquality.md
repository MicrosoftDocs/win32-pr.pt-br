---
title: Network.receptionQuality
description: A propriedade receptionQuality recupera a porcentagem de pacotes recebidos nos últimos 30 segundos.
ms.assetid: 432f7f0a-0130-4485-b4a3-daa80ce9bb36
keywords:
- Network.receptionQuality Windows Media Player
topic_type:
- apiref
api_name:
- Network.receptionQuality
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159bcac192d5a5bd9197ecc3ea935027dd6d707dde42a54c64a318459ae00040
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574152"
---
# <a name="networkreceptionquality"></a>Network.receptionQuality

A **propriedade receptionQuality** recupera a porcentagem de pacotes recebidos nos últimos 30 segundos.

## <a name="syntax"></a>Sintaxe

*player*. *network*. **igualdade de recepção**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um Número somente **leitura** (**long**).

## <a name="remarks"></a>Comentários

O número de pacotes recebidos, perdidos e recuperados durante o streaming é monitorado uma vez por segundo. **receptionQuality** é o percentual de pacotes não perdidos durante os últimos 30 segundos.

Sempre que a reprodução é interrompida e reiniciada, essa propriedade é definida como zero. Ele não será redefinido se a reprodução estiver em pausa.

Essa propriedade retorna informações válidas somente durante o tempo de run e somente se o *Player*. **A propriedade URL** também está definida.

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa *Rede*. **receptionQuality** para exibir o percentual de pacotes recebidos. As informações são exibidas em um HTML DIV criado com ID = "RQ". O exemplo usa um temporizador com um intervalo de 30 segundos para atualizar a exibição. O **objeto** Player foi criado com ID = "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
         // Start the timer. Update the display every 30 seconds.
         idI = window.setInterval("UpdateRQ()", 30000);
   }

      else{
         // Not playing; stop the timer.
         window.clearInterval(idI);
      }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRQ(){
         RQ.innerHTML = "";
         RQ.innerHTML = "Reception quality: " + Player.network.receptionQuality;
         RQ.innerHTML += "%";         
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

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





