---
title: Instrução de linguagem
description: Define o idioma para todos os recursos até a próxima instrução de idioma ou para o final do arquivo.
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- Menus de instrução de linguagem e outros recursos
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9563ba2ec00362a3b9caa3911a701919a81cae1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499042"
---
# <a name="language-statement"></a>Instrução de linguagem

Define o idioma para todos os recursos até a próxima instrução de **idioma** ou para o final do arquivo.

Quando a instrução de **idioma** aparece antes do início do corpo de uma definição de recurso de [**aceleradores**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE**](stringtable-resource.md) , o idioma especificado aplica-se somente a esse recurso.

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span id="language"></span><span id="LANGUAGE"></span>*idioma*
</dt> <dd>

Identificador de idioma.

</dd> <dt>

<span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*subidioma*
</dt> <dd>

Identificador de subidioma.

</dd> </dl>

Para obter mais informações, consulte [constantes e cadeias de caracteres de identificador de linguagem](/windows/desktop/Intl/language-identifier-constants-and-strings).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**CARACTERÍSTICAS**](characteristics-statement.md)
</dt> <dt>

[**ADICIONARMENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versão**](version-statement.md)
</dt> </dl>

 

 