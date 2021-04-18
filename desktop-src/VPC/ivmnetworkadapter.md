---
title: Interface IVMNetworkAdapter (VPCCOMInterfaces. h)
description: Serve como a interface para uma placa de interface de rede virtual.
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- Virtual PC de interface IVMNetworkAdapter
- Virtual PC de interface IVMNetworkAdapter, descrito
topic_type:
- apiref
api_name:
- IVMNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74a0ccf722715896743129b6666609bd8a88df3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369661"
---
# <a name="ivmnetworkadapter-interface"></a>Interface IVMNetworkAdapter

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Serve como a interface para uma NIC (placa de interface de rede) virtual. Ele é usado para configurar como uma máquina virtual é em rede. As placas de interface de rede podem ser adicionadas e removidas usando [**IVMVirtualMachine:: AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) e [**IVMVirtualMachine:: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md). Você também pode recuperar um objeto **IVMNetworkAdapter** da coleção [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) retornada pelas propriedades [**IVMVirtualMachine:: adaptadores**](ivmvirtualmachine-networkadapters.md) ou [**IVMVirtualNetwork:: adaptadores**](ivmvirtualnetwork-networkadapters.md) .

## <a name="members"></a>Membros

A interface **IVMNetworkAdapter** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMNetworkAdapter** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMNetworkAdapter** tem esses métodos.



| Método                                                                         | Descrição                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**\_SESSÃO**](ivmnetworkadapter--id.md)                                          | Recupera o identificador interno desta interface de rede.<br/>     |
| [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md)     | Anexa a interface de rede à rede virtual especificada.<br/> |
| [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) | Desanexa a interface de rede de sua rede virtual.<br/>         |



 

### <a name="properties"></a>Propriedades

A interface **IVMNetworkAdapter** tem essas propriedades.



| Propriedade                                                                                  | Tipo de acesso           | Descrição                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md)<br/>                   | Leitura/gravação<br/> | O endereço Ethernet (MAC) da interface de rede.<br/>             |
| [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | Leitura/gravação<br/> | Indica se o endereço Ethernet é gerado dinamicamente.<br/> |
| [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md)<br/>                     | Somente leitura<br/>  | A máquina virtual associada a esta interface de rede.<br/>      |
| [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md)<br/>                     | Somente leitura<br/>  | A rede virtual à qual a interface de rede está conectada.<br/>  |



 

## <a name="remarks"></a>Comentários

O endereço Ethernet padrão para uma interface de rede é "00-00-00-00-00-00", que é considerado um endereço Ethernet inválido pela maioria dos sistemas operacionais. Se [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) for definido como **false**, [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) deverá ser inicializado com um endereço de rede Ethernet válido.

Os procedimentos a seguir explicam como usar a interface **IVMNetworkAdapter** .

**Para anexar uma NIC virtual a uma NIC de host**

-   NICs virtuais (convidados) não são anexadas diretamente a uma NIC de host. Em vez disso, a NIC virtual é anexada a uma rede virtual anexada a uma NIC de host. Para obter mais informações sobre como configurar redes virtuais, consulte [**IVMVirtualNetwork**](ivmvirtualnetwork.md). Para anexar a NIC virtual a uma rede virtual, use o método [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) .

**Para desconectar uma NIC virtual da rede virtual**

-   O método [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) desanexará a NIC virtual da rede virtual. Depois que essa função for chamada, a propriedade [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) retornará uma ID de rede virtual que não é válida.

**Para remover uma NIC virtual de uma máquina virtual se você tiver o objeto NIC virtual**

1.  Obtenha a máquina virtual associada à NIC virtual usando a propriedade [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) .
2.  Use o objeto atual como um parâmetro para o método [**IVMVirtualMachine:: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter é definido como e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



 

