---
description: A função GetFrameRecognizeData retorna uma tabela de estruturas RECOGNIZEDATA. Cada uma dessas estruturas contém um identificador de protocolo e um deslocamento que aponta para o início do protocolo especificado nos dados.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: Função GetFrameRecognizeData (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameRecognizeData
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2b04472e0fee0238677a6592cace0d1c7fbe078635ac85b92ff8922c68da3c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366493"
---
# <a name="getframerecognizedata-function"></a>Função GetFrameRecognizeData

A **função GetFrameRecognizeData** retorna uma tabela de **estruturas RECOGNIZEDATA.** Cada uma dessas estruturas contém um identificador de protocolo e um deslocamento que aponta para o início do protocolo especificado nos dados.

## <a name="syntax"></a>Sintaxe


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ Em\]
</dt> <dd>

Lidar com um quadro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um ponteiro para uma estrutura **RECOGNIZEDATATABLE.**

Se a função não for bem-sucedida, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

[*Especialistas*](e.md) e [*analisadores podem*](p.md) chamar a **função GetFrameRecognizeData.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




