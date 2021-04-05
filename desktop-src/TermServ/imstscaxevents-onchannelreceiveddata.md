---
title: Método IMsTscAxEvents OnChannelReceivedData
description: Chamado quando o cliente recebe dados em um canal virtual programável.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnChannelReceivedData
- Método OnChannelReceivedData Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnChannelReceivedData
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnChannelReceivedData
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1cae4f35435138e219c628dd504c595939adfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085485"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a>Método IMsTscAxEvents:: OnChannelReceivedData

Chamado quando o cliente recebe dados em um canal virtual programável.

## <a name="syntax"></a>Sintaxe


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*canalname* \[ no\]
</dt> <dd>

O nome do canal virtual em que os dados foram recebidos. Esse nome corresponde a um dos canais criados pela chamada para [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md).

</dd> <dt>

*dados* \[ do no\]
</dt> <dd>

Os dados recebidos no canal virtual programável.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Consulte [implementando canais virtuais programáveis usando conexão Web de área de trabalho remota](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) para obter mais informações sobre esse evento.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





