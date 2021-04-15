---
description: O método Play reproduz o título do DVD atual.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Método play (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500361"
---
# <a name="play-method-directshow"></a>Método play (DirectShow)

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `Play` método reproduz o título do DVD atual.

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se a reprodução for pausada ou interrompida e [**EnableResetOnStop**](enableresetonstop-property.md) for true, chamar **Play** retomará a reprodução em velocidade normal no local atual. Se a reprodução for interrompida e **EnableResetOnStop** for false, chamar **Play** fará com que o disco comece a ser reproduzido no início do primeiro título.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Retomar**](resume-method.md)
</dt> </dl>

 

 



