---
title: Tipos de dados simples de ADSI (IADs. h)
description: As interfaces de serviço Active Directory (ADSI) definem e usam os seguintes tipos de dados simples.
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5530fda2ca1f4fe967eaf376b668a0bedc29c4b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009006"
---
# <a name="adsi-simple-data-types"></a>Tipos de dados simples de ADSI

As interfaces de serviço Active Directory (ADSI) definem e usam os seguintes tipos de dados simples.


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

**\_booliano do ADS**
</dt> <dd>

DWORD

</dd> <dt>

**\_cadeia de \_ caracteres exata do caso ADS \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_cadeia de \_ caracteres de ignorar caso de anúncios \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**Cadeia de caracteres de \_ DN do ADS \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_número inteiro de ADS**
</dt> <dd>

DWORD

</dd> <dt>

**\_inteiro grande do ADS \_**
</dt> <dd>

[**\_inteiro grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

**\_cadeia de \_ caracteres numérica ADS**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_classe de objeto ADS \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_cadeia de caracteres imprimíveis do ADS \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_identificador de pesquisa do ADS \_**
</dt> <dd>

PROCESSAMENTO

</dd> <dt>

**\_hora UTC do ADS \_**
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando a ADSI lê um atributo que foi definido como um **inteiro** no esquema LDAP, ele sempre tratará o inteiro como um valor de 32 bits e poderá truncar os dados. Isso é apenas uma preocupação para servidores LDAP que permitem valores inteiros de tamanho arbitrário. Se o atributo for um atributo personalizado definido pela extensão do esquema, esse problema poderá ser evitado definindo o atributo personalizado como uma cadeia de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                    |
| parâmetro<br/>                   | <dl> <dt>IADs. h</dt> </dl> |



 

