---
title: Instrução VERSION
description: Define informações de versão sobre um recurso que pode ser usado por ferramentas que leem e escrevem arquivos de recurso.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- Menus de instrução VERSION e outros recursos
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c95f2af63d5c7bdb499d371892d0c2fa6ddb875fda5daf5b19fd0d188a478fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776656"
---
# <a name="version-statement"></a>Instrução VERSION

Define informações de versão sobre um recurso que pode ser usado por ferramentas que leem e escrevem arquivos de recurso. O valor *dword especificado* aparece com o recurso no compilado. Arquivo RES. No entanto, o valor não é armazenado no arquivo executável e não tem nenhum significado para o sistema.

A **instrução VERSION** aparece antes do início do corpo de uma definição de recurso [**ACCELERATORS,**](accelerators-resource.md) [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE.**](stringtable-resource.md) O valor especificado se aplica somente a esse recurso.

``` syntax
VERSION dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*Dword*
</dt> <dd>

Um valor **DWORD** definido pelo usuário.

</dd> </dl>

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Aceleradores**](accelerators-resource.md)
</dt> <dt>

[**Características**](characteristics-statement.md)
</dt> <dt>

[**Língua**](language-statement.md)
</dt> <dt>

[**Menu**](menu-resource.md)
</dt> <dt>

[**Rcdata**](rcdata-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> </dl>

 

 




