---
title: Propriedade IVMVirtualNetwork HostAdapter (VPCCOMInterfaces. h)
description: Nome do adaptador ao qual a rede virtual está conectada.
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- Propriedade HostAdapter Virtual PC
- Propriedade HostAdapter Virtual PC, interface IVMVirtualNetwork
- IVMVirtualNetwork interface virtual PC, Propriedade HostAdapter
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
ms.openlocfilehash: 0485303c2328a85c70779f16652121729546f3ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009625"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a>Propriedade IVMVirtualNetwork:: HostAdapter

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                 | O parâmetro é **NULL**.<br/>                                                                                                                                 |
| <dl> <dt>VM \_ \_Adaptador E \_ não \_ encontrado</dt> <dt>0xA0040700</dt> </dl> | O adaptador de Ethernet do host ao qual essa rede virtual estava conectada não está mais disponível. O adaptador Ethernet do host pode ter sido removido ou desabilitado.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>         | Ocorreu um erro inesperado.<br/>                                                                                                                          |



## <a name="remarks"></a>Comentários

O adaptador de rede virtual permite que uma rede virtual se comunique com redes externas. Normalmente, há um adaptador por adaptador Ethernet instalado no computador host. Por exemplo, digamos que uma máquina host tivesse um adaptador chamado "10/100 ENET". Para conectar uma NIC virtual à rede anexada a "10/100 ENET", defina a propriedade **HostAdapter** de rede da rede virtual como "10/100 enet" e conecte a NIC virtual a essa rede virtual.

Se a propriedade **HostAdapter** for definida como uma cadeia de caracteres vazia (""), o adaptador NIC virtual será conectado à rede "rede interna" ou "rede compartilhada (NAT)". As NICs virtuais conectadas à rede "rede interna" não terão acesso a redes externas no host do sistema. No entanto, as NICs virtuais conectadas a essa rede virtual ainda podem se comunicar entre si.

A lista completa de adaptadores pode ser acessada por meio da propriedade [**IVMHostInfo:: adaptadores**](ivmhostinfo-networkadapters.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork é definido como 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

