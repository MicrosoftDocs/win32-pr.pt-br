---
description: Compara duas cadeias de caracteres Unicode.
ms.assetid: D2703180-946C-4762-AFBA-1E882B01B944
title: Função RtlCompareUnicodeString (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlCompareUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9de12f218c37916c7e30393c0701efcf1889973f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826358"
---
# <a name="rtlcompareunicodestring-function"></a>Função RtlCompareUnicodeString

Compara duas cadeias de caracteres Unicode.

## <a name="syntax"></a>Sintaxe


```C++
LONG RtlCompareUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Seqüência1* \[ no\]
</dt> <dd>

Ponteiro para a primeira cadeia de caracteres.

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

Um valor assinado que fornece os resultados da comparação:



| Código de retorno                                                                               | Descrição                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**Zero**</dt> </dl>       | *Seqüência1* é igual a *seqüência2*.<br/>          |
| <dl> <dt>**< zero**</dt> </dl>  | *Seqüência1* é menor que *seqüência2*.<br/>    |
| <dl> <dt>**> zero**</dt> </dl> | *Seqüência1* é maior que *seqüência2*.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| parâmetro<br/>                   | <dl> <dt>WDM. h (incluindo WDM. h, Ntddk. h ou Ntifs. h)</dt> </dl>                   |
| Biblioteca<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RtlCompareString**](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlcomparestring)
</dt> <dt>

[**RtlEqualString**](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlequalstring)
</dt> </dl>

 

 
