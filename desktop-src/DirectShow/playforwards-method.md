---
description: O método PlayForwards começa a enviar a reprodução do local atual na velocidade especificada.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Método PlayForwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d49d8d6d80613c4dd5b2b8a374002b37d9baa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645973"
---
# <a name="playforwards-method"></a>Método PlayForwards

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `PlayForwards` método começa a redirecionar a reprodução do local atual na velocidade especificada.

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*
</dt> <dd>

Especifica a velocidade na qual reproduzir como um valor inteiro. Esse valor é um multiplicador — 1,0 é a velocidade de reprodução normal; 2,0 é a velocidade dupla, 0,5 é meia velocidade e assim por diante. Quando **nSpeed** não for igual a 1,0, o áudio ficará mudo e a subimagem será desativada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**PlayBackwards**](playbackwards-method.md)
</dt> </dl>

 

 



