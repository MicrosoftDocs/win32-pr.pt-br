---
title: Propriedade de domínio IMsTscAx
description: Especifica o domínio no qual o usuário atual faz logon.
ms.assetid: 5d9a2048-5f5d-43ca-a8b8-400dac7d7472
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, propriedade de domínio
topic_type:
- apiref
api_name:
- IMsTscAx.Domain
- IMsTscAx.get_Domain
- IMsTscAx.put_Domain
- IMsRdpClient.Domain
- IMsRdpClient.get_Domain
- IMsRdpClient.put_Domain
- IMsRdpClient2.Domain
- IMsRdpClient2.get_Domain
- IMsRdpClient2.put_Domain
- IMsRdpClient3.Domain
- IMsRdpClient3.get_Domain
- IMsRdpClient3.put_Domain
- IMsRdpClient4.Domain
- IMsRdpClient4.get_Domain
- IMsRdpClient4.put_Domain
- IMsRdpClient5.Domain
- IMsRdpClient5.get_Domain
- IMsRdpClient5.put_Domain
- IMsRdpClient6.Domain
- IMsRdpClient6.get_Domain
- IMsRdpClient6.put_Domain
- IMsRdpClient7.Domain
- IMsRdpClient7.get_Domain
- IMsRdpClient7.put_Domain
- IMsRdpClient8.Domain
- IMsRdpClient8.get_Domain
- IMsRdpClient8.put_Domain
- IMsRdpClient9.Domain
- IMsRdpClient9.get_Domain
- IMsRdpClient9.put_Domain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf95c02de10fe8db38a53b75d4d20cf796020f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919044"
---
# <a name="imstscaxdomain-property"></a>IMsTscAx: Propriedade omain de:D

Especifica o domínio no qual o usuário atual faz logon.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Domain(
  [in]  BSTR newVal
);

HRESULT get_Domain(
  [out] BSTR *pDomain
);
```



## <a name="property-value"></a>Valor da propriedade

O novo nome de domínio.

## <a name="error-codes"></a>Códigos do Erro

Retornar **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

A definição da propriedade **Domain** é opcional. Se não estiver definido, o usuário poderá escolher um domínio quando a caixa de diálogo de logon do Windows aparecer durante a conexão.

O método **obter \_ domínio** aloca a memória necessária para o buffer apontado pelo parâmetro *pDomain* . Chamar aplicativos C/C++ deve liberar a memória com uma chamada para a função [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . Isso não é necessário para clientes de Visual Basic e de script.

Essa propriedade só poderá ser definida se o controle não estiver no estado conectado. Retornará **E \_ falhará** se for chamado quando o controle estiver conectado. Você pode verificar se o controle está conectado respondendo a eventos de conexão em [**IMsTscAxEvents**](imstscaxevents-interface.md) ou examinando a propriedade [**Connected**](imstscax-connected.md) .

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

[**Conectado**](imstscax-connected.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

