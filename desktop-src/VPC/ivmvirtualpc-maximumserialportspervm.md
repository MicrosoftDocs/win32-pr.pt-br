---
title: Propriedade IVMVirtualPC MaximumSerialPortsPerVM (VPCCOMInterfaces. h)
description: Recupera o número máximo de portas seriais por máquina virtual.
ms.assetid: e7b874df-105e-4ca8-90ec-2368071dafa0
keywords:
- Propriedade MaximumSerialPortsPerVM Virtual PC
- Propriedade MaximumSerialPortsPerVM Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, Propriedade MaximumSerialPortsPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumSerialPortsPerVM
- IVMVirtualPC.get_MaximumSerialPortsPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9819c5e566018c347d100d1f1cf8dd0c7976b19455942f3198ee968d3a619a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591746"
---
# <a name="ivmvirtualpcmaximumserialportspervm-property"></a>Propriedade IVMVirtualPC:: MaximumSerialPortsPerVM

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o número máximo de portas seriais por máquina virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MaximumSerialPortsPerVM(
  [out, retval] long *maxPorts
);
```



## <a name="property-value"></a>Valor da propriedade

O número máximo de portas seriais por máquina virtual.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                           | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                                | O parâmetro é **NULL**.<br/>                                                           |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |
| <dl> <dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt> </dl> | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

