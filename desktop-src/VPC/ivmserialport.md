---
title: Interface IVMSerialPort (VPCCOMInterfaces. h)
description: Define uma porta serial dentro de uma máquina virtual.
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- Virtual PC de interface IVMSerialPort
- Virtual PC de interface IVMSerialPort, descrito
topic_type:
- apiref
api_name:
- IVMSerialPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6edc758ffecca9a0d4788e5586c902cf0b21dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499580"
---
# <a name="ivmserialport-interface"></a>Interface IVMSerialPort

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define uma porta serial dentro de uma máquina virtual. Essa interface permite que você configure portas seriais dentro de uma máquina virtual. Você pode recuperar um objeto **IVMSerialPort** do objeto [**IVMSerialPortCollection**](ivmserialportcollection.md) retornado da propriedade [**IVMVirtualMachine:: SerialPorts**](ivmvirtualmachine-serialports.md) .

## <a name="members"></a>Membros

A interface **IVMSerialPort** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMSerialPort** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMSerialPort** tem esses métodos.



| Método                                       | Descrição                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [**\_ID**](ivmserialport--id.md)            | Recupera o identificador interno da porta serial.<br/> |
| [**Configurar**](ivmserialport-configure.md) | Configura a porta serial.<br/>                           |



 

### <a name="properties"></a>Propriedades

A interface **IVMSerialPort** tem essas propriedades.



| Propriedade                                                                  | Tipo de acesso          | Descrição                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [**ConnectImmediately**](ivmserialport-connectimmediately.md)<br/> | Somente leitura<br/> | Indica se a porta serial deve ser aberta sem aguardar a recepção de um comando de modem.<br/> |
| [**Nome**](ivmserialport-name.md)<br/>                             | Somente leitura<br/> | O nome da porta serial.<br/>                                                                           |
| [**Tipo**](ivmserialport-type.md)<br/>                             | Somente leitura<br/> | O tipo da porta serial.<br/>                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort é definido como 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



 

