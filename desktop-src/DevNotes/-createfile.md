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
ms.openlocfilehash: becd7fed9e32385409b78e00169191a12b550e3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749062"
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

 

