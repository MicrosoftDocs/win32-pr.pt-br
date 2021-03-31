---
title: Instrução de versão
description: Define informações de versão sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- Menus de instrução de versão e outros recursos
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302ffcee38b287afff2697b9c5a5241fa406b55c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638572"
---
# <a name="version-statement"></a>Instrução de versão

Define informações de versão sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos. O valor *DWORD* especificado aparece com o recurso no compilado. Arquivo RES. No entanto, o valor não é armazenado no arquivo executável e não tem significado para o sistema.

A instrução de **versão** aparece antes do início do corpo de uma definição de recurso de [**aceleradores**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE**](stringtable-resource.md) . O valor especificado aplica-se somente a esse recurso.

``` syntax
VERSION dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*DWORD*
</dt> <dd>

Um valor **DWORD** definido pelo usuário.

</dd> </dl>

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**CARACTERÍSTICAS**](characteristics-statement.md)
</dt> <dt>

[**IDIOMA**](language-statement.md)
</dt> <dt>

[**ADICIONARMENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




