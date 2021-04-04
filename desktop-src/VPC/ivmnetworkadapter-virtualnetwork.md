---
title: Propriedade IVMNetworkAdapter VirtualNetwork (VPCCOMInterfaces. h)
description: Recupera a rede virtual à qual a interface de rede está conectada.
ms.assetid: 7f52fd86-5f83-41d8-ba48-7db65e9c357c
keywords:
- Propriedade VirtualNetwork Virtual PC
- Propriedade VirtualNetwork Virtual PC, interface IVMNetworkAdapter
- Virtual PC interface IVMNetworkAdapter, Propriedade VirtualNetwork
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
ms.openlocfilehash: b932ef553d3952fbc69edba3416ac20049984810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008806"
---
# <a name="ivmnetworkadaptervirtualnetwork-property"></a>Propriedade IVMNetworkAdapter:: VirtualNetwork

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a rede virtual à qual a interface de rede está conectada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_VirtualNetwork(
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a>Valor da propriedade

Uma interface [**IVMVirtualNetwork**](ivmvirtualnetwork.md) que representa a rede virtual à qual essa interface de rede virtual está anexada.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                       | Significado                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida.<br/>                                                  |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                            | O parâmetro é **NULL**.<br/>                                                     |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                                       | Esta interface de rede está desconectada e não está conectada a uma rede virtual.<br/> |
| <dl> <dt>VM \_ E \_ \_ ID de \_ rede \_ virtual inválida</dt> <dt>0xA00400702</dt> </dl> | Esta interface está conectada a uma rede virtual com uma ID inválida.<br/>           |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                    | Ocorreu um erro inesperado.<br/>                                              |



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

 

