---
title: Network. bufferingCount
description: A propriedade bufferingCount recupera o número de vezes que o buffer ocorreu durante a reprodução do clipe.
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- Network. bufferingCount Windows Media Player
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
ms.openlocfilehash: 524dc66c7f4ed1d413f264a91ae9385d458d632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796148"
---
# <a name="networkbufferingcount"></a>Network. bufferingCount

A propriedade **bufferingCount** recupera o número de vezes que o buffer ocorreu durante a reprodução do clipe.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **bufferingCount**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="remarks"></a>Comentários

Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é definida como zero. Ele não será redefinido se a reprodução for pausada.

O armazenamento em buffer só se aplica ao conteúdo de streaming. Essa propriedade retorna informações válidas somente durante o tempo de execução quando o *Player*. A propriedade de **URL** está definida.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **bufferingCount** para exibir o número de vezes que o buffer ocorre durante a reprodução. As informações são exibidas em uma DIV HTML criada com ID = "CB". O objeto de **jogador** foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





