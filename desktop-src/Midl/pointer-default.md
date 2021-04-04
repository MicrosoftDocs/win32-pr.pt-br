---
title: Atributo pointer_default
description: O atributo \ padrão \ pointername \_ especifica o atributo de ponteiro padrão para todos os ponteiros, exceto os ponteiros de nível superior que aparecem nas listas de parâmetros.
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- pointer_default do atributo MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08555358eb0abd42957d60527e18a4fd4f49165a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007402"
---
# <a name="pointer_default-attribute"></a>\_atributo padrão de ponteiro

O atributo **\[ \_ padrão \] de ponteiro** especifica o atributo de ponteiro padrão para todos os ponteiros, exceto para os ponteiros de nível superior que aparecem nas listas de parâmetros.

``` syntax
pointer_default ( ptr | ref | unique )
```

## <a name="parameters"></a>Parâmetros

Este atributo não tem parâmetros.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(6B29FC40-CA47-1067-B31D-00DD010662DA), 
    version(3.3), 
    pointer_default(unique)
] 
interface dictionary 
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**interface**](interface.md)
</dt> <dt>

[Atributos de matriz e de Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**Storage**](arrays-1.md)
</dt> <dt>

[Matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> <dt>

[Tipos de ponteiro padrão](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 