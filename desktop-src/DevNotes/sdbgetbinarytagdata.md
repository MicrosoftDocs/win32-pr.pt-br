---
description: Recupera os dados binários para o TAGID especificado.
ms.assetid: 18992406-67b4-4c48-9629-04d6bf1c5824
title: Função SdbGetBinaryTagData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetBinaryTagData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 028b073b149482b79b848216e44b8a425d6ffb56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762860"
---
# <a name="sdbgetbinarytagdata-function"></a>Função SdbGetBinaryTagData

Recupera os dados binários para o **TagId** especificado.

## <a name="syntax"></a>Sintaxe


```C++
PVOID WINAPI SdbGetBinaryTagData(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PDB* \[ no\]
</dt> <dd>

Um identificador para o banco de dados de Shim.

</dd> <dt>

*tiWhich* \[ no\]
</dt> <dd>

O **TagId** que corresponde aos dados a serem recuperados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retornará um ponteiro para os dados binários ou **nulo** se o **TagId** for inválido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> <dt>

[**SdbReadQWORDTag**](sdbreadqwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 




