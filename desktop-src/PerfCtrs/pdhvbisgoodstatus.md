---
description: A função PdhVbIsGoodStatus testa um valor de status para determinar se ele é um código de êxito ou de falha. Se o valor de status for bem-sucedido, o valor de retorno será diferente de zero. Se for um código de status de falha, o valor de retorno será zero.
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: Função PdhVbIsGoodStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbIsGoodStatus
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: e0b142da988143d7304a6b9b01bc5163e741fdaff77d7e0d796882607fc73044
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683766"
---
# <a name="pdhvbisgoodstatus-function"></a>Função PdhVbIsGoodStatus

A função **PdhVbIsGoodStatus** testa um valor de status para determinar se ele é um código de êxito ou de falha. Se o valor de status for bem-sucedido, o valor de retorno será diferente de zero. Se for um código de status de falha, o valor de retorno será zero.

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).

Função PdhVbIsGoodStatus ( \_ ByVal statusvalue como longo \_ ) enquanto longo

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Statusvalue* 
</dt> <dd>

Valor de status retornado por outra função PDH a ser testada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retornará zero se o código de status for um código de status de falha. Ele retornará diferente de zero se o código de status for um código de status de êxito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhVbGetDoubleCounterValue**](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




