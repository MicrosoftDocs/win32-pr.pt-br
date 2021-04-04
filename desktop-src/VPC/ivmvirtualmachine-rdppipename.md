---
title: Propriedade IVMVirtualMachine RdpPipeName (VPCCOMInterfaces. h)
description: Recupera o nome da conexão RDP chamada pipe usado para vídeo e entrada.
ms.assetid: 0c2d0f23-40cd-4a86-96dd-546fb3570871
keywords:
- Propriedade RdpPipeName Virtual PC
- Propriedade RdpPipeName Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade RdpPipeName
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RdpPipeName
- IVMVirtualMachine.get_RdpPipeName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86e49463c5e443a07d1fa86736047435eaf60a06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008803"
---
# <a name="ivmvirtualmachinerdppipename-property"></a>Propriedade IVMVirtualMachine:: RdpPipeName

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o nome da conexão RDP chamada pipe usado para vídeo e entrada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_RdpPipeName(
  [out, retval] BSTR *RdpPipeName
);
```



## <a name="property-value"></a>Valor da propriedade

Nome da conexão RDP chamada pipe usado para vídeo e entrada.

## <a name="error-codes"></a>Códigos do Erro

Se o método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .



| Nome/valor                                                                                                                                                         | Significado                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | A operação foi bem-sucedida.<br/>          |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>              | O parâmetro RdpPipeName é **nulo**.<br/> |
| <dl> <dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt> </dl> | A máquina virtual não está em execução.<br/>    |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>      | Erro desconhecido.<br/>             |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

