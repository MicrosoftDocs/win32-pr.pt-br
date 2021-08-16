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
ms.openlocfilehash: 67755d96d87530f450627714de7c1526750967b87bdf51901b788662c4534045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827977"
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

 

 
