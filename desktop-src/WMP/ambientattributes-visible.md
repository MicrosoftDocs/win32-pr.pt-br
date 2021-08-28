---
title: Ambienteattributes. visível
description: O atributo Visible especifica ou recupera a visibilidade do controle.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- Ambiente Windows Media Player. visível
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6136bbdba7fe222c16e6185bc2ddfa243c5387443122fb93eb1d6564ad01c956
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124046"
---
# <a name="ambientattributesvisible"></a>Ambienteattributes. visível

O atributo **Visible** especifica ou recupera a visibilidade do controle.

``` syntax
        elementID.visible
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                      |
|-------|----------------------------------|
| true  | Padrão. O controle é visível. |
| false | O controle não está visível.      |



 

## <a name="remarks"></a>Comentários

Esse atributo é útil para ocultar controles, por exemplo, ao alternar um botão de pausa para um botão de reprodução.

Se o valor for false, o controle não será visível e os eventos de clique serão passados para o controle por trás dele. Se o valor for true, o controle ficará visível e receberá o próprio evento de clique.

O valor padrão para o elemento **Automenu** é false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





