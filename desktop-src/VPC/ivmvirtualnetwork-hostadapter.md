---
title: Propriedade IvMVirtualNetwork HostAdapter (VPCCOMInterfaces.h)
description: Nome do adaptador ao qual a rede virtual está conectada.
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- Propriedade HostAdapter Pc Virtual
- Propriedade HostAdapter Pc Virtual , interface IVMVirtualNetwork
- IVMVirtualNetwork interface Virtual PC , propriedade HostAdapter
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.HostAdapter
- IVMVirtualNetwork.get_HostAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72db5d8349572b2bd3549c2ee54d20e994bdfe8aed6ba0fbe31875e04f6942f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122676"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a>Propriedade IVMVirtualNetwork::HostAdapter

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o nome do adaptador ao qual a rede virtual está conectada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a>Valor da propriedade

O nome do adaptador de host ao qual a rede virtual está conectada.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                            | Significado                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                               | A operação foi bem-sucedida.<br/>                                                                                                                              |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                 | O parâmetro é **NULL.**<br/>                                                                                                                                 |
| <dl> <dt>VM \_ ADAPTADOR \_ E NÃO ENCONTRADO \_ \_ 0XA0040700</dt> <dt></dt> </dl> | O adaptador Ethernet do host ao qual essa rede virtual estava conectada não está mais disponível. O adaptador Ethernet do host pode ter sido removido ou desabilitado.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>         | Ocorreu um erro inesperado.<br/>                                                                                                                          |



## <a name="remarks"></a>Comentários

O adaptador de rede virtual permite que uma rede virtual fale com redes externas. Normalmente, há um adaptador por adaptador Ethernet instalado no computador host. Por exemplo, digamos que um computador host tenha um adaptador rotulado como "ENET 10/100". Para conectar uma NIC virtual à rede anexada à "ENET 10/100", de definir a propriedade **HostAdapter** de Rede da rede virtual como "ENET 10/100" e conectar a NIC virtual a essa rede virtual.

Se a **propriedade HostAdapter** for definida como uma cadeia de caracteres vazia (""), o adaptador de NIC virtual será conectado à rede "Rede Interna" ou "NAT (Rede Compartilhada)". As NICs virtuais anexadas à rede "Rede Interna" não terão acesso a redes externas no host do sistema. No entanto, as NICs virtuais anexadas a essa rede virtual ainda podem se comunicar entre si.

A lista completa de adaptadores pode ser acessada por meio da [**propriedade IVMHostInfo::NetworkAdapters.**](ivmhostinfo-networkadapters.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork é definido como 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

