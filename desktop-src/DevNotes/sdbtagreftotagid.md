---
description: Recupera o TAGID e um handle para o banco de dados shim para o TAGREF especificado.
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: Função SdbTagRefToTagID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagRefToTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: feeb622fd196ed20efb60d866d59b634fdcd9ecd955a97a1d7af0aef1347c8f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815315"
---
# <a name="sdbtagreftotagid-function"></a>Função SdbTagRefToTagID

Recupera o **TAGID e** um handle para o banco de dados shim para o [**TAGREF especificado.**](tagref.md)

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbTagRefToTagID(
  _In_  HSDB   hSDB,
  _In_  TAGREF trWhich,
  _Out_ PDB    *ppdb,
  _Out_ TAGID  *ptiWhich
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSDB* \[ Em\]
</dt> <dd>

Um handle para o banco de dados shim retornado pela [**função SdbInitDatabase.**](sdbinitdatabase.md)

</dd> <dt>

*trWhich* \[ Em\]
</dt> <dd>

O [**TAGREF.**](tagref.md)

</dd> <dt>

*ppdb* \[ out\]
</dt> <dd>

O alça resultante para o banco de dados shim.

</dd> <dt>

*ptiWhich* \[ out\]
</dt> <dd>

O **TAGID resultante.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna **TRUE em** caso de êxito **ou FALSE** em caso de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




