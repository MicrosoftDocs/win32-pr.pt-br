---
title: Método IMsTscAx SendOnVirtualChannel
description: Envia dados para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) por meio de um canal virtual que foi criado anteriormente usando o método CreateVirtualChannels.
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método SendOnVirtualChannel
topic_type:
- apiref
api_name:
- IMsTscAx.SendOnVirtualChannel
- IMsRdpClient.SendOnVirtualChannel
- IMsRdpClient2.SendOnVirtualChannel
- IMsRdpClient3.SendOnVirtualChannel
- IMsRdpClient4.SendOnVirtualChannel
- IMsRdpClient5.SendOnVirtualChannel
- IMsRdpClient6.SendOnVirtualChannel
- IMsRdpClient7.SendOnVirtualChannel
- IMsRdpClient8.SendOnVirtualChannel
- IMsRdpClient9.SendOnVirtualChannel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03c5b84ff9cb272d5560f3b6588301a05a3e9a003db1b28f841a77b2e0618b37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125296"
---
# <a name="imstscaxsendonvirtualchannel-method"></a>Método IMsTscAx:: SendOnVirtualChannel

Envia dados para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) por meio de um canal virtual que foi criado anteriormente usando o método [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Canalname* \[ no\]
</dt> <dd>

O nome do canal virtual que foi especificado na chamada para [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).

</dd> <dt>

*ChanData* \[ no\]
</dt> <dd>

Os dados a serem enviados pelo canal virtual, na forma **BSTR** . Não há nenhuma restrição de que esses dados devem ser cadeias de caracteres terminadas em nulo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

Consulte [registro de cliente de canal virtual](virtual-channel-client-registration.md) para obter informações sobre restrições de nomenclatura de canal virtual.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





