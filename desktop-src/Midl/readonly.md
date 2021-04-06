---
title: atributo readonly
description: O atributo \ ReadOnly \ proíbe a atribuição a uma variável.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- MIDL de atributo ReadOnly
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917255"
---
# <a name="readonly-attribute"></a>atributo readonly

O atributo **\[ ReadOnly \]** proíbe a atribuição a uma variável.

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*opcional-atributos* 
</dt> <dd>

Zero ou mais atributos MIDL.

</dd> <dt>

*tipo de dados* 
</dt> <dd>

O tipo dos dados contidos no *identificador*.

</dd> <dt>

*identifier* 
</dt> <dd>

Um nome pelo qual o software pode se referir ao local de armazenamento de dados.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ ReadOnly \]** proíbe a atribuição a uma variável. somente há suporte para **\[ ReadOnly \]** no nível do parâmetro, não no nível do método.

### <a name="flags"></a>Flags

VARFLAG \_ FREADONLY

## <a name="examples"></a>Exemplos

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 