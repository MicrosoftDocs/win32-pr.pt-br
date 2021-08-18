---
title: Propriedade VirtualNetworkAdapter IVM (VPCCOMInterfaces.h)
description: Recupera a rede virtual à qual o interface de rede está anexado.
ms.assetid: 7f52fd86-5f83-41d8-ba48-7db65e9c357c
keywords:
- VirtualNetwork property Virtual PC
- Propriedade VirtualNetwork Pc Virtual , interface IVMNetworkAdapter
- INTERFACE IVMNetworkAdapter PC virtual, propriedade VirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualNetwork
- IVMNetworkAdapter.get_VirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1bc3a3d58553d403f5e0ca6a8decbcbd3369b48450e9ec190b2f42f83de57e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136609"
---
# <a name="ivmnetworkadaptervirtualnetwork-property"></a>Propriedade IVMNetworkAdapter::VirtualNetwork

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a rede virtual à qual o interface de rede está anexado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_VirtualNetwork(
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a>Valor da propriedade

Uma [**interface IVMVirtualNetwork**](ivmvirtualnetwork.md) que representa a rede virtual à qual esse interface de rede virtual está anexado.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                       | Significado                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida.<br/>                                                  |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                            | O parâmetro é **NULL.**<br/>                                                     |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                       | Esse interface de rede é desconectado e não está conectado a uma rede virtual.<br/> |
| <dl> <dt>VM \_ E \_ \_ \_ \_ ID DE REDE VIRTUAL INVÁLIDA</dt> <dt>0XA00400702</dt> </dl> | Essa interface está conectada a uma rede virtual com uma ID inválida.<br/>           |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Ocorreu um erro inesperado.<br/>                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMNetworkAdapter é definido como \_ e32e4165-22b8-4dc0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

