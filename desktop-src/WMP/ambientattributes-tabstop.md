---
title: Ambiente. tabStop
description: O atributo tabStop especifica ou recupera um valor que indica se o controle está na ordem de tabulação. Você define a ordem de tabulação colocando o controle no script geral antes ou depois de outras marcas de controle.
ms.assetid: 3d4b7fe4-1032-44e1-bae5-f253d00881bf
keywords:
- Windows Media Player de ambiente. tabStop
topic_type:
- apiref
api_name:
- AmbientAttributes.tabStop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4005fc26a2bc5f928cde0f5ed67ec2098cf3e6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763380"
---
# <a name="ambientattributestabstop"></a>Ambiente. tabStop

O atributo **tabStop** especifica ou recupera um valor que indica se o controle está na ordem de tabulação. Você define a ordem de tabulação colocando o controle no script geral antes ou depois de outras marcas de controle.

``` syntax
        elementID.tabStop
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | O controle está na ordem de tabulação (o controle terá uma parada de tabulação: requisito de acessibilidade). |
| false | O controle não está na ordem de tabulação.                                                       |



 

## <a name="remarks"></a>Comentários

O atributo **tabStop** não é aplicável ao elemento **Effects** .

O valor padrão para esse atributo é true para todos os elementos, exceto **menu** e **texto**, que têm um valor padrão de false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





