---
title: Instrução de características
description: Define informações sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de definição de recursos.
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- Menus de instruções de características e outros recursos
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de681785fa2ec815b1edbdda913dd8032f8feb8e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006524"
---
# <a name="characteristics-statement"></a>Instrução de características

Define informações sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de definição de recursos. O valor **DWORD** especificado aparece com o recurso no arquivo. res compilado. No entanto, o valor não é armazenado no arquivo executável e não tem significado para o sistema.

A instrução **características** é exibida antes do início do corpo de uma definição de recurso de [**aceleradores**](accelerators-resource.md), [**diálogo**](dialog-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE**](stringtable-resource.md) . O valor especificado aplica-se somente a esse recurso.

``` syntax
CHARACTERISTICS dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*DWORD*
</dt> <dd>

Valor **DWORD** definido pelo usuário.

</dd> </dl>

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**'**](dialog-resource.md)
</dt> <dt>

[**LANGUAGE**](language-statement.md)
</dt> <dt>

[**ADICIONARMENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




