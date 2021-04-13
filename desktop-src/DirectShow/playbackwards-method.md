---
description: O método PlayBackwards inicia a reprodução regressiva do local atual na velocidade especificada.
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: Método PlayBackwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b396c3829569d3f3ad25f0c0e8718dfd23f268
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456343"
---
# <a name="playbackwards-method"></a>Método PlayBackwards

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `PlayBackwards` método inicia a reprodução regressiva do local atual na velocidade especificada.

``` syntax
MSWebDVD.PlayBackwards(nSpeed)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*
</dt> <dd>

Especifica a velocidade na qual reproduzir como um número. Esse número é um multiplicador – 1.0 é a velocidade de reprodução normal; 2,0 é a velocidade dupla, 0,5 é meia velocidade e assim por diante. Quando **nSpeed** não for igual a 1,0, o áudio ficará mudo e a subimagem será desativada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**PlayForwards**](playforwards-method.md)
</dt> </dl>

 

 



