---
title: Interface IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Define uma rede virtual.
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- Virtual PC de interface IVMVirtualNetwork
- Virtual PC de interface IVMVirtualNetwork, descrito
topic_type:
- apiref
api_name:
- IVMVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9caf5accb0add3354953d09e74a0893e2392deee7720b7a2cba0136b3f4b7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592581"
---
# <a name="ivmvirtualnetwork-interface"></a>Interface IVMVirtualNetwork

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define uma rede virtual. Os objetos **IVMVirtualNetwork** são retornados do método [**IVMVirtualPC**](ivmvirtualpc.md) [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md). Você também pode recuperar um objeto **IVMVirtualNetwork** do objeto [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) retornado da propriedade [**IVMVirtualPC:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .

Uma rede virtual consiste em um comutador virtual, que executa todo o roteamento interno e várias conexões que estão "conectadas" ao comutador virtual. Essas conexões podem ser uma conexão de host externo real, uma "rede interna" ou uma rede compartilhada (NAT).

## <a name="members"></a>Membros

A interface **IVMVirtualNetwork** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualNetwork** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMVirtualNetwork** tem esses métodos.



| Método                                | Descrição                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [**\_SESSÃO**](ivmvirtualnetwork--id.md) | Recupera o identificador interno da rede virtual.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IVMVirtualNetwork** tem essas propriedades.



| Propriedade                                                                | Tipo de acesso          | Descrição                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**HostAdapter**](ivmvirtualnetwork-hostadapter.md)<br/>         | Somente leitura<br/> | O nome do adaptador ao qual a rede virtual está conectada.<br/>  |
| [**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))<br/>             | Somente leitura<br/> | Determina se a instância de rede virtual é sem fio ou não.<br/> |
| [**Nome**](ivmvirtualnetwork-name.md)<br/>                       | Somente leitura<br/> | O nome exclusivo da instância de rede virtual.<br/>                    |
| [**Adaptadores**](ivmvirtualnetwork-networkadapters.md)<br/> | Somente leitura<br/> | Uma coleção enumerável de NICs anexadas à rede virtual.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork é definido como 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



 

