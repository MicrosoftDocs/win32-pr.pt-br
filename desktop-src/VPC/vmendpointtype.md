---
title: Enumeração VMEndpointType (VPCCOMInterfaces. h)
description: Especifica o tipo de ponto de extremidade.
ms.assetid: b48bd860-50dc-4c8c-b65b-69c407d4612a
keywords:
- VMEndpointType de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMEndpointType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912eb43147af03dd2b9923c4bdb778044f40d023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824376"
---
# <a name="vmendpointtype-enumeration"></a>Enumeração VMEndpointType

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Especifica o tipo de ponto de extremidade.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum  { 
  vmEndpoint_NamedPipe  = 0,
  vmEndpoint_TCPIP      = 1
} VMEndpointType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**vmEndpoint \_ NamedPipe**
</dt> <dd>

O lado do host.

</dd> <dt>

<span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**\_tcpip vmEndpoint**
</dt> <dd>

O lado do convidado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IVMVirtualMachine::StartCommunicationChannel**](ivmvirtualmachine-startcommunicationchannel.md)
</dt> </dl>

 

