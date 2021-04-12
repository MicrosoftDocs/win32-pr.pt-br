---
description: Compara duas cadeias de caracteres Unicode para determinar se uma cadeia é um prefixo da outra.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: Função RtlPrefixUnicodeString (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlPrefixUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 47382daab1bac5e71098f79a601d89255f1cf0e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456978"
---
# <a name="rtlprefixunicodestring-function"></a>Função RtlPrefixUnicodeString

Compara duas cadeias de caracteres Unicode para determinar se uma cadeia é um prefixo da outra.

## <a name="syntax"></a>Sintaxe


```C++
BOOLEAN RtlPrefixUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Seqüência1* \[ no\]
</dt> <dd>

Ponteiro para a primeira cadeia de caracteres, que pode ser um prefixo da cadeia de caracteres Unicode em buffer em *seqüência2*.

</dd> <dt>

*Seqüência2* \[ no\]
</dt> <dd>

Ponteiro para a segunda cadeia de caracteres.

</dd> <dt>

*CaseInSensitive* \[ no\]
</dt> <dd>

Se **for true**, o caso deverá ser ignorado ao fazer a comparação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**True** se *seqüência1* for um prefixo de *seqüência2*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| parâmetro<br/>                   | <dl> <dt>Ntddk. h (incluir Ntddk. h)</dt> </dl>                                    |
| Biblioteca<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RtlCompareUnicodeString**](rtlcompareunicodestring.md)
</dt> </dl>

 

 




