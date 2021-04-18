---
description: Essa API destina-se somente ao uso interno e não deve ser usada em seu código.
ms.assetid: 836A7515-8C22-4032-9E99-F89B32C21685
title: Função ApiSetQueryApiSetPresence (Apiquery. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApiSetQueryApiSetPresence
api_type:
- DllExport
api_location:
- api-ms-win-core-apiquery-l1-1-0.dll
- ntdll.dll
ms.openlocfilehash: 738a69b0d08f7e619dbd64229d0c13b2ae7dfaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756128"
---
# <a name="apisetqueryapisetpresence-function"></a>Função ApiSetQueryApiSetPresence

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Essa API destina-se somente ao uso interno e não deve ser usada em seu código.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI ApiSetQueryApiSetPresence(
  _In_  PCUNICODE_STRING Namespace,
  _Out_ PBOOLEAN         Present
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Namespace* \[ do no\]
</dt> <dd></dd> <dt>

*Presente* \[ fora\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                                                                                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                                                                                                                  |
| parâmetro<br/>                   | <dl> <dt>Apiquery. h</dt> </dl>                                                                                                                 |
| Biblioteca<br/>                  | <dl> <dt>API-MS-Win-Core-apiquery-L1. lib; </dt> <dt>API-MS-Win-Core-apiquery-L1-1-0. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt> </dl>                                                                                        |



 

 




