---
description: A função ExpertSubmitEvent indica que existe uma condição de evento e fornece uma estrutura de dados que descreve a condição.
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: Função ExpertSubmitEvent (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertSubmitEvent
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b6ce73d378e4d8432459a23a76b30ebf4d558a5f82ec230e6841eeeb621aed13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744216"
---
# <a name="expertsubmitevent-function"></a>Função ExpertSubmitEvent

A função **ExpertSubmitEvent** indica que existe uma condição de evento e fornece uma estrutura de dados que descreve a condição.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hExpertKey* \[ no\]
</dt> <dd>

Identificador exclusivo do especialista. Monitor de Rede passa *hExpertKey* para o especialista ao chamar a função [Run](run.md) .

</dd> <dt>

*pExpertEvent* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura **NMEVENTDATA** que descreve a condição do evento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno indicará o motivo da falha. Se o valor de retorno for NMERR \_ expert \_ Finalize, o especialista limpará e retornará imediatamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




