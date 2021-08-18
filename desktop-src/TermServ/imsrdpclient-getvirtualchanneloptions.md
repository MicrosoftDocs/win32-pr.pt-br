---
title: Método GetVirtualChannelOptions de IMsRdpClient
description: Recupera as opções definidas para um canal virtual.
ms.assetid: d2ec9fb2-c0dc-49f1-a86b-d7abca13a322
ms.tgt_platform: multiple
keywords:
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota interface , IMsRdpClient
- Interface IMsRdpClient Serviços de Área de Trabalho Remota , método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota interface , IMsRdpClient2
- Interface IMsRdpClient2 Serviços de Área de Trabalho Remota , método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota interface , IMsRdpClient3
- Interface IMsRdpClient3 Serviços de Área de Trabalho Remota , método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota interface , IMsRdpClient4
- Interface IMsRdpClient4 Serviços de Área de Trabalho Remota , método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota interface , IMsRdpClient5
- Interface IMsRdpClient5 Serviços de Área de Trabalho Remota , método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota interface , IMsRdpClient6
- Interface IMsRdpClient6 Serviços de Área de Trabalho Remota , método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota interface , IMsRdpClient7
- Interface IMsRdpClient7 Serviços de Área de Trabalho Remota , método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota interface , IMsRdpClient8
- Interface IMsRdpClient8 Serviços de Área de Trabalho Remota , método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota interface , IMsRdpClient9
- Interface IMsRdpClient9 Serviços de Área de Trabalho Remota , método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota interface , IMsRdpClient10
- Interface IMsRdpClient10 Serviços de Área de Trabalho Remota , método GetVirtualChannelOptions
topic_type:
- apiref
api_name:
- IMsRdpClient.GetVirtualChannelOptions
- IMsRdpClient2.GetVirtualChannelOptions
- IMsRdpClient3.GetVirtualChannelOptions
- IMsRdpClient4.GetVirtualChannelOptions
- IMsRdpClient5.GetVirtualChannelOptions
- IMsRdpClient6.GetVirtualChannelOptions
- IMsRdpClient7.GetVirtualChannelOptions
- IMsRdpClient8.GetVirtualChannelOptions
- IMsRdpClient9.GetVirtualChannelOptions
- IMsRdpClient10.GetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d51ad6ccd1924c78817f76f385d65e1963b68c1b1329c3d6ba924f25a827a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059084"
---
# <a name="imsrdpclientgetvirtualchanneloptions-method"></a>Método IMsRdpClient::GetVirtualChannelOptions

Recupera as opções definidas para um canal virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetVirtualChannelOptions(
  [in]  BSTR ChanName,
  [out] LONG *pChanOptions
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ChanName* \[ Em\]
</dt> <dd>

O nome de um canal virtual que foi especificado na chamada para [**o método CreateVirtualChannels.**](imstscax-createvirtualchannels.md)

</dd> <dt>

*pChanOptions* \[ out\]
</dt> <dd>

As opções definidas para o canal virtual especificado pelo *parâmetro ChanName.* Para ver uma descrição das opções possíveis, consulte [**CHANNEL \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar **S \_ OK se** for bem-sucedido.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient é definido como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Imsrdpclient**](imsrdpclient-interface.md)
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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**CHANNEL \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)
</dt> </dl>

 

 





