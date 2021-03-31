---
title: Propriedade IMsRdpClient7 TransportSettings3
description: Recupera um objeto que dá suporte à interface IMsRdpClientTransportSettings3.
ms.assetid: d11f0943-241e-44cd-a98c-595916ab0718
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade TransportSettings3
- Propriedade TransportSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade TransportSettings3
- Propriedade TransportSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade TransportSettings3
- Propriedade TransportSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade TransportSettings3
- Propriedade TransportSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade TransportSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.TransportSettings3
- IMsRdpClient7.get_TransportSettings3
- IMsRdpClient8.TransportSettings3
- IMsRdpClient8.get_TransportSettings3
- IMsRdpClient9.TransportSettings3
- IMsRdpClient9.get_TransportSettings3
- IMsRdpClient10.TransportSettings3
- IMsRdpClient10.get_TransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c60b58f8f2438de0d43f69ce0b3bb73607e7551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644415"
---
# <a name="imsrdpclient7transportsettings3-property"></a>Propriedade IMsRdpClient7:: TransportSettings3

Recupera um objeto que dá suporte à interface [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_TransportSettings3(
  [out, retval] IMsRdpClientTransportSettings3 **ppXportSet3
);
```



## <a name="property-value"></a>Valor da propriedade

O endereço de um ponteiro de interface [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) que recebe o objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient7 é definido como b2a5b5ce-3461-444A-91D4-add26d070638<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





