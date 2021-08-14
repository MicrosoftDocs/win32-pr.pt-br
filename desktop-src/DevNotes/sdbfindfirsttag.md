---
description: Procura uma correspondência de marca dentro do pai especificado e retorna o TAGID da primeira correspondência.
ms.assetid: ecbe216c-1e46-4472-b1d1-e2ac7ace82ab
title: Função SdbFindFirstTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f6562589158e5c3a5e1b65273451f812802c1c73b76f52c47274c06b9639f5ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390226"
---
# <a name="sdbfindfirsttag-function"></a>Função SdbFindFirstTag

Procura uma correspondência de marca dentro do pai especificado e retorna o **TagId** da primeira correspondência.

## <a name="syntax"></a>Sintaxe


```C++
TAGID WINAPI SdbFindFirstTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAG   tTag
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

*tTag* \[ no\]
</dt> <dd>

A marca a ser correspondida. Consulte a [marca](tag.md) para obter uma lista de valores possíveis.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O **TagId** da primeira correspondência.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 




