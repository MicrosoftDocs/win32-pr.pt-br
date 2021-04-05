---
description: Pesquisa a próxima marca filha dentro do pai especificado e retorna o TAGID do próximo filho.
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
ms.openlocfilehash: 4f2943eaf0baec84a9473b679743b9eafad3b7fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826354"
---
# <a name="sdbgetnextchild-function"></a>Função SdbGetNextChild

Pesquisa a próxima marca filha dentro do pai especificado e retorna o **TagId** do próximo filho.

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

*PDB* \[ no\]
</dt> <dd>

Um identificador para o banco de dados de Shim.

</dd> <dt>

*tiParent* \[ no\]
</dt> <dd>

O **TagId** do início da pesquisa. Esse parâmetro pode ser **TagId \_ raiz** ou **\_ \_ lista de tipos de marca**.

</dd> <dt>

*tiPrev* \[ no\]
</dt> <dd>

O **TagId** do filho anterior.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O **TagId** do filho ou **TagId \_ nulo** se nenhum filho for encontrado.

## <a name="remarks"></a>Comentários

Antes de chamar essa função, chame a função [**SdbGetFirstChild**](sdbgetfirstchild.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbGetFirstChild**](sdbgetfirstchild.md)
</dt> </dl>

 

 




