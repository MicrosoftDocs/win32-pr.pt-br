---
description: Inicializa uma tabela de cadeia de caracteres.
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: função pSetupStringTableInitialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitialize
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 67436dd0befbef01c5b6f55a68082b9e23870592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755275"
---
# <a name="psetupstringtableinitialize-function"></a>função pSetupStringTableInitialize

\[Essa função não está disponível no Windows Vista ou no Windows Server 2008.\]

Inicializa uma tabela de cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
