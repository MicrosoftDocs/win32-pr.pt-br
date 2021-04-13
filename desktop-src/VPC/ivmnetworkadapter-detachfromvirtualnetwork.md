---
title: Método IVMNetworkAdapter DetachFromVirtualNetwork (VPCCOMInterfaces. h)
description: Desanexa a interface de rede de sua rede virtual.
ms.assetid: f1a00ea2-2b79-4b5c-a4bd-3cab66deb0d0
keywords:
- DetachFromVirtualNetwork do método virtual PC
- Método DetachFromVirtualNetwork Virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface virtual PC, método DetachFromVirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.DetachFromVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d5046844764fe9e9eb6552fe1a04b6140201b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369689"
---
# <a name="ivmnetworkadapterdetachfromvirtualnetwork-method"></a>IVMNetworkAdapter: método etachFromVirtualNetwork de:D

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Desanexa a interface de rede de sua rede virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DetachFromVirtualNetwork();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                 | Descrição                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter é definido como e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

