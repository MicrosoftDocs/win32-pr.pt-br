---
description: Traduz a cadeia de caracteres Unicode especificada em uma nova cadeia de caracteres, usando a página de código UTF-8 (Unicode Transformation Format) de 8 bits.
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: Função RtlUnicodeToUTF8N (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUnicodeToUTF8N
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 46153dd152ed5a45a65de50ca214fbb24a6dc2ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089071"
---
# <a name="rtlunicodetoutf8n-function"></a>Função RtlUnicodeToUTF8N

Traduz a cadeia de caracteres Unicode especificada em uma nova cadeia de caracteres, usando a página de código UTF-8 (Unicode Transformation Format) de 8 bits.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI RtlUnicodeToUTF8N(
  _Out_     PCHAR  UTF8StringDestination,
  _In_      ULONG  UTF8StringMaxByteCount,
  _Out_opt_ PULONG UTF8StringActualByteCount,
  _In_      PCWSTR UnicodeStringSource,
  _In_      ULONG  UnicodeStringByteCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UTF8StringDestination* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer alocado pelo chamador para receber a cadeia de caracteres traduzida.

</dd> <dt>

*UTF8StringMaxByteCount* \[ no\]
</dt> <dd>

Número máximo de bytes a serem gravados em *UTF8StringDestination*. Se esse valor fizer com que a cadeia de caracteres traduzida seja truncada, **RtlUnicodeToUTF8N** retornará um status de erro.

</dd> <dt>

*UTF8StringActualByteCount* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável alocada pelo chamador que recebe o comprimento, em bytes, da cadeia de caracteres traduzida. Esse parâmetro é opcional e pode ser **nulo**. Se a cadeia de caracteres for truncada, o número retornado contará a contagem de cadeia de caracteres truncada real.

</dd> <dt>

*UnicodeStringSource* \[ no\]
</dt> <dd>

Um ponteiro para a cadeia de caracteres de origem Unicode a ser traduzido.

</dd> <dt>

* UnicodeStringByteCount * \[ in\]
</dt> <dd>

Especifica o número de bytes na cadeia de caracteres de origem Unicode ao qual o parâmetro *UnicodeStringSource* aponta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**RtlUnicodeToUTF8N** retorna um dos seguintes valores de NTSTATUS:



| Código de retorno                                                                                                  | Descrição                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**STATUS com \_ êxito**</dt> </dl>               | A cadeia de caracteres Unicode foi convertida em UTF-8.<br/>                                                           |
| <dl> <dt>**STATUS \_ alguns \_ não \_ mapeados**</dt> </dl>     | Um caractere de entrada inválido foi encontrado e substituído. Esse status é considerado um status de êxito.<br/> |
| <dl> <dt>**parâmetro de STATUS \_ inválido \_**</dt> </dl>    | Ambos os ponteiros para *UTF8StringDestination* e *UTF8StringActualByteCount* eram **nulos**.<br/>              |
| <dl> <dt>**\_Parâmetro inválido \_ \_ 4 do status**</dt> </dl> | O *UnicodeStringSource* era **nulo**.<br/>                                                              |
| <dl> <dt>**BUFFER de STATUS \_ \_ muito \_ pequeno**</dt> </dl>    | *UTF8StringDestination* foi truncado.<br/>                                                               |



 

## <a name="remarks"></a>Comentários

Embora *UTF8StringActualByteCount* seja opcional e possa ser **NULL**, os chamadores devem fornecer armazenamento para ele, pois o comprimento recebido pode ser usado para determinar se a conversão foi bem-sucedida. Essa rotina não modifica a cadeia de caracteres de origem. Ele retornará uma cadeia de caracteres UTF-8 terminada em nulo se o *UnicodeStringSource* fornecido incluísse um terminador nulo e se o *UTF8StringMaxByteCount* especificado não causar truncamento.

Se a saída estiver truncada e um caractere de entrada inválido for encontrado, a função retornará um erro de buffer de STATUS \_ \_ muito \_ pequeno.

Se *UTF8StringDestination* for definido como **NULL** , a função retornará o número necessário de bytes para hospedar a cadeia de caracteres traduzida sem qualquer truncamento em *UTF8StringActualByteCount*.

Os chamadores de **RtlUnicodeToUTF8N** devem estar em execução em IRQL < nível de expedição \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>WDM. h</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RtlUTF8ToUnicodeN**](rtlutf8tounicoden.md)
</dt> </dl>

 

 




