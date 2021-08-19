---
description: Cria ou abre um arquivo.
ms.assetid: 2a993f45-7f87-4b9e-bccc-277477558d3c
title: Função _CreateFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _CreateFile
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 8ff69057397fd887d4c7489c350579e7c3a31e432c3716b3107fc483315376fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956755"
---
# <a name="_createfile-function"></a>\_Função CreateFile

\[Essa função é um wrapper sobre a função **CreateFile** . Essa função pode ser alterada ou não estar disponível no futuro. Os aplicativos devem chamar **CreateFile** diretamente.\]

Cria ou abre um arquivo. Consulte [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea).

## <a name="syntax"></a>Sintaxe


```C++
BOOL _CreateFile(
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

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> </dl>

 

