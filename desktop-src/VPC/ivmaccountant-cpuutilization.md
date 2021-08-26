---
title: Propriedade IVMAccountant CPUUtilization (VPCCOMInterfaces.h)
description: Recupera o percentual de utilização atual da CPU para essa máquina virtual.
ms.assetid: 69bb61ec-af41-4bd0-95bd-4698a1d33098
keywords:
- CPUUtilization property Virtual PC
- Propriedade CPUUtilization Pc Virtual , interface IVMAccountant
- INTERFACE IVMAccountant Pc Virtual, propriedade CPUUtilization
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilization
- IVMAccountant.get_CPUUtilization
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba54d7ec3a3fc447a49e9a72addd72fc5e3929b486c8fd4271276a40a7041f4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007297"
---
# <a name="ivmaccountantcpuutilization-property"></a>Propriedade IVMAccountant::CPUUtilization

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o percentual de utilização atual da CPU para essa máquina virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_CPUUtilization(
  [out, retval] long *percentageUtilization
);
```



## <a name="property-value"></a>Valor da propriedade

O percentual de utilização atual da CPU.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>       |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>         | O parâmetro é **NULL.**<br/>          |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | A máquina virtual não está em execução.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ocorreu um erro inesperado.<br/>   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMAccountant é definido como \_ 6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

