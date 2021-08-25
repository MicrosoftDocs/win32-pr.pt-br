---
description: A propriedade CurrentCCService define ou recupera o serviço de legenda fechada atual.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Propriedade CurrentCCService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d836e852d1a144abb5422f71d0127eb9c37b8f333dce0723db2c2b3b1889ec50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075956"
---
# <a name="currentccservice-property"></a>Propriedade CurrentCCService

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `CurrentCCService` propriedade define ou recupera o serviço de legenda fechada atual.

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que indica o tipo de serviço de legenda fechado habilitado.

## <a name="remarks"></a>Comentários

Os valores possíveis dessa propriedade são:



| Valor | Descrição                                                          |
|-------|----------------------------------------------------------------------|
| 0x0   | Nenhum serviço atual. Esse é o valor padrão.                       |
| 0x1   | Legenda verdadeira, primeiro campo. Serviço padrão.                       |
| 0x2   | Legenda para idioma secundário, segundo campo. Geralmente não usado. |



 

Essa propriedade é leitura/gravação.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**CCActive**](ccactive-property.md)
</dt> </dl>

 

 



