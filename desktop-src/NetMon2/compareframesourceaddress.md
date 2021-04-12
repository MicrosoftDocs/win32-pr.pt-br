---
description: A função CompareFrameSourceAddress compara um endereço com o endereço de origem de um quadro.
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: Função CompareFrameSourceAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a100273c37e25a7b1deba86ed2704886dbfccc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170827"
---
# <a name="compareframesourceaddress-function"></a>Função CompareFrameSourceAddress

A função **CompareFrameSourceAddress** compara um endereço com o endereço de origem de um quadro.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CompareFrameSourceAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Identificador para um quadro.

</dd> <dt>

*lpAddress* \[ no\]
</dt> <dd>

Ponteiro para um endereço.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se os endereços forem iguais, o valor de retorno será **true**.

Se os endereços não forem iguais, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

Para que a função **CompareFrameSourceAddress** tenha sucesso, o tipo de endereço de origem deve corresponder ao tipo de endereço especificado no parâmetro *lpAddress* .

Monitor de Rede fornece duas outras funções para comparar endereços: [CompareFrameDestAddress](compareframedestaddress.md) e [CompareAddresses](compareaddresses.md). A função **CompareFrameDestAddress** compara um determinado endereço com o endereço de destino do quadro e a função **CompareAddress** compara dois endereços fornecidos.

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **CompareFrameSourceAddress** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[CompareAddresses](compareaddresses.md)
</dt> <dt>

[CompareFrameDestAddress](compareframedestaddress.md)
</dt> </dl>

 

 




