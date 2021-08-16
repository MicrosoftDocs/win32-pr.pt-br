---
description: A função GetCaptureTimeStamp retorna a hora e a data em que a captura começou a gravar quadros.
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: Função GetCaptureTimeStamp (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 93ae1c94a5e83d0029aba4403ad4ba23db0f4006bb5b9be68cc469939e63c734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366631"
---
# <a name="getcapturetimestamp-function"></a>Função GetCaptureTimeStamp

A **função GetCaptureTimeStamp** retorna a hora e a data em que a captura começou a gravar quadros.

## <a name="syntax"></a>Sintaxe


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hCapture* \[ Em\]
</dt> <dd>

Lidar com a captura. Para obter informações sobre como obter o alça de captura, consulte a seção Comentários deste **tópico GetCaptureTimeStamp.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um ponteiro para uma [estrutura SYSTEMTIME.](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

Se a função não for bem-sucedida, o valor de retorno será **NULL.**

## <a name="remarks"></a>Comentários

A **função GetCaptureTimeStamp** retorna a hora em que o NPP (Provedor de Pacotes de Rede) começa a coletar dados, não quando o especialista carrega a captura para análise.

Não substituir os dados na estrutura **SYSTEMTIME.** Os dados fazem parte da captura. Tentar modificar os dados causa uma violação de acesso.

[*Especialistas*](e.md) e [*analisadores podem*](p.md) chamar a **função GetCaptureTimeStamp.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Systemtime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

