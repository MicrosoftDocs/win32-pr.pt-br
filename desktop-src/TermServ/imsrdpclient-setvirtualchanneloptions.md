---
title: Método IMsRdpClient SetVirtualChannelOptions
description: define as opções de canal virtual para o controle de ActiveX de Área de Trabalho Remota.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método SetVirtualChannelOptions
topic_type:
- apiref
api_name:
- IMsRdpClient.SetVirtualChannelOptions
- IMsRdpClient2.SetVirtualChannelOptions
- IMsRdpClient3.SetVirtualChannelOptions
- IMsRdpClient4.SetVirtualChannelOptions
- IMsRdpClient5.SetVirtualChannelOptions
- IMsRdpClient6.SetVirtualChannelOptions
- IMsRdpClient7.SetVirtualChannelOptions
- IMsRdpClient8.SetVirtualChannelOptions
- IMsRdpClient9.SetVirtualChannelOptions
- IMsRdpClient10.SetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 804d4bde2fec9cb6273cc78f79d733f61a08772746439aa1cbb6e7b2d3c29716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871576"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a>Método IMsRdpClient:: SetVirtualChannelOptions

define as opções de canal virtual para o controle de ActiveX de Área de Trabalho Remota.

chame esse método depois de chamar o método [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) , mas antes de estabelecer uma conexão com o método [**Conexão**](imstscax-connect.md) . Esse método define opções adicionais em canais virtuais que foram criados com **CreateVirtualChannels**.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Canalname* \[ no\]
</dt> <dd>

O nome do canal virtual que foi especificado na chamada para o método [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .

</dd> <dt>

*canal* \[ no\]
</dt> <dd>

As opções a serem definidas para o canal virtual especificado pelo parâmetro de *canal* . Para obter uma descrição das opções possíveis, confira [**\_ definição de canal**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def). Para obter mais informações, consulte a seção Comentários a seguir.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

Um exemplo de como usar esse método seria declarar o canal como controle remoto persistente, definindo a **opção de canal sinalizador \_ \_ \_ \_ persistente de controle remoto** . Isso significa que o canal não seria fechado quando um controle remoto se conecta ou desconecta da sessão conectada ao cliente. Para obter mais informações, consulte [controle remoto de canais virtuais persistentes](remote-control-persistent-virtual-channels.md).

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**DEF. de canal \_**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





