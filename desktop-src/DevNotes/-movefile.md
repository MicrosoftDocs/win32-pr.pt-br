---
description: Move um arquivo ou diretório existente, incluindo seus filhos.
ms.assetid: 1c533b02-6674-4390-bc49-6420403778a8
title: Função _MoveFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MoveFile
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 44c57d562feff62e21c4c769bfc9d6a650f4984c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756012"
---
# <a name="_movefile-function"></a>\_Função MoveFile

\[Essa função é um wrapper sobre a função **MoveFile** . Essa função pode ser alterada ou não estar disponível no futuro. Os aplicativos devem chamar **MoveFile** diretamente.\]

Move um arquivo ou diretório existente, incluindo seus filhos. Consulte [ **MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)

## <a name="syntax"></a>Sintaxe


```C++
BOOL _MoveFile(
    ...
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)
</dt> </dl>

 

 
