---
description: O método PlayForwards inicia a reprodução de encaminhamento do local atual na velocidade especificada.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Método PlayForwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e607779147ba057b9cfd747ebfe827a25e294e2b04cdfa7e61a0691ecf293c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830626"
---
# <a name="playforwards-method"></a>Método PlayForwards

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `PlayForwards` método inicia a reprodução de encaminhamento do local atual na velocidade especificada.

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*
</dt> <dd>

Especifica a velocidade na qual reproduzir como um valor Inteiro. Esse valor é um multiplicador — 1.0 é a velocidade de reprodução normal; 2.0 é velocidade dupla, 0,5 é meia velocidade e assim por diante. Quando **nSpeed não** é igual a 1.0, o áudio é mudo e a subtípica é desligada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**PlayBackwards**](playbackwards-method.md)
</dt> </dl>

 

 



