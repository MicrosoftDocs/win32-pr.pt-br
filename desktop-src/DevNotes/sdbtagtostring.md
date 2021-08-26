---
description: Recupera o nome de exibição do TAG especificado.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: Função SdbTagToString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 22ddb526e332b335e88ecc7aaa770615220f6b0dde838386093e2813fe964e17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044836"
---
# <a name="sdbtagtostring-function"></a>Função SdbTagToString

Recupera o nome de exibição do TAG especificado.

## <a name="syntax"></a>Sintaxe


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tag* \[ Em\]
</dt> <dd>

A TAG.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna um ponteiro para a cadeia de caracteres terminada em nulo ou "InvalidTag".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tag**](tag.md)
</dt> </dl>

 

 




