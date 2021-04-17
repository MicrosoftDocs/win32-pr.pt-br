---
description: Recupera o nome de exibição da marca especificada.
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
ms.openlocfilehash: 5c781db801077bcef001a860c4ff08c4455daff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456975"
---
# <a name="sdbtagtostring-function"></a>Função SdbTagToString

Recupera o nome de exibição da marca especificada.

## <a name="syntax"></a>Sintaxe


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*marca* \[ de no\]
</dt> <dd>

A marca.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna um ponteiro para a cadeia de caracteres terminada em nulo ou "InvalidTag".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tags**](tag.md)
</dt> </dl>

 

 




