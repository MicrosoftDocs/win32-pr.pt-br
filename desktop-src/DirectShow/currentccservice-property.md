---
description: A propriedade CurrentCCService define ou recupera o serviço de legendagem oculta atual.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Propriedade CurrentCCService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5c1ddf243b0ec943be1f22930a8802d28d1bda
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825860"
---
# <a name="currentccservice-property"></a>Propriedade CurrentCCService

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `CurrentCCService` propriedade define ou recupera o serviço de legendagem oculta atual.

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que indica o tipo de serviço de legendagem oculta habilitado.

## <a name="remarks"></a>Comentários

Os valores possíveis dessa propriedade são:



| Valor | Descrição                                                          |
|-------|----------------------------------------------------------------------|
| 0x0   | Nenhum serviço atual. Esse é o valor padrão.                       |
| 0x1   | Legenda verdadeira, primeiro campo. Serviço padrão.                       |
| 0x2   | Legenda do idioma secundário, segundo campo. Geralmente não usado. |



 

Esta propriedade é de leitura/gravação.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**CCActive**](ccactive-property.md)
</dt> </dl>

 

 



