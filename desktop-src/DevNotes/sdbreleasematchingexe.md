---
description: Libera recursos usados pela função SdbGetMatchingExe.
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: Função SdbReleaseMatchingExe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 710874fc0e57775eb6ad1c9c6681a5b74dc66d133b22ce23d2ac0d27270ef7f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044916"
---
# <a name="sdbreleasematchingexe-function"></a>Função SdbReleaseMatchingExe

Libera recursos usados pela função [**SdbGetMatchingExe**](sdbgetmatchingexe.md) .

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSDB* \[ no\]
</dt> <dd>

Um identificador para o banco de dados de Shim retornado pela função [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> <dt>

*trExe* \[ no\]
</dt> <dd>

O [**TAGREF**](tagref.md) retornado por [**SdbGetMatchingExe**](sdbgetmatchingexe.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




