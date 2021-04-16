---
description: A função CompareAddresses compara dois endereços, indicando que um dos endereços é maior que, menor ou igual ao outro endereço.
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: Função CompareAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fd72ef0281615c0b56176e86ee9bb3659b498a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758943"
---
# <a name="compareaddresses-function"></a>Função CompareAddresses

A função **CompareAddresses** compara dois endereços, indicando que um dos endereços é maior que, menor ou igual ao outro endereço.

## <a name="syntax"></a>Sintaxe


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpAddress1* \[ no\]
</dt> <dd>

Ponteiro para o primeiro endereço.

</dd> <dt>

*lpAddress2* \[ no\]
</dt> <dd>

Ponteiro para o segundo endereço.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se os endereços forem iguais, a função retornará zero.

Se o parâmetro *lpAddress1* especificar um endereço menor que o endereço especificado pelo parâmetro *lpAddress2* , o valor de retorno será um número negativo.

Se o parâmetro *lpAddress1* especificar um endereço maior do que o endereço especificado pelo parâmetro *lpAddress2* , o valor de retorno será um número positivo.

## <a name="remarks"></a>Comentários

Um endereço menor que outro endereço indica um quadro anterior. Um endereço maior que outro endereço indica um quadro posterior.

Monitor de Rede fornece duas outras funções, [CompareFrameDestAddress](compareframedestaddress.md) e [CompareFrameSourceAddress](compareframesourceaddress.md), que você pode usar para comparar endereços. A função **CompareFrameDestAddress** compara um determinado endereço com o endereço de destino do quadro e a função **CompareFrameSourceAddress** compara um determinado endereço com o endereço de origem do quadro.

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

[CompareFrameDestAddress](compareframedestaddress.md)
</dt> <dt>

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




