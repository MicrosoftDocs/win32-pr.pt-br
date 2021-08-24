---
description: Converte a cadeia de caracteres Unicode especificada em uma nova cadeia de caracteres, usando a página de código formato de transformação Unicode de 8 bits (UTF-8).
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: Função RtlUnicodeToUTF8N (Wdm.h)
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
ms.openlocfilehash: 3580eb86deba77bcc214cf69fbd21f65fee2735ef3a5ff73319b415d2c814d88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538026"
---
# <a name="rtlunicodetoutf8n-function"></a>Função RtlUnicodeToUTF8N

Converte a cadeia de caracteres Unicode especificada em uma nova cadeia de caracteres, usando a página de código formato de transformação Unicode de 8 bits (UTF-8).

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

*UTF8StringDestination* \[ out\]
</dt> <dd>

Um ponteiro para um buffer alocado pelo chamador para receber a cadeia de caracteres traduzida.

</dd> <dt>

*UTF8StringMaxByteCount* \[ Em\]
</dt> <dd>

Número máximo de bytes a serem gravados *em UTF8StringDestination.* Se esse valor faz com que a cadeia de caracteres traduzida seja truncada, **RtlUnicodeToUTF8N** retornará um status de erro.

</dd> <dt>

*UTF8StringActualByteCount* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável alocada pelo chamador que recebe o comprimento, em bytes, da cadeia de caracteres traduzida. Esse parâmetro é opcional e pode ser **NULL.** Se a cadeia de caracteres for truncada, o número retornado contará a contagem real de cadeias de caracteres truncadas.

</dd> <dt>

*UnicodeStringSource* \[ Em\]
</dt> <dd>

Um ponteiro para a cadeia de caracteres de origem Unicode a ser traduzida.

</dd> <dt>

*UnicodeStringByteCount * \[ em\]
</dt> <dd>

Especifica o número de bytes na cadeia de caracteres de origem Unicode para o que o *parâmetro UnicodeStringSource* aponta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**RtlUnicodeToUTF8N** retorna um dos seguintes valores NTSTATUS:



| Código de retorno                                                                                                  | Descrição                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**STATUS \_ ÊXITO**</dt> </dl>               | A cadeia de caracteres Unicode foi convertida em UTF-8.<br/>                                                           |
| <dl> <dt>**STATUS \_ ALGUNS \_ NÃO \_ MAPEADOS**</dt> </dl>     | Um caractere de entrada inválido foi encontrado e substituído. Esse status é considerado um status de êxito.<br/> |
| <dl> <dt>**STATUS \_ PARÂMETRO \_ INVÁLIDO**</dt> </dl>    | Ambos os ponteiros *para UTF8StringDestination* e *UTF8StringActualByteCount* eram **NULL.**<br/>              |
| <dl> <dt>**STATUS \_ PARÂMETRO \_ INVÁLIDO \_ 4**</dt> </dl> | O *UnicodeStringSource* era **NULL.**<br/>                                                              |
| <dl> <dt>**BUFFER \_ DE STATUS MUITO \_ \_ PEQUENO**</dt> </dl>    | *UTF8StringDestination* foi truncado.<br/>                                                               |



 

## <a name="remarks"></a>Comentários

Embora *UTF8StringActualByteCount* seja opcional e possa ser **NULL,** os chamadores devem fornecer armazenamento para ele, pois o comprimento recebido pode ser usado para determinar se a conversão foi bem-sucedida. Essa rotina não modifica a cadeia de caracteres de origem. Ele retornará uma cadeia de caracteres UTF-8 terminada em nulo se *o UnicodeStringSource* determinado incluir um terminador NULL e se o *UTF8StringMaxByteCount* determinado não tiver causado truncamento.

Se a saída for truncada e um caractere de entrada inválido for encontrado, a função retornará o erro \_ BUFFER DE STATUS MUITO \_ \_ PEQUENO.

Se *UTF8StringDestination* for definido como **NULL,** a função retornará o número necessário de bytes para hospedar a cadeia de caracteres traduzida sem nenhum truncamento *em UTF8StringActualByteCount.*

Os chamadores **de RtlUnicodeToUTF8N** devem estar em execução em IRQL < DISPATCH \_ LEVEL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Wdm.h</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RtlUTF8ToUnicodeN**](rtlutf8tounicoden.md)
</dt> </dl>

 

 




