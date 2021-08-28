---
description: Obtém o endereço de uma função de uma DLL.
ms.assetid: e425948c-5588-4a4f-994c-4e608af18439
title: Função _GetProcAddress_
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetProcAddress_
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d35d623ff7c7873534bd835c138dba490274e5caddf839fc71765cda59b9f00f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053196"
---
# <a name="_getprocaddress_-function"></a>\_\_Função GetProcAddress

\[Essa função é um wrapper sobre a função **GetProcAddress** . Essa função pode ser alterada ou não estar disponível no futuro. Os aplicativos devem chamar o **GetProcAddress** diretamente.\]

Obtém o endereço de uma função de uma DLL. Consulte [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).

## <a name="syntax"></a>Sintaxe


```C++
FARPROC _GetProcAddress_(
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

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 
