---
title: Ambienteattributes. visível
description: O atributo Visible especifica ou recupera a visibilidade do controle.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- Ambiente do Windows Media Player visível.
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72794b7bbba0237a687dc70bda761c505b839e59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762108"
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

 

 





