---
title: Método Conexão IMsTscAx
description: Inicia uma conexão usando as propriedades atualmente definidas no controle .
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- Conexão método Serviços de Área de Trabalho Remota
- Conexão método Serviços de Área de Trabalho Remota , interface IMsTscAx
- Interface IMsTscAx Serviços de Área de Trabalho Remota , Conexão método
- Conexão método Serviços de Área de Trabalho Remota , interface IMsRdpClient
- Interface IMsRdpClient Serviços de Área de Trabalho Remota , Conexão método
- Conexão método Serviços de Área de Trabalho Remota interface , IMsRdpClient2
- Interface IMsRdpClient2 Serviços de Área de Trabalho Remota , Conexão método
- Conexão método Serviços de Área de Trabalho Remota , interface IMsRdpClient3
- Interface IMsRdpClient3 Serviços de Área de Trabalho Remota , Conexão método
- Conexão método Serviços de Área de Trabalho Remota , interface IMsRdpClient4
- Interface IMsRdpClient4 Serviços de Área de Trabalho Remota , Conexão método
- Conexão método Serviços de Área de Trabalho Remota , interface IMsRdpClient5
- Interface IMsRdpClient5 Serviços de Área de Trabalho Remota , Conexão método
- Conexão método Serviços de Área de Trabalho Remota , interface IMsRdpClient6
- Interface IMsRdpClient6 Serviços de Área de Trabalho Remota , Conexão método
- Conexão método Serviços de Área de Trabalho Remota , interface IMsRdpClient7
- Interface IMsRdpClient7 Serviços de Área de Trabalho Remota , Conexão método
- Conexão método Serviços de Área de Trabalho Remota , interface IMsRdpClient8
- Interface IMsRdpClient8 Serviços de Área de Trabalho Remota , Conexão método
- Conexão método Serviços de Área de Trabalho Remota , interface IMsRdpClient9
- Interface IMsRdpClient9 Serviços de Área de Trabalho Remota , Conexão método
topic_type:
- apiref
api_name:
- IMsTscAx.Connect
- IMsRdpClient.Connect
- IMsRdpClient2.Connect
- IMsRdpClient3.Connect
- IMsRdpClient4.Connect
- IMsRdpClient5.Connect
- IMsRdpClient6.Connect
- IMsRdpClient7.Connect
- IMsRdpClient8.Connect
- IMsRdpClient9.Connect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4372b19c9dba51714c6927d5e54468e143033689bfd9c74db78bbff8812e45ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513106"
---
# <a name="imstscaxconnect-method"></a>Método IMsTscAx::Conexão

Inicia uma conexão usando as propriedades atualmente definidas no controle .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Connect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornar **S \_ OK se** for bem-sucedido.

## <a name="remarks"></a>Comentários

A única propriedade necessária é o nome do servidor. Consulte a [**propriedade**](imstscax-server.md) Server.

O controle se conecta de forma assíncrona, portanto, um retorno de uma chamada Conexão indica apenas que a conexão foi iniciada com êxito, não que ela foi concluída. Você deve responder a eventos na interface [**IMsTscAxEvents**](imstscaxevents-interface.md) para determinar quando o controle se conectou com êxito (ou foi desconectado.)

Esse método **retornará E \_ FAIL** se for chamado enquanto o controle já estiver conectado ou no estado de conexão.

Depois **Conexão** tiver sido chamada, a maioria das propriedades de controle não poderá mais ser definida até que o controle retorne ao estado desconectado.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsTscAx é definido como \_ 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



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

[**Desconectar**](imstscax-disconnect.md)
</dt> <dt>

[**Imstscax**](imstscax-interface.md)
</dt> </dl>

 

 





