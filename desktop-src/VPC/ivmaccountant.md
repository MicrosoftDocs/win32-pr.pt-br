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
ms.openlocfilehash: ae791ce6cd1cd401beba4ff200ffbb54213b89d642c478eca7eb3b3057b4acb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473706"
---
# <a name="ivmaccountant-interface"></a>Interface IVMAccountant

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant é definido como 6376c067-7f57-4D63-b754-06e2e4f51d73<br/>              |



 

