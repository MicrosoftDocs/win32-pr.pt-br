---
description: Grava um valor DWORD no banco de dados especificado.
ms.assetid: 2ecbfcac-5bb1-4129-9501-79210672aa1b
title: Função SdbWriteDWORDTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 730d171f964205638b44d5676e39abc20fb40426f7721fa6a5060d80c58805a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044786"
---
# <a name="sdbwritedwordtag-function"></a>Função SdbWriteDWORDTag

Grava um valor **DWORD** no banco de dados especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbWriteDWORDTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ DWORD dwData
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

A marca para a entrada. Essa marca deve ser do tipo **marca de tipo \_ \_ DWORD**.

</dd> <dt>

*dwData* \[ no\]
</dt> <dd>

O valor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna **true** em caso de êxito ou **false** em caso de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbWriteBinaryTag**](sdbwritebinarytag.md)
</dt> <dt>

[**SdbWriteQWORDTag**](sdbwriteqwordtag.md)
</dt> <dt>

[**SdbWriteStringTag**](sdbwritestringtag.md)
</dt> <dt>

[**SdbWriteWORDTag**](sdbwritewordtag.md)
</dt> </dl>

 

 




