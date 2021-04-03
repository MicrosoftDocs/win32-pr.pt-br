---
title: Interface IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Define a coleção de portas seriais na máquina virtual. Para obter um objeto IVMSerialPortCollection, use a propriedade SerialPorts IVMVirtualMachine.
ms.assetid: c0ee9799-f3f7-477e-b33b-52f424752aad
keywords:
- Virtual PC de interface IVMSerialPortCollection
- Virtual PC de interface IVMSerialPortCollection, descrito
topic_type:
- apiref
api_name:
- IVMSerialPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d2ec37789423b5f9446d667da69eca346a2286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644709"
---
# <a name="ivmserialportcollection-interface"></a>Interface IVMSerialPortCollection

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a coleção de portas seriais na máquina virtual. Para obter um objeto **IVMSerialPortCollection** , use a propriedade [**IVMVirtualMachine:: SerialPorts**](ivmvirtualmachine-serialports.md) .

## <a name="members"></a>Membros

A interface **IVMSerialPortCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMSerialPortCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMSerialPortCollection** tem essas propriedades.



| Propriedade                                                         | Tipo de acesso          | Descrição                                                                |
|:-----------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------|
| [**\_NewEnum**](ivmserialportcollection--newenum.md)<br/> | Somente leitura<br/> | Um enumerador para a coleção.<br/>                               |
| [**Contar**](ivmserialportcollection-count.md)<br/>        | Somente leitura<br/> | O número de portas seriais nesta coleção.<br/>                  |
| [**Item**](ivmserialportcollection-item.md)<br/>          | Somente leitura<br/> | O objeto de porta serial que corresponde ao índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPortCollection é definido como dd3c6175-1f04-4341-9f85-104074880289<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> <dt>

[**IVMVirtualMachine:: SerialPorts**](ivmvirtualmachine-serialports.md)
</dt> </dl>

 

