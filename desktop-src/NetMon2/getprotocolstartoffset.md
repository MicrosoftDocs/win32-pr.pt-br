---
description: Retorna o deslocamento de um protocolo especificado no quadro.
ms.assetid: bfe5f477-c9de-4bb9-99e5-b8db895b0ae6
title: Função GetProtocolStartOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ff760c4a61cb39ba897351d706c39d240389bf49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757104"
---
# <a name="getprotocolstartoffset-function"></a>Função GetProtocolStartOffset

A função **GetProtocolStartOffset** retorna o deslocamento de um protocolo especificado no quadro.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI GetProtocolStartOffset(
   HFRAME hFrame,
   LPSTR  ProtocolName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* 
</dt> <dd>

Um identificador para o quadro.

</dd> <dt>

*ProtocolName* 
</dt> <dd>

O nome do protocolo, como TCP.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um deslocamento **DWORD** para o início do protocolo que está sendo pesquisado por um valor de retorno igual a zero indicará que o protocolo é o primeiro protocolo no quadro.

Se a função não for bem-sucedida, o protocolo não estará no quadro, o valor de retorno será-1.

## <a name="remarks"></a>Comentários

Quando você recebe o identificador para um quadro, essa função retorna o deslocamento para um protocolo especificado no quadro. Por exemplo, para determinar se o quadro é um quadro DNS, o analisador DNS requer o endereço de porta do protocolo TCP. O analisador DNS chamaria essa função com TCP como o valor de *ProtocolName* . Se o quadro for reconhecido pelo protocolo TCP, o deslocamento da **palavra** do início do quadro até o início do quadro TCP será retornado. Se não houver nenhum protocolo TCP, o valor de retorno será zero.

Essa função localiza o início de um protocolo em um quadro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




