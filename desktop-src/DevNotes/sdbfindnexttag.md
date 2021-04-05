---
description: Pesquisa a próxima marca correspondente no pai especificado e retorna o TAGID da correspondência.
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: Função SdbFindNextTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a5baf728a75e4c02c20ed4207b7d6b9a968af1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826276"
---
# <a name="sdbfindnexttag-function"></a>Função SdbFindNextTag

Pesquisa a próxima marca correspondente no pai especificado e retorna o **TagId** da correspondência.

## <a name="syntax"></a>Sintaxe


```C++
TAGID WINAPI SdbFindNextTag(
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

O **TagId** da correspondência anterior.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O **TagId** da correspondência.

## <a name="remarks"></a>Comentários

Antes de chamar essa função, chame a função [**SdbFindFirstTag**](sdbfindfirsttag.md) .

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

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 




