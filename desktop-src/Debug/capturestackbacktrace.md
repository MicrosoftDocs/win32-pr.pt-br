---
UID: ''
title: Função CaptureStackBackTrace
description: Captura um rastreamento de voltar da pilha, a caminho da pilha.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: RtlCaptureStackBackTrace
ms.topic: reference
req.header: WinBase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-rtlsupport-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-rtlsupport-l1-1-0.dll
api_name:
- CaptureStackBackTrace
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0b6cad22d7a52908c3aa02bef7e23a57899e421f87bda00660519750de742919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279497"
---
# <a name="capturestackbacktrace-function"></a>Função CaptureStackBackTrace

## <a name="description"></a>Description

Captura um rastreamento de voltar da pilha, a caminho da pilha e registrando as informações de cada quadro.

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a>Parâmetros

### <a name="framestoskip-in"></a>FramesToSkip [in]

O número de quadros a ignorar desde o início do rastreamento de fundo.

### <a name="framestocapture-in"></a>FramesToCapture [in]

O número de quadros a serem capturados.
Você pode capturar até **quadros MAXUSHORT.**

**Windows Server 2003 e Windows XP:**  A soma dos *parâmetros FramesToSkip* e *FramesToCapture* deve ser menor que 63.

### <a name="backtrace-out"></a>BackTrace [out]

Uma matriz de ponteiros capturados do rastreamento de pilha atual.

### <a name="backtracehash-out-optional"></a>BackTraceHash [out, optional]

Um valor que pode ser usado para organizar tabelas de hash.
Se esse parâmetro for **NULL,** nenhum valor de hash será computado.

Esse valor é calculado com base nos valores dos ponteiros retornados na matriz BackTrace.
Dois rastreamentos de pilha idênticos gerarão valores de hash idênticos.

## <a name="returns"></a>Retornos

O número de quadros capturados.

## <a name="remarks"></a>Comentários

A **função CaptureStackBackTrace** é definida como a função **RtlCaptureStackBackTrace** (a definição é incluída no SDK do Windows a partir do Windows Vista).
Para obter mais informações, consulte WinBase.h e WinNT.h.

## <a name="see-also"></a>Confira também
