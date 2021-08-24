---
description: Verifica se o processo de chamada tem acesso de leitura a uma cadeia de caracteres. Caso não seja, a macro chamará a macro DbgBreak.
ms.assetid: 749a8c22-7a4a-49c2-a214-fc64dc5a0202
title: Macro ValidateStringPtr (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadPtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: e6b04b83f3bd3b938f7cc6cc488a931e34bcca6207770b44cbd3c77c01dc9624
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755686"
---
# <a name="validatestringptr-macro"></a>Macro ValidateStringPtr

Verifica se o processo de chamada tem acesso de leitura a uma cadeia de caracteres. Caso não seja, a macro chamará a macro [**DbgBreak.**](dbgbreak.md)

> [!Note]  
> Essa macro foi preterida. No SDK Windows para Windows Vista (e posterior), essa macro não faz nada.

 

## <a name="syntax"></a>Sintaxe


```C++
void ValidateReadPtr(
   LPCTSTR p
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*P* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres TCHAR terminada **em NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

Essa macro é ignorada, a menos que DEBUG, DEBUG ou VFWROBUST seja definido quando o arquivo de DirectShow de classe \_ base for incluído. Essa macro pode ter um custo de desempenho significativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug.h (incluir Fluxos.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros de validação de ponteiro](pointer-validation-macros.md)
</dt> </dl>

 

 




