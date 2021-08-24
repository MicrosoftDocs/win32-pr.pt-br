---
title: atributo readonly
description: O atributo \ readonly\ proíbe a atribuição a uma variável.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- atributo readonly MIDL
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d0d534efe8df1f4d05cd0b536a78094f903870d896114ee8b614511e067025b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013674"
---
# <a name="readonly-attribute"></a>atributo readonly

O **\[ atributo \] readonly** proíbe a atribuição a uma variável.

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*atributos opcionais* 
</dt> <dd>

Zero ou mais atributos MIDL.

</dd> <dt>

*tipo de dados* 
</dt> <dd>

O tipo dos dados contidos pelo *identificador*.

</dd> <dt>

*identifier* 
</dt> <dd>

Um nome pelo qual o software pode se referir ao local de armazenamento de dados.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **\[ atributo \] readonly** proíbe a atribuição a uma variável. **\[ somente leitura \] tem** suporte no nível do parâmetro, não no nível do método.

### <a name="flags"></a>Flags

VARFLAG \_ FREADONLY

## <a name="examples"></a>Exemplos

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 