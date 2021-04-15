---
description: Exclui uma tabela de cadeia de caracteres.
ms.assetid: a3ac1672-f898-44a0-bb7b-64ac24bdb9bf
title: função pSetupStringTableDestroy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableDestroy
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 472ee152d98c064edb8bac5d4de849b505b634da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753681"
---
# <a name="psetupstringtabledestroy-function"></a>função pSetupStringTableDestroy

\[Essa função não está disponível no Windows Vista ou no Windows Server 2008.\]

Exclui uma tabela de cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI pSetupStringTableDestroy(
  _In_ PVOID StringTable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*STRINGTABLE* \[ no\]
</dt> <dd>

Um ponteiro para a tabela de cadeia de caracteres.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
