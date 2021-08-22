---
title: Propriedade de tempo de atividade IVMAccountant (VPCCOMInterfaces. h)
description: Recupera o número de segundos em que a máquina virtual está em execução.
ms.assetid: 0c62d51b-fdf1-43f6-81d8-a5f0538c510f
keywords:
- Propriedade de tempo de atividade Virtual PC
- Propriedade de tempo de atividade Virtual PC, interface IVMAccountant
- Virtual PC de interface IVMAccountant, propriedade de tempo de atividade
topic_type:
- apiref
api_name:
- IVMAccountant.UpTime
- IVMAccountant.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df0c7731ab50d1967d59eb7178fb6bcee008b6d45fed69ab66279ae3fd8beb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654376"
---
# <a name="ivmaccountantuptime-property"></a>Propriedade IVMAccountant:: tempo de atividade

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o número de segundos em que a máquina virtual está em execução.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a>Valor da propriedade

O número de segundos.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>       |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>          |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                    | A máquina virtual não está em execução.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant é definido como 6376c067-7f57-4D63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

