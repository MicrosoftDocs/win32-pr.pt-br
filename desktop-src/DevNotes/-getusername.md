---
description: Obtém o nome do usuário.
ms.assetid: 1373fc9d-ab1c-49b9-8b82-de2e99c4821c
title: Função _GetUserName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetUserName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: f61be4596c5076dd7763ed171124888382f3ef6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751756"
---
# <a name="_getusername-function"></a>\_Função GetUserName

\[Essa função é um wrapper sobre a função **GetUserName** . Essa função pode ser alterada ou não estar disponível no futuro. Os aplicativos devem chamar **GetUserName** diretamente.\]

Obtém o nome do usuário. Consulte [**GetUserName**](/windows/win32/api/winbase/nf-winbase-getusernamea).

## <a name="syntax"></a>Sintaxe


```C++
BOOL _GetUserName(
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

[**GetUserName**](/windows/win32/api/winbase/nf-winbase-getusernamea)
</dt> </dl>

 

 
