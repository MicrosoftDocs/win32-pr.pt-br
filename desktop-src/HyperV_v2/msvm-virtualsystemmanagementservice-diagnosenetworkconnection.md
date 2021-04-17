---
description: Diagnostica a conectividade de rede de uma VM em um ambiente de virtualização de rede do Windows.
ms.assetid: c18f48bf-1f57-4a23-a495-462afad42750
title: Método DiagnoseNetworkConnection da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DiagnoseNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 70760f771e3908265a4ac70ebc1cbdf957d652c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770211"
---
# <a name="diagnosenetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método DiagnoseNetworkConnection da \_ classe VirtualSystemManagementService Msvm

Diagnostica a conectividade de rede de uma VM em um ambiente de virtualização de rede do Windows.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DiagnoseNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  string                                     DiagnosticSettings,
  [out] string                                     DiagnosticInformation,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TargetNetworkAdapter* \[ no\]
</dt> <dd>

Referência a um [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) que descreve o adaptador de rede de destino.

</dd> <dt>

*DiagnosticSettings* \[ no\]
</dt> <dd>

As configurações de diagnóstico a serem usadas.

</dd> <dt>

*DiagnosticInformation* \[ fora\]
</dt> <dd>

Em caso de sucesso, retorna as informações de diagnóstico.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 ou 4096 em caso de êxito; caso contrário, retornará um erro.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Falha** (2)
</dt> <dt>

**Tempo limite** (3)
</dt> <dt>

**Parâmetro inválido** (4)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
</dt> <dt>

**Método reservado** (4097.. 32767)
</dt> <dt>

**Específico do fornecedor** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

