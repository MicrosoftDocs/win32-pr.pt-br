---
title: Instrução CHARACTERISTICS
description: Define informações sobre um recurso que pode ser usado por ferramentas que leem e escrevem arquivos de definição de recurso.
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- Menus de instrução CHARACTERISTICS e outros recursos
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9910a86263d14dd928fb01347dfea4fd6c796c23b4e5d42d69cdba4bc40e14c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034305"
---
# <a name="characteristics-statement"></a>Instrução CHARACTERISTICS

Define informações sobre um recurso que pode ser usado por ferramentas que leem e escrevem arquivos de definição de recurso. O valor **DWORD especificado** aparece com o recurso no arquivo .res compilado. No entanto, o valor não é armazenado no arquivo executável e não tem nenhum significado para o sistema.

A **instrução CHARACTERISTICS** aparece antes do início do corpo de uma definição de recurso [**ACCELERATORS,**](accelerators-resource.md) [**DIALOG**](dialog-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE.**](stringtable-resource.md) O valor especificado se aplica somente a esse recurso.

``` syntax
CHARACTERISTICS dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*Dword*
</dt> <dd>

Valor **DWORD** definido pelo usuário.

</dd> </dl>

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Aceleradores**](accelerators-resource.md)
</dt> <dt>

[**Diálogo**](dialog-resource.md)
</dt> <dt>

[**Língua**](language-statement.md)
</dt> <dt>

[**Menu**](menu-resource.md)
</dt> <dt>

[**Rcdata**](rcdata-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> </dl>

 

 




