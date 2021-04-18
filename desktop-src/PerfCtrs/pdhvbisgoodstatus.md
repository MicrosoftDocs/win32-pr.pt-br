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
ms.openlocfilehash: d21686be0398a84a57a303ad816b8a25f50aa611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756698"
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

## <a name="return-value"></a>Retornar valor

A função retornará zero se o código de status for um código de status de falha. Ele retornará diferente de zero se o código de status for um código de status de êxito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhVbGetDoubleCounterValue**](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




