---
title: Método IMsTscAxEvents OnNetworkStatusChanged
description: Chamado quando o status da rede é alterado. | Método IMsTscAxEvents OnNetworkStatusChanged
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnNetworkStatusChanged
- Método OnNetworkStatusChanged Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b9bdcd7774493fcc54e1390ad199a6a56a7c51
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105756808"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a>Método IMsTscAxEvents:: OnNetworkStatusChanged

Chamado quando o status da rede é alterado.

## <a name="syntax"></a>Sintaxe


```C++
void OnNetworkStatusChanged(
  [in] ULONG qualityLevel,
  [in] LONG  bandwidth,
  [in] LONG  rtt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*qualityLevel* \[ no\]
</dt> <dd>

Especifica a nova velocidade de conexão. Esse será um dos valores a seguir.

<dt>

1
</dt> <dd>

Menos de 512 quilobytes por segundo (KBps).

</dd> <dt>

2
</dt> <dd>

512 a 1.999 KBps.

</dd> <dt>

3
</dt> <dd>

2.000 a 9.999 KBps.

</dd> <dt>

4
</dt> <dd>

Maior ou igual a 10.000 KBps.

</dd> </dl> </dd> <dt>

*largura de banda* \[ no\]
</dt> <dd>

Especifica a largura de banda da conexão.

</dd> <dt>

*RTT* \[ no\]
</dt> <dd>

Especifica a latência de conexão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





