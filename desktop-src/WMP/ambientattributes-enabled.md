---
title: Ambienteattributes. habilitado
description: O atributo Enabled especifica ou recupera um valor que indica se o controle está habilitado ou desabilitado.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- Ambiente do Windows Media Player habilitado para ambientes.
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c34d24e86118a1cca0939d535b6da6e86c2df34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784922"
---
# <a name="ambientattributesenabled"></a>Ambienteattributes. habilitado

O atributo **Enabled** especifica ou recupera um valor que indica se o controle está habilitado ou desabilitado.

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição               |
|-------|---------------------------|
| true  | Padrão. Controle habilitado. |
| false | Controle desabilitado.         |



 

## <a name="remarks"></a>Comentários

Se o controle estiver habilitado, ele poderá ter uma parada de tabulação e receberá todos os eventos de ambiente. Quando desabilitado, o controle não tem uma parada de tabulação e não recebe nenhum evento de teclado ou mouse de ambiente acionado para ele. (No entanto, ele continuará a receber todos os outros eventos de ambiente acionados para ele.)

Não há suporte para esse atributo no elemento **subview** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





