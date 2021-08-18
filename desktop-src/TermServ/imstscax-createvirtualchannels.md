---
title: Método IMsTscAx CreateVirtualChannels
description: Cria um objeto de canal virtual do lado do cliente para cada nome de canal virtual especificado.
ms.assetid: 3afd2f1c-abd5-4f85-93fb-6d1173f09b07
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método CreateVirtualChannels
topic_type:
- apiref
api_name:
- IMsTscAx.CreateVirtualChannels
- IMsRdpClient.CreateVirtualChannels
- IMsRdpClient2.CreateVirtualChannels
- IMsRdpClient3.CreateVirtualChannels
- IMsRdpClient4.CreateVirtualChannels
- IMsRdpClient5.CreateVirtualChannels
- IMsRdpClient6.CreateVirtualChannels
- IMsRdpClient7.CreateVirtualChannels
- IMsRdpClient8.CreateVirtualChannels
- IMsRdpClient9.CreateVirtualChannels
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d3ef4e7c8471c655d4ecfaf54a1c4b0f35b2362c67c334bd94e57da8e99d390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138479"
---
# <a name="imstscaxcreatevirtualchannels-method"></a>Método IMsTscAx:: CreateVirtualChannels

Cria um objeto de canal virtual do lado do cliente para cada nome de canal virtual especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateVirtualChannels(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ no\]
</dt> <dd>

Uma lista separada por vírgulas de nomes de canais virtuais válidos. O comprimento de cada nome nessa lista pode ser um mínimo de um e um máximo de sete caracteres alfabéticos. O comprimento de toda a cadeia de caracteres pode ser um mínimo de um e um máximo de 300 caracteres alfabéticos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se for bem-sucedido. Retorna **E \_ INVALIDARG** se o parâmetro passado não atender aos critérios especificados.

## <a name="remarks"></a>Comentários

chame esse método antes de chamar o método [**Conexão**](imstscax-connect.md) .

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

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





