---
title: Interface IVMSerialPort (VPCCOMInterfaces.h)
description: Define uma porta serial dentro de uma máquina virtual.
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- COMPUTADOR Virtual da interface IVMSerialPort
- COMPUTADOR Virtual da interface IVMSerialPort , descrito
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
ms.openlocfilehash: 385f22caf7b843a91987eea01a7713544475c24be741bbb56d59610cb2cd521d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752816"
---
# <a name="ivmserialport-interface"></a>Interface IVMSerialPort

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define uma porta serial dentro de uma máquina virtual. Essa interface permite configurar portas seriais dentro de uma máquina virtual. Você pode recuperar um **objeto IVMSerialPort** do objeto [**IVMSerialPortCollection**](ivmserialportcollection.md) retornado da [**propriedade IVMVirtualMachine::SerialPorts.**](ivmvirtualmachine-serialports.md)

## <a name="members"></a>Membros

A **interface IVMSerialPort** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMSerialPort** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMSerialPort** tem esses métodos.



| Método                                       | Descrição                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [**\_ID**](ivmserialport--id.md)            | Recupera o identificador interno da porta serial.<br/> |
| [**Configurar**](ivmserialport-configure.md) | Configura a porta serial.<br/>                           |



 

### <a name="properties"></a>Propriedades

A **interface IVMSerialPort** tem essas propriedades.



| Propriedade                                                                  | Tipo de acesso          | Descrição                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [**ConnectImmediately**](ivmserialport-connectimmediately.md)<br/> | Somente leitura<br/> | Indica se a porta serial deve ser aberta sem esperar que um comando de modem seja recebido.<br/> |
| [**Nome**](ivmserialport-name.md)<br/>                             | Somente leitura<br/> | O nome da porta serial.<br/>                                                                           |
| [**Tipo**](ivmserialport-type.md)<br/>                             | Somente leitura<br/> | O tipo da porta serial.<br/>                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMSerialPort é definido como \_ 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



 

