---
title: Propriedade IVMNetworkAdapter VirtualMachine (VPCCOMInterfaces. h)
description: Recupera a máquina virtual associada a esta interface de rede.
ms.assetid: a3519041-0081-44e7-aa76-760d59ca8587
keywords:
- Propriedade VirtualMachine Virtual PC
- Propriedade VirtualMachine Virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface virtual PC, Propriedade VirtualMachine
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualMachine
- IVMNetworkAdapter.get_VirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea50e43bdcffcd16f668ef596a0f9db9d9bccfe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008807"
---
# <a name="ivmnetworkadaptervirtualmachine-property"></a>Propriedade IVMNetworkAdapter:: VirtualMachine

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a máquina virtual associada a esta interface de rede.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_VirtualMachine(
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a>Valor da propriedade

Uma interface [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa a máquina virtual.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>        |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>           |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl> | Não é possível encontrar a máquina virtual.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>    |



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

 

