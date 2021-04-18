---
description: Obtém o nome do computador.
ms.assetid: 8b6fd61a-dd5a-46b8-920e-cc8a848732b6
title: Função _GetComputerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetComputerName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: a8fc124e9a5b036e1be83e49e504d2a4d42ea27a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749060"
---
# <a name="_getcomputername-function"></a>\_Função GetComputerName

\[Essa função é um wrapper sobre a função **GetComputerName** . Essa função pode ser alterada ou não estar disponível no futuro. Os aplicativos devem chamar **Getcomputernamename** diretamente.\]

Obtém o nome do computador. Consulte [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).

## <a name="syntax"></a>Sintaxe


```C++
BOOL _GetComputerName(
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

[**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> </dl>

 

 
