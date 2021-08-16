---
description: Traduz a cadeia de caracteres de origem especificada em uma cadeia de caracteres Unicode, usando a página de código UTF-8 (Unicode Transformation Format) de 8 bits.
ms.assetid: 2871a81b-74f9-462e-9e5c-c59d06bb6841
title: Função RtlUTF8ToUnicodeN (WDM. h)
ms.topic: reference
ms.date: 02/21/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUTF8ToUnicodeN
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8d6268857387d4caf4b024eb6dd308ac11349fe839173d307a311bf63ef84b56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119385556"
---
# <a name="rtlutf8tounicoden-function"></a>Função RtlUTF8ToUnicodeN

Traduz a cadeia de caracteres de origem especificada em uma cadeia de caracteres Unicode, usando a página de código UTF-8 (Unicode Transformation Format) de 8 bits.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI RtlUTF8ToUnicodeN(
  _Out_     PWSTR  UnicodeStringDestination,
  _In_      ULONG  UnicodeStringMaxByteCount,
  _Out_opt_ PULONG UnicodeStringActualByteCount,
  _In_      PCCH   UTF8StringSource,
  _In_      ULONG  UTF8StringByteCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UnicodeStringDestination* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer alocado pelo chamador que recebe a cadeia de caracteres traduzida.

</dd> <dt>

*UnicodeStringMaxByteCount* \[ no\]
</dt> <dd>

Número máximo de bytes a serem gravados em *UnicodeStringDestination*. Se esse valor fizer com que a cadeia de caracteres traduzida seja truncada, **RtlUTF8ToUnicodeN** retornará um status de erro.

</dd> <dt>

*UnicodeStringActualByteCount* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável alocada pelo chamador que recebe o comprimento, em bytes, da cadeia de caracteres traduzida. Esse parâmetro é opcional e pode ser **nulo**. Se a cadeia de caracteres for truncada, o número retornado contará a contagem de cadeia de caracteres truncada real.

</dd> <dt>

*UTF8StringSource* \[ no\]
</dt> <dd>

Um ponteiro para a cadeia de caracteres a ser traduzida.

</dd> <dt>

*UTF8StringByteCount* \[ no\]
</dt> <dd>

Tamanho, em bytes, da cadeia de caracteres em *UTF8StringSource*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**RtlUTF8ToUnicodeN** retorna um dos seguintes valores de NTSTATUS:



| Código de retorno                                                                                                  | Description                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**STATUS com \_ êxito**</dt> </dl>               | A cadeia de caracteres foi convertida em Unicode.<br/>                                                                 |
| <dl> <dt>**STATUS \_ alguns \_ não \_ mapeados**</dt> </dl>     | Um caractere de entrada inválido foi encontrado e substituído. Esse status é considerado um status de êxito.<br/> |
| <dl> <dt>**parâmetro de STATUS \_ inválido \_**</dt> </dl>    | Ambos os ponteiros para *UnicodeStringDestination* e *UnicodeStringActualByteCount* eram **nulos**.<br/>       |
| <dl> <dt>**\_Parâmetro inválido \_ \_ 4 do status**</dt> </dl> | O *UTF8StringSource* era **nulo**.<br/>                                                                 |
| <dl> <dt>**BUFFER de STATUS \_ \_ muito \_ pequeno**</dt> </dl>    | *UnicodeStringDestination* foi truncado.<br/>                                                            |



 

## <a name="remarks"></a>Comentários

Embora *UnicodeStringActualByteCount* seja opcional e possa ser **NULL**, os chamadores devem fornecer armazenamento para ele, pois o comprimento recebido pode ser usado para determinar se a conversão foi bem-sucedida.

Se a saída estiver truncada e um caractere de entrada inválido for encontrado, a função retornará um erro de buffer de STATUS \_ \_ muito \_ pequeno.

Se *UnicodeStringDestination* for definido como **NULL** , a função retornará o número necessário de bytes para hospedar a cadeia de caracteres traduzida sem qualquer truncamento em *UnicodeStringActualByteCount*.

**RtlUTF8ToUnicodeN** não modifica a cadeia de caracteres de origem, a menos que os ponteiros *UnicodeStringDestination* e *UTF8StringSource* sejam equivalentes. A cadeia de caracteres Unicode retornada não é terminada em nulo.

Os chamadores de **RtlUTF8ToUnicodeN** devem estar em execução em IRQL < nível de expedição \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>WDM. h</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RtlUnicodeToUTF8N**](rtlunicodetoutf8n.md)
</dt> </dl>

 

 




