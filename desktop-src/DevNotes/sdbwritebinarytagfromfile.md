---
description: Grava dados binários do arquivo especificado no banco de dado especificado.
ms.assetid: 960633a8-5cec-462b-b7dc-72eb3e4fd0a2
title: Função SdbWriteBinaryTagFromFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTagFromFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75b45a935fd9630afcefe8f7d30338a6ad6b10a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920261"
---
# <a name="sdbwritebinarytagfromfile-function"></a>Função SdbWriteBinaryTagFromFile

Grava dados binários do arquivo especificado no banco de dado especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbWriteBinaryTagFromFile(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PDB* \[ no\]
</dt> <dd>

Um identificador para o banco de dados de Shim.

</dd> <dt>

*tTag* \[ no\]
</dt> <dd>

A marca para a entrada. Essa marca deve ser do tipo **tipo de marca \_ \_ Binary**.

</dd> <dt>

*pwszPath* \[ no\]
</dt> <dd>

O caminho para o arquivo que contém os dados. Este parâmetro não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna **true** em caso de êxito ou **false** em caso de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbWriteBinaryTag**](sdbwritebinarytag.md)
</dt> </dl>

 

 




