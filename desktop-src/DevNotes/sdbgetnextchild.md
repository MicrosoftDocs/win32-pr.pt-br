---
description: Pesquisa a próxima TAG filho dentro do pai especificado e retorna a TAGID do próximo filho.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: Função SdbGetNextChild
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 210e0aab8cb5e43bfc649e8abb72cf565c4d4f892f651708286f7a3f87d11ce2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045298"
---
# <a name="sdbgetnextchild-function"></a>Função SdbGetNextChild

Pesquisa a próxima TAG filho dentro do pai especificado e retorna **a TAGID** do próximo filho.

## <a name="syntax"></a>Sintaxe


```C++
TAGID WINAPI SdbGetNextChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdb* \[ Em\]
</dt> <dd>

Um alça para o banco de dados shim.

</dd> <dt>

*tiParent* \[ Em\]
</dt> <dd>

O **TAGID** do início da pesquisa. Esse parâmetro pode ser **TAGID \_ ROOT ou** **TAG TYPE \_ \_ LIST.**

</dd> <dt>

*tiPrev* \[ Em\]
</dt> <dd>

O **TAGID** do filho anterior.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O **TAGID** do filho ou **TAGID \_ NULL** se nenhum filho for encontrado.

## <a name="remarks"></a>Comentários

Antes de chamar essa função, chame a [**função SdbGetFirstChild.**](sdbgetfirstchild.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbGetFirstChild**](sdbgetfirstchild.md)
</dt> </dl>

 

 




