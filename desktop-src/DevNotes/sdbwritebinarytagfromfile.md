---
description: Grava dados binários do arquivo especificado no banco de dados especificado.
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
ms.openlocfilehash: ec2acf733a870d3dcff57ceb7cdea996c6b6dc1e5d950ec85944285e6ba6cc35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815136"
---
# <a name="sdbwritebinarytagfromfile-function"></a>Função SdbWriteBinaryTagFromFile

Grava dados binários do arquivo especificado no banco de dados especificado.

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

*pdb* \[ Em\]
</dt> <dd>

Um alça para o banco de dados shim.

</dd> <dt>

*tTag* \[ Em\]
</dt> <dd>

A TAG para a entrada. Essa TAG deve ser do tipo **TAG \_ TYPE \_ BINARY**.

</dd> <dt>

*pwszPath* \[ Em\]
</dt> <dd>

O caminho para o arquivo que contém os dados. Esse parâmetro não pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna **TRUE em** caso de êxito **ou FALSE** em caso de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbWriteBinaryTag**](sdbwritebinarytag.md)
</dt> </dl>

 

 




