---
description: Recupera o TAGID e um identificador para o banco de dados de Shim para o TAGREF especificado.
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
ms.openlocfilehash: faff00adc25a741342e586adea2f645a62eca36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089067"
---
# <a name="sdbtagreftotagid-function"></a>Função SdbTagRefToTagID

Recupera o **TagId** e um identificador para o banco de dados de Shim para o [**TAGREF**](tagref.md)especificado.

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

*hSDB* \[ no\]
</dt> <dd>

Um identificador para o banco de dados de Shim retornado pela função [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> <dt>

*trWhich* \[ no\]
</dt> <dd>

O [**TAGREF**](tagref.md).

</dd> <dt>

*ppdb* \[ fora\]
</dt> <dd>

O identificador resultante para o banco de dados de Shim.

</dd> <dt>

*ptiWhich* \[ fora\]
</dt> <dd>

O **TagId** resultante.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna **true** em caso de êxito ou **false** em caso de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




