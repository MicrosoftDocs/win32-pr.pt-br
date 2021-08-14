---
description: A função CompareFrameDestAddress compara um endereço com o endereço de destino de um quadro.
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: Função CompareFrameDestAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 153d1a5768791a33fd4f7629e071a125a4ee2ee46feaae366e2c1a21d8118f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367384"
---
# <a name="compareframedestaddress-function"></a>Função CompareFrameDestAddress

A função **CompareFrameDestAddress** compara um endereço com o endereço de destino de um quadro.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CompareFrameDestAddress(
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

## <a name="return-value"></a>Valor retornado

Se os endereços forem iguais, o valor de retorno será **true**.

Se os endereços não forem iguais, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

Para que a função **CompareFrameDestAddress** seja retornada com êxito, o tipo de endereço de destino deve corresponder ao tipo de endereço especificado no parâmetro *lpAddress* .

Monitor de Rede fornece duas outras funções, [CompareFrameSourceAddress](compareframesourceaddress.md) e [CompareAddresses](compareaddresses.md), que você pode usar para comparar endereços. A função **CompareFrameSourceAddress** compara um determinado endereço com o endereço de origem do quadro e a função **CompareAddress** compara dois endereços fornecidos.

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **CompareFrameDestAddress** .

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

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




