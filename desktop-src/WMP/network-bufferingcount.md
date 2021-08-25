---
title: Network.bufferingCount
description: A propriedade bufferingCount recupera o número de vezes que o buffer ocorreu durante a reprodução do clipe.
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- Network.bufferingCount Windows Media Player
topic_type:
- apiref
api_name:
- Network.bufferingCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d19c80715ca04965927bb0a50450213d707beeb124fd671fd8071e2cdd90e3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901756"
---
# <a name="networkbufferingcount"></a>Network.bufferingCount

A **propriedade bufferingCount** recupera o número de vezes que o buffer ocorreu durante a reprodução do clipe.

## <a name="syntax"></a>Syntax

*player*. *network*. **bufferingCount**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um Número somente **leitura** (**long**).

## <a name="remarks"></a>Comentários

Sempre que a reprodução é interrompida e reiniciada, essa propriedade é definida como zero. Ele não será redefinido se a reprodução estiver em pausa.

O buffer só se aplica ao conteúdo de streaming. Essa propriedade retorna informações válidas somente durante o tempo de executar quando o *Player*. **A propriedade URL** está definida.

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa *Rede*. **bufferingCount** para exibir o número de vezes que o buffer ocorre durante a reprodução. As informações são exibidas em um HTML DIV criado com ID = "CB". O **objeto** Player foi criado com ID = "Player".


```JScript
<!-- Create an event handler. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   if (true == Start) 
      CB.innerHTML = "Buffering count: " + Player.network.bufferingCount;
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

 

 





