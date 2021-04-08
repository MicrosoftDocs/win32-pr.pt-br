---
description: A função GetFrameRecognizeData retorna uma tabela de estruturas RECOGNIZEDATA. Cada uma dessas estruturas contém um identificador de protocolo e um deslocamento que aponta para o início do protocolo especificado nos dados.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: Função GetFrameRecognizeData (Netmon. h)
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
ms.openlocfilehash: 627ba046b3adead0291239f5d94f4e56958e6a80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920696"
---
# <a name="getframerecognizedata-function"></a>Função GetFrameRecognizeData

A função **GetFrameRecognizeData** retorna uma tabela de estruturas **RECOGNIZEDATA** . Cada uma dessas estruturas contém um identificador de protocolo e um deslocamento que aponta para o início do protocolo especificado nos dados.

## <a name="syntax"></a>Sintaxe


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Identificador para um quadro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um ponteiro para uma estrutura **RECOGNIZEDATATABLE** .

Se a função não for bem-sucedida, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrameRecognizeData** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




