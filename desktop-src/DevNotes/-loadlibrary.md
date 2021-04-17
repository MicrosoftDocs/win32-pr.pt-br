---
description: Carrega uma biblioteca.
ms.assetid: 191fcbd8-4542-4cad-955e-6951f3005fc5
title: Função _LoadLibrary
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _LoadLibrary
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: ce4502813c1ca2a292486a18f1946f4c605c96cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748518"
---
# <a name="_loadlibrary-function"></a>\_Função LoadLibrary

\[Essa função é um wrapper sobre a função **LoadLibrary** . Essa função pode ser alterada ou não estar disponível no futuro. Os aplicativos devem chamar **LoadLibrary** diretamente.\]

Carrega uma biblioteca. Consulte [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).

## <a name="syntax"></a>Sintaxe


```C++
HMODULE _LoadLibrary(
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

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
