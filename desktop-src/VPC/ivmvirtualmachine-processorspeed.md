---
title: Propriedade IVMVirtualMachine ProcessorSpeed (VPCCOMInterfaces. h)
description: Velocidade do processador, em megahertz (MHz) ou gigahertz (GHz).
ms.assetid: 465157a9-08ad-4636-b7c6-a188ff21e131
keywords:
- Propriedade ProcessorSpeed Virtual PC
- Propriedade ProcessorSpeed Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade ProcessorSpeed
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ProcessorSpeed
- IVMVirtualMachine.get_ProcessorSpeed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeb6f17e867d7618241b099b765ff450a2a4e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455799"
---
# <a name="ivmvirtualmachineprocessorspeed-property"></a>IVMVirtualMachine: Propriedade rocessorSpeed de:P

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a velocidade do processador, em megahertz (MHz) ou gigahertz (GHz).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ProcessorSpeed(
  [out, retval] long *processorSpeed
);
```



## <a name="property-value"></a>Valor da propriedade

A velocidade, em megahertz ou gigahertz.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>        |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl> | A configuração é desconhecida.<br/>     |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/> |



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

 

