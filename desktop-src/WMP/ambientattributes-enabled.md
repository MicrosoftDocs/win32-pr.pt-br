---
title: AmbientAttributes.enabled
description: O atributo habilitado especifica ou recupera um valor que indica se o controle está habilitado ou desabilitado.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- AmbienteAttributes.enabled Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9d8e000d64ef92212cd7c6cf37c7fd79036107e1d3be0d7669d73b40c759de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055174"
---
# <a name="ambientattributesenabled"></a>AmbientAttributes.enabled

O **atributo habilitado** especifica ou recupera um valor que indica se o controle está habilitado ou desabilitado.

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um booliana **de leitura/gravação.**



| Valor | Descrição               |
|-------|---------------------------|
| true  | Padrão. Controle habilitado. |
| false | Controle desabilitado.         |



 

## <a name="remarks"></a>Comentários

Se o controle estiver habilitado, ele poderá ter uma parada de tabulação e receberá todos os eventos de ambiente. Quando desabilitado, o controle não tem uma parada de tabulação e não recebe nenhum evento de mouse ou teclado ambiente disparado para ele. (No entanto, ele continuará a receber todos os outros eventos de ambiente acionados para ele.)

Não há suporte para esse atributo para o **elemento SUBVIEW.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





