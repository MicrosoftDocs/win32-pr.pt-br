---
title: Interface IVMAccountant (VPCCOMInterfaces. h)
description: Fornece acesso a informações relacionadas à contabilidade para uma máquina virtual.
ms.assetid: 047fa4c9-cb2e-4830-bab8-0513247eff9b
keywords:
- Virtual PC de interface IVMAccountant
- Virtual PC de interface IVMAccountant, descrito
topic_type:
- apiref
api_name:
- IVMAccountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d207833b92794510789e66e31b10e94d70b319fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645143"
---
# <a name="ivmaccountant-interface"></a>Interface IVMAccountant

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Fornece acesso a informações relacionadas à contabilidade para uma máquina virtual. Para recuperar o **IVMAccountant** de uma máquina virtual, use a propriedade [**IVMVirtualMachine:: contador**](ivmvirtualmachine-accountant.md) .

## <a name="members"></a>Membros

A interface **IVMAccountant** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMAccountant** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMAccountant** tem essas propriedades.



| Propriedade                                                                        | Tipo de acesso          | Descrição                                                                                             |
|:--------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [**CPUUtilization**](ivmaccountant-cpuutilization.md)<br/>               | Somente leitura<br/> | A porcentagem de utilização da CPU atual para esta máquina virtual.<br/>                          |
| [**CPUUtilizationHistory**](ivmaccountant-cpuutilizationhistory.md)<br/> | Somente leitura<br/> | A utilização de CPU recente desta máquina virtual (como uma matriz de valores percentuais).<br/>       |
| [**DiskBytesRead**](ivmaccountant-diskbytesread.md)<br/>                 | Somente leitura<br/> | O número total de bytes lidos por todos os controladores de armazenamento para esta máquina virtual.<br/>          |
| [**DiskBytesWritten**](ivmaccountant-diskbyteswritten.md)<br/>           | Somente leitura<br/> | O número total de bytes gravados por todos os controladores de armazenamento para esta máquina virtual.<br/>       |
| [**NetworkBytesReceived**](ivmaccountant-networkbytesreceived.md)<br/>   | Somente leitura<br/> | O número total de bytes recebidos por todos os adaptadores de rede virtual para esta máquina virtual.<br/> |
| [**NetworkBytesSent**](ivmaccountant-networkbytessent.md)<br/>           | Somente leitura<br/> | O número total de bytes enviados por todos os adaptadores de rede virtual para esta máquina virtual.<br/>     |
| [**Atividade**](ivmaccountant-uptime.md)<br/>                               | Somente leitura<br/> | O número de segundos em que a máquina virtual está em execução.<br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant é definido como 6376c067-7f57-4D63-b754-06e2e4f51d73<br/>              |



 

