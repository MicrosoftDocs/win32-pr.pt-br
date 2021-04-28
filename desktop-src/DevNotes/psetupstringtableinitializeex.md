---
description: função pSetupStringTableInitializeEx – Inicializa uma tabela de cadeia de caracteres.
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: função pSetupStringTableInitializeEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 78ee96e7e366fdff821e8202300ff28de0a14af3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096644"
---
# <a name="psetupstringtableinitializeex-function"></a>função pSetupStringTableInitializeEx

\[Essa função não está disponível no Windows Vista ou no Windows Server 2008.\]

Inicializa uma tabela de cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ExtraDataSize* \[ no\]
</dt> <dd>

Tamanho do objeto de dados extra.

</dd> <dt>

*Reservado* \[ para no\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
