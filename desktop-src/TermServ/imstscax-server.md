---
title: Propriedade do servidor IMsTscAx (Asptlb. h)
description: Especifica o nome do servidor ao qual o controle atual está conectado.
ms.assetid: 81118ddd-2662-47f5-8e9d-9c2a5056820b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de Propriedade do servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, propriedade de servidor
topic_type:
- apiref
api_name:
- IMsTscAx.Server
- IMsTscAx.get_Server
- IMsTscAx.put_Server
- IMsRdpClient.Server
- IMsRdpClient.get_Server
- IMsRdpClient.put_Server
- IMsRdpClient2.Server
- IMsRdpClient2.get_Server
- IMsRdpClient2.put_Server
- IMsRdpClient3.Server
- IMsRdpClient3.get_Server
- IMsRdpClient3.put_Server
- IMsRdpClient4.Server
- IMsRdpClient4.get_Server
- IMsRdpClient4.put_Server
- IMsRdpClient5.Server
- IMsRdpClient5.get_Server
- IMsRdpClient5.put_Server
- IMsRdpClient6.Server
- IMsRdpClient6.get_Server
- IMsRdpClient6.put_Server
- IMsRdpClient7.Server
- IMsRdpClient7.get_Server
- IMsRdpClient7.put_Server
- IMsRdpClient8.Server
- IMsRdpClient8.get_Server
- IMsRdpClient8.put_Server
- IMsRdpClient9.Server
- IMsRdpClient9.get_Server
- IMsRdpClient9.put_Server
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7be04c149e2ac10c1a3e905678bd2b5f663cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918070"
---
# <a name="imstscaxserver-property"></a>Propriedade IMsTscAx:: Server

Especifica o nome do servidor ao qual o controle atual está conectado.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Server(
  [in]  BSTR newVal
);

HRESULT get_Server(
  [out] BSTR *pServer
);
```



## <a name="property-value"></a>Valor da propriedade

O novo nome do servidor. Esse parâmetro pode ser um nome DNS ou endereço IP.

## <a name="error-codes"></a>Códigos do Erro

Se os métodos forem bem-sucedidos, será retornado **S \_ OK** . Qualquer outro valor **HRESULT** indica que a chamada falhou.

## <a name="remarks"></a>Comentários

Essa propriedade deve ser definida antes de chamar o método [**Connect**](imstscax-connect.md) . É a única propriedade que deve ser definida antes da conexão.

Essa propriedade só poderá ser definida se o controle não estiver no estado conectado. Essa propriedade retornará **E \_ falhará** se for chamada quando o controle estiver conectado. Você pode verificar o estado conectado usando a propriedade [**Connected**](imstscax-connected.md) .

Esse método aloca a memória necessária para o buffer apontado pelo parâmetro *pserver* . Chamar aplicativos C/C++ deve liberar a memória com uma chamada para a função [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . Isso não é necessário para clientes de Visual Basic e de script.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>Asptlb. h</dt> </dl>    |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Consulte também

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

 

