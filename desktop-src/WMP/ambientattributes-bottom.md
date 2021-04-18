---
title: Ambiente de nível inferior
description: O atributo inferior especifica ou recupera a coordenada inferior do controle.
ms.assetid: a07af5b0-154d-4c3f-be8b-39aeb52a6f1e
keywords:
- Ambiente. Windows Media Player inferior
topic_type:
- apiref
api_name:
- AmbientAttributes.bottom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ed707dbd821119963a46c5ac9a8301c20f4d39e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794531"
---
# <a name="ambientattributesbottom"></a>Ambiente de nível inferior

O atributo **inferior** especifica ou recupera a coordenada inferior do controle.

``` syntax
        elementID.bottom
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (**longo**) que representa a distância em pixels do controle até a borda inferior da **exibição** ou **subexibição** pai. Ele tem um valor padrão de zero. O comportamento para valores negativos ou quando [ambienteattributes. Height](ambientattributes-height.md) não é especificado, é indefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.id**](ambientattributes-id.md)
</dt> </dl>

 

 





